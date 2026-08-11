# ATS — Event Engine + State Engine + Flow Matrix

> Compact specification cho 3 lớp cốt lõi của Intelligent Trading System.

---

# 1. EVENT ENGINE

## Vai trò

Event Engine trả lời:

> **“Cái gì vừa thay đổi?”**

Indicator chỉ cho biết giá trị. Event Engine biến sự thay đổi của nhiều giá trị thành **market event có ý nghĩa**.

```text
Raw Data
   ↓
Indicator Values
   ↓
Change / Relationship
   ↓
EVENT
```

## OI Events

### Fresh Long Expansion
```text
Price ↑
OI ↑ BuI
CVD ↑
```
→ `FRESH_LONG_EXPANSION`

### Fresh Short Expansion
```text
Price ↓
OI ↑ BeI
CVD ↓
Auction ↓
```
→ `FRESH_SHORT_EXPANSION`

### Short Covering
```text
Price ↑
OI ↓ BeO
CVD ↑ / stable
```
→ `SHORT_COVERING`

### Long Unwind
```text
Price ↓
OI ↓ BuO
CVD ↓ / stable
```
→ `LONG_UNWIND`

### Expansion Decay
```text
BeI
+1.05
→ +0.72
→ +0.44
→ +0.20
→ +0.02
→ BeO
```
→ `SHORT_EXPANSION_DECAY`

## CVD Events

Theo dõi:
```text
CVD direction
CVD slope
CVD acceleration
CVD deceleration
Price/CVD swing relationship
```

Core events:
```text
CVD_ACCELERATION
CVD_DECELERATION
CVD_BULLISH_DIVERGENCE
CVD_BEARISH_DIVERGENCE
CVD_CONFIRMATION
```

### Bearish Divergence
```text
Price:
High 1 < High 2

CVD:
High 1 > High 2
```
→ `CVD_BEARISH_DIVERGENCE`

### Bullish Divergence
```text
Price:
Low 1 > Low 2

CVD:
Low 1 < Low 2
```
→ `CVD_BULLISH_DIVERGENCE`

## Auction Events

So sánh:
```text
Auction_current
vs
Auction_EMA20
```

Events:
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
→ `AUCTION_IMPROVING`

## Reference Events

POC5:
```text
POC5_TEST
POC5_RECLAIM
POC5_REJECTION
POC5_ACCEPTANCE
```

VP1:
```text
VP1_TEST
VP1_RECLAIM
VP1_REJECTION
VP1_ACCEPTANCE
```

Range:
```text
REFERENCE_ROTATION
FAILED_BREAK
ACCEPTED_BREAK
```

Nguyên tắc:
```text
POC5 ≠ POC30
```

## Event Persistence

Mỗi event nên có:
```text
timestamp
strength
persistence
confirmation
invalidation
```

Ví dụ:
```text
CVD_DIVERGENCE
Strength: 72
Persistence: 4 bars
OI confirmation: Yes
Auction confirmation: No
```

---

# 2. STATE ENGINE

## Vai trò

State Engine trả lời:

> **“Toàn bộ flow hiện tại đang ở trạng thái nào?”**

```text
Events
  +
Price Structure
  +
OI
  +
CVD
  +
Auction
  +
VPIN
  +
References
       ↓
STATE
```

## Core States

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

## State Example — Short Covering

```text
Price ↑
OI ↓ BeO
CVD ↑
Auction improving
VPIN ↓
```

→ `SHORT_COVERING`

Nếu Price tiếp tục reclaim POC5:

```text
SHORT_COVERING
       ↓
RECOVERY
```

## State Example — Fresh Short

```text
Price ↓
OI ↑ BeI
CVD ↓
Auction ↓
VPIN ↑
```

→ `FRESH_SHORT_EXPANSION`

## State Transition

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
```

Tại VP1:

```text
       ┌─────────────────┐
       ↓                 ↓
VP1_REJECTION      VP1_ACCEPTANCE
       ↓                 ↓
