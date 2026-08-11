# ATS — Market Context Matrix
## Price + OI + CVD + Auction + VPIN + POC5/VP1

> **Tên file:** `ATS_Market_Context_Matrix.md`
>
> Mục tiêu: tạo một bảng context thống nhất để ATS đọc **Price + Positioning + Flow + Auction + Stress + Reference** như một hệ thống liên kết, thay vì đọc từng indicator riêng lẻ.

---

# 1. Core Model

```text
PRICE
  +
OI
  +
CVD
  +
AUCTION
  +
VPIN
  +
POC5 / VP1
       ↓
MARKET CONTEXT
       ↓
EVENT
       ↓
STATE
       ↓
DECISION
```

Vai trò của từng lớp:

| Component | Câu hỏi |
|---|---|
| Price | Giá đang làm gì? |
| OI | Position đang được mở hay đóng? |
| CVD | Aggressive flow đang nghiêng bên nào? |
| Auction | Flow/auction đang cải thiện hay xấu đi? |
| VPIN | Mức độ stress/imbalance là bao nhiêu? |
| POC5 / VP1 | Giá đang ở đâu trong reference structure? |

---

# 2. Master Context Matrix

| Price | OI | CVD | Auction | VPIN | POC5/VP1 | Primary Context |
|---|---|---|---|---|---|---|
| ↑ | ↑ BuI | ↑ | ↑ | ↓/normal | Above POC5 / toward VP1 | **Fresh Bullish Expansion** |
| ↑ | ↑ BuI | ↑ | ↑ | ↑ | Reclaim POC5 | **Strong Long Expansion** |
| ↑ | ↓ BeO | ↑ | ↑ | ↓ | Reclaim POC5 | **Short Covering → Recovery** |
| ↑ | ↓ BeO | ↑ | ↓ | ↑ | Reject VP1 | **Short Covering Exhaustion Risk** |
| ↓ | ↑ BeI | ↓ | ↓ | ↑ | Below POC5 / toward VP1 | **Fresh Bearish Expansion** |
| ↓ | ↑ BeI | ↓ | ↓ | ↑ | Reject POC5 | **Strong Short Expansion** |
| ↓ | ↓ BuO | ↓ | ↓ | ↓/normal | Lose POC5 | **Long Unwind → Bearish Pressure** |
| ↓ | ↓ BuO | ↓ | ↑ | ↓ | Near POC5 | **Selling Exhaustion Risk** |
| ↑ | ↑ BeI | ↓ | ↑ | ↑ | Reclaim POC5 | **Short Trap Risk** |
| ↓ | ↑ BuI | ↑ | ↓ | ↑ | Lose POC5 | **Long Trap Risk** |
| ↑ | mixed | ↑ | ↑ | normal | Between POC5 ↔ VP1 | **Recovery / Rotation** |
| ↓ | mixed | ↓ | ↓ | normal | Between POC5 ↔ VP1 | **Bearish Rotation** |
| ↑/↓ | weak | mixed | mixed | high | At VP1 | **Decision Zone / Stress** |
| ↑/↓ | weak | mixed | mixed | low | POC5 ↔ VP1 | **Balance / Rotation** |

> Đây là **context classification**, không phải automatic entry/exit signal.

---

# 3. Price + OI + CVD Base Matrix

| Price | OI | CVD | Flow Interpretation |
|---|---|---|---|
| ↑ | ↑ BuI | ↑ | **Fresh Long** |
| ↑ | ↓ BeO | ↑ | **Short Covering** |
| ↓ | ↑ BeI | ↓ | **Fresh Short** |
| ↓ | ↓ BuO | ↓ | **Long Unwind** |
| ↑ | ↑ BeI | ↓ | **Short Trap Risk** |
| ↓ | ↑ BuI | ↑ | **Long Trap Risk** |

Core principle:

```text
Price ↑ ≠ automatically Long
Price ↓ ≠ automatically Short
```

Cần đọc Price cùng OI để biết:

```text
New Position
hay
Position Exit
```

---

# 4. Auction Layer

Auction được đọc theo:

```text
Auction_current
vs
Auction_EMA20
```

### Auction states

```text
AUCTION_BULLISH
AUCTION_BEARISH
AUCTION_IMPROVING
AUCTION_DETERIORATING
AUCTION_EXHAUSTION
```

### Context

| Flow | Auction | Interpretation |
|---|---|---|
| Fresh Long | Improving | Long expansion quality ↑ |
| Fresh Long | Deteriorating | Expansion quality ↓ |
| Short Covering | Improving | Recovery quality ↑ |
| Short Covering | Deteriorating | Recovery exhaustion risk |
| Fresh Short | Deteriorating | Short expansion quality ↑ |
| Fresh Short | Improving | Bearish pressure weakening |
| Long Unwind | Deteriorating | Bearish pressure ↑ |
| Long Unwind | Improving | Selling exhaustion risk |

