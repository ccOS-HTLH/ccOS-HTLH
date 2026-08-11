# POC5 & VP1 Reference Framework

Phiên bản: v0.1

---

# 1. Purpose

`POC5 & VP1 Reference Framework` định nghĩa cách AI Trader sử dụng **POC5** và **VP1** như các Reference Level để đọc Price Location, Reference Interaction, Acceptance, Rejection, Reference Rotation và phân biệt Rotation với Breakout / Breakdown.

Framework không tự tạo Trading Decision. Nó cung cấp **Reference Context** cho Trading Domain, Planner và Decision Engine.

---

# 2. Scope

Framework tập trung vào:

- POC5
- VP1
- Price Location giữa hai Reference
- Reference Interaction
- Acceptance
- Rejection
- Reference Rotation
- Breakout / Breakdown
- OI
- CVD
- Auction Flow
- Confirmation
- Failure Conditions

**POC30 không thuộc POC5–VP1 pair logic.**

---

# 3. Definitions

## 3.1 POC5

`POC5` là Point of Control của Volume Profile 5m trong realtime context.

POC5 là một short-term Reference Level có thể dùng để đánh giá:

- Price Interaction
- Acceptance / Rejection
- Reclaim / Failure
- Reference Rotation

POC5 phải được cập nhật khi xuất hiện giá trị POC5 mới.

## 3.2 VP1

`VP1` là Volume Profile Reference Level được feed vào realtime context.

VP1 là một Reference độc lập với POC5 và có thể được dùng làm:

- Rotation target
- Support / resistance context
- Acceptance / rejection reference
- Breakout / breakdown boundary

## 3.3 POC5 ≠ POC30

Đây là nguyên tắc bắt buộc:

```text
POC5  = Volume Profile 5m Reference
POC30 = Volume Profile 30m Reference
```

Không được thay thế, gộp hoặc trộn hai level này.

Nếu cần POC30, phải xử lý nó như một higher-timeframe Reference riêng.

---

# 4. Reference Pair

Khi POC5 và VP1 cùng hiện diện:

```text
POC5 = 64344
VP1  = 63800
```

Price có thể nằm trong:

```text
64344
  │
  │
Price
  │
  │
63800
```

AI Trader phải xác định:

1. Price đang ở đâu trong Reference Range?
2. Price đang tiến về Reference nào?
3. Reference gần nhất đang được Accepted hay Rejected?
4. Có evidence cho Rotation hay Breakout không?

---

# 5. Price Location

Các trạng thái chính:

```text
ABOVE_POC5
AT_POC5
BETWEEN_POC5_AND_VP1
AT_VP1
BELOW_VP1
```

Khi:

```text
VP1 < Price < POC5
```

Price đang ở **Reference Range**.

Đây là context quan trọng để đánh giá Reference Rotation.

---

# 6. Reference Rotation

**Reference Rotation** là trạng thái Price di chuyển từ một Reference về phía Reference đối diện sau khi không tạo được Acceptance rõ ràng tại Reference hiện tại.

Ví dụ:

```text
POC5
  ↓
Price
  ↓
VP1
```

Nếu Price không thể establish acceptance tại POC5 và tiếp tục di chuyển xuống, VP1 trở thành Reference Target tự nhiên của rotation.

Ngược lại:

```text
VP1
  ↑
Price
  ↑
POC5
```

Nếu Price reject VP1 và recovery, POC5 có thể trở thành Reference Target.

---

# 7. Rotation Is Conditional

Không được hiểu:

> Price luôn chạy từ POC5 sang VP1.

Cách hiểu đúng:

> Khi Price nằm giữa hai established references và chưa tạo Acceptance rõ ràng vượt khỏi một Reference, Price có xu hướng test Reference còn lại.

Đây là **conditional market behavior**, không phải deterministic rule.

---

# 8. Conditions Supporting Rotation

Rotation có độ tin cậy cao hơn khi:

- Price nằm giữa POC5 và VP1.
- Một Reference vừa bị Rejection.
- Price chưa tạo Acceptance vượt Reference đó.
- Price tiếp tục di chuyển về Reference đối diện.
- OI không phản ánh một Position Expansion ngược chiều quá mạnh.
- CVD và Auction không phản bác mạnh hướng Rotation.

---

# 9. Acceptance

Acceptance là trạng thái Price không chỉ xuyên Reference mà còn duy trì giao dịch và flow tương ứng ở phía bên kia Reference.

Một wick đơn lẻ không phải Acceptance.

Nên đánh giá bằng:

- Price location
- Persistence
- OI
- CVD
- Auction Flow
- Subsequent Price behavior

