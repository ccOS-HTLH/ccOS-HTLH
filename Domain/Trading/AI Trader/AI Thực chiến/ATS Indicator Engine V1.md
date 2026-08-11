# ATS Indicator Engine V1
## Smart Flow / Event / State Engine — BTC

> Mục tiêu: xây một indicator engine theo hướng “TDV-like nhưng intelligence cao hơn”, trong đó indicator không chỉ vẽ giá trị mà còn phát hiện **event**, phân loại **market state**, và cung cấp context compact cho ATS Decision Engine.

---

## 1. Core Philosophy

### Traditional indicator

```text
Raw Data
  ↓
Formula
  ↓
Value
  ↓
Chart
```

### ATS Indicator Engine

```text
Raw Realtime Data
        ↓
Deterministic Calculation
        ↓
Event Engine
        ↓
Context / Reference Engine
        ↓
State Engine
        ↓
Signal Confidence
        ↓
Decision Engine
        ↓
Compact Reasoning
```

Nguyên tắc:

1. **Không để LLM tính indicator.**
2. Indicator và event phải được tính deterministic ở backend.
3. AI chỉ nhận structured context để reasoning/synthesis.
4. Không dùng một indicator đơn lẻ làm Entry Signal.
5. Event → Context → State → Confirmation.
6. Price luôn được đọc cùng Position Participation và Flow.
7. POC5 và POC30 là **hai reference độc lập**.

---

# 2. Data Layer

## 2.1 Market Chart (MC)

```text
Price
OHLC
Volume
RSI
EMA
Timeframe
```

Timeframes:

```text
D1
H4
H1
M30
M15
M5
```

## 2.2 Quant Dashboard (QD)

```text
OI
Funding
CVD
VPIN
Agg Liquidation
Auction Flow
Long/Short Ratio
```

QD mặc định:

```text
5 minutes
```

## 2.3 Exchange / Order Flow (EX)

```text
Delta
Volume
Footprint
Orderbook Heatmap
Liquidation Heatmap
```

## 2.4 Volume Profile

Tách riêng:

```text
POC5
POC30
VP1
VAH
VAL
```

Không được gộp:

```text
POC5 ≠ POC30
```

---

# 3. Normalized Data Schema

Backend nên chuẩn hóa dữ liệu thành một object thống nhất.

```json
{
  "timestamp": 0,
  "symbol": "BTCUSDT",
  "price": 0,
  "oi": {
    "value": 0,
    "direction": "BuI | BeI | BuO | BeO | Neutral",
    "delta": 0
  },
  "cvd": {
    "value": 0,
    "delta": 0
  },
  "auction": {
    "value": 0,
    "ema20": 0
  },
  "vpin": 0,
  "rsi": {
    "value": 0
  },
  "volume": 0,
  "delta": 0,
  "volume_profile": {
    "poc5": 0,
    "poc30": 0,
    "vp1": 0,
    "vah": 0,
    "val": 0
  }
}
```

---

# 4. Position Participation Model

OI phải được đọc theo **hướng + thay đổi**, không chuyển thành absolute value để làm mất dấu.

Core states:

```text
BuI = Buy-side Increase
BeI = Bear-side Increase
BuO = Buy-side Outflow
BeO = Bear-side Outflow
```

Engine không chỉ lưu giá trị hiện tại mà phải lưu:

```text
current
previous
delta
slope
persistence
```

---

# 5. OI Event Engine

## Fresh Long Expansion

```text
Price ↑
OI ↑ BuI
CVD ↑
```

→ `FRESH_LONG_EXPANSION`

## Fresh Short Expansion

```text
Price ↓
OI ↑ BeI
CVD ↓
Auction ↓
```

→ `FRESH_SHORT_EXPANSION`

## Short Covering

```text
Price ↑
OI ↓ BeO
CVD ↑ / stable
```

→ `SHORT_COVERING`

## Long Unwind

```text
Price ↓
OI ↓ BuO
CVD ↓ / stable
```

→ `LONG_UNWIND`

## Position Expansion Decay

Ví dụ:

```text
BeI:
+1.05
→ +0.72
→ +0.44
→ +0.20
→ +0.02
→ BeO
```

→ `SHORT_EXPANSION_DECAY`

Tương tự cho Long.

---

# 6. CVD Engine

Core calculations:

```text
CVD_delta = CVD_current - CVD_previous
```

Theo dõi:

```text
CVD slope
CVD acceleration
CVD deceleration
CVD high / low
Price high / low
```

---

# 7. Smart CVD Divergence

Không đánh dấu divergence chỉ vì một điểm CVD khác hướng.

Cần xác định swing structure.

### Bearish divergence

