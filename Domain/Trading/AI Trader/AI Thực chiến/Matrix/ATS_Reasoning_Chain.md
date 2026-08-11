# ATS — Reasoning Chain
## Market Context → Event → State → Decision

> Chuỗi reasoning cốt lõi của ATS: biến nhiều indicator thành một kết luận ngắn, có context và có thể kiểm chứng.

---

# 1. Core Chain

```text
REALTIME DATA
     ↓
MARKET CONTEXT
     ↓
FLOW CLASSIFICATION
     ↓
EVENT ENGINE
     ↓
STATE ENGINE
     ↓
DECISION ENGINE
```

---

# 2. Market Context

Input chính:

```text
Price
OI
CVD
Auction
VPIN
POC5 / VP1
```

Mục tiêu:

> **What is happening?**

Ví dụ:

```text
Price ↑
OI ↓ BeO
CVD ↑
Auction improving
VPIN ↓
POC5 reclaimed
VP1 ahead
```

↓

```text
MARKET CONTEXT:
Bullish recovery context
```

---

# 3. Flow Classification

Flow State Matrix xác định:

> **What are participants doing?**

Ví dụ:

```text
Price ↑
OI ↓ BeO
CVD ↑
```

↓

```text
SHORT COVERING
```

Phân biệt:

```text
Price ↑ + OI ↑ BuI
→ Fresh Long

Price ↑ + OI ↓ BeO
→ Short Covering

Price ↓ + OI ↑ BeI
→ Fresh Short

Price ↓ + OI ↓ BuO
→ Long Unwind
```

---

# 4. Event Engine

Event Engine hỏi:

> **What just changed?**

Nó không chỉ nhìn trạng thái hiện tại mà so sánh với trước đó.

Ví dụ:

```text
SHORT COVERING
        ↓
CVD accelerating
Auction improving
POC5 reclaimed
```

Events:

```text
CVD_ACCELERATION
AUCTION_IMPROVING
POC5_RECLAIM
```

---

# 5. State Engine

State Engine hỏi:

> **What does the combination mean?**

Kết hợp:

```text
Flow
+
Events
+
Price Structure
+
Reference
+
Persistence
+
Contradictions
```

Ví dụ:

```text
SHORT COVERING
+
CVD_ACCELERATION
+
AUCTION_IMPROVING
+
POC5_RECLAIM
```

↓

```text
STATE:
RECOVERY
```

---

# 6. Context Quality

Không phải mọi `RECOVERY` đều giống nhau.

### Strong Recovery

```text
CVD ↑
Auction ↑
VPIN ↓
POC5 reclaimed
Price acceptance
```

### Weak Recovery

```text
CVD weakening
Auction ↓
VPIN ↑
VP1 rejection
CVD divergence
```

Vì vậy ATS cần phân biệt:

```text
STATE
+
QUALITY
+
CONFIDENCE
```

---

# 7. Reference Layer

POC5 và VP1 trả lời:

> **Where does this behavior matter?**

Ví dụ:

```text
SHORT COVERING
        ↓
POC5 RECLAIM
        ↓
VP1 TEST
```

Tại VP1:

```text
VP1 rejection
→ Recovery Exhaustion Risk

VP1 acceptance
→ Recovery continuation
```

---

# 8. Contradiction Check

Trước khi kết luận, ATS phải hỏi:

```text
Do all major components agree?
```

Ví dụ:

```text
Price ↑
OI BeO
CVD ↑
Auction ↓
VPIN ↑
VP1 rejection
```

Flow:

```text
SHORT COVERING
```

nhưng context quality thấp.

↓

```text
RECOVERY
WARNING:
EXHAUSTION RISK
```

---

# 9. Decision Engine

Decision Engine nhận:

```text
Context
+
Flow
+
Events
+
State
+
Quality
+
Reference
+
Warnings
```

và compact thành:

```text
STATE:
Recovery

DRIVER:
Short Covering

QUALITY:
Moderate

EVENT:
POC5 Reclaim

REFERENCE:
VP1

WARNING:
CVD Divergence

CONFIDENCE:
72
```

> Decision Engine **không cần lặp lại toàn bộ raw indicators**.

---

# 10. The Full Reasoning Example

```text
RAW
Price ↑
OI ↓ BeO
CVD ↑
Auction improving
VPIN ↓
POC5 reclaimed
VP1 ahead
```

↓

```text
CONTEXT
Bullish recovery environment
```

↓

```text
FLOW
SHORT COVERING
```

↓

```text
EVENTS
CVD acceleration
Auction improving
POC5 reclaim
```

↓

```text
STATE
RECOVERY
```

↓

```text
REFERENCE
VP1 = next decision zone
```

↓

```text
QUALITY
Strong
```

↓

```text
DECISION CONTEXT
Recovery toward VP1;
watch acceptance/rejection.
```

---

# 11. Core Principle

```text
Indicator
   ↓
Relationship
   ↓
Context
   ↓
Flow
   ↓
Event
   ↓
State
   ↓
Reference
   ↓
Quality
   ↓
Decision
```

### Một câu tóm gọn

> **Market Context nói “đang xảy ra gì”.  
> Flow Matrix nói “ai đang làm gì”.  
> Event Engine nói “cái gì vừa thay đổi”.  
> State Engine nói “thị trường đang trở thành gì”.  
> Decision Engine nói “điều gì đáng quan tâm nhất lúc này”.**