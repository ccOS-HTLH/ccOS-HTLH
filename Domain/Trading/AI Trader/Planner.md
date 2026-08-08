# Planner

Phiên bản: 0.1

---

# Tổng quan

Planner là module chịu trách nhiệm xây dựng kế hoạch giao dịch.

Planner nhận Trading Report từ Analyzer và chuyển kết quả phân tích thành một hoặc nhiều kịch bản giao dịch.

Planner không quyết định có vào lệnh hay không.

---

# Mục tiêu

Planner chịu trách nhiệm:

- Xây dựng kế hoạch giao dịch.
- Xác định các kịch bản.
- Xác định vùng vào lệnh.
- Xác định vùng vô hiệu (Invalidation).
- Xác định mục tiêu lợi nhuận.
- Đánh giá tỷ lệ Risk / Reward.

Planner không chịu trách nhiệm:

- Ra quyết định giao dịch.
- Quản lý khối lượng lệnh.
- Theo dõi vị thế.

---

# Luồng hoạt động

```
Trading Report

↓

Xây dựng kịch bản

↓

Trading Plan

↓

Decision Engine
```

---

# Đầu vào

Planner nhận:

- Trading Report.

Trading Report bao gồm:

- Market Structure
- Auction Analysis
- Order Flow
- Positioning
- Liquidity
- Volume Profile
- Confluence

---

# Quy trình lập kế hoạch

Planner thực hiện theo trình tự:

```
Đánh giá bối cảnh

↓

Xây dựng các kịch bản

↓

Xác định Entry

↓

Xác định Invalidation

↓

Xác định Target

↓

Đánh giá Risk / Reward

↓

Hoàn thành Trading Plan
```

---

# Trading Plan

Một Trading Plan bao gồm:

## Bias

Ví dụ:

- Bullish
- Bearish
- Neutral

---

## Kịch bản

Có thể bao gồm:

- Kịch bản chính.
- Kịch bản thay thế.

---

## Entry Zone

Vùng giá dự kiến để tìm điểm vào lệnh.

---

## Invalidation

Điều kiện làm kế hoạch mất hiệu lực.

Ví dụ:

- Mất vùng hỗ trợ.
- Phá vỡ cấu trúc.
- Thay đổi Order Flow.

---

## Take Profit

Có thể chia thành:

- TP1
- TP2
- TP3

---

## Risk / Reward

Đánh giá tỷ lệ lợi nhuận so với rủi ro của từng kịch bản.

---

# Đầu ra

Planner tạo:

Trading Plan.

Trading Plan sẽ được chuyển sang Decision Engine.

---

# Giới hạn trách nhiệm

Planner được phép:

- Lập kế hoạch.
- Xây dựng kịch bản.
- Đề xuất vùng giao dịch.

Planner không được phép:

- LONG.
- SHORT.
- HOLD.
- NO TRADE.

Quyết định cuối cùng thuộc về Decision Engine.

---

# Nguyên tắc thiết kế

Planner phải:

- Dựa trên Trading Report.
- Có nhiều kịch bản nếu cần.
- Luôn xác định điều kiện vô hiệu.
- Luôn cân nhắc Risk / Reward.

Planner không được xây dựng kế hoạch dựa trên cảm tính.

---

# Quan hệ với các module khác

```
Analyzer

↓

Planner

↓

Decision Engine
```

Planner chỉ nhận dữ liệu từ Analyzer và chuyển Trading Plan cho Decision Engine.

---

# Khả năng mở rộng

Trong tương lai Planner có thể hỗ trợ:

- Nhiều chiến lược giao dịch.
- Nhiều khung thời gian.
- Nhiều tài sản.
- Nhiều phong cách giao dịch.

Mọi kế hoạch đều phải dựa trên Trading Report.

---

# Phiên bản

Phiên bản hiện tại:

v0.1