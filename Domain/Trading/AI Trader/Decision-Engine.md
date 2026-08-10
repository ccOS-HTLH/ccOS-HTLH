# Decision Engine

Phiên bản: 0.2

---

# Tổng quan

Decision Engine là module chịu trách nhiệm tạo ra Trading Decision cuối cùng từ Trading Plan.

Decision Engine nhận:

- Analysis Report
- Trading Plan
- Market Confirmation
- Risk / Reward
- Invalidation

Sau đó đánh giá mức độ sẵn sàng để thực hiện giao dịch.

---

# Vai trò

Decision Engine trả lời một câu hỏi duy nhất:

> Với Trading Plan hiện tại, có nên thực hiện giao dịch ngay lúc này hay chưa?

Decision Engine là lớp chuyển:

```text
Analysis + Trading Plan
        ↓
Trading Decision
```

---

# Operating Rules

Decision Engine được vận hành theo ba nhóm quy tắc:

```text
MUST
→ Những việc Decision Engine bắt buộc phải thực hiện.

MAY
→ Những việc Decision Engine được phép sử dụng hoặc thực hiện khi phù hợp.

MUST NOT
→ Những giới hạn Decision Engine tuyệt đối không được vượt qua.
```

---

## MUST

Decision Engine phải:

- Tuân thủ Trading Plan.
- Kiểm tra tính hợp lệ của Trading Plan.
- Kiểm tra Market Condition.
- Kiểm tra Confirmation.
- Kiểm tra Invalidation.
- Kiểm tra Risk / Reward.
- Đánh giá Confidence.
- Tạo một Trading Decision hợp lệ.
- Xác định Next Action phù hợp với Decision.
- Chuyển Decision sang module tiếp theo khi đủ điều kiện.

Decision Engine phải phân biệt rõ:

```text
Bias
↓
Confirmation
↓
Decision
```

Decision Engine phải ưu tiên:

```text
Trading Plan
    ↓
Confirmation
    ↓
Invalidation
    ↓
Risk / Reward
    ↓
Confidence
    ↓
Decision
```

---

## MAY

Decision Engine được phép tham khảo các dữ liệu đã có trong Analysis Report và Trading Plan, bao gồm:

- Price Structure
- Trend
- Momentum
- OI
- Flow Type
- CVD
- Auction Flow
- RSI
- Volume
- Liquidity
- POC5
- POC / VAH / VAL
- Entry Zone
- Support / Resistance
- Các Confirmation Signal

Decision Engine có thể sử dụng:

```text
Price + Flow
Auction + EMA20
POC5 + Structure
Momentum + Flow
```

để đánh giá Confirmation.

Decision Engine có thể tạo:

```text
LONG
SHORT
HOLD
WAIT CONFIRMATION
NO TRADE
```

Decision Engine có thể yêu cầu:

```text
WAIT CONFIRMATION
```

khi Trading Plan vẫn hợp lệ nhưng điều kiện kích hoạt chưa đầy đủ.

Decision Engine có thể sử dụng Confidence để biểu thị mức độ tin cậy của Decision.

---

## MUST NOT

Decision Engine không được:

- Tự xây dựng Trading Plan.
- Tự tạo Analysis Report.
- Tự thay đổi Bias của Planner mà không có cơ sở từ Trading Plan và dữ liệu hiện tại.
- Tự thay đổi Entry.
- Tự thay đổi Stop Loss.
- Tự thay đổi Take Profit.
- Tự thay đổi Risk / Reward.
- Tự suy diễn dữ liệu còn thiếu.
- Dùng một tín hiệu đơn lẻ để tạo Trading Decision.
- Bỏ qua Invalidation.
- Bỏ qua Risk / Reward.
- Thay thế Risk Manager.
- Quản lý Position.
- Tự thực hiện Position Management.
- Tự ý thay đổi kiến trúc hoặc trách nhiệm của module khác.

Nếu dữ liệu chưa đủ:

```text
Không suy diễn.
```

Nếu Trading Plan không còn hợp lệ:

```text
Không tiếp tục sử dụng Trading Plan cũ.
```

Nếu Risk / Reward không còn phù hợp:

```text
Không tự điều chỉnh Trading Plan.
```

---

# Vị trí trong AI Trader

