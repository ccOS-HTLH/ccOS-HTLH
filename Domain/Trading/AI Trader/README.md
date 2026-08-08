# AI Trader

Version: 0.1

---

# Tổng quan

AI Trader là tầng thực thi được xây dựng trên nền tảng Trading Domain.

Trading Domain chịu trách nhiệm:

- Tri thức giao dịch
- Chuẩn hóa dữ liệu
- Hệ thống suy luận
- Tri thức tích lũy
- Báo cáo phân tích

AI Trader sử dụng kết quả từ Trading Domain để hỗ trợ ra quyết định giao dịch.

Trading Domain là bộ não.

AI Trader là người giao dịch.

---

# Mục tiêu

AI Trader được xây dựng để:

- Tiếp nhận dữ liệu ATS.
- Phân tích trạng thái thị trường.
- Xây dựng kế hoạch giao dịch.
- Đánh giá cơ hội giao dịch.
- Quản trị rủi ro.
- Hỗ trợ ra quyết định.
- Lưu trữ lịch sử giao dịch.
- Học hỏi từ kết quả thực tế.

AI Trader là trợ lý giao dịch có kỷ luật, không phải hệ thống dự đoán thị trường.

---

# Triết lý thiết kế

AI Trader không cố gắng dự đoán tương lai.

AI Trader tập trung vào:

- Hiểu thị trường.
- Đánh giá xác suất.
- Quản trị rủi ro.
- Thực thi kế hoạch nhất quán.
- Học hỏi từ mọi giao dịch đã hoàn thành.

Nguyên tắc cốt lõi:

> Nhất quán quan trọng hơn dự đoán.

> Bảo toàn vốn quan trọng hơn lợi nhuận.

---

# Kiến trúc

```text
ATS
│
▼
Scanner
│
▼
Analyzer
│
▼
Planner
│
▼
Decision Engine
│
▼
Risk Manager
│
▼
Journal
│
▼
Learning Engine
```

---

# Cấu trúc thư mục

```text
AI Trader
│
├── README.md
├── Scanner.md
├── Analyzer.md
├── Planner.md
├── Decision-Engine.md
├── Risk-Manager.md
├── Journal.md
└── Learning-Engine.md
```

---

# Quy trình hoạt động

```text
Nhận ATS
↓
Kiểm tra dữ liệu
↓
Phân tích thị trường
↓
Tạo Trading Report
↓
Lập kế hoạch giao dịch
↓
Đánh giá rủi ro
↓
Ra quyết định
↓
Theo dõi vị thế
↓
Đánh giá sau giao dịch
↓
Cập nhật Trading Memory
```

---

# Các thành phần chính

## Scanner

Tiếp nhận và chuẩn hóa dữ liệu ATS.

Đầu ra: dữ liệu thị trường có cấu trúc.

---

## Analyzer

Sử dụng Trading Domain để phân tích thị trường.

Đầu ra: Trading Report.

---

## Planner

Chuyển kết quả phân tích thành kế hoạch giao dịch.

Đầu ra: Entry, Stop Loss, Take Profit và Invalidation.

---

## Decision Engine

Đưa ra quyết định cuối cùng.

Các trạng thái:

- LONG
- SHORT
- HOLD
- NO TRADE
- WAIT CONFIRMATION

---

## Risk Manager

Bảo vệ vốn giao dịch.

Bao gồm:

- Kích thước vị thế.
- Mức rủi ro.
- Kiểm soát drawdown.
- Quản lý tổng mức phơi nhiễm.

---

## Journal

Lưu trữ toàn bộ lịch sử giao dịch.

Bao gồm:

- Setup.
- Entry.
- Exit.
- Kết quả.
- Ghi chú.

---

## Learning Engine

Học hỏi từ giao dịch đã hoàn thành.

Quy trình:

```text
Review
↓
Rút kinh nghiệm
↓
Cập nhật Trading Memory
↓
Cải thiện các quyết định trong tương lai
```

---

# Mối quan hệ với Trading Domain

```text
Trading Domain
├── Knowledge
├── Data
├── Reasoning
├── Memory
└── Report
│
▼
AI Trader
```

Trading Domain có thể hoạt động độc lập.

AI Trader bắt buộc phải sử dụng Trading Domain.

---

# Nguyên tắc vận hành

Mọi quyết định giao dịch phải:

- Có quy tắc rõ ràng.
- Có thể giải thích.
- Có đánh giá rủi ro.
- Có xác nhận đa tầng.
- Có tính nhất quán.

Không quyết định dựa trên một chỉ báo duy nhất.

Mỗi quyết định phải được xác nhận bởi:

- Cấu trúc thị trường.
- SonicR.
- Auction Flow.
- Order Flow.
- Liquidity.
- Risk Assessment.

---

# Phiên bản

Phiên bản hiện tại: **v0.1**.