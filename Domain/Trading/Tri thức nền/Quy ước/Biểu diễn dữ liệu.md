---
title: Biểu diễn dữ liệu
id: convention-data-representation
version: 2.1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-25
last_updated: 2026-07-31
review_cycle: Monthly
confidence: 100%
tags:
  - convention
  - data
  - representation
---

# Biểu diễn dữ liệu

> Chuẩn hóa cách biểu diễn dữ liệu trong Trading Domain.

---

# Mục đích

Tài liệu này chuẩn hóa cách biểu diễn mọi dữ liệu được sử dụng trong Trading Domain.

Việc chuẩn hóa giúp:

- Xác định đúng ngữ cảnh của dữ liệu.
- Thống nhất cách biểu diễn trong toàn bộ Domain.
- Chuẩn hóa dữ liệu đầu vào của Hệ thống suy luận.
- Chuẩn hóa Tri thức tích luỹ.
- Giảm sai lệch khi trao đổi giữa AI và con người.

---

# Triết lý

Dữ liệu luôn gắn với ngữ cảnh.

Khung thời gian là một phần của dữ liệu khi dữ liệu phụ thuộc thời gian.

Mọi dữ liệu phải được chuẩn hóa trước khi tham gia Hệ thống suy luận.

---

# Phạm vi áp dụng

Quy ước này được sử dụng thống nhất trong:

- Nguồn dữ liệu.
- Hệ thống suy luận.
- Tri thức nền.
- Tri thức tích luỹ.
- Build.

---

# Phân loại dữ liệu

Trading Domain sử dụng hai cách biểu diễn dữ liệu.

```text
Biểu diễn dữ liệu

├── Dữ liệu phụ thuộc khung thời gian

└── Dữ liệu tức thời
```

---

# Dữ liệu theo khung thời gian

Các dữ liệu này luôn gắn với một khung thời gian cụ thể.

Cấu trúc biểu diễn:

```text
<Tên dữ liệu> <Khung thời gian>
```

Ví dụ:

```text
EMA34 5m

EMA200 4H

RSI 15m

Volume 1H

OI 5m

Relative OI 5m

CVD 5m

Delta 5m

Agg Liq 5m

Long/Short Ratio 1H
```

Khung thời gian luôn được xem là một phần của dữ liệu.

---

# Dữ liệu tức thời

Các dữ liệu này phản ánh trạng thái tại thời điểm quan sát.

Ví dụ:

```text
Funding

Fear & Greed

News

Macro
```

Các dữ liệu tức thời không bổ sung khung thời gian khi được sử dụng dưới dạng giá trị hiện hành.

---

# Trường hợp đặc biệt

## Funding

Funding có hai cách biểu diễn khác nhau tùy theo ngữ cảnh.

### Funding tức thời

Khi sử dụng giá trị hiện hành:

```text
Funding
```

Ví dụ:

```text
Funding đang dương.
```

---

### Funding theo khung thời gian

Khi phân tích chuỗi lịch sử Funding:

```text
Funding 8H

Funding D

Funding W
```

Ví dụ:

```text
Funding W đang giảm.
```

Funding là dữ liệu duy nhất trong Trading Domain có thể xuất hiện dưới cả hai dạng biểu diễn.

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

Volume Profile luôn gắn với khung thời gian tương ứng.

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

POC5 và VP1 luôn được hiểu trong ngữ cảnh của Auction Flow.

---

## Dữ liệu dòng tiền

Ví dụ:

```text
OI 5m

Relative OI 5m

Funding

Funding 8H

CVD 5m

Delta 5m

Agg Liq 5m
```

Trong đó:

- OI luôn đi kèm khung thời gian tương ứng.
- Relative OI luôn đi kèm khung thời gian tương ứng.
- CVD luôn đi kèm khung thời gian tương ứng.
- Delta luôn đi kèm khung thời gian tương ứng.
- Agg Liq luôn đi kèm khung thời gian tương ứng.
- Funding được biểu diễn theo ngữ cảnh tương ứng.

Định nghĩa và ý nghĩa của từng dữ liệu được trình bày trong các tài liệu **Khái niệm** tương ứng.