```text
Price:
High 1 < High 2

CVD:
High 1 > High 2
```

→ `CVD_BEARISH_DIVERGENCE`

### Bullish divergence

```text
Price:
Low 1 > Low 2

CVD:
Low 1 < Low 2
```

→ `CVD_BULLISH_DIVERGENCE`

---

# 8. Divergence Strength

Không phải divergence nào cũng có cùng giá trị.

```text
Divergence Strength =
    Swing Separation
  + CVD Separation
  + Volume Confirmation
  + Persistence
  + OI Confirmation
  + Auction Confirmation
```

Ví dụ:

```text
0–30   Weak
31–60  Moderate
61–80  Strong
81–100 Extreme
```

Triangle nên phản ánh **strength**, không chỉ binary ON/OFF.

---

# 9. Smart Triangle System

Triangle = **Warning**, không phải Entry.

Một triangle chỉ có nghĩa:

```text
ATTENTION
```

Không được mặc định:

```text
Triangle = SELL
Triangle = BUY
```

Ví dụ:

```text
🔺
CVD Divergence
Strength: 72

OI: BeO
Auction: Improving
VPIN: 0.32

State:
Recovery

Risk:
Pullback
```

---

# 10. Divergence Confirmation Engine

### Bearish confirmation

```text
Price ↓
CVD ↓
OI ↑ BeI
Auction ↓
VPIN ↑
```

→ `CONFIRMED_BEARISH_REVERSAL_RISK`

### Bullish confirmation

```text
Price ↑
CVD ↑
OI ↑ BuI
Auction ↑
VPIN ↑
```

→ `CONFIRMED_BULLISH_EXPANSION`

---

# 11. Auction Engine

Auction phải được so sánh với baseline:

```text
Auction_current
vs
Auction_EMA20
```

States:

```text
AUCTION_BULLISH
AUCTION_BEARISH
AUCTION_IMPROVING
AUCTION_DETERIORATING
AUCTION_EXHAUSTION
```

Ví dụ:

```text
Auction = -6.8k
EMA20   = -8.7k
```

Vì:

```text
-6.8k > -8.7k
```

→ `AUCTION_IMPROVING`

Không được chỉ nhìn dấu âm/dương.

---

# 12. VPIN Engine

VPIN dùng để đo mức độ imbalance/stress.

Ví dụ state bands:

```text
< 0.30
LOW STRESS

0.30–0.50
NORMAL

0.50–0.70
ELEVATED

0.70–0.85
HIGH

> 0.85
EXTREME
```

Không nên dùng VPIN một mình để dự báo direction.

VPIN chủ yếu trả lời:

> “Flow đang stressed đến mức nào?”

---

# 13. Reference Engine

Core references:

```text
POC5
POC30
VP1
VAH
VAL
```

POC5 và POC30:

```text
POC5 ≠ POC30
```

### POC5 role

```text
Short-term active reference
```

### POC30 role

```text
Broader intraday value reference
```

### VP1

```text
Opposing / next reference zone
```

---

# 14. Price-Reference Events

Engine phải phát hiện:

```text
POC5_TEST
POC5_REJECTION
POC5_RECLAIM
POC5_ACCEPTANCE

VP1_TEST
VP1_REJECTION
VP1_RECLAIM
VP1_ACCEPTANCE

REFERENCE_ROTATION
FAILED_BREAK
ACCEPTED_BREAK
```

---

# 15. POC5 → VP1 Rotation

Một core pattern của ATS:

```text
Price
  │
VP1
  │
  │
POC5
```

Nếu Price không thoát khỏi vùng reference range:

```text
POC5 ↔ VP1
```

thì engine theo dõi khả năng rotation.

Ví dụ:

```text
POC5 rejection
→ price remains inside range
→ VP1 becomes next target
```

Hoặc:

```text
VP1 rejection
→ price remains inside range
→ POC5 becomes next target
```

---

# 16. State Engine

State engine tổng hợp events.

Core states:

```text
FRESH_LONG_EXPANSION
FRESH_SHORT_EXPANSION

LONG_UNWIND
SHORT_COVERING

RECOVERY
BEARISH_PRESSURE

BULLISH_ACCEPTANCE
BEARISH_ACCEPTANCE

EXHAUSTION
ABSORPTION

TRAP_RISK
REVERSAL_RISK

RANGE_ROTATION
```

---

# 17. State Transition Example

```text
FRESH_SHORT_EXPANSION
        ↓
SHORT_EXPANSION_DECAY
        ↓
EXHAUSTION
        ↓
SHORT_COVERING
        ↓
RECOVERY
        ↓
POC5_RECLAIM
        ↓
VP1_TEST
        ↓
       ┌──────────────┐
       ↓              ↓
VP1_REJECTION   VP1_ACCEPTANCE
       ↓              ↓
ROTATION         BULLISH_ACCEPTANCE
```

