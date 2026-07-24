---
author: HTLH
confidence: 100%
created: 2026-07-20
id: trading-discrete-data
language: vi
last_updated: 2026-07-21
review_cycle: Manual
status: Stable
tags:
- trading
- data
title: Dữ liệu rời rạc
version: 1
---

# Trading Data

------------------------------------------------------------------------

# README(16)

# Nguồn dữ liệu

> Nguồn dữ liệu là thành phần tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

------------------------------------------------------------------------

# Mục đích

Nguồn dữ liệu trả lời:

> Thực tế được ghi nhận như thế nào?

Nguồn dữ liệu chuẩn hóa dữ liệu từ Thực tế để cung cấp đầu vào cho Hệ
thống suy luận.

------------------------------------------------------------------------

# Triết lý

Dữ liệu luôn đi trước suy luận.

Không có dữ liệu.

Không có suy luận.

------------------------------------------------------------------------

# Kiến trúc

``` text
Nguồn dữ liệu

├── README.md
├── 01-ATS
└── 02-Dữ liệu rời rạc
```

------------------------------------------------------------------------

# Mối quan hệ với Trading

``` text
            Tri thức nền
                  │
                  ▼

Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận
```

Tri thức nền cung cấp các khái niệm và quy ước để chuẩn hóa dữ liệu.

Mọi suy luận đều bắt đầu từ dữ liệu.

------------------------------------------------------------------------

# Đầu vào

-   Thực tế.
-   Tri thức nền.

------------------------------------------------------------------------

# Đầu ra

Dữ liệu chuẩn hóa.

------------------------------------------------------------------------

# Thành phần

## 01 · ATS

ATS là một mẫu ghi nhận Thực tế theo cấu trúc thống nhất.

ATS giúp quan sát đồng thời nhiều khía cạnh của thị trường.

------------------------------------------------------------------------

## 02 · Dữ liệu rời rạc

Dữ liệu rời rạc ghi nhận một hoặc nhiều khía cạnh của Thực tế.

Ví dụ:

-   Funding Rate
-   Open Interest
-   CVD
-   VPIN
-   Fear & Greed
-   Long / Short Ratio
-   News
-   Macro
-   ...

Dữ liệu rời rạc có thể được sử dụng độc lập hoặc kết hợp với ATS.

------------------------------------------------------------------------

# Nguyên tắc

Mọi dữ liệu đều phản ánh Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa theo Tri thức nền trước khi được sử dụng.

ATS và Dữ liệu rời rạc đều là các nguồn dữ liệu của Hệ thống suy luận.

------------------------------------------------------------------------

# Vai trò trong Trading

``` text
Trading

├── Nguồn dữ liệu
│      Tiếp nhận
│
├── Hệ thống suy luận
│      Suy luận
│
├── Tri thức nền
│      Chuẩn hóa
│
└── Tri thức tích lũy
       Học hỏi
```

Nguồn dữ liệu là đầu vào của Hệ thống suy luận.

------------------------------------------------------------------------

# Tóm tắt

``` text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận
```

Nguồn dữ liệu định nghĩa:

-   Cách tiếp nhận Thực tế.
-   Cách chuẩn hóa dữ liệu.
-   Cấu trúc dữ liệu đầu vào của Hệ thống suy luận.

------------------------------------------------------------------------

# 01-ATS(1)

# ATS

> ATS là một mẫu ghi nhận và chuẩn hóa dữ liệu từ Thực tế.

------------------------------------------------------------------------

# Mục đích

ATS chuẩn hóa việc ghi nhận đồng thời nhiều khía cạnh của thị trường.

ATS không tham gia vào quá trình suy luận.

ATS chỉ tạo ra dữ liệu đầu vào cho Hệ thống suy luận.

------------------------------------------------------------------------

# Quy ước

Trong ATS, các ký hiệu được quy ước như sau.

## Auction Flow

-   **VP1**: Chỉ số VP1 của indicator Auction Flow.
-   **POC5**: Point of Control trên biểu đồ BTC khung 5m của indicator
    Auction Flow.
-   **Auction Line**: Đường Auction Flow.
-   **EMA20**: Đường EMA20 của Auction Flow.

## SonicR

-   **Cụm EMA34**: 3 đường màu xanh dương.
-   **EMA89**: Đường màu cam.
-   **EMA200**: Đường màu tím.
-   **EMA610**: Đường màu trắng.

## Volume Profile M30

-   **POC30**: Point of Control của Volume Profile khung 30m.
-   **VAH30**: Value Area High của Volume Profile khung 30m.
-   **VAL30**: Value Area Low của Volume Profile khung 30m.