```text
Analyzer
   ↓
Planner
   ↓
Decision Engine
   ↓
Risk Manager
   ↓
Execution / Position
```

Decision Engine là cầu nối giữa:

```text
Trading Plan
      ↓
Trading Decision
      ↓
Risk Manager
```

---

# Đầu vào

Decision Engine nhận từ Planner:

```text
Bias
Scenario
Entry Zone
Stop Loss
Take Profit
Invalidation
Risk / Reward
Prerequisites
Confirmation Conditions
```

Có thể sử dụng thêm Analysis Report để kiểm tra tính nhất quán của Trading Plan.

Decision Engine sử dụng Analysis Report như nguồn tham khảo cho việc đánh giá, không tạo lại Analysis Report.

---

# Nguyên tắc ra quyết định

Decision Engine không dựa trên một tín hiệu đơn lẻ.

Phải đánh giá sự đồng thuận giữa:

- Price Structure
- Trend
- Momentum
- Flow
- Auction
- OI
- CVD
- RSI
- Volume / Liquidity nếu có
- Confirmation
- Invalidation
- Risk / Reward

Không bắt buộc mọi tín hiệu phải đồng thuận tuyệt đối.

Mục tiêu là xác định:

> Trading Plan có đủ điều kiện để thực thi hay chưa?

---

# Quy trình

```text
Trading Plan
    ↓
Kiểm tra Plan
    ↓
Kiểm tra Market Condition
    ↓
Kiểm tra Confirmation
    ↓
Kiểm tra Invalidation
    ↓
Kiểm tra Risk / Reward
    ↓
Đánh giá Confidence
    ↓
Trading Decision
    ↓
Next Action
    ↓
Risk Manager
```

---

# 01 · Kiểm tra Trading Plan

Decision Engine kiểm tra:

- Bias có rõ ràng không?
- Scenario có rõ ràng không?
- Entry có xác định không?
- Stop Loss có xác định không?
- Take Profit có xác định không?
- Invalidation có xác định không?
- Risk / Reward có đạt yêu cầu không?

Nếu Trading Plan không đầy đủ:

```text
Decision:
NO TRADE
```

Decision Engine không tự tạo phần còn thiếu.

---

# 02 · Kiểm tra Market Condition

Decision Engine kiểm tra trạng thái hiện tại so với Trading Plan.

Các yếu tố có thể bao gồm:

- Giá so với Entry Zone.
- Giá so với POC / Value Area.
- Trend.
- Momentum.
- OI.
- CVD.
- Auction Flow.
- RSI.
- Liquidity.
- Các Confirmation Signal.

Mục tiêu:

> Xác định thị trường hiện tại có còn phù hợp với Trading Plan hay không.

---

# 03 · Kiểm tra Confirmation

Confirmation là điều kiện cần thiết để Trading Plan được kích hoạt.

Ví dụ:

```text
LONG

- Giá giữ trên POC5.
- Auction Line > EMA20.
- CVD phục hồi / tăng.
- OI chuyển BuI.
- Momentum duy trì.
```

Hoặc:

```text
SHORT

- Giá mất Support.
- Auction Line < EMA20.
- CVD suy yếu.
- OI chuyển BeI.
- Momentum bearish.
```

Confirmation không nhất thiết phải giống nhau cho mọi Setup.

Nó phụ thuộc vào Trading Plan.

---

# 04 · Kiểm tra Invalidation

Decision Engine phải kiểm tra:

> Trading Plan còn hiệu lực hay đã bị vô hiệu?

Nếu Invalidation đã xảy ra:

```text
Decision:
NO TRADE
```

Trading Plan cũ không được tiếp tục sử dụng.

---

# 05 · Kiểm tra Risk / Reward

Decision Engine kiểm tra:

- Risk có phù hợp không?
- Reward có đủ không?
- Risk / Reward có đạt yêu cầu không?
- Entry có còn hợp lý không?
- Giá hiện tại có khiến Setup trở nên quá muộn không?

Nếu Risk / Reward không còn phù hợp:

```text
Decision:
NO TRADE
```

Decision Engine giữ nguyên các tham số của Trading Plan:

- Entry
- Stop Loss
- Take Profit
- Risk / Reward

Mọi thay đổi thuộc module có trách nhiệm.

---

# 06 · Confidence

