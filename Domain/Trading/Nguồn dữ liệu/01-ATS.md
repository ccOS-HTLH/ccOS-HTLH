---
title: ATS
id: trading-ats
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-19
last_updated: 2026-07-21
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - ats
---

# ATS

> ATS là một mẫu ghi nhận và chuẩn hóa dữ liệu từ Thực tế.

---

# Mục đích

ATS chuẩn hóa việc ghi nhận đồng thời nhiều khía cạnh của thị trường.

ATS không tham gia vào quá trình suy luận.

ATS chỉ tạo ra dữ liệu đầu vào cho Hệ thống suy luận.

---

# Quy ước

Trong ATS, các ký hiệu được quy ước như sau.

## Auction Flow

- **VP1**: Chỉ số VP1 của indicator Auction Flow.
- **POC5**: Point of Control trên biểu đồ BTC khung 5m của indicator Auction Flow.
- **Auction Line**: Đường Auction Flow.
- **EMA20**: Đường EMA20 của Auction Flow.

## SonicR

- **Cụm EMA34**: 3 đường màu xanh dương.
- **EMA89**: Đường màu cam.
- **EMA200**: Đường màu tím.
- **EMA610**: Đường màu trắng.

## Volume Profile M30

- **POC30**: Point of Control của Volume Profile khung 30m.
- **VAH30**: Value Area High của Volume Profile khung 30m.
- **VAL30**: Value Area Low của Volume Profile khung 30m.

---

# Kiến trúc

```text
ATS

├── Ảnh 1 · Đa khung thời gian
├── Ảnh 2 · Auction Flow
├── Ảnh 3 · Thực thi
└── Chỉ số bổ sung
```

---

# Thứ tự đọc

```text
Ảnh 1

↓

Ảnh 2

↓

Ảnh 3

↓

Chỉ số bổ sung
```

---

# Ảnh 1 · Đa khung thời gian

## Bố cục

```text
┌───────────────┬───────────────┐
│       D       │      4H       │
├───────────────┼───────────────┤
│      1H       │      15m      │
└───────────────┴───────────────┘
```

## Thứ tự đọc

```text
D

↓

4H

↓

1H

↓

15m
```

## Ghi nhận

- Giá
- Cấu trúc
- Cấu trúc SonicR
- Khối lượng
- RSI

---

# Ảnh 2 · Auction Flow

## Bố cục

```text
Biểu đồ BTC
(VP1 + POC5)

↓

RSI

↓

OI

↓

Auction Flow
(Auction Line + EMA20)
```

## Thứ tự đọc

```text
Biểu đồ BTC

↓

RSI

↓

OI

↓

Auction Flow
```

## Ghi nhận

### Biểu đồ BTC

- Giá
- VP1
- POC5

### RSI

- RSI

### OI

- Open Interest

### Auction Flow

- Auction Line
- EMA20

---

# Ảnh 3 · Thực thi

## Bố cục

```text
┌─────────────────────────┬─────────────────────────┐
│      5m + Delta         │ Heatmap Thanh lý 24H   │
├─────────────────────────┼─────────────────────────┤
│ Heatmap Sổ lệnh 1H      │ Volume Profile M30     │
└─────────────────────────┴─────────────────────────┘
```

## Thứ tự đọc

```text
5m + Delta

↓

Heatmap Thanh lý

↓

Heatmap Sổ lệnh

↓

Volume Profile M30
```

## Ghi nhận

### 5m + Delta

- Giá
- Cấu trúc SonicR
- Delta
- Khối lượng

### Heatmap Thanh lý

- Các cụm thanh khoản còn tồn tại.

### Heatmap Sổ lệnh

- Tường mua.
- Tường bán.

### Volume Profile M30

Theo bảng thông tin của indicator:

- POC30
- VAH30
- VAL30

---

# Chỉ số bổ sung

Được ghi nhận cùng ba ảnh.

- Funding Rate
- CVD
- VPIN
- Agg Liquidation
- Fear & Greed
- Long / Short Ratio (1H)
  - Global
  - Top Accounts
  - Top Positions

---

# Triết lý

ATS chuẩn hóa cách ghi nhận dữ liệu.

ATS không tạo ra suy luận.

ATS chỉ cung cấp dữ liệu cho Hệ thống suy luận.