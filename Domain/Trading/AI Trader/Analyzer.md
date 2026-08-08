# Analyzer

Phiên bản: 0.1

---

# Tổng quan

Analyzer là module chịu trách nhiệm phân tích dữ liệu thị trường.

Analyzer nhận Structured ATS từ Scanner và sử dụng Trading Domain để tạo ra Trading Report.

Analyzer không đưa ra quyết định giao dịch.

---

# Mục tiêu

Analyzer chịu trách nhiệm:

- Phân tích dữ liệu thị trường.
- Xác định bối cảnh thị trường.
- Tổng hợp tín hiệu.
- Đánh giá mức độ đồng thuận.
- Tạo Trading Report.

Analyzer không chịu trách nhiệm:

- Lập kế hoạch giao dịch.
- Quản lý rủi ro.
- Quyết định vào lệnh.

---

# Luồng hoạt động

```
Structured ATS

↓

Trading Domain

↓

Knowledge

↓

Data

↓

Reasoning

↓

Memory

↓

Report

↓

Trading Report
```

---

# Đầu vào

Analyzer nhận:

- Structured ATS từ Scanner.

Bao gồm:

- Market Charts
- Auction Data
- Exchange Data
- ATS Metrics
- Context

---

# Quy trình phân tích

Analyzer sử dụng Trading Domain theo đúng thứ tự.

```
Trading Knowledge

↓

Trading Data

↓

Trading Reasoning

↓

Trading Memory

↓

Trading Report
```

Không được bỏ qua bất kỳ bước nào.

---

# Nhiệm vụ

Analyzer phải:

- Đọc toàn bộ dữ liệu.
- Phân tích đa khung thời gian.
- Phân tích Auction.
- Phân tích Order Flow.
- Phân tích Liquidity.
- Phân tích Positioning.
- Phân tích Volume Profile.
- Tổng hợp kết quả.

---

# Đầu ra

Analyzer tạo:

Trading Report.

Trading Report bao gồm:

- Market Structure
- Auction Analysis
- Order Flow
- Positioning
- Liquidity
- Volume Profile
- Confluence
- Trading Summary

Analyzer không tạo Trading Plan.

---

# Giới hạn trách nhiệm

Analyzer được phép:

- Phân tích.
- Đánh giá.
- Tổng hợp.

Analyzer không được phép:

- LONG.
- SHORT.
- HOLD.
- NO TRADE.

Analyzer chỉ mô tả thị trường.

---

# Nguyên tắc thiết kế

Analyzer phải:

- Khách quan.
- Có thể giải thích.
- Nhất quán.
- Dựa trên dữ liệu.

Không suy diễn khi thiếu dữ liệu.

Không bỏ qua dữ liệu đầu vào.

---

# Quan hệ với các module khác

```
Scanner

↓

Analyzer

↓

Planner
```

Analyzer chỉ giao tiếp:

- Nhận dữ liệu từ Scanner.
- Trả Trading Report cho Planner.

---

# Khả năng mở rộng

Trong tương lai Analyzer có thể bổ sung:

- Phân tích liên thị trường.
- Phân tích On-chain.
- Phân tích Tin tức.
- Phân tích AI Vision.
- Phân tích nhiều tài sản.

Các chức năng mới phải tích hợp thông qua Trading Domain.

---

# Phiên bản

Phiên bản hiện tại:

v0.1