### Acceptance Above POC5

```text
642xx
→ 64344
→ 644xx
→ hold
```

Nếu:

```text
BuI
CVD ↑
Auction ↑
```

thì khả năng POC5 được Accepted từ phía trên tăng lên.

### Acceptance Below VP1

```text
639xx
→ 63800
→ 637xx
→ hold
```

Nếu:

```text
BeI
CVD ↓
Auction ↓
```

thì khả năng VP1 được Accepted từ phía dưới tăng lên.

---

# 10. Rejection

Rejection là trạng thái Price test một Reference nhưng không thể duy trì phía bên kia và quay trở lại.

Ví dụ:

```text
Price → POC5
       ↓
    rejection
       ↓
Price < POC5
```

Hoặc:

```text
Price → VP1
       ↑
    rejection
       ↑
Price > VP1
```

Rejection có thể được củng cố bởi:

- Failed push
- Wick
- CVD không follow-through
- OI không support breakout
- Auction Flow đảo chiều
- Price quay lại Reference Range

---

# 11. Breakout / Breakdown

Không xác định Breakout / Breakdown chỉ bằng việc Price vượt Reference.

```text
Reference Touch
      ≠
Reference Break
      ≠
Reference Acceptance
```

Một move xuyên Reference rồi quay lại có thể là:

```text
POTENTIAL_FALSE_BREAK
```

Một move xuyên Reference và duy trì phía bên kia cùng flow xác nhận có thể trở thành:

```text
ACCEPTED_BREAKOUT
ACCEPTED_BREAKDOWN
```

---

# 12. OI Confirmation

OI dùng để xác định **Position Participation** phía sau Price Movement.

Không đọc OI một mình.

Các context cơ bản:

```text
Price ↓ + BeI ↑
→ New Short Participation context

Price ↓ + BuO
→ Position Unwind / Long Exit context

Price ↑ + BuI ↑
→ New Long Participation context

Price ↑ + BeO
→ Position Unwind / Short Exit context
```

Đây là context, không phải kết luận tuyệt đối.

Phải đối chiếu với CVD và Auction.

---

# 13. CVD Confirmation

CVD dùng để đánh giá aggressive execution.

```text
Price ↓
CVD ↓
```

→ seller aggression hỗ trợ Price movement.

```text
Price ↓
CVD ↑
```

→ Price decline không được aggressive selling xác nhận đầy đủ.

Có thể là context của:

- Absorption
- Exhaustion
- Position unwind
- Potential reversal

Không được tự động kết luận reversal chỉ từ divergence.

---

# 14. Auction Flow Confirmation

Auction Flow dùng để đánh giá current auction pressure tương đối với baseline, ví dụ EMA20 của Auction Line khi được feed.

```text
Auction < EMA20
```

có thể hỗ trợ bearish current flow.

```text
Auction > EMA20
```

có thể hỗ trợ bullish current flow.

Auction phải được đọc **theo signed value**.

Ví dụ:

```text
-100 < +100
```

Không được đổi thành:

```text
|-100| > |+100|
```

khi mục tiêu là so sánh hướng flow.

---

# 15. Combined Confirmation

Reference interaction nên được đánh giá theo tầng:

```text
Layer 1
Price Location
    ↓
Layer 2
Reference Interaction
    ↓
Layer 3
OI
    ↓
Layer 4
CVD
    ↓
Layer 5
Auction Flow
    ↓
Layer 6
Subsequent Price Behavior
```

Không một indicator đơn lẻ nào được phép override toàn bộ context.

---

# 16. Reference Rotation Matrix

| Price State | OI | CVD | Auction | Interpretation |
|---|---|---|---|---|
| Reject POC5 ↓ | BeI | ↓ | ↓ | Bearish rotation toward VP1 |
| Reject POC5 ↓ | BuO | ↑ | ↑ | Possible rejection / recovery |
| Reject VP1 ↑ | BuI | ↑ | ↑ | Bullish rotation toward POC5 |
| Reject VP1 ↑ | BeO | ↓ | ↓ | Possible recovery failure |
| Break POC5 ↑ | BuI | ↑ | ↑ | Potential accepted breakout |
| Break VP1 ↓ | BeI | ↓ | ↓ | Potential accepted breakdown |
| Break Reference + opposing flow | Any | Opposing | Opposing | Potential false break |

---

# 17. Reference States

Framework có thể trả về:

```text
ROTATION_TOWARD_POC5
ROTATION_TOWARD_VP1
POC5_REJECTION
VP1_REJECTION
POC5_ACCEPTANCE
VP1_ACCEPTANCE
POTENTIAL_FALSE_BREAK
ACCEPTED_BREAKOUT
ACCEPTED_BREAKDOWN
REFERENCE_RANGE_BALANCE
INSUFFICIENT_CONFIRMATION
```

---

# 18. POC5 → VP1 Rotation

Ví dụ:

```text
POC5 = 64344
VP1  = 63800

642xx
 ↓
640xx
 ↓
639xx
```

Nếu Price không reclaim / accept trên POC5:

```text
POC5_REJECTION
```

có thể chuyển thành:

```text
ROTATION_TOWARD_VP1
```

VP1 là **Reference Target**, không phải guaranteed target.

---

# 19. VP1 → POC5 Rotation

Ngược lại:

```text
Price → VP1
```

Nếu VP1 bị reject:

```text
VP1_REJECTION
      ↓
Price ↑
      ↓
ROTATION_TOWARD_POC5
```

Nếu POC5 được reclaim và accepted, Rotation có thể chuyển thành Recovery / Breakout state.

---

# 20. Reference Range Balance

Khi:

```text
VP1 < Price < POC5
```

và:

- Price không breakout.
- OI không expand mạnh.
- CVD không tạo directional expansion.
- Auction không tạo directional expansion.

State có thể là:

```text
REFERENCE_RANGE_BALANCE
```

Trong trạng thái này:

- Không chase.
- Không assume breakout.
- Chờ Reference Interaction.

---

# 21. Must

Framework **MUST**:

- Xác định POC5 chính xác.
- Xác định VP1 chính xác.
- Giữ POC5 và POC30 là hai Reference khác nhau.
- Xác định Price Location trước khi đánh giá Rotation.
- Kiểm tra Reference Interaction.
- Phân biệt Acceptance và Rejection.
- Đối chiếu OI với Price.
- Đối chiếu CVD với Price.
- Đọc Auction Flow theo signed value.
- Phân biệt Rotation với Breakout / Breakdown.
- Gắn mức độ xác nhận phù hợp với dữ liệu.

---

# 22. May

Framework **MAY**:

- Dùng POC5 làm short-term Reference.
- Dùng VP1 làm opposing Reference.
- Dùng OI để xác định participation context.
- Dùng CVD để đánh giá aggressive execution.
- Dùng Auction Flow để đánh giá current auction pressure.
- Dùng RSI / VPIN như contextual information nếu được feed.
- Gợi ý Reference Target.
- Gợi ý potential absorption / exhaustion.
- Chuyển Reference State cho Decision Engine.

---

# 23. Must Not

Framework **MUST NOT**:

- Xem POC5 và POC30 là cùng một level.
- Tự động giả định Price luôn đi từ POC5 đến VP1.
- Gọi Rotation chỉ vì Price đang tăng hoặc giảm.
- Gọi Acceptance chỉ từ một wick.
- Gọi Breakout chỉ vì Price xuyên Reference.
- Gọi Reversal chỉ từ CVD divergence.
- Gọi New Short chỉ vì Price giảm.
- Gọi New Long chỉ vì Price tăng.
- Bỏ qua OI khi đánh giá Position Participation.
- Dùng absolute value để thay thế signed Auction comparison.
- Chase Price chỉ vì Price gần POC5 hoặc VP1.
- Override Risk Manager.
- Tự tạo Entry / Stop Loss / Take Profit.
- Tự đưa ra Trading Decision cuối cùng.

---

# 24. Compact Reference Output

Framework có thể xuất context compact:

```text
Reference Context

POC5: 64344
VP1: 63800

Price:
63917

Location:
BETWEEN_POC5_AND_VP1

Interaction:
ROTATION_TOWARD_VP1

POC5:
REJECTION / NO ACCEPTANCE

VP1:
NOT TESTED

OI:
BuO

CVD:
-290

Auction:
-1.5k < EMA20 -770

Confirmation:
PARTIAL

State:
ROTATION_TOWARD_VP1

Next Reference:
VP1 63800
```

Compact output chỉ mô tả **Reference State**.

Trading Decision thuộc về Decision Engine.

---

# 25. Example: Bearish Rotation

```text
POC5 = 64344
VP1  = 63800

Price:
642xx → 640xx → 639xx

OI:
BeI

CVD:
↓

Auction:
< EMA20
```

Result:

```text
POC5 rejection
+
bearish flow confirmation
+
rotation toward VP1
```

Output:

```text
State:
ROTATION_TOWARD_VP1

Next Reference:
VP1
```

---

# 26. Example: Bullish Rotation