Confidence phản ánh mức độ tin cậy của Trading Decision.

Confidence không phải xác suất chắc chắn giao dịch sẽ thắng.

Confidence phản ánh:

- Mức độ đồng thuận của các tín hiệu.
- Chất lượng Confirmation.
- Độ rõ của Structure.
- Chất lượng Flow.
- Khoảng cách tới Invalidation.
- Chất lượng Risk / Reward.
- Mức độ phù hợp với Trading Plan.

Ví dụ:

```text
Confidence:
92%
```

Không được hiểu là:

```text
92% xác suất thắng.
```

---

# Các Decision

Decision Engine chỉ được phép tạo một trong các Decision sau:

```text
LONG
SHORT
HOLD
WAIT CONFIRMATION
NO TRADE
```

---

# LONG

LONG được chọn khi:

- Bias = LONG.
- Trading Plan còn hiệu lực.
- Confirmation đủ mạnh.
- Invalidation chưa xảy ra.
- Risk / Reward đạt yêu cầu.

---

# SHORT

SHORT được chọn khi:

- Bias = SHORT.
- Trading Plan còn hiệu lực.
- Confirmation đủ mạnh.
- Invalidation chưa xảy ra.
- Risk / Reward đạt yêu cầu.

---

# HOLD

HOLD được sử dụng khi:

- Đã có vị thế hoặc quyết định đang được duy trì.
- Trading Plan vẫn còn hiệu lực.
- Chưa có lý do để thoát hoặc đảo chiều.
- Không cần mở thêm vị thế mới.

HOLD không đồng nghĩa với WAIT CONFIRMATION.

```text
HOLD
=
Giữ trạng thái hiện tại.
```

---

# WAIT CONFIRMATION

WAIT CONFIRMATION được sử dụng khi:

- Bias đã tương đối rõ.
- Trading Plan vẫn hợp lệ.
- Nhưng Confirmation chưa đầy đủ.

Ví dụ:

```text
Bias:
LONG

Price:
Trên POC5

OI:
BuI

CVD:
Tăng

Auction:
Chưa vượt EMA20

Decision:
WAIT CONFIRMATION
```

WAIT CONFIRMATION không phải là NO TRADE.

Nó có nghĩa:

> Setup vẫn còn giá trị nhưng chưa được kích hoạt.

---

# NO TRADE

NO TRADE được sử dụng khi:

- Trading Plan mất hiệu lực.
- Invalidation xảy ra.
- Risk / Reward không còn phù hợp.
- Confirmation mâu thuẫn nghiêm trọng.
- Dữ liệu không đủ để đánh giá Plan một cách hợp lệ.
- Điều kiện thị trường không còn phù hợp.

NO TRADE có nghĩa:

> Không thực hiện giao dịch với Trading Plan hiện tại.

---

# Bias và Decision

Bias và Decision không phải là một.

Ví dụ:

```text
Bias:
LONG

Decision:
WAIT CONFIRMATION
```

Điều này có nghĩa:

> Thiên hướng vẫn là LONG nhưng chưa đủ điều kiện để vào lệnh.

Hoặc:

```text
Bias:
LONG

Decision:
NO TRADE
```

Có nghĩa:

> Trading Plan LONG hiện tại đã mất hiệu lực.

---

# Flow Type

Decision Engine có thể sử dụng OI Flow Type như một thành phần xác nhận:

```text
BuI = Bull In
BuO = Bull Out
BeI = Bear In
BeO = Bear Out
```

Flow Type không được sử dụng độc lập để tạo Decision.

Phải được đánh giá cùng:

- Price
- CVD
- Auction
- Structure
- Momentum
- Trading Plan

---

# Price + Flow

Decision Engine đặc biệt chú ý đến mối quan hệ giữa Price và Flow.

Ví dụ:

```text
Price ↑
OI BuI
CVD ↑
Auction ↑
```

→ Confirmation cho LONG mạnh hơn.

Ví dụ:

```text
Price ↑
OI BuI
CVD ↓
Auction ↓
```

→ Cần cảnh giác với suy yếu / failed breakout.

Ví dụ:

```text
Price ↓
OI BuO
CVD ↓
Auction ↓
```

→ Có thể là deleveraging / liquidation.

Mẫu này không tự động tạo SHORT Decision.

---

# Auction Confirmation