RANGE_ROTATION     BULLISH_ACCEPTANCE
```

## Confidence

```text
0–30    Weak
31–50   Early
51–70   Moderate
71–85   Strong
86–100  Extreme
```

Confidence không phải xác suất thắng trade. Nó phản ánh **mức độ đồng thuận của evidence đối với State hiện tại**.

---

# 3. FLOW MATRIX

## Vai trò

Flow Matrix là mapping nhanh giữa:

```text
Price
+
OI Direction
+
CVD
```

để nhận diện **position behavior**.

## Core Matrix

| Price | OI | CVD | Primary Interpretation |
|---|---|---|---|
| ↑ | ↑ BuI | ↑ | Fresh Long |
| ↑ | ↓ BeO | ↑ | Short Covering |
| ↓ | ↑ BeI | ↓ | Fresh Short |
| ↓ | ↓ BuO | ↓ | Long Unwind |
| ↑ | ↑ BeI | ↓ | Short Trap Risk |
| ↓ | ↑ BuI | ↑ | Long Trap Risk |

## Fresh Long

```text
Price ↑
OI ↑ BuI
CVD ↑
```

→ `FRESH_LONG_EXPANSION`

## Short Covering

```text
Price ↑
OI ↓ BeO
CVD ↑
```

→ `SHORT_COVERING`

Quan trọng:

```text
Short Covering ≠ Fresh Long
```

## Fresh Short

```text
Price ↓
OI ↑ BeI
CVD ↓
```

→ `FRESH_SHORT_EXPANSION`

## Long Unwind

```text
Price ↓
OI ↓ BuO
CVD ↓
```

→ `LONG_UNWIND`

---

# 4. FLOW MATRIX + EVENT ENGINE

Flow Matrix nhận diện **base behavior**.

Event Engine phát hiện **change**.

Ví dụ:

```text
Price ↑
OI BeO
CVD ↑
```

Flow Matrix:
```text
SHORT_COVERING
```

Event Engine:
```text
CVD acceleration ↑
Auction improving
POC5 reclaimed
```

→ State Engine nâng:

```text
SHORT_COVERING
      ↓
RECOVERY
```

---

# 5. FLOW MATRIX + STATE ENGINE

Không dùng Flow Matrix như absolute signal.

Ví dụ:

```text
Price ↑
OI BeO
CVD ↑
```

Có thể là:
```text
SHORT_COVERING
```

Nhưng nếu:
```text
Auction ↓
CVD weakening
VPIN ↑
VP1 rejection
```

thì State có thể chuyển thành:
```text
RECOVERY_EXHAUSTION
```

Do đó:

```text
Flow Matrix
= Base Classification

Event Engine
= What changed?

State Engine
= What does the combination mean?
```

---

# 6. THREE-LAYER MODEL

```text
                 RAW MARKET DATA
                        ↓
              ┌─────────────────┐
              │   FLOW MATRIX   │
              │                 │
              │ Price + OI+CVD  │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │  EVENT ENGINE   │
              │                 │
              │ What changed?   │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │  STATE ENGINE   │
              │                 │
              │ What does it    │
              │ mean together?  │
              └────────┬────────┘
                       ↓
                 MARKET STATE
```

---

# 7. DESIGN PRINCIPLE

### Flow Matrix
> **Behavior**

### Event Engine
> **Change**

### State Engine
> **Meaning**

Hay nói ngắn gọn:

```text
FLOW
"What are participants doing?"

EVENT
"What just changed?"

STATE
"What is the market becoming?"
```

---

# 8. ATS COMPACT OUTPUT

Thay vì trả về hàng loạt raw indicators:

```text
OI -0.64
CVD +1k
Auction -6.8k
VPIN 0.29
RSI 67
```

Engine nên trả:

```text
STATE:
RECOVERY

DRIVER:
SHORT COVERING

FLOW:
OI → BeO
CVD → Positive
Auction → Improving
VPIN → Low Stress

EVENT:
CVD Bearish Divergence

REFERENCE:
POC5 → Reclaimed
VP1 → Next Decision Zone

CONFIDENCE:
78
```

---

# 9. CORE PRINCIPLE

> **Một app không cần thật nhiều indicator.**

> **Một app cần hiểu quan hệ giữa những indicator quan trọng.**

```text
Indicator
   ↓
Flow
   ↓
Event
   ↓
State
   ↓
Decision
```

**Flow Matrix + Event Engine + State Engine** là lõi để biến một Trading Dashboard thành một **Intelligent Market State Engine**.