```text
POC5 = 64344
VP1  = 63800

Price:
638xx → 639xx → 641xx

OI:
BuI

CVD:
↑

Auction:
↑
```

Result:

```text
VP1 rejection
+
bullish flow confirmation
+
rotation toward POC5
```

Output:

```text
State:
ROTATION_TOWARD_POC5

Next Reference:
POC5
```

---

# 27. Example: False Breakdown

```text
639xx
 ↓
63800
 ↓
637xx
 ↑
639xx
```

Nếu:

```text
BeI không tăng
CVD không giảm tương ứng
Auction hồi
```

thì:

```text
State:
POTENTIAL_FALSE_BREAK
```

Không tự động gọi bullish reversal.

---

# 28. Example: Accepted Breakdown

```text
639xx
 ↓
63800
 ↓
637xx
 ↓
636xx
```

Nếu đồng thời:

```text
BeI ↑
CVD ↓
Auction ↓
```

và Price duy trì dưới VP1:

```text
State:
ACCEPTED_BREAKDOWN
```

VP1 có thể chuyển vai trò thành Resistance Reference.

---

# 29. Example: Reference Range Balance

```text
POC5 = 64344
VP1  = 63800

Price:
640xx

OI:
neutral / low expansion

CVD:
flat

Auction:
flat
```

Output:

```text
State:
REFERENCE_RANGE_BALANCE

Next Action:
WAIT_FOR_REFERENCE_INTERACTION
```

---

# 30. Failure Cases

## Case 1: Wick Only

```text
Price > POC5
→ immediate return
```

Không gọi Acceptance.

## Case 2: Price Down ≠ New Short

```text
Price ↓
OI BuO
```

Không kết luận New Short.

## Case 3: Price Up ≠ New Long

```text
Price ↑
OI BeO
```

Không kết luận New Long.

## Case 4: CVD Divergence

```text
Price ↓
CVD ↑
```

Đây là opposing-flow context, không tự động là reversal.

## Case 5: Auction Sign Error

```text
Auction = -500
EMA20 = +300
```

Phải đọc:

```text
-500 < +300
```

Không đổi thành:

```text
500 > 300
```

---

# 31. Integration with Trading Domain

```text
Market Data
    ↓
Volume Profile
    ↓
POC5 + VP1
    ↓
Reference Framework
    ↓
Price Location
    ↓
Reference Interaction
    ↓
OI + CVD + Auction
    ↓
Reference State
    ↓
Trading Domain / Reasoning Layer
    ↓
Planner
    ↓
Decision Engine
```

Framework không bypass Planner hoặc Decision Engine.

---

# 32. Integration with Decision Engine

Decision Engine nhận compact context:

```text
Reference:
POC5 = 64344
VP1 = 63800

Price Location:
BETWEEN

State:
ROTATION_TOWARD_VP1

Confirmation:
PARTIAL

OI:
BuO

CVD:
Negative

Auction:
Bearish

Next Reference:
VP1
```

Decision Engine kết hợp với:

- Trading Plan
- Bias
- Scenario
- Entry
- Invalidation
- Risk / Reward
- Other market context

Reference Framework không quyết định:

```text
LONG
SHORT
HOLD
WAIT CONFIRMATION
NO TRADE
```

---

# 33. Core Principle

POC5 và VP1 là **Reference**, không phải Prediction.

```text
Price Location
→ Where is Price?

Reference Interaction
→ What is Price doing at the Reference?

OI
→ What type of Position Participation is occurring?

CVD
→ Who is aggressively executing?

Auction Flow
→ Which side is controlling the current auction?

Decision Engine
→ What should the AI Trader do?
```

---

# 34. Compact Formula

```text
Reference Context
=
Price Location
+
Reference Interaction
+
OI
+
CVD
+
Auction Flow
```

Và:

```text
Reference Rotation
=
Reference Rejection
+
No Clear Acceptance
+
Directional Price Movement
+
Supporting / Non-Contradicting Flow
```

Trong đó:

```text
Rotation ≠ Guarantee
```

Rotation là một **probabilistic market state**.

---

# 35. Final Principle

Không hỏi:

> “Giá có chắc chắn chạy từ POC5 đến VP1 không?”

Hãy hỏi:

> “Price đang nằm giữa hai Reference nào, Reference nào vừa bị reject, Reference nào chưa được accepted, và flow có đang hỗ trợ rotation hay breakout?”

Đó là cách Reference Framework được sử dụng trong AI Trader.

---

# 36. Version

Phiên bản hiện tại:

`v0.1`

Tên module:

`POC5 & VP1 Reference Framework`

File:

`POC5-VP1-Reference-Framework.md`