Auction Line được đánh giá cùng EMA20.

```text
Auction Line > EMA20
```

→ bullish confirmation.

```text
Auction Line < EMA20
```

→ bearish pressure / bullish confirmation chưa đầy đủ.

Auction không được sử dụng đơn độc để tạo Decision.

---

# POC5 và Structure Confirmation

POC5 có thể đóng vai trò:

- Pivot.
- Support.
- Resistance.
- Reclaim level.
- Invalidation reference.

```text
Price > POC5
```

không tự động tạo:

```text
LONG
```

Cần kết hợp với:

- Flow.
- CVD.
- Auction.
- Momentum.
- Trading Plan.

---

# Decision Matrix

```text
Plan hợp lệ
+
Confirmation đầy đủ
+
Risk / Reward đạt
+
Invalidation chưa xảy ra
=
LONG / SHORT
```

```text
Plan hợp lệ
+
Bias rõ
+
Confirmation chưa đủ
=
WAIT CONFIRMATION
```

```text
Plan còn hiệu lực
+
Đang duy trì trạng thái
+
Chưa cần thay đổi
=
HOLD
```

```text
Plan mất hiệu lực
OR
Invalidation xảy ra
OR
Risk / Reward không phù hợp
=
NO TRADE
```

---

# Mẫu Trading Decision chuẩn

```text
Trading Decision

Decision:
LONG

Bias:
LONG

Confidence:
92%

Reason:
- Giá giữ trên POC5.
- OI duy trì BuI.
- CVD xác nhận lực mua.
- Auction Line > EMA20.
- Structure vẫn bullish.
- Risk / Reward đạt yêu cầu.

Prerequisites:
- Giá giữ trên Entry Zone.
- Không mất Invalidation.
- Confirmation tiếp tục duy trì.

Key Support:
POC5

Key Resistance:
VP1

Risk:
- RSI cao.
- Có khả năng pullback.

Next Action:
Chuyển sang Risk Manager.
```

---

# Mẫu WAIT CONFIRMATION

```text
Trading Decision

Decision:
WAIT CONFIRMATION

Bias:
LONG

Confidence:
89%

Reason:
- Giá vẫn trên POC5.
- OI đã chuyển BuI.
- CVD đang cải thiện.
- Nhưng Auction Line chưa vượt EMA20.

Prerequisites:
- Giá giữ POC5.
- Auction Line > EMA20.
- CVD tiếp tục tăng.

Next Action:
Chờ Confirmation.
```

---

# Mẫu HOLD

```text
Trading Decision

Decision:
HOLD

Bias:
LONG

Confidence:
90%

Reason:
- Trading Plan vẫn còn hiệu lực.
- Giá giữ trên vùng hỗ trợ.
- Confirmation vẫn được duy trì.
- Invalidation chưa xảy ra.

Next Action:
Chuyển sang Risk Manager.
```

---

# Mẫu NO TRADE

```text
Trading Decision

Decision:
NO TRADE

Bias:
LONG

Confidence:
95%

Reason:
- Giá mất Invalidation.
- Auction xác nhận suy yếu.
- Risk / Reward không còn phù hợp.

Next Action:
Hủy Trading Plan hiện tại.
Quay lại Planner khi có Setup mới.
```

---

# Quy tắc Next Action

Next Action phải phản ánh đúng trạng thái Decision.

```text
LONG
→ Risk Manager

SHORT
→ Risk Manager

HOLD
→ Risk Manager

WAIT CONFIRMATION
→ Chờ Confirmation

NO TRADE
→ Hủy Trading Plan
```

Decision Engine chuyển kết quả sang module tiếp theo theo đúng Decision.

---

# Chuyển sang Risk Manager

Khi Decision yêu cầu quản trị Risk:

```text
LONG
SHORT
HOLD
```

Decision Engine chuyển kết quả sang Risk Manager.

Risk Manager chịu trách nhiệm tiếp tục đánh giá:

- Position Size
- Risk
- Stop Loss
- Exposure
- Drawdown
- Portfolio Risk
- Execution Risk

Decision Engine không thực hiện các nhiệm vụ thuộc Risk Manager.

---

# Giới hạn trách nhiệm

Decision Engine chịu trách nhiệm:

