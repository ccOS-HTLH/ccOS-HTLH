# ATS — Flow State Matrix
## Intelligent Flow Classification Layer

> Mục tiêu: biến quan hệ giữa **Price + OI + CVD** thành một lớp phân loại flow đơn giản, dễ đọc và có thể dùng làm nền cho Event Engine + State Engine.

---

# 1. Core Concept

Flow State Matrix không hỏi:

> “Indicator này đang tăng hay giảm?”

Mà hỏi:

> **“Participant đang làm gì với vị thế của họ?”**

Ba input chính:

```text
PRICE
  +
OI DIRECTION
  +
CVD
  ↓
FLOW STATE
```

---

# 2. Core Matrix

| Price | OI | CVD | Flow State | Interpretation |
|---|---|---|---|---|
| ↑ | ↑ BuI | ↑ | **Fresh Long** | Long mới đang được mở rộng |
| ↑ | ↓ BeO | ↑ | **Short Covering** | Short cũ đang đóng |
| ↓ | ↑ BeI | ↓ | **Fresh Short** | Short mới đang được mở rộng |
| ↓ | ↓ BuO | ↓ | **Long Unwind** | Long cũ đang đóng |
| ↑ | ↑ BeI | ↓ | **Short Trap Risk** | Short tăng nhưng Price không giảm |
| ↓ | ↑ BuI | ↑ | **Long Trap Risk** | Long tăng nhưng Price không tăng |

---

# 3. Fresh Long

```text
Price ↑
OI ↑ BuI
CVD ↑
```

### Meaning

```text
New long participation
+
Aggressive buying
+
Price acceptance higher
```

State:

```text
FRESH_LONG_EXPANSION
```

### Stronger confirmation

```text
Auction ↑
Volume ↑
Price above reference
```

→ Fresh Long quality tăng.

---

# 4. Short Covering

```text
Price ↑
OI ↓ BeO
CVD ↑
```

### Meaning

```text
Short positions are being closed
```

Đây là điểm cực kỳ quan trọng:

```text
SHORT COVERING
        ≠
FRESH LONG
```

Price tăng không đồng nghĩa với Long mới.

### Confirmation

```text
OI ↓ BeO
CVD ↑
Auction improving
VPIN ↓
```

→ Short Covering mạnh hơn.

Nếu sau đó:

```text
OI → BuI
CVD ↑
Price acceptance
```

thì có thể chuyển:

```text
SHORT_COVERING
        ↓
FRESH_LONG_EXPANSION
```

---

# 5. Fresh Short

```text
Price ↓
OI ↑ BeI
CVD ↓
```

### Meaning

```text
New short participation
+
Aggressive selling
+
Price acceptance lower
```

State:

```text
FRESH_SHORT_EXPANSION
```

### Stronger confirmation

```text
Auction ↓
Volume ↑
Price below reference
```

---

# 6. Long Unwind

```text
Price ↓
OI ↓ BuO
CVD ↓
```

### Meaning

```text
Existing longs are exiting
```

Đây không giống Fresh Short:

```text
LONG_UNWIND
        ≠
FRESH_SHORT
```

Fresh Short:

```text
OI ↑ BeI
```

Long Unwind:

```text
OI ↓ BuO
```

---

# 7. Short Trap Risk

```text
Price ↑
OI ↑ BeI
CVD ↓
```

### Meaning

Short participation tăng nhưng Price không giảm.

Có khả năng:

```text
Shorts entering
        ↓
Price refuses to fall
        ↓
Shorts become trapped
```

State:

```text
SHORT_TRAP_RISK
```

### Strong confirmation

```text
Price ↑
OI ↑ BeI
CVD divergence
Auction improving
Price reclaims POC5
```

→ Short Trap Risk tăng mạnh.

Nếu shorts bắt đầu unwind:

```text
OI BeI
   ↓
OI BeO
   ↓
Price ↑
```

→ có thể chuyển:

```text
SHORT_TRAP
   ↓
SHORT_COVERING
```

---

# 8. Long Trap Risk

```text
Price ↓
OI ↑ BuI
CVD ↑
```

### Meaning

Long participation tăng nhưng Price không thể tăng.

Có khả năng:

```text
Longs entering
       ↓
Price refuses to rise
       ↓
Longs become trapped
```

State:

```text
LONG_TRAP_RISK
```

Nếu Longs bắt đầu unwind:

```text
OI BuI
   ↓
OI BuO
   ↓
Price ↓
```

→ có thể chuyển:

```text
LONG_TRAP
   ↓
LONG_UNWIND
```

---

# 9. Matrix Interpretation Hierarchy

Flow Matrix nên được đọc theo 3 tầng:

```text
TIER 1
Price Direction

       ↓

TIER 2
OI Participation

       ↓

TIER 3
CVD Confirmation
```

Ví dụ:

```text
Price ↑
```

chưa đủ để nói Bullish.

Phải hỏi:

```text
OI ↑ BuI ?
```

Nếu có:

```text
Fresh Long
```

Nếu:

```text
OI ↓ BeO
```

thì:

```text
Short Covering
```

Nếu:

```text
OI ↑ BeI
CVD ↓
```

thì:

```text
Short Trap Risk
```

---

# 10. Flow Matrix + Auction

Flow Matrix chỉ phân loại **position behavior**.

Auction giúp xác định **quality**.

Ví dụ:

```text
Price ↑
OI ↓ BeO
CVD ↑
```

→ Short Covering.

Nếu:

```text
Auction ↑
```

→ Recovery quality tốt hơn.

Nếu:

```text
Auction ↓
```

