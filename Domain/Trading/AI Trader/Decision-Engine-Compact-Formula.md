# Decision Engine — Compact Formula

Phiên bản: 0.1

---

# 1. Core Formula

Context + Realtime Feed
        ↓
Decision Engine
        ↓
Compact Decision

---

# 2. Context

Context là trạng thái nền của thị trường.

Có thể bao gồm:

- Trading Domain
- HTF Structure
- Market Structure
- Multi-Timeframe Bias
- Volume Profile
- Liquidity
- Orderbook
- Liquidation
- Funding
- OI Structure
- CVD Context
- Auction Flow Context
- Market Regime
- Existing Trade / Position State

Context trả lời:

> "Thị trường đang ở trạng thái nào?"

---

# 3. Realtime Feed

Realtime Feed là dữ liệu biến động theo thời gian thực.

Ví dụ:

- Price
- POC5
- OI Change
- OI Flow Type
- CVD
- Auction Line
- Auction Line vs EMA20
- RSI
- Delta
- Volume
- Liquidation Events
- Signal / Marker Events

Realtime Feed trả lời:

> "Điều gì đang xảy ra ngay lúc này?"

---

# 4. Context + Realtime Feed

Context:

    Stable / Structural

Realtime Feed:

    Dynamic / Immediate

Do đó:

Context
+
Realtime Feed
=
Current Market State

---

# 5. Current Market State

Decision Engine tổng hợp:

- Structural Bias
- Current Flow
- Momentum
- Key Levels
- Confirmation State
- Invalidation State
- Risk State

để tạo:

Current Market State

Ví dụ:

    Bearish HTF
    +
    M5 Recovery
    +
    Price above POC5
    +
    BuI
    +
    Auction > EMA20
    +
    CVD still negative

→

    Bullish Recovery Candidate
    inside Bearish Structure

---

# 6. Decision Compression

Current Market State
        ↓
Decision Filter
        ↓
Compact Decision

Decision Engine không cần xuất toàn bộ quá trình suy luận.

---

# 7. Compact Decision Format

```text
Bias:
[Market Bias]

Decision:
[LONG / SHORT / HOLD / WAIT CONFIRMATION / NO TRADE]

Confidence:
[0–100%]

Key Level:
[Decision Level]

Invalidation:
[Invalidation Level / Condition]

Next Action:
[Next Action]
```

---

# 8. Compact Decision Example

Input:

```text
Context:

HTF Bias = Bearish
POC30 = 64993
VAL30 = 63960
VP1 = 64092

Realtime Feed:

Price = 64015
POC5 = 63800
OI = +0.03% BeI
CVD = -638
Auction = -2.4k
EMA20 = -2.1k
RSI = 37
```

Decision Engine:

```text
Bias:
BEARISH

Decision:
WAIT CONFIRMATION

Confidence:
84%

Key Level:
64092 VP1

Invalidation:
Reclaim and acceptance above 64092
with bullish flow confirmation

Next Action:
Monitor 64092 and 63800
```

---

# 9. Why the Output Is Compact

Nếu thông tin đã có trong Context, Decision Engine không cần lặp lại toàn bộ:

- Trading Domain
- Market Analysis
- Indicator Definitions
- Historical Data
- Multi-Timeframe Analysis
- Internal Reasoning

Decision Engine chủ yếu cần trả lời:

```text
What is the Bias?
What is the Decision?
What confirms it?
What invalidates it?
What happens next?
```

---

# 10. Decision Compression Principle

> Deep Context → Simple Decision

Không phải:

> Simple Context → Simple Decision

Mà là:

```text
Deep Context
+
Realtime Data
+
Structured Reasoning
        ↓
Compact Decision
```

Output càng ngắn không có nghĩa hệ thống càng đơn giản.

Một Decision ngắn có thể là kết quả của một quá trình đánh giá rất sâu.

---

# 11. 10-Layer Reasoning Relationship

