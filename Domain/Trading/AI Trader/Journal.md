# Journal

Phiên bản: 0.1

---

# Tổng quan

Journal là module chịu trách nhiệm ghi nhận toàn bộ lịch sử giao dịch.

Journal lưu lại các quyết định, quá trình thực hiện và kết quả của từng giao dịch.

Journal không phân tích giao dịch.

Journal không đánh giá đúng hay sai.

---

# Mục tiêu

Journal chịu trách nhiệm:

- Ghi nhận giao dịch.
- Lưu lịch sử giao dịch.
- Lưu kết quả giao dịch.
- Lưu bối cảnh giao dịch.
- Chuyển dữ liệu sang Learning Engine.

---

# Luồng hoạt động

```
Kế hoạch quản trị rủi ro

↓

Thực hiện giao dịch

↓

Ghi nhận kết quả

↓

Nhật ký giao dịch

↓

Learning Engine
```

---

# Đầu vào

Journal nhận:

- Kế hoạch quản trị rủi ro.
- Thông tin giao dịch thực tế.

Bao gồm:

- Hành động.
- Entry.
- Stop Loss.
- Take Profit.
- Thời gian.
- Kết quả.

---

# Quy trình ghi nhận

Journal thực hiện theo trình tự:

```
Nhận giao dịch

↓

Lưu thông tin

↓

Lưu kết quả

↓

Hoàn thành Nhật ký giao dịch
```

---

# Nội dung ghi nhận

Journal lưu các thông tin sau.

## Trade ID

Ví dụ:

BTC-20260807-001

---

## Thông tin giao dịch

- Thời gian.
- Tài sản.
- Khung thời gian.

---

## Kế hoạch giao dịch

- Bias.
- Kịch bản.
- Entry.
- Stop Loss.
- Take Profit.

---

## Quyết định giao dịch

- Hành động.
- Mức độ tin cậy.
- Lý do.

---

## Quản trị rủi ro

- Position Size.
- Risk / Reward.
- Rủi ro mỗi lệnh.

---

## Kết quả giao dịch

- Giá vào.
- Giá thoát.
- Lợi nhuận / Thua lỗ.
- Risk / Reward thực tế.
- Trạng thái.

Ví dụ:

- TP
- SL
- Manual Exit
- Cancelled

---

## Ghi chú

Thông tin bổ sung nếu có.

---

# Đầu ra

Journal tạo:

Nhật ký giao dịch.

Mẫu chuẩn:

```text
Nhật ký giao dịch

Trade ID:
BTC-20260807-001

Thời gian:
2026-08-07 14:30 UTC+7

Tài sản:
BTCUSDT

Khung thời gian:
M15

Hành động:
LONG

Entry:
64250

Stop Loss:
63980

Take Profit:
64800

Risk / Reward:
1 : 2

Kết quả:
TP

Lợi nhuận:
+2R

Ghi chú:
Đạt TP2.
```

---

# Giới hạn trách nhiệm

Journal được phép:

- Ghi nhận giao dịch.
- Lưu lịch sử.
- Lưu kết quả.

Journal không được phép:

- Phân tích giao dịch.
- Đánh giá giao dịch.
- Đề xuất cải thiện.
- Cập nhật Trading Memory.

Các nhiệm vụ trên thuộc về Learning Engine.

---

# Nguyên tắc thiết kế

Journal phải:

- Chính xác.
- Trung thực.
- Đầy đủ.
- Nhất quán.

Journal chỉ ghi nhận sự kiện đã xảy ra.

Không bổ sung nhận định.

Không suy luận.

Trade ID là định danh duy nhất của mỗi giao dịch.

Trade ID không được thay đổi sau khi được tạo.

Mọi module của AI Trader phải sử dụng cùng một Trade ID để đảm bảo khả năng truy vết toàn bộ vòng đời giao dịch.

---

# Quan hệ với các module khác

```
Risk Manager

↓

Journal

↓

Learning Engine
```

Journal nhận dữ liệu từ Risk Manager.

Sau khi giao dịch hoàn tất, Journal chuyển Nhật ký giao dịch sang Learning Engine.

---

# Khả năng mở rộng

Trong tương lai Journal có thể hỗ trợ:

- Lưu hình ảnh ATS.
- Lưu Trading Report.
- Lưu Kế hoạch giao dịch.
- Lưu Quyết định giao dịch.
- Lưu thống kê hiệu suất.
- Xuất báo cáo giao dịch.

Mọi dữ liệu đều được lưu dưới dạng lịch sử và không bị chỉnh sửa.

---

# Triết lý

Journal không quan tâm giao dịch thắng hay thua.

Journal chỉ quan tâm việc ghi nhận đầy đủ và chính xác.

Một nhật ký trung thực là nền tảng cho mọi quá trình học hỏi và cải thiện.

---

# Phiên bản

Phiên bản hiện tại:

v0.1