→ Recovery yếu.

Do đó:

```text
FLOW STATE
+
AUCTION
=
FLOW QUALITY
```

---

# 11. Flow Matrix + VPIN

VPIN không xác định direction.

VPIN trả lời:

> **“Flow đang stressed đến mức nào?”**

Ví dụ:

```text
SHORT_COVERING
+
VPIN ↓
```

→ Covering diễn ra trong môi trường stress giảm.

Trong khi:

```text
SHORT_COVERING
+
VPIN ↑
```

→ Có thể đang xảy ra forced / aggressive positioning.

---

# 12. Flow Matrix + Reference

Flow State trở nên mạnh hơn khi gắn với:

```text
POC5
POC30
VP1
VAH
VAL
```

Ví dụ:

```text
SHORT_COVERING
+
POC5_RECLAIM
```

→ Recovery quality tăng.

Ví dụ:

```text
SHORT_COVERING
+
VP1_REJECTION
+
CVD_DIVERGENCE
```

→ Recovery exhaustion risk tăng.

---

# 13. Flow State Transition Matrix

```text
FRESH_SHORT
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

Hoặc:

```text
FRESH_LONG
     ↓
LONG_EXPANSION
     ↓
EXHAUSTION
     ↓
LONG_UNWIND
     ↓
BEARISH_PRESSURE
```

Trap scenario:

```text
SHORT_TRAP_RISK
       ↓
SHORT_COVERING
       ↓
RECOVERY
```

```text
LONG_TRAP_RISK
       ↓
LONG_UNWIND
       ↓
BEARISH_PRESSURE
```

---

# 14. Compact Decision Table

| Flow | Main Driver | Typical Meaning | Risk |
|---|---|---|---|
| Fresh Long | New Longs | Bullish expansion | Long exhaustion |
| Short Covering | Shorts exiting | Bullish recovery | Recovery exhaustion |
| Fresh Short | New Shorts | Bearish expansion | Short exhaustion |
| Long Unwind | Longs exiting | Bearish pressure | Selling exhaustion |
| Short Trap Risk | Shorts trapped | Potential squeeze | False breakout |
| Long Trap Risk | Longs trapped | Potential flush | False breakdown |

---

# 15. Important Distinction

### Price ↑ does NOT automatically mean Fresh Long.

Có ít nhất hai trường hợp:

```text
Price ↑ + OI ↑ BuI
→ Fresh Long
```

và:

```text
Price ↑ + OI ↓ BeO
→ Short Covering
```

Tương tự:

### Price ↓ does NOT automatically mean Fresh Short.

```text
Price ↓ + OI ↑ BeI
→ Fresh Short
```

nhưng:

```text
Price ↓ + OI ↓ BuO
→ Long Unwind
```

Đây là một trong những lý do OI trở thành biến rất quan trọng trong ATS.

---

# 16. Flow State Matrix → Event Engine

Flow Matrix:

```text
Price ↑
OI ↓ BeO
CVD ↑
```

→

```text
SHORT_COVERING
```

Event Engine tiếp tục hỏi:

```text
CVD có acceleration không?
Auction có cải thiện không?
POC5 có reclaim không?
VP1 đang ở đâu?
VPIN đang tăng hay giảm?
```

Sau đó có thể tạo:

```text
SHORT_COVERING
+
CVD_ACCELERATION
+
POC5_RECLAIM
+
AUCTION_IMPROVING
```

→ State:

```text
RECOVERY
```

---

# 17. Flow State Matrix → State Engine

Flow Matrix là **base classification**.

Event Engine là **change detector**.

State Engine là **synthesis**.

```text
FLOW MATRIX
"What are participants doing?"

        ↓

EVENT ENGINE
"What just changed?"

        ↓

STATE ENGINE
"What is the market becoming?"
```

---

# 18. ATS Compact Output

Raw:

```text
Price     ↑
OI        -0.64 BeO
CVD       +1k
Auction   -6.8k
VPIN      0.29
```

Flow Matrix:

```text
SHORT COVERING
```

Event Engine:

```text
CVD positive
Auction improving
POC5 reclaimed
CVD divergence warning
```

State Engine:

```text
RECOVERY
Confidence: 78
```

Decision context:

```text
PRIMARY DRIVER:
Short Covering

STATE:
Recovery

WARNING:
CVD divergence

REFERENCE:
VP1 = next decision zone
```

---

# 19. Core Principle

> **Flow Matrix không dự đoán giá.**

Nó xác định:

> **“Ai đang làm gì?”**

```text
Price
  +
OI
  +
CVD
   ↓
WHO IS DOING WHAT?
   ↓
FLOW STATE
```

Sau đó:

```text
Flow State
   +
Events
   +
Reference
   +
Auction
   +
VPIN
   ↓
MARKET STATE
```

---

# 20. Final Model

```text
                  PRICE
                    │
                    ▼
              ┌───────────┐
              │ FLOW      │
        OI ──►│  MATRIX   │◄── CVD
              └─────┬─────┘
                    │
             Participant
              Behavior
                    ↓
              ┌───────────┐
              │  EVENT    │
              │  ENGINE   │
              └─────┬─────┘
                    │
              What changed?
                    ↓
              ┌───────────┐
              │  STATE    │
              │  ENGINE   │
              └─────┬─────┘
                    │
               Market State
                    ↓
              DECISION ENGINE
```

> **Flow Matrix = Behavior**  
> **Event Engine = Change**  
> **State Engine = Meaning**

Đây là lớp nền để ATS có thể có **ít indicator hơn nhưng hiểu quan hệ giữa chúng sâu hơn**.