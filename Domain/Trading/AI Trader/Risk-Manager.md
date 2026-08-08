# Risk Manager

Phiên bản: 0.1

---

# Tổng quan

Risk Manager là module chịu trách nhiệm quản trị rủi ro cho mọi giao dịch.

Risk Manager nhận Quyết định giao dịch từ Decision Engine và đánh giá xem giao dịch có đáp ứng các nguyên tắc quản trị rủi ro hay không.

Risk Manager không phân tích thị trường.

Risk Manager không thay đổi Quyết định giao dịch.

---

# Mục tiêu

Risk Manager chịu trách nhiệm:

- Kiểm tra mức độ rủi ro.
- Kiểm tra tỷ lệ Risk / Reward.
- Kiểm tra giới hạn tổn thất.
- Xác định Position Size.
- Tạo Trade ID.
- Tạo Kế hoạch quản trị rủi ro.
- Chuyển kết quả sang Journal.

---

# Luồng hoạt động

```
Quyết định giao dịch

↓

Đánh giá rủi ro

↓

Tính toán vị thế

↓

Kế hoạch quản trị rủi ro

↓

Journal
```

---

# Đầu vào

Risk Manager nhận:

- Quyết định giao dịch.

Bao gồm:

- Hành động
- Mức độ tin cậy
- Entry
- Stop Loss
- Take Profit
- Risk / Reward

---

# Quy trình quản trị rủi ro

Risk Manager thực hiện theo trình tự:

```
# Quy trình quản trị rủi ro

Risk Manager thực hiện theo trình tự:

```
Kiểm tra Quyết định giao dịch

↓

Kiểm tra giới hạn rủi ro

↓

Đánh giá Risk / Reward

↓

Tính Position Size

↓

Kiểm tra Drawdown

↓

Tạo Trade ID

↓

Hoàn thành Kế hoạch quản trị rủi ro
```
```

---

# Nội dung đánh giá

Risk Manager xem xét:

## Rủi ro trên mỗi giao dịch

Ví dụ:

- 0.5%
- 1%
- 2%

---

## Risk / Reward

Đánh giá tỷ lệ lợi nhuận so với rủi ro.

Nếu Risk / Reward không đạt yêu cầu:

Không thực hiện giao dịch.

---

## Position Size

Xác định khối lượng giao dịch phù hợp.

---

## Trade ID

Sau khi giao dịch vượt qua toàn bộ điều kiện quản trị rủi ro, Risk Manager tạo một Trade ID duy nhất.

Trade ID được sử dụng để liên kết toàn bộ dữ liệu của giao dịch trong AI Trader.

Trade ID được chuẩn hóa theo định dạng:

```
<Asset>-<YYYYMMDD>-<Sequence>
```

Ví dụ:

```
BTC-20260807-001

BTC-20260807-002

ETH-20260807-001
```

Trade ID chỉ được tạo một lần và không được thay đổi trong suốt vòng đời giao dịch.

---

## Stop Loss

Kiểm tra khoảng cách Stop Loss.

Đảm bảo phù hợp với kế hoạch.

---

## Take Profit

Đánh giá mục tiêu lợi nhuận.

---

## Drawdown

Kiểm tra mức sụt giảm hiện tại.

Nếu vượt giới hạn:

Dừng giao dịch.

---

## Giới hạn giao dịch

Ví dụ:

- Rủi ro tối đa mỗi lệnh.
- Rủi ro tối đa mỗi ngày.
- Rủi ro tối đa mỗi tuần.
- Số lệnh tối đa.
- Mức Drawdown tối đa.

---

# Đầu ra

Risk Manager tạo:

Kế hoạch quản trị rủi ro.

Kế hoạch bao gồm:

- Trade ID
- Rủi ro mỗi lệnh
- Position Size
- Stop Loss
- Take Profit
- Risk / Reward
- Drawdown hiện tại
- Kết quả đánh giá

Mẫu chuẩn:

```text
Kế hoạch quản trị rủi ro

Trade ID:
BTC-20260807-001

Rủi ro mỗi lệnh:
1%

Risk / Reward:
1 : 2.5

Position Size:
...

Stop Loss:
...

Take Profit:
...

Drawdown hiện tại:
...

Kết quả:

ĐỦ ĐIỀU KIỆN
```

Hoặc

```text
Kế hoạch quản trị rủi ro

Kết quả:

KHÔNG ĐỦ ĐIỀU KIỆN

Lý do:

- Risk / Reward không đạt.
- Drawdown vượt giới hạn.

Trade ID:

Không được tạo.
```

---

# Giới hạn trách nhiệm

Risk Manager được phép:

- Kiểm tra rủi ro.
- Tính toán Position Size.
- Từ chối thực hiện giao dịch nếu vi phạm nguyên tắc quản trị rủi ro.

Risk Manager không được phép:

- Thay đổi Báo cáo phân tích.
- Thay đổi Kế hoạch giao dịch.
- Thay đổi Quyết định giao dịch.

---

# Nguyên tắc thiết kế

Risk Manager phải:

- Bảo vệ vốn trước.
- Tuân thủ nguyên tắc quản trị rủi ro.
- Nhất quán.
- Có thể giải thích.

Nếu rủi ro vượt giới hạn:

Không giao dịch.

Nếu Drawdown vượt ngưỡng:

Không giao dịch.

Nếu Position Size không phù hợp:

Không giao dịch.

Trade ID chỉ được tạo sau khi giao dịch vượt qua toàn bộ kiểm tra quản trị rủi ro.

Trade ID là định danh duy nhất của giao dịch.

Trade ID không được chỉnh sửa hoặc tái sử dụng.

Mọi module phía sau Risk Manager phải sử dụng cùng một Trade ID để đảm bảo khả năng truy vết toàn bộ vòng đời giao dịch.

---

# Quan hệ với các module khác

```
Decision Engine

↓

Risk Manager

↓

Trade ID

↓

Journal
```

Risk Manager nhận Quyết định giao dịch từ Decision Engine.

Nếu giao dịch đáp ứng toàn bộ nguyên tắc quản trị rủi ro, Risk Manager sẽ tạo Trade ID và chuyển Kế hoạch quản trị rủi ro sang Journal.

Nếu giao dịch không đáp ứng yêu cầu, Trade ID sẽ không được tạo.

---

# Khả năng mở rộng

Trong tương lai Risk Manager có thể hỗ trợ:

- Quản trị nhiều tài khoản.
- Quản trị nhiều danh mục.
- Điều chỉnh Position Size theo biến động.
- Giới hạn theo ngày, tuần, tháng.
- Kiểm soát tương quan giữa nhiều vị thế.

Mọi giao dịch đều phải vượt qua Risk Manager trước khi được thực hiện.

---

# Triết lý

Risk Manager không tối đa hóa lợi nhuận.

Risk Manager tối đa hóa khả năng tồn tại trên thị trường.

Một giao dịch bị từ chối vì rủi ro không phải là một cơ hội bị bỏ lỡ.

Đó là một quyết định đúng để bảo vệ vốn.

---

# Phiên bản

Phiên bản hiện tại:

v0.1