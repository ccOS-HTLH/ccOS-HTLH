# Scanner

Phiên bản: 0.1

---

# Tổng quan

Scanner là module đầu tiên của AI Trader.

Nhiệm vụ của Scanner là tiếp nhận, kiểm tra và chuẩn hóa toàn bộ dữ liệu đầu vào trước khi chuyển sang Analyzer.

Scanner không thực hiện bất kỳ hành động phân tích hay suy luận nào.

---

# Mục tiêu

Scanner chịu trách nhiệm:

- Tiếp nhận dữ liệu ATS.
- Kiểm tra dữ liệu đầu vào.
- Phát hiện dữ liệu thiếu.
- Chuẩn hóa dữ liệu.
- Chuyển dữ liệu sang định dạng thống nhất.

Đầu ra của Scanner là dữ liệu ATS đã được chuẩn hóa.

---

# Luồng hoạt động

```
ATS Input

↓

Kiểm tra dữ liệu

↓

Chuẩn hóa

↓

Structured ATS

↓

Analyzer
```

---

# Nguồn dữ liệu đầu vào

Scanner hỗ trợ các nguồn dữ liệu sau.

## 1. Ảnh ATS

Bao gồm:

- Ảnh 1
- Ảnh 2
- Ảnh 3

---

## 2. Chỉ số ATS

Ví dụ:

- CVD
- Funding
- VPIN
- Agg Liquidation
- Long / Short Ratio
- Fear & Greed

---

## 3. Dữ liệu bổ sung (Tùy chọn)

Có thể bao gồm:

- DXY
- Vàng
- Nasdaq
- Dầu
- Tin tức
- Lịch kinh tế

---

# Kiểm tra dữ liệu

Scanner phải kiểm tra:

## Ảnh

- Có đủ số lượng ảnh.
- Đúng thứ tự.
- Có thể đọc được.
- Không bị che.

---

## Chỉ số

- Có đầy đủ.
- Đúng định dạng.
- Không bị thiếu giá trị.

---

# Chuẩn hóa dữ liệu

Scanner chuyển toàn bộ dữ liệu về một cấu trúc thống nhất.

Ví dụ:

```
ATS

├── Image 1
├── Image 2
├── Image 3
│
├── Metrics
│   ├── CVD
│   ├── Funding
│   ├── VPIN
│   ├── Agg Liq
│   ├── Long / Short
│   └── Fear & Greed
│
└── Context
```

---

# Đầu ra

Sau khi hoàn thành, Scanner tạo ra một đối tượng:

Structured ATS

Đối tượng này sẽ được chuyển sang Analyzer.

---

# Giới hạn trách nhiệm

Scanner được phép:

- Đọc dữ liệu.
- Kiểm tra dữ liệu.
- Chuẩn hóa dữ liệu.

Scanner không được phép:

- Phân tích xu hướng.
- Đánh giá tín hiệu.
- Dự đoán giá.
- Đưa ra quyết định giao dịch.

Mọi hoạt động phân tích thuộc về Analyzer.

---

# Nguyên tắc thiết kế

Scanner phải:

- Chính xác.
- Nhất quán.
- Có khả năng mở rộng.
- Không phụ thuộc vào chiến lược giao dịch.

Scanner chỉ quan tâm dữ liệu đầu vào.

Không quan tâm kết quả giao dịch.

---

# Khả năng mở rộng

Trong tương lai Scanner có thể hỗ trợ:

- Video.
- API.
- CSV.
- JSON.
- TradingView.
- Exchange API.
- On-chain Data.
- AI Vision.

Mọi nguồn dữ liệu mới đều phải được chuẩn hóa trước khi chuyển sang Analyzer.

---

# Phiên bản

Phiên bản hiện tại:

v0.1