------------------------------------------------------------------------

# Kiến trúc

``` text
ATS

├── Ảnh 1 · Đa khung thời gian
├── Ảnh 2 · Auction Flow
├── Ảnh 3 · Thực thi
└── Chỉ số bổ sung
```

------------------------------------------------------------------------

# Thứ tự đọc

``` text
Ảnh 1

↓

Ảnh 2

↓

Ảnh 3

↓

Chỉ số bổ sung
```

------------------------------------------------------------------------

# Ảnh 1 · Đa khung thời gian

## Bố cục

``` text
┌───────────────┬───────────────┐
│       D       │      4H       │
├───────────────┼───────────────┤
│      1H       │      15m      │
└───────────────┴───────────────┘
```

## Thứ tự đọc

``` text
D

↓

4H

↓

1H

↓

15m
```

## Ghi nhận

-   Giá
-   Cấu trúc
-   Cấu trúc SonicR
-   Khối lượng
-   RSI

------------------------------------------------------------------------

# Ảnh 2 · Auction Flow

## Bố cục

``` text
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

``` text
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

-   Giá
-   VP1
-   POC5

### RSI

-   RSI

### OI

-   Open Interest

### Auction Flow

-   Auction Line
-   EMA20

------------------------------------------------------------------------

# Ảnh 3 · Thực thi

## Bố cục

``` text
┌─────────────────────────┬─────────────────────────┐
│      5m + Delta         │ Heatmap Thanh lý 24H   │
├─────────────────────────┼─────────────────────────┤
│ Heatmap Sổ lệnh 1H      │ Volume Profile M30     │
└─────────────────────────┴─────────────────────────┘
```

## Thứ tự đọc

``` text
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

-   Giá
-   Cấu trúc SonicR
-   Delta
-   Khối lượng

### Heatmap Thanh lý

-   Các cụm thanh khoản còn tồn tại.

### Heatmap Sổ lệnh

-   Tường mua.
-   Tường bán.

### Volume Profile M30

Theo bảng thông tin của indicator:

-   POC30
-   VAH30
-   VAL30

------------------------------------------------------------------------

# Chỉ số bổ sung

Được ghi nhận cùng ba ảnh.

-   Funding Rate
-   CVD
-   VPIN
-   Agg Liquidation
-   Fear & Greed
-   Long / Short Ratio (1H)
    -   Global
    -   Top Accounts
    -   Top Positions

------------------------------------------------------------------------

# Triết lý

ATS chuẩn hóa cách ghi nhận dữ liệu.

ATS không tạo ra suy luận.

ATS chỉ cung cấp dữ liệu cho Hệ thống suy luận.

------------------------------------------------------------------------

# 02-Dữ liệu rời rạc(1)

# Dữ liệu rời rạc

> Dữ liệu rời rạc ghi nhận một hoặc nhiều khía cạnh của Thực tế.

------------------------------------------------------------------------

# Mục đích

Dữ liệu rời rạc ghi nhận những dữ liệu không nhất thiết phải nằm trong
ATS.

Dữ liệu rời rạc chuẩn hóa các dữ liệu đầu vào cho Hệ thống suy luận.

Dữ liệu rời rạc không tham gia vào quá trình suy luận.

------------------------------------------------------------------------

# Đặc điểm

Dữ liệu rời rạc có thể là:

-   Một chỉ số.
-   Một biểu đồ.
-   Một sự kiện.
-   Một tập dữ liệu.

Dữ liệu rời rạc có thể được sử dụng độc lập hoặc kết hợp với ATS.

------------------------------------------------------------------------

# Ví dụ

## Chỉ số

-   Funding Rate
-   Open Interest
-   CVD
-   VPIN
-   Fear & Greed
-   Long / Short Ratio

------------------------------------------------------------------------

## Dữ liệu

-   News
-   Macro
-   On-chain
-   Lịch kinh tế
-   Dữ liệu khác

------------------------------------------------------------------------

# Nguyên tắc

Mỗi dữ liệu phản ánh một phần của Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa trước khi được sử dụng.

ATS và Dữ liệu rời rạc đều là các nguồn dữ liệu của Hệ thống suy luận.

------------------------------------------------------------------------

# Triết lý

Dữ liệu rời rạc không tạo ra suy luận.

Dữ liệu rời rạc chỉ cung cấp dữ liệu cho Hệ thống suy luận.

------------------------------------------------------------------------

# Tóm tắt

``` text
Thực tế

↓

Dữ liệu rời rạc

↓

Hệ thống suy luận
```

Dữ liệu rời rạc là một nguồn dữ liệu của Hệ thống suy luận.