```text
Trading Domain
      ↓
Layer 1
      ↓
Layer 2
      ↓
Layer 3
      ↓
Layer 4
      ↓
Layer 5
      ↓
Layer 6
      ↓
Layer 7
      ↓
Layer 8
      ↓
Layer 9
      ↓
Layer 10
      ↓
Planner
      ↓
Decision Engine
      ↓
Compact Decision
      ↓
Risk Manager
```

Decision Engine không cần tái hiện toàn bộ 10 tầng trong output.

---

# 12. Three-Layer Information Model

## Layer A — Domain Context

```text
What is the market environment?
```

Bao gồm:

- Structure
- Regime
- HTF Bias
- Liquidity
- Volume Profile
- Macro Context
- Historical Context

## Layer B — Realtime State

```text
What is happening now?
```

Bao gồm:

- Price
- OI
- Flow Type
- CVD
- Auction
- RSI
- Delta
- Volume
- Liquidation
- Signal Events

## Layer C — Decision

```text
What should we do now?
```

Bao gồm:

- Bias
- Decision
- Confidence
- Key Level
- Invalidation
- Next Action

---

# 13. Information Flow

```text
DOMAIN CONTEXT
      +
REALTIME FEED
      ↓
CURRENT MARKET STATE
      ↓
DECISION ENGINE
      ↓
COMPACT DECISION
      ↓
RISK MANAGER
```

---

# 14. Decision State Machine

```text
MARKET CONTEXT
      ↓
NO CONFIRMATION
      ↓
WAIT CONFIRMATION
      ↓
CONFIRMATION
      ↓
LONG / SHORT
```

Hoặc:

```text
ANY STATE
   ↓
INVALIDATION
   ↓
NO TRADE
```

---

# 15. Confirmation Logic

Một Decision không nên dựa trên một metric đơn lẻ.

Ví dụ:

```text
Price
+
OI Flow
+
CVD
+
Auction
+
Momentum
+
Key Level
```

→ Confirmation Quality

Không phải:

```text
RSI > 50
→ LONG
```

---

# 16. Key Level Principle

```text
Current Price
      ↓
Nearest Decision Level
      ↓
Reaction
      ↓
Confirmation / Failure
```

Các Decision Level có thể là:

- POC5
- POC30
- VP1
- VAH
- VAL
- Support
- Resistance
- Liquidity Zone
- Invalidation Level

---

# 17. Signed Data Principle

Các metric có dấu phải được xử lý theo giá trị signed thực tế.

Ví dụ:

```text
Auction = -1.5k
EMA20   = -2.1k
```

Quan hệ:

```text
-1.5k > -2.1k
```

Không được tự động chuyển sang absolute value.

Áp dụng cho:

- Auction
- CVD
- Delta
- OI Change
- Funding
- Flow Metrics

Nguyên tắc:

```text
Compare(value_A, value_B)
```

không phải:

```text
Compare(abs(value_A), abs(value_B))
```

trừ khi bài toán explicitly yêu cầu so sánh magnitude.

---

# 18. Compact Output Principle

Decision Engine ưu tiên:

```text
Short
Clear
Actionable
Explainable
Consistent
```

Thay vì:

```text
Long
Repetitive
Raw Data Dump
```

---

# 19. Decision Output Hierarchy

```text
1. Decision
2. Bias
3. Key Level
4. Confirmation State
5. Invalidation
6. Next Action
7. Supporting Evidence
```

---

# 20. Final Formula

```text
Trading Domain
        +
10-Layer Reasoning
        +
Realtime Feed
        ↓
Current Market State
        ↓
Decision Engine
        ↓
Compact Decision
        ↓
Risk Manager
```

Phiên bản rút gọn nhất:

```text
Context + Realtime Feed
        ↓
Decision Engine
        ↓
Bias + Decision + Key Level + Next Action
```

---

# 21. Core Philosophy

> The system may reason deeply,
> but the decision should remain simple.

Hoặc:

> Deep Reasoning → Compact Decision.

Decision Engine cần chứng minh rằng:

- Decision rõ ràng.
- Logic nhất quán.
- Điều kiện xác nhận rõ ràng.
- Invalidation rõ ràng.
- Next Action rõ ràng.

---

# Version

Version: 0.1

Status: Draft / Architecture Note