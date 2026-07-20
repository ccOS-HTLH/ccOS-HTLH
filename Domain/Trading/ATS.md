---
title: ATS
id: trading-ats
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-19
last_updated: 2026-07-20
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - ats
---

# ATS

> ATS là tiêu chuẩn quan sát của Trading.

---

# Mục đích

ATS chuẩn hóa cách ghi nhận Thực tế.

ATS đảm bảo mọi lần quan sát đều có cùng cấu trúc, cùng thứ tự và cùng phạm vi thông tin.

---

# Triết lý

Quan sát trước.

Suy luận sau.

Quan sát nhất quán tạo nên suy luận nhất quán.

---

# Quy tắc quan sát

ATS ghi nhận Thực tế tại thời điểm quan sát.

Quan sát luôn nhất quán về cấu trúc, thứ tự và phạm vi thông tin.

---

# Quy ước

Các ký hiệu trong ATS được hiểu như sau.

## Auction Flow

- VP1: Chỉ số VP1 của indicator Auction Flow.
- POC5: Point of Control trên biểu đồ BTC khung 5m của indicator Auction Flow.
- Auction Line: Đường Auction Flow.
- EMA20: Đường EMA20 của Auction Flow.

## SonicR

Bao gồm:

- EMA34 (xanh dương)
- EMA89 (cam)
- EMA200 (tím)
- EMA610 (trắng)

## Volume Profile M30

- POC30: Point of Control của Volume Profile M30.
- VAH30: Value Area High.
- VAL30: Value Area Low.

---

# Kiến trúc

```text
ATS

├── Ảnh 1 · Đa khung thời gian
├── Ảnh 2 · Auction Flow
├── Ảnh 3 · Thực thi
└── Metrics
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

Metrics
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

## Nội dung quan sát

Trên mỗi khung thời gian, quan sát:

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

## Nội dung quan sát

### Biểu đồ BTC

Quan sát:

- Giá
- VP1
- POC5

### RSI

Quan sát:

- RSI

### OI

Quan sát:

- Open Interest

### Auction Flow

Quan sát:

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

## Nội dung quan sát

### 5m + Delta

Quan sát:

- Giá
- Cấu trúc SonicR
- Delta
- Khối lượng

### Heatmap Thanh lý

Quan sát:

- Các cụm thanh khoản còn tồn tại tại thời điểm quan sát.

### Heatmap Sổ lệnh

Quan sát:

- Tường mua còn tồn tại.
- Tường bán còn tồn tại.

### Volume Profile M30

Quan sát:

- POC30
- VAH30
- VAL30

---

# Metrics

## Chỉ số cốt lõi

- Giá
- VP1
- POC5
- POC30
- VAH30
- VAL30
- Cấu trúc SonicR
- EMA20
- RSI
- OI
- Delta
- Auction Line

## Chỉ số bổ sung

Được đính kèm cùng ba ảnh:

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

# Vai trò trong Trading

```text
ATS

↓

Hệ thống suy luận

↓

Thực tế

↓

ATS
```

ATS là điểm bắt đầu của quá trình suy luận trong Trading.

ATS chuẩn hóa Quan sát trước khi chuyển sang Hệ thống suy luận.

---

# Tóm tắt

```text
ATS

↓

Ảnh 1
Đa khung thời gian

↓

Ảnh 2
Auction Flow

↓

Ảnh 3
Thực thi

↓

Metrics
```

ATS định nghĩa:

- Kiến trúc quan sát.
- Bố cục quan sát.
- Thứ tự đọc.
- Nội dung quan sát.
- Metrics.

ATS chuẩn hoá cách ghi nhận Thực tế.

ATS là tầng Quan sát của Trading.