Ví dụ:

```text
Auction = -6.8k
EMA20   = -8.7k
```

→ Auction đang **improving** vì giá trị hiện tại ít âm hơn baseline.

---

# 5. VPIN Layer

VPIN chủ yếu đo:

```text
FLOW STRESS
```

Không dùng VPIN một mình để xác định direction.

| VPIN | Context |
|---|---|
| < 0.30 | Low Stress |
| 0.30–0.50 | Normal |
| 0.50–0.70 | Elevated |
| 0.70–0.85 | High |
| > 0.85 | Extreme |

### Flow + VPIN

| Flow State | VPIN | Interpretation |
|---|---|---|
| Fresh Long | Low | Controlled expansion |
| Fresh Long | High | Aggressive / stressed expansion |
| Fresh Short | Low | Controlled bearish expansion |
| Fresh Short | High | Aggressive / stressed selling |
| Short Covering | Falling | Recovery quality ↑ |
| Short Covering | Rising | Potential forced covering |
| Long Unwind | Falling | Selling stress reducing |
| Long Unwind | Rising | Potential forced liquidation |

---

# 6. POC5 / VP1 Reference Layer

> **POC5 ≠ POC30**

POC5:

```text
Short-term active reference
```

VP1:

```text
Next major reference / opposing decision zone
```

Core events:

```text
POC5_TEST
POC5_RECLAIM
POC5_REJECTION
POC5_ACCEPTANCE

VP1_TEST
VP1_RECLAIM
VP1_REJECTION
VP1_ACCEPTANCE
```

---

# 7. Price Location Matrix

| Price Location | Interpretation |
|---|---|
| Above POC5 | Short-term bullish acceptance candidate |
| Below POC5 | Short-term bearish acceptance candidate |
| Exactly around POC5 | Immediate decision / balance |
| Between POC5 and VP1 | Potential rotation zone |
| Approaching VP1 | Major decision zone |
| Rejected from VP1 | Rotation back toward POC5 |
| Accepted beyond VP1 | Structure expansion |
| Failed break beyond VP1 | Trap / reversal risk |

---

# 8. POC5 ↔ VP1 Rotation Model

Core pattern:

```text
VP1
 │
 │
 │   Price
 │    ↕
 │
POC5
```

Nếu Price không thể tạo acceptance ra ngoài vùng:

```text
POC5 ↔ VP1
```

thì theo dõi:

```text
POC5 → VP1
```

hoặc:

```text
VP1 → POC5
```

### Rotation logic

```text
POC5 rejection
      ↓
Price remains inside range
      ↓
VP1 becomes next reference
```

Ngược lại:

```text
VP1 rejection
      ↓
Price remains inside range
      ↓
POC5 becomes next reference
```

---

# 9. Full Context Combinations

## A. Fresh Bullish Expansion

```text
Price ↑
OI ↑ BuI
CVD ↑
Auction ↑
VPIN normal / rising
Price above POC5
```

Context:

```text
FRESH_BULLISH_EXPANSION
```

Quality ↑ nếu:

```text
POC5 reclaimed
Auction improving
CVD accelerating
```

---

## B. Short Covering Recovery

```text
Price ↑
OI ↓ BeO
CVD ↑
Auction improving
VPIN falling
POC5 reclaimed
```

Context:

```text
SHORT_COVERING_RECOVERY
```

Next reference:

```text
VP1
```

---

## C. Short Covering Exhaustion

```text
Price ↑
OI ↓ BeO
CVD ↑ but weakening
Auction deteriorating
VPIN rising
VP1 rejection
```

Context:

```text
SHORT_COVERING_EXHAUSTION
```

Warning:

```text
Recovery may fail
```

---

## D. Fresh Bearish Expansion

```text
Price ↓
OI ↑ BeI
CVD ↓
Auction ↓
VPIN ↑
Price below POC5
```

Context:

```text
FRESH_BEARISH_EXPANSION
```

---

## E. Long Unwind

```text
Price ↓
OI ↓ BuO
CVD ↓
Auction ↓
VPIN elevated
POC5 lost
```

Context:

```text
LONG_UNWIND
```

---

## F. Short Trap

```text
Price ↑
OI ↑ BeI
CVD ↓ / weak
Auction ↑
VPIN ↑
POC5 reclaimed
```

Context:

```text
SHORT_TRAP_RISK
```

If:

```text
OI switches BeI → BeO
```

then:

```text
SHORT_TRAP
      ↓
SHORT_COVERING
```

---

## G. Long Trap

```text
Price ↓
OI ↑ BuI
CVD ↑ / weak
Auction ↓
VPIN ↑
POC5 lost
```

Context:

```text
LONG_TRAP_RISK
```

If:

```text
OI switches BuI → BuO
```

then:

```text
LONG_TRAP
      ↓
LONG_UNWIND
```

---

# 10. Context Quality Matrix