---

# 18. Flow Matrix

| Price | OI | CVD | Interpretation |
|---|---|---|---|
| ↑ | ↑ BuI | ↑ | Fresh Long |
| ↑ | ↓ BeO | ↑ | Short Covering |
| ↓ | ↑ BeI | ↓ | Fresh Short |
| ↓ | ↓ BuO | ↓ | Long Unwind |
| ↑ | ↑ BeI | ↓ | Short Trap Risk |
| ↓ | ↑ BuI | ↑ | Long Trap Risk |

Không dùng bảng này như absolute rule. Các event khác phải xác nhận.

---

# 19. Smart Signal Score

Mỗi state có confidence score:

```text
0–30
Weak

31–50
Early

51–70
Moderate

71–85
Strong

86–100
Extreme
```

Ví dụ:

```text
SHORT_COVERING

OI evidence       +25
CVD evidence      +20
Auction            +15
VPIN               +10
Price structure    +15
Persistence         +10
Contradiction       -5

Total = 90
```

---

# 20. Contradiction Layer

Engine phải biết khi indicators không đồng thuận.

Ví dụ:

```text
Price ↑
OI BeO
CVD ↑
Auction ↑
```

→ strong Short Covering.

Nhưng:

```text
Price ↑
OI BeO
CVD ↓
Auction ↓
```

→ recovery quality thấp.

Output:

```text
SHORT_COVERING
Confidence: 48
Warning: Flow disagreement
```

---

# 21. Realtime Context Buffer

Không chỉ lưu current snapshot.

Nên giữ:

```text
N = 100–500 recent observations
```

Tối thiểu:

```text
timestamp
price
OI
OI state
CVD
Auction
Auction EMA
VPIN
RSI
POC5
VP1
events
state
```

Điều này cho phép engine phát hiện:

```text
trend
slope
acceleration
decay
persistence
sequence
```

---

# 22. Example: Sequence Detection

Input:

```text
OI:
+1.05 BeI
+0.72 BeI
+0.44 BeI
+0.20 BeI
+0.02 BuI
-0.11 BeO
-0.42 BeO
-0.64 BeO
```

Engine output:

```text
SHORT_EXPANSION
        ↓
DECAY
        ↓
NEUTRALIZATION
        ↓
SHORT_UNWIND
```

Combined with:

```text
CVD:
-2.1k → +1.0k
```

and:

```text
VPIN:
0.97 → 0.29
```

Final state:

```text
SHORT_COVERING_RECOVERY
Confidence: Strong
```

---

# 23. AI Context Packet

AI không nhận toàn bộ raw stream.

Nó nhận compact structured context:

```json
{
  "price": 63618,
  "references": {
    "poc5": 63416,
    "vp1": 63800,
    "location": "BETWEEN_POC5_AND_VP1"
  },
  "flow": {
    "oi": {
      "value": -0.61,
      "state": "SHORT_UNWIND"
    },
    "cvd": {
      "value": 347,
      "state": "POSITIVE"
    },
    "auction": {
      "value": -7100,
      "ema20": -8400,
      "state": "IMPROVING"
    },
    "vpin": {
      "value": 0.32,
      "state": "LOW_STRESS"
    }
  },
  "events": [
    "CVD_DIVERGENCE",
    "POC5_RECLAIMED"
  ],
  "state": {
    "name": "RECOVERY",
    "confidence": 76
  }
}
```

---

# 24. Decision Engine Output

AI output nên compact:

```text
STATE:
RECOVERY

DRIVER:
Short covering

CONFIRMATION:
CVD positive
Auction improving
VPIN normalized

WARNING:
CVD divergence

REFERENCE:
POC5 63416
VP1 63800

NEXT DECISION:
Watch VP1 reaction
```

Không cần AI nhắc lại toàn bộ raw data.

---

# 25. Frontend UI

## Main Chart

Hiển thị:

```text
Price
POC5
POC30
VP1
VAH
VAL
EMA
```

## Smart markers

```text
🔺 CVD Divergence
🟢 Short Covering
🔴 Fresh Short
🟡 Exhaustion
🔵 POC5 Reclaim
```

Marker phải có tooltip.

---

# 26. Indicator Panel

### Flow State

```text
OI        SHORT UNWIND
CVD       POSITIVE
AUCTION   IMPROVING
VPIN      LOW STRESS
```

### Market State

```text
RECOVERY
Confidence 76
```

### Reference

```text
POC5  63416
VP1   63800
```