---

## Dữ liệu thị trường

Ví dụ:

```text
Long/Short Ratio 1H

Fear & Greed

News

Macro
```

Trong đó:

- Long/Short Ratio luôn đi kèm khung thời gian tương ứng.
- Fear & Greed, News và Macro được biểu diễn dưới dạng dữ liệu tức thời.

---

# Ví dụ

## EMA

Biểu diễn chuẩn:

```text
EMA200 4H đang là kháng cự.
```

---

## RSI

Biểu diễn chuẩn:

```text
RSI 15m đang tiến vào vùng quá mua.
```

---

## EMA hỗ trợ

Biểu diễn chuẩn:

```text
Giá giữ trên EMA34 15m.
```

---

## OI

Biểu diễn chuẩn:

```text
OI 5m đang tăng.
```

---

## Relative OI

Biểu diễn chuẩn:

```text
Relative OI 5m đang tăng.
```

---

## CVD

Biểu diễn chuẩn:

```text
CVD 5m đang tăng.
```

---

## Delta

Biểu diễn chuẩn:

```text
Delta 5m đang dương.
```

---

## Agg Liq

Biểu diễn chuẩn:

```text
Agg Liq 5m nghiêng về Long.
```

---

## Long / Short Ratio

Biểu diễn chuẩn:

```text
Long/Short Ratio 1H nghiêng về phe Long.
```

---

## Funding

Biểu diễn chuẩn:

```text
Funding đang dương.
```

hoặc

```text
Funding W đang giảm.
```

Tùy theo ngữ cảnh sử dụng.

---

## Fear & Greed

Biểu diễn chuẩn:

```text
Fear & Greed = 23.
```

---

## Volume Profile

Biểu diễn chuẩn:

```text
POC30 đang được giữ.

VAH30 là vùng kháng cự.

VAL30 là vùng hỗ trợ.
```

---

## Auction Flow

Biểu diễn chuẩn:

```text
Giá reclaim POC5.

Giá phản ứng tại VP1.

Auction Line quay lại EMA20.
```

POC5 và VP1 luôn được hiểu theo ngữ cảnh của Auction Flow.

---

# Nguyên tắc

Dữ liệu được biểu diễn theo một trong hai quy ước:

- Dữ liệu theo khung thời gian.
- Dữ liệu tức thời.

Khung thời gian luôn là một phần của dữ liệu khi dữ liệu phụ thuộc thời gian.

Mọi tài liệu trong Trading Domain sử dụng thống nhất các quy ước này.

Mọi dữ liệu được chuẩn hóa trước khi tham gia Hệ thống suy luận.

Định nghĩa và ý nghĩa của dữ liệu được trình bày trong các tài liệu **Khái niệm** tương ứng.

---

# Vai trò

Quy ước này giúp:

- Chuẩn hóa dữ liệu.
- Chuẩn hóa tài liệu.
- Chuẩn hóa Nguồn dữ liệu.
- Chuẩn hóa Hệ thống suy luận.
- Chuẩn hóa Tri thức nền.
- Chuẩn hóa Tri thức tích luỹ.
- Duy trì tính nhất quán trong toàn bộ Trading Domain.

Đây là quy ước chung về cách biểu diễn dữ liệu của Trading Domain.

---

# Tóm tắt

Dữ liệu luôn được biểu diễn theo đúng ngữ cảnh.

- Dữ liệu theo khung thời gian luôn đi cùng khung thời gian tương ứng.
- Dữ liệu tức thời được biểu diễn trực tiếp theo trạng thái hiện hành.

Mọi thành phần trong Trading Domain sử dụng thống nhất quy ước này trước khi dữ liệu tham gia Hệ thống suy luận.

```text
Thực tế

↓

Chuẩn hóa dữ liệu

↓

Biểu diễn theo quy ước

↓

Hệ thống suy luận

↓

Tri thức tích luỹ
```

Tài liệu này chuẩn hóa cách biểu diễn dữ liệu.

Các tài liệu trong nhóm **Khái niệm** cung cấp định nghĩa, cơ chế hoạt động và ý nghĩa của từng dữ liệu.