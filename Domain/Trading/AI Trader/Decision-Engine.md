# Decision Engine

Phiên bản: 0.1

---

# Tổng quan

Decision Engine là module chịu trách nhiệm đưa ra quyết định giao dịch cuối cùng.

Decision Engine nhận Kế hoạch giao dịch từ Planner và đánh giá xem có nên thực hiện giao dịch hay không.

Decision Engine không phân tích thị trường.

Decision Engine không xây dựng Kế hoạch giao dịch.

---

# Mục tiêu

Decision Engine chịu trách nhiệm:

- Đánh giá Kế hoạch giao dịch.
- Kiểm tra điều kiện thực thi.
- Lựa chọn hành động phù hợp.
- Tạo Quyết định giao dịch.
- Chuyển kết quả sang Risk Manager.

---

# Luồng hoạt động

```
Kế hoạch giao dịch

↓

Đánh giá điều kiện

↓

Ra quyết định

↓

Quyết định giao dịch

↓

Risk Manager
```

---

# Đầu vào

Decision Engine nhận:

- Kế hoạch giao dịch.

Bao gồm:

- Bias
- Kịch bản giao dịch
- Entry
- Stop Loss
- Take Profit
- Invalidation
- Risk / Reward

---

# Quy trình ra quyết định

Decision Engine thực hiện theo trình tự:

```
Kiểm tra Kế hoạch giao dịch

↓

Kiểm tra điều kiện thị trường

↓

Kiểm tra điều kiện xác nhận

↓

Đánh giá mức độ phù hợp

↓

Ra quyết định
```

---

# Các hành động

Decision Engine chỉ được phép tạo một trong các hành động sau.

## LONG

Thực hiện kế hoạch Long.

---

## SHORT

Thực hiện kế hoạch Short.

---

## HOLD

Không mở vị thế mới.

Tiếp tục theo dõi thị trường.

---

## WAIT CONFIRMATION

Kế hoạch hợp lệ.

Nhưng điều kiện xác nhận chưa đầy đủ.

Tiếp tục chờ.

---

## NO TRADE

Không giao dịch.

Hủy toàn bộ kế hoạch hiện tại.

---

# Điều kiện đánh giá

Decision Engine phải xem xét:

- Báo cáo phân tích.
- Kế hoạch giao dịch.
- Mức độ đồng thuận.
- Điều kiện xác nhận.
- Risk / Reward.
- Điều kiện vô hiệu.

Không được dựa trên một tín hiệu đơn lẻ.

---

# Đầu ra

Decision Engine tạo ra một **Quyết định giao dịch**.

Mẫu chuẩn:

```text
Quyết định giao dịch

Hành động:
LONG

Mức độ tin cậy:
82%

Lý do:

- Xu hướng đa khung thời gian đồng thuận.
- Auction Flow xác nhận.
- Risk / Reward đạt yêu cầu.

Điều kiện tiên quyết:

- Giá giữ trên vùng Entry.
- Chưa mất vùng Invalidation.
- Chưa xuất hiện tín hiệu đảo chiều mạnh.

Hành động tiếp theo:

Chuyển sang Risk Manager.
```

---

# Giới hạn trách nhiệm

Decision Engine được phép:

- Quyết định giao dịch.
- Từ chối giao dịch.
- Yêu cầu chờ xác nhận.

Decision Engine không được phép:

- Thay đổi Báo cáo phân tích.
- Thay đổi Kế hoạch giao dịch.
- Thay đổi Risk / Reward.
- Quản lý vị thế.

Các nhiệm vụ trên thuộc về module khác.

---

# Nguyên tắc thiết kế

Decision Engine phải:

- Khách quan.
- Có thể giải thích.
- Dựa trên dữ liệu.
- Tuân thủ Kế hoạch giao dịch.
- Ưu tiên quản trị rủi ro.

Nếu điều kiện chưa đầy đủ:

Không giao dịch.

Nếu rủi ro không phù hợp:

Không giao dịch.

Nếu Kế hoạch giao dịch mất hiệu lực:

Không giao dịch.

---

# Quan hệ với các module khác

```
Planner

↓

Decision Engine

↓

Risk Manager
```

Decision Engine chỉ nhận Kế hoạch giao dịch từ Planner.

Sau khi hoàn thành sẽ chuyển Quyết định giao dịch sang Risk Manager.

---

# Khả năng mở rộng

Trong tương lai Decision Engine có thể hỗ trợ:

- Nhiều chiến lược giao dịch.
- Nhiều chế độ giao dịch.
- Tự động đánh giá mức độ tin cậy.
- Hệ thống chấm điểm quyết định.
- Bộ lọc điều kiện giao dịch.

Mọi quyết định đều phải dựa trên Kế hoạch giao dịch.

---

# Triết lý

Decision Engine không cố gắng dự đoán thị trường.

Decision Engine chỉ lựa chọn hành động phù hợp nhất dựa trên:

- Báo cáo phân tích.
- Kế hoạch giao dịch.
- Điều kiện thị trường.
- Mức độ rủi ro.

Một quyết định đúng không phải là một giao dịch có lợi nhuận.

Một quyết định đúng là một quyết định tuân thủ đầy đủ quy trình và nguyên tắc của AI Trader.

---

# Phiên bản

Phiên bản hiện tại:

v0.1