- Đánh giá Trading Plan.
- Kiểm tra Confirmation.
- Kiểm tra Invalidation.
- Đánh giá Confidence.
- Tạo Trading Decision.
- Yêu cầu chờ Confirmation.
- Từ chối giao dịch.
- Chuyển Decision sang Risk Manager.

Các trách nhiệm khác thuộc module tương ứng.

---

# Dữ liệu chưa đủ

Nếu dữ liệu chưa đủ nhưng Trading Plan vẫn có thể tiếp tục được đánh giá sau khi có Confirmation bổ sung:

```text
Decision:
WAIT CONFIRMATION
```

Nếu dữ liệu thiếu khiến Trading Plan không thể được đánh giá một cách hợp lệ:

```text
Decision:
NO TRADE
```

Nguyên tắc:

```text
Dữ liệu chưa đủ
↓
Không suy diễn
↓
WAIT CONFIRMATION hoặc NO TRADE
```

---

# Nguyên tắc ưu tiên

Decision Engine phải ưu tiên:

```text
Trading Plan
    ↓
Confirmation
    ↓
Invalidation
    ↓
Risk / Reward
    ↓
Confidence
    ↓
Decision
```

Không sử dụng:

```text
Signal
↓
Decision
```

Một tín hiệu đơn lẻ không đủ để tạo Trading Decision.

---

# Quan hệ với các Module

```text
Scanner
   ↓
Analyzer
   ↓
Planner
   ↓
Decision Engine
   ↓
Risk Manager
   ↓
Journal
   ↓
Learning Engine
```

Decision Engine không thay thế Analyzer hoặc Planner.

Nó là lớp chuyển:

```text
Phân tích + Kế hoạch
        ↓
Quyết định
```

---

# Trading Domain Integration

Decision Engine là một phần của Hệ thống suy luận.

Trading Domain định nghĩa chuỗi:

```text
Thực tế
   ↓
Nguồn dữ liệu
   ↓
Hệ thống suy luận
   ↓
Quyết định
   ↓
Thực tế
   ↓
Tri thức tích lũy
```

Decision Engine nằm tại lớp:

```text
Quyết định
```

và phải vận hành đúng vị trí này.

---

# Nguyên tắc thiết kế

Decision Engine phải:

- Khách quan.
- Có thể giải thích.
- Dựa trên dữ liệu.
- Tuân thủ Trading Plan.
- Không dựa trên một tín hiệu đơn lẻ.
- Ưu tiên Risk / Reward.
- Tôn trọng Invalidation.
- Đánh giá Entry theo điều kiện của Trading Plan.
- Không tự suy diễn dữ liệu thiếu.
- Không thay thế module khác.

---

# Triết lý

Decision Engine không cần dự đoán chắc chắn hướng đi của thị trường.

Decision Engine chỉ cần trả lời:

> Trading Plan hiện tại có đủ điều kiện để thực hiện hay chưa?

Vì vậy:

```text
Bias ≠ Decision
```

```text
Bullish ≠ LONG ngay lập tức
```

```text
Bearish ≠ SHORT ngay lập tức
```

Decision Engine phải phân biệt:

```text
Bias
↓
Confirmation
↓
Decision
```

Một quyết định tốt không phải là một giao dịch chắc chắn có lợi nhuận.

Một quyết định tốt là một quyết định:

- Đúng dữ liệu.
- Đúng Trading Plan.
- Đúng Confirmation.
- Đúng Risk / Reward.
- Đúng Invalidation.
- Đúng quy trình AI Trader.

---

# Phiên bản

Phiên bản hiện tại:

v0.2

Lịch sử:

```text
v0.1
→ Initial Decision Engine structure

v0.2
→ Chuẩn hóa Trading Decision
→ Tách Bias khỏi Decision
→ Bổ sung Confidence
→ Bổ sung Prerequisites
→ Bổ sung Key Support / Resistance
→ Bổ sung Price + Flow confirmation
→ Bổ sung Auction / EMA20 confirmation
→ Bổ sung POC5 confirmation
→ Chuẩn hóa Next Action
→ Chuẩn hóa LONG / SHORT / HOLD / WAIT CONFIRMATION / NO TRADE
→ Bổ sung Operating Rules: MUST / MAY / MUST NOT
→ Làm rõ ranh giới trách nhiệm giữa các module
```