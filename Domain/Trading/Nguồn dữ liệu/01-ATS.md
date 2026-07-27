---
title: ATS
id: trading-ats
version: 1.1
status: Stable
author: HTLH
language: vi
created: 2026-07-19
last_updated: 2026-07-27
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - ats
---

# ATS

> ATS là mẫu chuẩn để ghi nhận và chuẩn hóa dữ liệu từ Thực tế.

---

# Mục đích

ATS chuẩn hóa việc ghi nhận dữ liệu từ Thực tế theo một cấu trúc thống nhất.

ATS không tham gia vào quá trình suy luận.

ATS chỉ tạo ra dữ liệu đầu vào cho Hệ thống suy luận.

---

# Triết lý

ATS chuẩn hóa cách ghi nhận dữ liệu.

ATS không tạo ra suy luận.

ATS chỉ cung cấp dữ liệu cho Hệ thống suy luận.

---

# Quy ước dữ liệu

Trong ATS, các ký hiệu được quy ước như sau.

## Auction Flow

- **VP1**: Chỉ số VP1 của indicator Auction Flow.
- **POC5**: Point of Control trên biểu đồ BTC khung 5m của indicator Auction Flow.
- **Auction Line**: Đường Auction Flow.
- **EMA20**: Đường EMA20 của Auction Flow.

---

## SonicR

- **Cụm EMA34**: Ba đường EMA34 màu xanh dương.
- **EMA89**: Đường EMA89 màu cam.
- **EMA200**: Đường EMA200 màu tím.
- **EMA610**: Đường EMA610 màu trắng.

---

## Volume Profile M30

- **POC30**: Point of Control của Volume Profile khung 30 phút.
- **VAH30**: Value Area High của Volume Profile khung 30 phút.
- **VAL30**: Value Area Low của Volume Profile khung 30 phút.

---

# Kiến trúc

```text
ATS

├── 01 · Đa khung thời gian
├── 02 · Auction Flow
├── 03 · Thực thi
└── 04 · Chỉ số bổ sung
```

---

# Thứ tự đọc

```text
01 · Đa khung thời gian

↓

02 · Auction Flow

↓

03 · Thực thi

↓

04 · Chỉ số bổ sung
```

---

# 01 · Đa khung thời gian

## Bố cục

```text
┌───────────────┬───────────────┐
│       D       │      4H       │
├───────────────┼───────────────┤
│      1H       │      15m      │
└───────────────┴───────────────┘
```

---

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

---

## Ghi nhận

- Giá.
- Cấu trúc.
- Cấu trúc SonicR.
- Khối lượng.
- RSI.

---

# 02 · Auction Flow

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

---

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

---

## Ghi nhận

### Biểu đồ BTC

- Giá.
- VP1.
- POC5.

### RSI

- RSI.

### OI

- Open Interest.

### Auction Flow

- Auction Line.
- EMA20.

---

# 03 · Thực thi

## Bố cục

```text
┌─────────────────────────┬─────────────────────────┐
│      5m + Delta         │ Heatmap Thanh khoản    │
├─────────────────────────┼─────────────────────────┤
│ Heatmap Sổ lệnh         │ Volume Profile M30     │
└─────────────────────────┴─────────────────────────┘
```

---

## Thứ tự đọc

```text
5m + Delta

↓

Heatmap Thanh khoản

↓

Heatmap Sổ lệnh

↓

Volume Profile M30
```

---

## Ghi nhận

### 5m + Delta

- Giá.
- Cấu trúc SonicR.
- Delta.
- Khối lượng.

### Heatmap Thanh khoản

- Các cụm thanh khoản còn tồn tại.

### Heatmap Sổ lệnh

- Tường mua.
- Tường bán.

### Volume Profile M30

Theo bảng thông tin của indicator:

- POC30.
- VAH30.
- VAL30.

---

# 04 · Chỉ số bổ sung

Được ghi nhận cùng ba ảnh.

## Dòng tiền

- Funding Rate.
- CVD.
- VPIN.
- Agg Liquidation.

---

## Tâm lý thị trường

- Fear & Greed.

---

## Vị thế thị trường

Long / Short Ratio (1H)

- Global.
- Top Accounts.
- Top Positions.

---

# Nguyên tắc

Mọi dữ liệu đều phản ánh Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa theo các quy ước trong Tri thức nền trước khi được sử dụng.

ATS chỉ ghi nhận dữ liệu.

ATS không tạo ra nhận định.

ATS không tạo ra suy luận.

ATS là một trong các nguồn dữ liệu của Hệ thống suy luận.

---

# Vai trò trong Nguồn dữ liệu

```text
Thực tế

↓

ATS

↓

Dữ liệu chuẩn hóa

↓

Hệ thống suy luận
```

ATS là mẫu chuẩn để ghi nhận dữ liệu.

ATS giúp chuẩn hóa:

- Cấu trúc dữ liệu.
- Thứ tự quan sát.
- Quy ước dữ liệu.

ATS không tham gia vào quá trình suy luận.

---

# Tóm tắt

```text
Thực tế

↓

ATS

↓

Dữ liệu chuẩn hóa

↓

Hệ thống suy luận
```

ATS chuẩn hóa:

- Cách ghi nhận Thực tế.
- Thứ tự quan sát.
- Cấu trúc dữ liệu.
- Quy ước dữ liệu.

ATS tạo ra dữ liệu đầu vào thống nhất cho Hệ thống suy luận.