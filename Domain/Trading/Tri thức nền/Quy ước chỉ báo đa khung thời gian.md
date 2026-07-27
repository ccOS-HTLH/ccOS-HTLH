---
title: Quy ước chỉ báo đa khung thời gian
id: convention-multi-timeframe-indicators
version: 1.1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-25
last_updated: 2026-07-27
review_cycle: Monthly
confidence: 100%
tags:
  - convention
  - indicator
  - timeframe
---

# Quy ước chỉ báo đa khung thời gian

> Chuẩn hóa cách biểu diễn các chỉ báo và dữ liệu phụ thuộc khung thời gian trong Trading Domain.

---

# Mục đích

Quy ước này chuẩn hóa cách biểu diễn các chỉ báo và dữ liệu phụ thuộc khung thời gian trong Trading Domain.

Việc chuẩn hóa giúp:

- Xác định rõ ngữ cảnh.
- Thống nhất cách biểu diễn dữ liệu.
- Hỗ trợ Hệ thống suy luận.
- Hỗ trợ Tri thức tích luỹ.

---

# Triết lý

Chỉ báo luôn gắn với ngữ cảnh.

Khung thời gian là một phần của dữ liệu.

Dữ liệu được chuẩn hóa trước khi tham gia Hệ thống suy luận.

---

# Phạm vi áp dụng

Quy ước này được sử dụng thống nhất trong:

- Nguồn dữ liệu.
- Hệ thống suy luận.
- Tri thức nền.
- Tri thức tích luỹ.
- Bộ nhớ.

---

# Cấu trúc biểu diễn

Các chỉ báo được biểu diễn theo cấu trúc:

```text
<Tên chỉ báo> <Khung thời gian>
```

Ví dụ:

```text
EMA34 15m

RSI 1H

Volume 5m

CVD 5m
```

---

# Các nhóm dữ liệu

## Chỉ báo kỹ thuật

Ví dụ:

```text
EMA34 5m
EMA89 15m
EMA200 1H
EMA610 4H

RSI 5m
RSI 15m
RSI 1H
RSI 4H

Volume 5m
Volume 15m
Volume 1H
```

---

## Volume Profile

Ví dụ:

```text
POC30

VAH30

VAL30
```

Trong đó:

- POC30 = Point of Control khung 30 phút.
- VAH30 = Value Area High khung 30 phút.
- VAL30 = Value Area Low khung 30 phút.

---

## Auction Flow

Ví dụ:

```text
Auction Line

EMA20

POC5

VP1
```

Trong đó:

- Auction Line = Đường Auction Flow.
- EMA20 = EMA20 của Auction Flow.
- POC5 = Point of Control khung 5 phút.
- VP1 = Value Pivot của Auction Flow.

---

## Dữ liệu dòng tiền

Ví dụ:

```text
OI

Funding

CVD 5m

Delta 5m

Agg Liq 5m
```

Trong đó:

- OI = Open Interest hiện tại.
- Funding = Funding Rate hiện tại.
- CVD 5m = Cumulative Volume Delta khung 5 phút.
- Delta 5m = Delta khung 5 phút.
- Agg Liq 5m = Aggressive Liquidation khung 5 phút.

---

## Dữ liệu thị trường

Ví dụ:

```text
Long/Short Ratio 1H

Fear & Greed
```

Trong đó:

- Long/Short Ratio luôn đi kèm khung thời gian tương ứng.
- Fear & Greed sử dụng giá trị hiện tại.

---

# Ngoại lệ

Một số dữ liệu không phụ thuộc khung thời gian.

Ví dụ:

```text
OI

Funding

Fear & Greed

News

Macro
```

Các dữ liệu này được biểu diễn theo quy ước riêng của từng dữ liệu.

Không bổ sung khung thời gian nếu dữ liệu không phụ thuộc khung thời gian.

---

# Ví dụ

## EMA

Biểu diễn chuẩn:

```text
EMA200 4H đang là kháng cự.
```

Khung thời gian được biểu diễn cùng tên chỉ báo.

---

## RSI

Biểu diễn chuẩn:

```text
RSI 15m đang tiến vào vùng quá mua.
```

Khung thời gian phản ánh đúng ngữ cảnh của chỉ báo.

---

## EMA hỗ trợ

Biểu diễn chuẩn:

```text
Giá giữ trên EMA34 15m.
```

Mỗi EMA luôn đi kèm khung thời gian tương ứng.

---

## CVD

Biểu diễn chuẩn:

```text
CVD 5m đang tăng.
```

Khung thời gian giúp xác định đúng dữ liệu được quan sát.

---

## Long / Short Ratio

Biểu diễn chuẩn:

```text
Long/Short Ratio 1H nghiêng về phe Long.
```

Khung thời gian là một phần của dữ liệu.

---

## Funding

Biểu diễn chuẩn:

```text
Funding đang dương.
```

Funding sử dụng giá trị hiện tại.

---

## OI

Biểu diễn chuẩn:

```text
OI đang tăng.
```

OI sử dụng giá trị hiện tại.

---

# Nguyên tắc

Khung thời gian là một phần của dữ liệu.

Mọi chỉ báo được biểu diễn cùng khung thời gian tương ứng.

Mọi dữ liệu phụ thuộc khung thời gian sử dụng cùng một quy ước biểu diễn.

Các dữ liệu không phụ thuộc khung thời gian không bổ sung khung thời gian.

Mọi tài liệu trong Trading Domain sử dụng thống nhất quy ước này.

Mọi dữ liệu được chuẩn hóa trước khi tham gia Hệ thống suy luận.

---

# Vai trò

Quy ước này giúp:

- Chuẩn hóa dữ liệu.
- Chuẩn hóa tài liệu.
- Chuẩn hóa Hệ thống suy luận.
- Chuẩn hóa Tri thức tích luỹ.
- Chuẩn hóa Bộ nhớ.

Đây là quy ước chung của toàn bộ Trading Domain.

---

# Tóm tắt

Khung thời gian là một phần của dữ liệu.

Chỉ báo luôn đi cùng khung thời gian tương ứng.

Các dữ liệu không phụ thuộc khung thời gian sử dụng quy ước biểu diễn riêng.

Mọi thành phần trong Trading Domain sử dụng thống nhất quy ước này trước khi dữ liệu tham gia Hệ thống suy luận.