Flow direction alone is insufficient.

ATS should score context using:

```text
Flow
+
Auction
+
VPIN
+
Reference
+
Persistence
+
Contradiction
```

Example:

```text
SHORT_COVERING
```

### High quality

```text
CVD ↑
Auction ↑
VPIN ↓
POC5 reclaimed
Price acceptance
```

### Low quality

```text
CVD ↑ but weakening
Auction ↓
VPIN ↑
VP1 rejection
CVD divergence
```

Same base flow:

```text
SHORT_COVERING
```

but completely different context quality.

---

# 11. Contradiction Matrix

ATS phải phát hiện khi components không đồng thuận.

| Situation | Interpretation |
|---|---|
| Price ↑ + OI BuI + CVD ↓ | Long expansion disagreement |
| Price ↑ + OI BeO + CVD ↓ | Weak covering |
| Price ↓ + OI BeI + CVD ↑ | Short expansion disagreement |
| Price ↓ + OI BuO + CVD ↑ | Weak long unwind |
| Price ↑ + Auction ↓ | Rally quality warning |
| Price ↓ + Auction ↑ | Sell pressure weakening |
| Price ↑ + VP1 rejection | Upside acceptance failed |
| Price ↓ + POC5 reclaim | Downside acceptance failed |

Output:

```text
CONTEXT_CONFLICT
```

Confidence phải giảm.

---

# 12. Context Score

Suggested scoring:

```text
Flow Alignment       0–25
CVD Confirmation     0–20
Auction Confirmation 0–15
VPIN Context         0–10
Reference Structure  0–20
Persistence           0–10
Contradiction         -20 → 0
```

Maximum:

```text
100
```

Interpretation:

```text
0–30    Weak
31–50   Early
51–70   Moderate
71–85   Strong
86–100  Extreme
```

> Score là **context confidence**, không phải xác suất trade thắng.

---

# 13. State Mapping

```text
Market Context
      ↓
Flow Classification
      ↓
Events
      ↓
State
```

Ví dụ:

```text
Price ↑
OI BeO
CVD ↑
Auction ↑
VPIN ↓
POC5 reclaimed
```

↓

```text
FLOW:
SHORT_COVERING
```

↓

```text
EVENTS:
SHORT_UNWIND
CVD_CONFIRMATION
AUCTION_IMPROVING
POC5_RECLAIM
```

↓

```text
STATE:
RECOVERY
```

---

# 14. Compact Context Output

Raw data:

```text
Price 63618
OI -0.61 BeO
CVD +347
Auction -7.1k
Auction EMA20 -8.4k
VPIN 0.32
POC5 63416
VP1 63800
```

ATS Context:

```text
FLOW:
Short Covering

AUCTION:
Improving

VPIN:
Low Stress

REFERENCE:
Above POC5
Approaching VP1

EVENTS:
POC5 Reclaim
CVD Divergence Warning

STATE:
Recovery

CONFIDENCE:
78
```

---

# 15. Decision Engine Handoff

Market Context Matrix không trực tiếp ra lệnh:

```text
BUY
SELL
```

Nó cung cấp:

```text
WHAT IS HAPPENING?
WHY?
WHERE?
HOW STRONG?
WHAT IS THE NEXT DECISION ZONE?
WHAT CAN INVALIDATE THE STATE?
```

Ví dụ:

```text
STATE:
RECOVERY

DRIVER:
SHORT COVERING

QUALITY:
STRONG

REFERENCE:
VP1 = 63800

WARNING:
CVD divergence

INVALIDATION:
Loss of POC5 + renewed BeI
```

---

# 16. Final Architecture

```text
                 REALTIME DATA
                      ↓
        ┌─────────────────────────┐
        │  MARKET CONTEXT MATRIX  │
        │                         │
        │ Price                   │
        │ OI                      │
        │ CVD                     │
        │ Auction                 │
        │ VPIN                    │
        │ POC5 / VP1              │
        └────────────┬────────────┘
                     ↓
              FLOW CLASSIFICATION
                     ↓
                EVENT ENGINE
                     ↓
                STATE ENGINE
                     ↓
             CONTEXT CONFIDENCE
                     ↓
              DECISION ENGINE
```

---

# 17. Core Philosophy

> **Price tells us what the market is doing.**

> **OI tells us whether positions are being created or removed.**

> **CVD tells us how aggressive flow is behaving.**

> **Auction tells us whether that flow is improving or deteriorating.**

> **VPIN tells us how stressed the flow is.**

> **POC5/VP1 tell us where the current behavior matters.**

Khi ghép lại:

```text
Price
+
Positioning
+
Flow
+
Auction
+
Stress
+
Reference
        ↓
MARKET CONTEXT
```

Và đó chính là mục tiêu của **ATS Market Context Matrix**:

> **Không cần thật nhiều indicator — cần hiểu sâu quan hệ giữa những indicator quan trọng.**