---

# 27. Realtime Architecture

```text
Exchange WebSocket
        ↓
Data Collector
        ↓
Normalizer
        ↓
Indicator Calculator
        ↓
Event Engine
        ↓
Reference Engine
        ↓
State Engine
        ↓
Signal Scoring
        ↓
Redis / Event Bus
        ↓
WebSocket API
        ↓
React UI
```

---

# 28. Recommended Tech Stack

## Frontend

```text
React
Next.js
TypeScript
TradingView Lightweight Charts
```

## Backend

```text
Python
FastAPI
NumPy
Pandas
```

## Storage

```text
PostgreSQL
TimescaleDB
```

## Realtime / Cache

```text
Redis
WebSocket
```

## AI Layer

```text
LLM
Decision Engine
Context Compressor
```

---

# 29. V1 Development Order

Không nên xây tất cả cùng lúc.

## Phase 1 — Data

```text
Price
OI
CVD
Auction
VPIN
POC5
VP1
```

## Phase 2 — Events

```text
OI Expansion
OI Unwind
CVD Divergence
Auction Shift
POC5 Reclaim
POC5 Rejection
VP1 Test
```

## Phase 3 — State

```text
Fresh Long
Fresh Short
Long Unwind
Short Covering
Recovery
Exhaustion
Trap
Rotation
```

## Phase 4 — Smart Markers

```text
Triangles
State markers
Reference markers
Confidence
```

## Phase 5 — ATS Decision Engine

```text
Context
+
Realtime Feed
+
State
+
Reference
↓
Compact Decision
```

---

# 30. Core Design Rule

### Indicator

```text
"What happened?"
```

### Event Engine

```text
"What changed?"
```

### State Engine

```text
"What does the combination mean?"
```

### Decision Engine

```text
"What matters now?"
```

### AI Trader

```text
"What should be monitored / considered next?"
```

---

# 31. Final Architecture

```text
                    ┌────────────────────┐
                    │ REALTIME BTC DATA  │
                    └─────────┬──────────┘
                              ↓
                    ┌────────────────────┐
                    │ DATA NORMALIZATION │
                    └─────────┬──────────┘
                              ↓
              ┌───────────────┼───────────────┐
              ↓               ↓               ↓
         INDICATORS        REFERENCES       HISTORY
              │           POC5 / VP1          │
              └───────────────┼───────────────┘
                              ↓
                    ┌────────────────────┐
                    │    EVENT ENGINE    │
                    └─────────┬──────────┘
                              ↓
                    ┌────────────────────┐
                    │    STATE ENGINE    │
                    └─────────┬──────────┘
                              ↓
                    ┌────────────────────┐
                    │  SIGNAL CONFIDENCE │
                    └─────────┬──────────┘
                              ↓
                    ┌────────────────────┐
                    │ CONTEXT COMPRESSOR │
                    └─────────┬──────────┘
                              ↓
                    ┌────────────────────┐
                    │  DECISION ENGINE   │
                    └─────────┬──────────┘
                              ↓
                    ┌────────────────────┐
                    │     AI TRADER      │
                    └────────────────────┘
```

---

# 32. Product Vision

Mục tiêu cuối cùng không phải là:

> “Một app có thật nhiều indicator.”

Mà là:

> **Một app có ít indicator hơn nhưng hiểu được quan hệ giữa chúng.**

Ví dụ thay vì hiển thị:

```text
OI -0.64
CVD +1k
Auction -6.8k
VPIN 0.29
RSI 67
```

app nói:

```text
RECOVERY

Primary driver:
SHORT COVERING

Flow:
CVD positive
Auction improving
VPIN normalized

Warning:
CVD divergence

Reference:
POC5 reclaimed
VP1 next decision zone

Confidence:
78%
```

Đây là điểm khác biệt cốt lõi giữa **Indicator Dashboard** và **Intelligent Market State Engine**.

---

## V1 Success Criteria

```text
✓ Realtime data ổn định
✓ OI direction được phân loại đúng
✓ CVD divergence được phát hiện theo swing
✓ Auction được so với EMA20
✓ VPIN state được phân loại
✓ POC5 / VP1 interaction được nhận diện
✓ Events có persistence
✓ State có confidence
✓ Contradiction được phát hiện
✓ AI nhận compact context
✓ UI hiển thị event/state thay vì chỉ raw values
```

**Kết quả kỳ vọng:**

```text
Raw Market Data
      ↓
Meaningful Events
      ↓
Market State
      ↓
Compact Context
      ↓
ATS Decision Engine
```

Đây là nền tảng để phát triển tiếp **ATS Indicator Engine V2 → AI Trader V5.x**.