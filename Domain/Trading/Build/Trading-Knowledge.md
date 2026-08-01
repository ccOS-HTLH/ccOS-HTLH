---
title: Tri thức nền
id: trading-knowledge
version: 2.0.0
status: Stable
author: HTLH
language: vi
created: 2026-07-27
last_updated: 2026-07-31
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - knowledge
---

# Tri thức nền

> Tri thức nền là thành phần chuẩn hóa toàn bộ cách hiểu, cách biểu diễn và cách vận hành của Trading Domain.

---

# Mục đích

Tri thức nền trả lời:

> Trading Domain hiểu, biểu diễn và vận hành dữ liệu theo cách nào?

Tri thức nền chuẩn hóa:

- Khái niệm.
- Quy ước.
- Luồng.

Nhờ đó mọi thành phần trong Trading Domain sử dụng cùng một cách hiểu, cùng một cách biểu diễn và cùng một cách vận hành.

---

# Triết lý

Một hệ thống thống nhất bắt đầu từ một nền tri thức thống nhất.

Tri thức nền chuẩn hóa:

- Cách hiểu.
- Cách biểu diễn.
- Cách vận hành.

trước khi dữ liệu tham gia Hệ thống suy luận.

---

# Kiến trúc

```text
Tri thức nền

├── README.md

├── Khái niệm
│   ├── README.md
│   └── ...

├── Quy ước
│   ├── README.md
│   ├── Biểu diễn dữ liệu.md
│   ├── Chữ ký tín hiệu
│   ├── Trường hợp.md
│   ├── Mẫu.md
│   ├── Bài học tích luỹ.md
│   └── Thống kê.md

└── Luồng
    ├── README.md
    └── Luồng suy luận.md
```

---

# Thành phần

## Khái niệm

Chuẩn hóa ý nghĩa và cơ chế hoạt động của các dữ liệu và đối tượng trong Trading Domain.

Trả lời:

- Là gì?
- Hoạt động như thế nào?
- Có ý nghĩa gì?

---

## Quy ước

Chuẩn hóa cách biểu diễn dữ liệu và tri thức.

Trả lời:

- Biểu diễn như thế nào?
- Viết như thế nào?
- Chuẩn hóa ra sao?

---

## Luồng

Chuẩn hóa trình tự vận hành của Trading Domain.

Trả lời:

- Vận hành như thế nào?
- Thành phần nào trước?
- Thành phần nào sau?

---

# Mối quan hệ với Trading

```text
Tri thức nền

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ
```

Trong đó:

- Nguồn dữ liệu tham khảo Tri thức nền để chuẩn hóa dữ liệu.
- Hệ thống suy luận tham khảo Tri thức nền để thống nhất cách hiểu, biểu diễn và vận hành.
- Tri thức tích luỹ tham khảo Tri thức nền để chuẩn hóa kinh nghiệm và Bộ nhớ.

---

# Nguyên tắc

Mọi thành phần trong Trading Domain tham khảo cùng một Tri thức nền.

Mọi dữ liệu đều được:

- Hiểu theo Khái niệm.
- Biểu diễn theo Quy ước.
- Vận hành theo Luồng.

trước khi tham gia Hệ thống suy luận.

---

# Vai trò trong Trading

```text
               Tri thức nền
        ┌──────────┼──────────┐
        ▼          ▼          ▼

   Khái niệm   Quy ước    Luồng
        │          │          │
        └──────────┼──────────┘
                   ▼

            Trading Domain
```

Tri thức nền là nền tảng thống nhất của toàn bộ Trading Domain.

---

# Tóm tắt

```text
Tri thức nền

↓

Khái niệm

↓

Quy ước

↓

Luồng

↓

Trading Domain
```

Tri thức nền chuẩn hóa:

- Cách hiểu.
- Cách biểu diễn.
- Cách vận hành.

để toàn bộ Trading Domain sử dụng chung một nền tri thức thống nhất.

---

---
title: Khái niệm
id: trading-concepts
version: 1.0.0
status: Stable
author: HTLH
language: vi
created: 2026-07-31
last_updated: 2026-07-31
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - concepts
---

# Khái niệm

> Chuẩn hóa các khái niệm được sử dụng trong Trading Domain.

---

# Mục đích

Khái niệm định nghĩa ý nghĩa, cơ chế hoạt động và vai trò của các đối tượng được sử dụng trong Trading Domain.

Khác với:

- Quy ước → chuẩn hóa cách biểu diễn dữ liệu.
- Luồng → chuẩn hóa trình tự vận hành.

Khái niệm trả lời:

> Dữ liệu này là gì?

> Hoạt động như thế nào?

> Có ý nghĩa gì trong Trading Domain?

---

# Triết lý

Mọi dữ liệu đều cần được hiểu trước khi được sử dụng.

Khái niệm giúp Trading Domain thống nhất cách hiểu về mọi đối tượng trước khi dữ liệu tham gia Hệ thống suy luận.

---

# Kiến trúc

```text
Khái niệm

├── README.md

├── EMA.md
├── RSI.md
├── Volume.md
├── Volume Profile.md
├── Auction Flow.md
├── Funding.md
├── OI.md
├── Relative OI.md
├── CVD.md
├── Delta.md
├── Agg Liq.md
├── Long-Short Ratio.md
├── Fear & Greed.md
├── News.md
└── Macro.md
```

> Danh sách tài liệu có thể được mở rộng khi Trading Domain phát triển.

---

# Thành phần

Mỗi tài liệu Khái niệm mô tả một đối tượng cụ thể.

Bao gồm:

- Định nghĩa.
- Cơ chế hoạt động.
- Ý nghĩa.
- Mối quan hệ với các dữ liệu khác.
- Vai trò trong Trading Domain.

---

# Mối quan hệ với Trading

```text
Tri thức nền

├── Khái niệm
├── Quy ước
└── Luồng

        │

        ▼

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ
```

Trong đó:

- Khái niệm định nghĩa dữ liệu và tri thức.
- Quy ước chuẩn hóa cách biểu diễn.
- Luồng chuẩn hóa trình tự vận hành.

Ba nhóm này tạo thành nền tảng tri thức của Trading Domain.

---

# Nguyên tắc

Mỗi tài liệu chỉ mô tả một khái niệm.

Khái niệm không quy định cách biểu diễn dữ liệu.

Khái niệm không mô tả trình tự vận hành.

Khái niệm là nền tảng để hiểu dữ liệu trước khi dữ liệu được chuẩn hóa và sử dụng.

---

# Vai trò

Khái niệm giúp:

- Chuẩn hóa cách hiểu về dữ liệu.
- Chuẩn hóa thuật ngữ.
- Giảm sai lệch trong quá trình suy luận.
- Làm nền tảng cho Quy ước và Luồng.

---

# Tóm tắt

```text
Khái niệm

↓

Chuẩn hóa

↓

Cách hiểu dữ liệu

↓

Trading Domain
```

Khái niệm định nghĩa ý nghĩa và cơ chế hoạt động của các đối tượng trong Trading Domain.

Mọi dữ liệu đều được hiểu thống nhất trước khi được biểu diễn, suy luận và tích luỹ.

---

---
title: Quy ước
id: trading-conventions
version: 1.0.0
status: Stable
author: HTLH
language: vi
created: 2026-07-31
last_updated: 2026-07-31
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - convention
---

# Quy ước

> Chuẩn hóa cách biểu diễn, tổ chức và sử dụng dữ liệu trong Trading Domain.

---

# Mục đích

Quy ước định nghĩa các nguyên tắc chung được sử dụng thống nhất trong toàn bộ Trading Domain.

Việc chuẩn hóa giúp:

- Thống nhất ngôn ngữ.
- Thống nhất cấu trúc dữ liệu.
- Thống nhất cách biểu diễn.
- Giảm sai lệch trong quá trình suy luận.
- Hỗ trợ Tri thức tích luỹ và Build.

---

# Triết lý

Mọi dữ liệu cần được biểu diễn theo cùng một quy ước trước khi tham gia Hệ thống suy luận.

Một quy ước thống nhất tạo nên một hệ thống thống nhất.

---

# Kiến trúc

```text
Quy ước

├── README.md
│
├── Biểu diễn dữ liệu.md
│
├── Chữ ký tín hiệu
│   ├── README.md
│   ├── 01 · Định nghĩa.md
│   ├── 02 · Cấu trúc.md
│   ├── 03 · Tạo chữ ký.md
│   ├── 04 · Sử dụng.md
│   └── 05 · Ví dụ.md
│
├── Trường hợp.md
├── Mẫu.md
├── Bài học tích luỹ.md
└── Thống kê.md
```

---

# Thành phần

## Biểu diễn dữ liệu

Chuẩn hóa cách biểu diễn dữ liệu trong Trading Domain.

Bao gồm:

- Dữ liệu theo khung thời gian.
- Dữ liệu tức thời.
- Quy tắc biểu diễn dữ liệu.

---

## Chữ ký tín hiệu

Chuẩn hóa cấu trúc Chữ ký tín hiệu.

Bao gồm:

- Định nghĩa.
- Cấu trúc.
- Quy trình tạo.
- Cách sử dụng.
- Ví dụ.

---

## Trường hợp

Chuẩn hóa cấu trúc của một Trường hợp.

---

## Mẫu

Chuẩn hóa cấu trúc của một Mẫu.

---

## Bài học tích luỹ

Chuẩn hóa cấu trúc của một Bài học tích luỹ.

---

## Thống kê

Chuẩn hóa cấu trúc của dữ liệu Thống kê.

---

# Mối quan hệ với Trading

```text
Quy ước

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Build
```

Trong đó:

- Nguồn dữ liệu sử dụng Quy ước để chuẩn hóa dữ liệu đầu vào.
- Hệ thống suy luận sử dụng Quy ước để diễn giải dữ liệu một cách thống nhất.
- Tri thức tích luỹ sử dụng Quy ước để lưu trữ kinh nghiệm.
- Build sử dụng Quy ước để duy trì tính nhất quán của tài liệu.

---

# Nguyên tắc

Mỗi quy ước chỉ chuẩn hóa một chủ đề.

Các quy ước không định nghĩa kiến thức chuyên môn.

Định nghĩa và ý nghĩa của dữ liệu được trình bày trong nhóm **Khái niệm**.

Mọi thành phần của Trading Domain đều tham khảo cùng một bộ Quy ước.

---

# Vai trò

Quy ước giúp:

- Chuẩn hóa dữ liệu.
- Chuẩn hóa cấu trúc.
- Chuẩn hóa cách biểu diễn.
- Chuẩn hóa ngôn ngữ.
- Duy trì tính nhất quán trong toàn bộ Trading Domain.

Đây là nền tảng chuẩn hóa của Trading Domain.

---

# Tóm tắt

```text
Quy ước

↓

Chuẩn hóa

↓

Trading Domain
```

Quy ước định nghĩa các nguyên tắc chung về:

- Biểu diễn dữ liệu.
- Chữ ký tín hiệu.
- Trường hợp.
- Mẫu.
- Bài học tích luỹ.
- Thống kê.

Mọi thành phần của Trading Domain đều sử dụng thống nhất các quy ước này trước khi tham gia Hệ thống suy luận hoặc được lưu trữ trong Tri thức tích luỹ.

---

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

---

# Quy ước Chữ ký tín hiệu

> Quy ước chuẩn hóa cách tạo và sử dụng Chữ ký tín hiệu trong Trading Domain.

---

# Mục đích

Quy ước Chữ ký tín hiệu định nghĩa cách Hệ thống suy luận tạo và sử dụng Chữ ký tín hiệu.

Chữ ký tín hiệu là biểu diễn chuẩn của toàn bộ trạng thái suy luận tại thời điểm Hệ thống suy luận hoàn thành tầng 07-Trọng số tín hiệu. Từ thời điểm đó, Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế để tham khảo và cập nhật Tri thức tích luỹ.

Mọi Chữ ký tín hiệu đều được tạo theo cùng một quy ước.

---

# Triết lý

Mỗi quá trình suy luận đều để lại một dấu vết.

Chữ ký tín hiệu là dấu vết chuẩn của quá trình suy luận.

Một quy ước thống nhất giúp Hệ thống suy luận và Tri thức tích luỹ sử dụng cùng một ngôn ngữ.

---

# Mối quan hệ với Trading

```text
07-Trọng số tín hiệu
        │
        ├── tạo
        ▼
  Chữ ký tín hiệu

08-Không gian kịch bản
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

09-Kế hoạch thực thi
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

10-Phản hồi thực tế
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Cập nhật Tri thức tích luỹ
```

Trong đó:

- Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.
- Từ tầng 08 đến tầng 10, Chữ ký tín hiệu được sử dụng thống nhất để tham khảo và cập nhật Tri thức tích luỹ.

---

# Vai trò

Quy ước này giúp:

- Chuẩn hóa trạng thái suy luận.
- Chuẩn hóa quá trình tra cứu.
- Nhận diện Trường hợp.
- Nhận diện Mẫu.
- Tham khảo Bài học tích luỹ.
- Tham khảo Thống kê.
- Đảm bảo tính nhất quán trong toàn bộ Trading Domain.

---

# Phạm vi

Quy ước này được sử dụng thống nhất trong:

- Hệ thống suy luận.
- Tri thức tích luỹ.

---

# Cấu trúc

```text
README

↓

01-Định nghĩa

↓

02-Cấu trúc

↓

03-Tạo Chữ ký

↓

04-Sử dụng

↓

05-Ví dụ
```

---

# Nguyên tắc

Mỗi quá trình suy luận tạo ra một Chữ ký tín hiệu.

Một Chữ ký tín hiệu phản ánh trạng thái của Hệ thống suy luận tại thời điểm hoàn thành tầng 07-Trọng số tín hiệu.

Mỗi Chữ ký tín hiệu được tạo theo cùng một quy ước và được sử dụng thống nhất trong các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế.

Cùng một trạng thái suy luận tạo ra cùng một Chữ ký tín hiệu.

---

# Tóm tắt

Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.

Từ thời điểm đó, Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế để tham khảo và cập nhật Tri thức tích luỹ.

---

# 01-Định nghĩa

> Bản chất của Chữ ký tín hiệu.

---

# Bản chất

Chữ ký tín hiệu là biểu diễn chuẩn của một trạng thái suy luận.

Chữ ký tín hiệu chuẩn hóa toàn bộ trạng thái suy luận của Hệ thống suy luận thành một biểu diễn thống nhất.

Mỗi Chữ ký tín hiệu đại diện cho toàn bộ trạng thái suy luận tại thời điểm Hệ thống suy luận hoàn thành tầng 07-Trọng số tín hiệu.

---

# Vai trò

Chữ ký tín hiệu giúp:

- Chuẩn hóa trạng thái suy luận.
- Nhận diện các trạng thái suy luận tương đồng.
- Tra cứu Bộ nhớ thông qua Tri thức tích luỹ.
- Liên kết giữa Hệ thống suy luận và Tri thức tích luỹ.
- Đảm bảo tính nhất quán trong toàn bộ Trading Domain.

---

# Mối quan hệ với Trading

```text
07-Trọng số tín hiệu
        │
        ├── tạo
        ▼
  Chữ ký tín hiệu

08-Không gian kịch bản
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

09-Kế hoạch thực thi
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

10-Phản hồi thực tế
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Cập nhật Tri thức tích luỹ
```

Trong đó:

- Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.
- Từ tầng 08 đến tầng 10, Chữ ký tín hiệu được sử dụng thống nhất để tham khảo và cập nhật Tri thức tích luỹ.

---

# Đặc điểm

Chữ ký tín hiệu là biểu diễn chuẩn của trạng thái suy luận.

Một Chữ ký tín hiệu có thể được liên kết với nhiều Trường hợp có cùng trạng thái suy luận.

Thông qua các Trường hợp, Tri thức tích luỹ hình thành Mẫu, Bài học tích luỹ và Thống kê.

Tri thức được Tri thức tích luỹ quản lý trong Bộ nhớ.

---

# Mối quan hệ

Một Chữ ký tín hiệu có thể:

- Chưa được liên kết với Trường hợp nào.
- Liên kết với một Trường hợp.
- Liên kết với nhiều Trường hợp.

Một Trường hợp luôn liên kết với đúng một Chữ ký tín hiệu.

Một Chữ ký tín hiệu có thể được nhiều Trường hợp cùng sử dụng nếu chúng có cùng trạng thái suy luận.

---

# Mục tiêu

Chữ ký tín hiệu được tạo ra để:

- Chuẩn hóa trạng thái suy luận.
- Nhận diện các trạng thái suy luận tương đồng.
- Hỗ trợ Tri thức tích luỹ tra cứu Bộ nhớ.
- Chuẩn hóa điểm tham chiếu giữa Hệ thống suy luận và Tri thức tích luỹ.
- Hỗ trợ tái sử dụng kinh nghiệm trong các Hệ thống suy luận tiếp theo.

---

# Nguyên tắc

Một trạng thái suy luận tạo ra một Chữ ký tín hiệu.

Một Chữ ký tín hiệu có thể được nhiều Trường hợp cùng sử dụng khi chúng có cùng trạng thái suy luận.

Một Trường hợp luôn liên kết với đúng một Chữ ký tín hiệu.

Mỗi Chữ ký tín hiệu được cố định sau khi được tạo.

Tri thức tích luỹ sử dụng Chữ ký tín hiệu để nhận diện, tra cứu và cập nhật dữ liệu trong Bộ nhớ.

Chữ ký tín hiệu là cầu nối thống nhất giữa Hệ thống suy luận và Tri thức tích luỹ.

---

# Tóm tắt

Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.

Từ thời điểm đó, Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế để tham khảo và cập nhật Tri thức tích luỹ.

---

# 02 · Cấu trúc

> Thành phần cấu thành Chữ ký tín hiệu.

---

# Mục đích

Định nghĩa các thành phần tạo nên một Chữ ký tín hiệu.

Mọi Chữ ký tín hiệu đều được hình thành từ cùng một cấu trúc.

Cấu trúc thống nhất giúp Tri thức tích luỹ nhận diện, tra cứu và đối chiếu các trạng thái suy luận tương đồng.

---

# Triết lý

Chữ ký tín hiệu được hình thành từ toàn bộ trạng thái của quá trình suy luận.

Mỗi thành phần đóng góp một phần vào cấu trúc thống nhất của Chữ ký tín hiệu.

---

# Thành phần

Một Chữ ký tín hiệu được hình thành từ:

- Trạng thái hành vi.
- Trạng thái bối cảnh.
- Trạng thái động lượng.
- Trạng thái cấu trúc.
- Trạng thái chất lượng.
- Trạng thái quyết định.
- Trọng số tín hiệu.

Mỗi thành phần phản ánh một khía cạnh khác nhau của quá trình suy luận.

Toàn bộ các thành phần cùng tạo nên trạng thái suy luận được chuẩn hóa thành một Chữ ký tín hiệu.

---

# Mối quan hệ với Trading

```text
07-Trọng số tín hiệu
        │
        ├── tạo
        ▼
  Chữ ký tín hiệu

08-Không gian kịch bản
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

09-Kế hoạch thực thi
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

10-Phản hồi thực tế
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Cập nhật Tri thức tích luỹ
```

Trong đó:

- Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.
- Từ tầng 08 đến tầng 10, Chữ ký tín hiệu được sử dụng thống nhất để tham khảo và cập nhật Tri thức tích luỹ.

---

# Mô hình

```text
01-Hành vi
      │
02-Bối cảnh
      │
03-Động lượng
      │
04-Cấu trúc
      │
05-Chất lượng
      │
06-Quyết định
      │
07-Trọng số tín hiệu
      │
      ├── tạo
      ▼
Chữ ký tín hiệu

08-Không gian kịch bản
      │
      └── sử dụng Chữ ký tín hiệu
            │
            └── Tham khảo Tri thức tích luỹ

09-Kế hoạch thực thi
      │
      └── sử dụng Chữ ký tín hiệu
            │
            └── Tham khảo Tri thức tích luỹ

10-Phản hồi thực tế
      │
      └── sử dụng Chữ ký tín hiệu
            │
            └── Cập nhật Tri thức tích luỹ
```

---

# Đặc điểm

Mỗi thành phần phản ánh một khía cạnh của trạng thái suy luận.

Sự kết hợp của các thành phần tạo nên một Chữ ký tín hiệu thống nhất.

Chữ ký tín hiệu phản ánh toàn bộ trạng thái suy luận tại thời điểm được tạo.

---

# Nguyên tắc

Mọi Chữ ký tín hiệu đều sử dụng cùng một cấu trúc.

Cấu trúc của Chữ ký tín hiệu được sử dụng thống nhất trong toàn bộ Trading Domain.

Thay đổi ở bất kỳ thành phần nào của trạng thái suy luận đều có thể hình thành một Chữ ký tín hiệu mới.

Mỗi Chữ ký tín hiệu phản ánh trạng thái suy luận tại thời điểm được tạo.

Chữ ký tín hiệu chuẩn hóa trạng thái suy luận của Hệ thống suy luận.

Chữ ký tín hiệu được sử dụng xuyên suốt các tầng Không gian kịch bản, Kế hoạch thực thi và Phản hồi thực tế để liên kết với Tri thức tích luỹ.

---

# Tóm tắt

Chữ ký tín hiệu được hình thành từ toàn bộ trạng thái suy luận sau tầng 07-Trọng số tín hiệu.

Cấu trúc thống nhất giúp Tri thức tích luỹ nhận diện, tra cứu và đối chiếu các trạng thái suy luận tương đồng.

Từ thời điểm được tạo, Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế để tham khảo và cập nhật Tri thức tích luỹ.

---

# 03 · Tạo Chữ ký

> Quy tắc tạo Chữ ký tín hiệu.

---

# Mục đích

Quy định thời điểm và nguyên tắc tạo Chữ ký tín hiệu.

Việc tạo Chữ ký tín hiệu đánh dấu sự hoàn thành tầng 07-Trọng số tín hiệu của Hệ thống suy luận.

---

# Triết lý

Chữ ký tín hiệu được tạo từ quá trình suy luận.

Kinh nghiệm được hình thành từ Thực tế.

Tri thức tích luỹ là cầu nối giữa suy luận và kinh nghiệm.

---

# Khi nào tạo?

Chữ ký tín hiệu được tạo sau khi:

- Trạng thái quyết định đã được xác định.
- Trọng số tín hiệu đã được lượng hóa.

Đây là đầu ra cuối cùng của tầng 07-Trọng số tín hiệu.

---

# Vai trò

Việc tạo Chữ ký tín hiệu giúp:

- Chuẩn hóa trạng thái suy luận.
- Liên kết Hệ thống suy luận với Tri thức tích luỹ.
- Làm đầu vào cho quá trình tham khảo Tri thức tích luỹ.

---

# Mối quan hệ với Trading

```text
07-Trọng số tín hiệu
        │
        ├── tạo
        ▼
  Chữ ký tín hiệu

08-Không gian kịch bản
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

09-Kế hoạch thực thi
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

10-Phản hồi thực tế
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Cập nhật Tri thức tích luỹ
```

Trong đó:

- Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.
- Từ tầng 08 đến tầng 10, Chữ ký tín hiệu được sử dụng thống nhất để tham khảo và cập nhật Tri thức tích luỹ.

---

# Nguyên tắc

Mỗi quá trình suy luận tạo ra một Chữ ký tín hiệu.

Cùng một trạng thái suy luận tạo ra cùng một Chữ ký tín hiệu.

Thay đổi trạng thái suy luận có thể hình thành một Chữ ký tín hiệu mới.

Mỗi Chữ ký tín hiệu được cố định sau khi được tạo.

---

# Mối quan hệ với Tri thức tích luỹ

Sau khi được tạo, Chữ ký tín hiệu giúp Tri thức tích luỹ:

- Nhận diện và tra cứu Trường hợp.
- Nhận diện Mẫu.
- Tổng hợp Bài học tích luỹ.
- Tham khảo Thống kê.

---

# Sau khi tầng Phản hồi thực tế hoàn tất

```text
Chữ ký tín hiệu

↓

Trường hợp

↓

Mẫu

↓

Bài học tích luỹ

↓

Thống kê
```

Sau khi Thực tế kiểm chứng hoàn tất, Tri thức tích luỹ cập nhật:

- Trường hợp.
- Mẫu.
- Bài học tích luỹ.
- Thống kê.

---

# Tóm tắt

Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.

Từ thời điểm đó, Chữ ký tín hiệu được sử dụng để:

- Tham khảo Tri thức tích luỹ.
- Cập nhật Tri thức tích luỹ sau khi Thực tế kiểm chứng.

Chữ ký tín hiệu là cầu nối giữa Hệ thống suy luận và Tri thức tích luỹ.

---

# 04 · Sử dụng

> Cách Chữ ký tín hiệu được sử dụng trong Trading Domain.

---

# Mục đích

Quy định cách Chữ ký tín hiệu được sử dụng trong Trading Domain.

Chữ ký tín hiệu là cầu nối giữa Hệ thống suy luận và Tri thức tích luỹ.

---

# Triết lý

Chữ ký tín hiệu kết nối suy luận với kinh nghiệm.

Tri thức tích luỹ kết nối kinh nghiệm với quyết định.

Bộ nhớ lưu giữ những kinh nghiệm đã được Thực tế kiểm chứng.

---

# Luồng sử dụng

```text
07-Trọng số tín hiệu
        │
        ├── tạo
        ▼
  Chữ ký tín hiệu

08-Không gian kịch bản
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

09-Kế hoạch thực thi
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

10-Phản hồi thực tế
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Cập nhật Tri thức tích luỹ
```

Trong đó:

- Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.
- Từ tầng 08 đến tầng 10, Chữ ký tín hiệu được sử dụng thống nhất để tham khảo và cập nhật Tri thức tích luỹ.

---

# Vai trò

Trong Trading Domain:

- Tầng 07 tạo Chữ ký tín hiệu.
- Các tầng 08-Không gian kịch bản và 09-Kế hoạch thực thi sử dụng Chữ ký tín hiệu để tham khảo Tri thức tích luỹ.
- Tầng 10-Phản hồi thực tế sử dụng Chữ ký tín hiệu để cập nhật Tri thức tích luỹ.

---

# Nguyên tắc

Chữ ký tín hiệu là biểu diễn chuẩn của trạng thái suy luận.

Tri thức tích luỹ sử dụng Chữ ký tín hiệu để nhận diện, tra cứu và cập nhật dữ liệu trong Bộ nhớ.

Quá trình hình thành Trường hợp được thực hiện sau khi Thực tế kiểm chứng hoàn tất.

Chữ ký tín hiệu được sử dụng sau khi hoàn thành tầng 07-Trọng số tín hiệu.

---

# Tóm tắt

Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế.

Thông qua Chữ ký tín hiệu:

- Tri thức tích luỹ được tham khảo trong quá trình xây dựng Không gian kịch bản và Kế hoạch thực thi.
- Tri thức tích luỹ được cập nhật sau khi Phản hồi thực tế hoàn tất.

Chữ ký tín hiệu là cầu nối giữa Hệ thống suy luận và Tri thức tích luỹ.

---

# 05 · Ví dụ

> Minh họa cách Chữ ký tín hiệu được tạo và sử dụng trong Trading Domain.

---

# Mục đích

Minh họa cách Chữ ký tín hiệu được tạo và được sử dụng trong Trading Domain.

Các ví dụ giúp làm rõ quy trình vận hành của Chữ ký tín hiệu từ khi được tạo đến khi được Tri thức tích luỹ sử dụng.

---

# Triết lý

Ví dụ giúp chuyển quy ước thành cách sử dụng cụ thể.

Thông qua ví dụ, có thể quan sát toàn bộ quá trình phối hợp giữa Hệ thống suy luận và Tri thức tích luỹ.

---

# Mẫu chuẩn

```text
Quá trình suy luận
↓
01-Hành vi
      │
02-Bối cảnh
      │
03-Động lượng
      │
04-Cấu trúc
      │
05-Chất lượng
      │
06-Quyết định
      │
07-Trọng số tín hiệu
      │
      ├── tạo
      ▼
Chữ ký tín hiệu

08-Không gian kịch bản
      │
      └── sử dụng Chữ ký tín hiệu
            │
            └── Tham khảo Tri thức tích luỹ

09-Kế hoạch thực thi
      │
      └── sử dụng Chữ ký tín hiệu
            │
            └── Tham khảo Tri thức tích luỹ

10-Phản hồi thực tế
      │
      └── sử dụng Chữ ký tín hiệu
            │
            └── Cập nhật Tri thức tích luỹ
```

---

# Ví dụ 01

## Quá trình suy luận

- Hành vi: Tăng.
- Bối cảnh: Thuận lợi.
- Động lượng: Mạnh.
- Cấu trúc: Tiếp diễn.
- Chất lượng: Cao.
- Quyết định: Ưu tiên Long.

↓

## Chữ ký tín hiệu

```text
SIG-EX01
```

↓

## Tri thức tích luỹ

```text
TH-0012
TH-0038

↓

M-0004

↓

BH-0007

↓

TK-0002
```

↓

## Kết quả

Tri thức tích luỹ trả về các Trường hợp, Mẫu, Bài học tích luỹ và Thống kê liên quan để Hệ thống suy luận tham khảo trước khi xây dựng Không gian kịch bản và Kế hoạch thực thi.

---

# Ví dụ 02

## Quá trình suy luận

- Hành vi: Đi ngang.
- Bối cảnh: Không rõ xu hướng.
- Động lượng: Yếu.
- Cấu trúc: Tích lũy.
- Chất lượng: Trung bình.
- Quyết định: Quan sát.

↓

## Chữ ký tín hiệu

```text
SIG-EX02
```

↓

## Tri thức tích luỹ

Tri thức tích luỹ chưa tìm thấy Trường hợp có trạng thái suy luận tương đồng.

↓

## Kết quả

Hệ thống suy luận tiếp tục đánh giá dựa trên dữ liệu hiện tại.

Sau khi xuất hiện các Trường hợp đã được Thực tế kiểm chứng, Tri thức tích luỹ sẽ cập nhật Bộ nhớ và tiếp tục hỗ trợ các chu kỳ suy luận sau.

---

# Nguyên tắc

Mỗi ví dụ minh họa một quá trình suy luận hoàn chỉnh.

Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.

Từ thời điểm đó, Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế.

Tri thức tích luỹ cập nhật Bộ nhớ sau khi Thực tế kiểm chứng hoàn tất.

---

# Tóm tắt

Các ví dụ minh họa toàn bộ vòng đời của Chữ ký tín hiệu trong Trading Domain:

- Được tạo sau tầng 07-Trọng số tín hiệu.
- Được sử dụng trong các tầng 08-Không gian kịch bản và 09-Kế hoạch thực thi để tham khảo Tri thức tích luỹ.
- Được sử dụng tại tầng 10-Phản hồi thực tế để cập nhật Tri thức tích luỹ.

Nhờ đó, cùng một quy ước Chữ ký tín hiệu có thể được áp dụng thống nhất trong toàn bộ Trading Domain.

---

# Quy ước Trường hợp

> Quy định cấu trúc chuẩn khi ghi nhận một Trường hợp.

---

# Mục đích

Quy ước này chuẩn hóa cách ghi nhận Trường hợp.

Mọi Trường hợp sử dụng cùng một cấu trúc để Tri thức tích luỹ có thể nhận diện, tra cứu, đối chiếu và tổng hợp thống nhất.

---

# Triết lý

Mỗi Trường hợp lưu giữ một lần vận hành của Hệ thống suy luận đã được Thực tế kiểm chứng.

Cấu trúc thống nhất giúp kinh nghiệm được tích luỹ và tái sử dụng trong các Hệ thống suy luận tiếp theo.

---

# Cấu trúc

```text
TH-xxxx

↓

Loại

↓

Bối cảnh

↓

Quan sát

- Hành vi giá
- Thanh khoản
- Dòng tiền

↓

Suy luận

↓

Thực thi

↓

Kết quả

↓

Nhận xét

↓

Từ khóa
```

---

# Nội dung

## Loại

Phân loại bản chất của Trường hợp.

Ví dụ:

- Tiếp diễn xu hướng.
- Đảo chiều xu hướng.
- Mở rộng vùng tích luỹ.
- Phá vỡ thất bại.

---

## Bối cảnh

Mô tả trạng thái thị trường tại thời điểm Trường hợp được hình thành.

---

## Quan sát

Ghi nhận dữ liệu quan sát từ Thực tế.

Bao gồm:

- Hành vi giá.
- Thanh khoản.
- Dòng tiền.

---

## Suy luận

Tóm tắt kết quả của Hệ thống suy luận tại thời điểm xây dựng phương án.

---

## Thực thi

Mô tả quá trình thực hiện phương án.

Có thể bao gồm:

- Điều kiện thực thi.
- Entry.
- Stop Loss.
- Take Profit.
- Quản trị vị thế.

---

## Kết quả

Ghi nhận kết quả sau khi được Thực tế kiểm chứng.

Ví dụ:

- Đạt TP.
- Dừng lỗ.
- Không vào lệnh.
- Phương án mất hiệu lực.

---

## Nhận xét

Tổng hợp những kinh nghiệm rút ra từ Trường hợp.

---

## Từ khóa

Liệt kê các từ khóa phục vụ tra cứu.

Ví dụ:

- Trend Continuation.
- POC Pullback.
- EMA89 1H.
- Positive CVD.
- OI Increase.

---

# Nguyên tắc

Mỗi Trường hợp được lưu trong một tệp riêng.

Mọi Trường hợp sử dụng cùng một cấu trúc và thứ tự trình bày.

Nội dung phản ánh dữ liệu và kết quả đã được Thực tế kiểm chứng.

---

# Vai trò

Quy ước này giúp Tri thức tích luỹ:

- Tra cứu và đối chiếu Trường hợp.
- Nhận diện Mẫu.
- Tổng hợp Bài học tích luỹ.
- Cập nhật Thống kê.

---

# Tóm tắt

```text
Thực tế

↓

Trường hợp

↓

Tri thức tích luỹ
```

Trường hợp là đơn vị tri thức cơ sở của Tri thức tích luỹ.

Từ các Trường hợp đã được Thực tế kiểm chứng, Tri thức tích luỹ hình thành Mẫu, Bài học tích luỹ và Thống kê.

---

# Quy ước Mẫu

> Quy định cấu trúc chuẩn khi ghi nhận một Mẫu.

---

# Mục đích

Quy ước này chuẩn hóa cách ghi nhận Mẫu trong Trading Domain.

Mỗi Mẫu được hình thành từ nhiều Trường hợp đã được Thực tế kiểm chứng.

Cấu trúc thống nhất giúp Tri thức tích luỹ nhận diện, đối chiếu và tái sử dụng các trạng thái suy luận lặp lại.

---

# Cấu trúc

```text
M-xxxx

↓

Tên Mẫu

↓

Nguồn hình thành

- Các Trường hợp liên quan

↓

Điều kiện xuất hiện

↓

Đặc điểm chung

↓

Điều kiện vô hiệu

↓

Mức độ xuất hiện

↓

Nhận xét

↓

Từ khóa
```

---

# Nội dung

## Tên Mẫu

Tên ngắn gọn phản ánh đặc điểm chung của Mẫu.

Ví dụ:

- POC Pullback
- EMA Multi-Timeframe Pullback
- Failed Breakout
- Trend Continuation

---

## Nguồn hình thành

Liệt kê các Trường hợp tạo nên Mẫu.

Ví dụ:

- TH-0001
- TH-0004
- TH-0012

---

## Điều kiện xuất hiện

Mô tả các điều kiện thường xuất hiện trước khi Mẫu hình thành.

Ví dụ:

- Giá giữ POC.
- OI tăng.
- CVD tăng.
- Delta dương.
- Auction Flow đồng thuận.

Điều kiện xuất hiện phản ánh những yếu tố lặp lại giữa các Trường hợp.

---

## Đặc điểm chung

Tóm tắt những đặc điểm lặp lại giữa các Trường hợp thuộc Mẫu.

Ví dụ:

- Giá thường Pullback trước khi tiếp diễn.
- POC thường dịch lên.
- Delta thường đồng thuận với CVD.

---

## Điều kiện vô hiệu

Mô tả những điều kiện làm Mẫu không còn phù hợp.

Ví dụ:

- Giá mất POC.
- CVD đảo chiều mạnh.
- Auction Flow suy yếu.
- Cấu trúc thị trường thay đổi.

---

## Mức độ xuất hiện

Mức độ xuất hiện phản ánh độ trưởng thành của Mẫu.

Ví dụ:

- Mới xuất hiện.
- Xuất hiện thường xuyên.
- Xuất hiện ổn định.

---

## Nhận xét

Tổng hợp những điểm đáng chú ý sau khi đối chiếu các Trường hợp.

---

## Từ khóa

Liệt kê các từ khóa phục vụ tra cứu.

Ví dụ:

- Trend Continuation
- POC Pullback
- EMA34 1H
- EMA89 15M
- Positive CVD
- OI Increase
- Auction Flow

---

# Nguyên tắc

- Mỗi tệp lưu một Mẫu.
- Một Mẫu được hình thành từ nhiều Trường hợp.
- Mẫu phản ánh những đặc điểm lặp lại đã được Thực tế kiểm chứng.
- Có thể mở rộng khi xuất hiện thêm Trường hợp phù hợp.
- Nguồn hình thành luôn duy trì khả năng truy ngược về các Trường hợp liên quan.

---

# Vai trò

Tri thức tích luỹ sử dụng Mẫu để:

- Nhận diện sự lặp lại.
- So sánh các Mẫu.
- Hình thành Bài học tích luỹ.
- Cập nhật Thống kê.
- Hỗ trợ Không gian kịch bản và Kế hoạch thực thi.

---

# Tóm tắt

```text
Nhiều Trường hợp

↓

Mẫu

↓

Tri thức tích luỹ

↓

Bài học tích luỹ

↓

Thống kê
```

Mẫu là tầng tổng hợp đầu tiên của Tri thức tích luỹ.

Từ nhiều Trường hợp đã được Thực tế kiểm chứng, Mẫu chuẩn hóa những đặc điểm lặp lại để có thể tái sử dụng.

---

# Triết lý

Nhiều Trường hợp tạo nên một Mẫu.

Mẫu là bước đầu tiên chuyển kinh nghiệm thành tri thức.

---

# Quy ước Bài học tích luỹ

> Quy định cấu trúc chuẩn khi ghi nhận một Bài học tích luỹ.

---

# Mục đích

Quy ước này chuẩn hóa cách ghi nhận Bài học tích luỹ.

Mỗi Bài học tích luỹ được hình thành từ nhiều Mẫu và nhiều Trường hợp đã được Thực tế kiểm chứng.

Cấu trúc thống nhất giúp Tri thức tích luỹ tổng hợp và tái sử dụng kinh nghiệm.

---

# Cấu trúc

```text
BH-xxxx

↓

Tên Bài học

↓

Nguồn hình thành

- Các Mẫu liên quan
- Các Trường hợp liên quan

↓

Bài học

↓

Điều kiện áp dụng

↓

Điều kiện chuyển ngữ cảnh

↓

Mức độ tin cậy

↓

Nhận xét

↓

Từ khóa
```

---

# Nội dung

## Tên Bài học

Tên ngắn gọn phản ánh nội dung kinh nghiệm được tích luỹ.

Ví dụ:

- Pullback tại POC có xác suất tiếp diễn cao.
- EMA đa khung thời gian giúp xác nhận hỗ trợ.
- Auction Flow đồng thuận giúp giảm False Break.

---

## Nguồn hình thành

Liệt kê các Mẫu và Trường hợp tạo nên Bài học.

Ví dụ:

Mẫu:

- M-0001
- M-0004

Trường hợp:

- TH-0001
- TH-0008
- TH-0016

---

## Bài học

Tóm tắt kinh nghiệm được rút ra.

Ví dụ:

- Pullback tại POC thường hiệu quả hơn khi OI, CVD và Delta cùng đồng thuận.
- EMA đa khung thời gian giúp xác nhận vùng hỗ trợ động.
- Auction Flow đồng thuận giúp tăng xác suất tiếp diễn.

---

## Điều kiện áp dụng

Mô tả những điều kiện phù hợp để tham khảo Bài học.

Ví dụ:

- Xu hướng tăng.
- POC được giữ.
- OI tăng.
- CVD đồng thuận.
- Auction Flow đồng thuận.

---

## Điều kiện chuyển ngữ cảnh

Điều kiện cho thấy nên tham khảo Bài học khác phù hợp hơn.

Ví dụ:

- Thị trường đi ngang.
- Cấu trúc xu hướng thay đổi.
- Thanh khoản biến động mạnh.
- Tin tức làm thay đổi hành vi thị trường.

---

## Mức độ tin cậy

Mức độ tin cậy phản ánh mức độ kiểm chứng của Bài học.

Ví dụ:

- Thấp.
- Trung bình.
- Cao.

---

## Nhận xét

Tổng hợp những điểm đáng chú ý sau khi đối chiếu các Mẫu và Trường hợp.

---

## Từ khóa

Liệt kê các từ khóa phục vụ tra cứu.

Ví dụ:

- Trend Continuation.
- POC Pullback.
- EMA Multi-Timeframe.
- Auction Flow.
- Positive CVD.
- OI Increase.

---

# Nguyên tắc

- Mỗi tệp lưu một Bài học tích luỹ.
- Một Bài học được hình thành từ nhiều Mẫu và nhiều Trường hợp.
- Bài học được xây dựng trên các dữ liệu đã được Thực tế kiểm chứng.
- Bài học có thể được cập nhật khi xuất hiện thêm Mẫu hoặc Trường hợp mới.
- Mỗi lần cập nhật đều dựa trên dữ liệu bổ sung từ Thực tế.

---

# Vai trò

Tri thức tích luỹ sử dụng Bài học tích luỹ để:

- Tham khảo kinh nghiệm.
- Hỗ trợ Không gian kịch bản.
- Hỗ trợ Kế hoạch thực thi.
- Cập nhật Thống kê.

---

# Tóm tắt

```text
Nhiều Trường hợp

↓

Nhiều Mẫu

↓

Bài học tích luỹ

↓

Tri thức tích luỹ
```

Bài học tích luỹ tổng hợp kinh nghiệm đã được Thực tế kiểm chứng thành tri thức có thể tham khảo và tái sử dụng.

---

# Triết lý

Nhiều Mẫu tạo nên một Bài học tích luỹ.

Bài học tích luỹ giúp chuyển kinh nghiệm thành tri thức có thể tái sử dụng.

---

# Quy ước Thống kê

> Quy định cấu trúc chuẩn khi ghi nhận một Thống kê.

---

# Mục đích

Quy ước này chuẩn hóa cách ghi nhận Thống kê.

Thống kê được tổng hợp từ nhiều Trường hợp đã được Thực tế kiểm chứng nhằm định lượng mức độ xuất hiện và hiệu quả của các trạng thái, Mẫu hoặc Bài học.

---

# Cấu trúc

```text
TK-xxxx

↓

Tên Thống kê

↓

Nguồn dữ liệu

- Trường hợp
- Mẫu
- Bài học

↓

Phạm vi thống kê

↓

Chỉ số

↓

Kết quả

↓

Điều kiện áp dụng

↓

Nhận xét

↓

Từ khóa
```

---

# Nội dung

## Tên Thống kê

Tên ngắn gọn phản ánh nội dung được thống kê.

Ví dụ:

- Hiệu quả Pullback tại POC.
- Tỷ lệ thành công Trend Continuation.
- Hiệu quả EMA đa khung thời gian.
- Phân bố Reward / Risk.

---

## Nguồn dữ liệu

Liệt kê nguồn dữ liệu dùng để tạo Thống kê.

Có thể bao gồm:

- Trường hợp
- Mẫu
- Bài học

### Trường hợp

- TH-0001
- TH-0005
- TH-0018

### Mẫu

- M-0002
- M-0004

### Bài học

- BH-0001

---

## Phạm vi thống kê

Mô tả phạm vi của Thống kê.

Ví dụ:

- Trend Continuation.
- BTC.
- Khung thời gian 15M–4H.
- POC Pullback.

Phạm vi giúp sử dụng Thống kê đúng ngữ cảnh.

---

## Chỉ số

Liệt kê các chỉ số được thống kê.

Ví dụ:

- Số Trường hợp
- Win Rate
- Reward / Risk trung bình
- Holding Time trung bình
- Drawdown trung bình
- Expectancy

---

## Kết quả

Trình bày kết quả thống kê.

Ví dụ:

- 52 Trường hợp.
- Win Rate: 71%.
- RR trung bình: 2.6.
- Holding Time trung bình: 7 giờ.

---

## Điều kiện áp dụng

Mô tả điều kiện phù hợp để tham khảo Thống kê.

Ví dụ:

- Xu hướng tăng.
- POC được giữ.
- OI đồng thuận.
- CVD đồng thuận.
- Delta đồng thuận.

---

## Nhận xét

Tóm tắt những điểm đáng chú ý từ kết quả thống kê.

Ví dụ:

- Win Rate tăng khi Auction Flow đồng thuận.
- Reward / Risk giảm trong thị trường Sideway.
- Delta đồng thuận giúp giảm False Break.

---

## Từ khóa

Liệt kê các từ khóa phục vụ tra cứu.

Ví dụ:

- Trend Continuation.
- POC Pullback.
- EMA Multi-Timeframe.
- Positive Delta.
- Positive CVD.
- Auction Flow.
- Statistics.

---

# Nguyên tắc

- Mỗi tệp lưu một Thống kê.
- Một Thống kê được tổng hợp từ nhiều Trường hợp và có thể tham khảo thêm Mẫu hoặc Bài học.
- Mọi số liệu đều dựa trên dữ liệu đã được Thực tế kiểm chứng.
- Thống kê được cập nhật khi có thêm dữ liệu phù hợp.
- Mọi số liệu đều truy ngược được nguồn dữ liệu.

---

# Vai trò

Thống kê giúp Tri thức tích luỹ:

- Định lượng mức độ tin cậy.
- So sánh hiệu quả.
- Hỗ trợ tham khảo trong quá trình suy luận.

---

# Tóm tắt

Thống kê tổng hợp dữ liệu đã được Thực tế kiểm chứng thành các chỉ số định lượng.

Nhờ đó Tri thức tích luỹ có cơ sở đánh giá mức độ xuất hiện và hiệu quả của các trạng thái, Mẫu và Bài học.

---

# Triết lý

Thống kê lượng hóa những gì Thực tế đã ghi nhận.

Dữ liệu được tổng hợp theo cùng một quy ước giúp Tri thức tích luỹ đánh giá kinh nghiệm một cách nhất quán.

---

---
title: Luồng
id: trading-workflows
version: 1.0.0
status: Stable
author: HTLH
language: vi
created: 2026-07-31
last_updated: 2026-07-31
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - workflow
---

# Luồng

> Chuẩn hóa các luồng vận hành của Trading Domain.

---

# Mục đích

Luồng định nghĩa cách các thành phần trong Trading Domain phối hợp với nhau để hoàn thành một chu trình làm việc.

Khác với:

- Khái niệm → định nghĩa dữ liệu và tri thức.
- Quy ước → chuẩn hóa cách biểu diễn.
- Luồng → chuẩn hóa trình tự vận hành.

---

# Triết lý

Mọi thành phần đều có vai trò riêng.

Mọi luồng đều có điểm bắt đầu, trình tự xử lý và điểm kết thúc rõ ràng.

Một luồng thống nhất giúp Trading Domain vận hành nhất quán.

---

# Kiến trúc

```text
Luồng

├── README.md

└── Luồng suy luận.md
```

---

# Thành phần

## Luồng suy luận

Chuẩn hóa toàn bộ quá trình Hệ thống suy luận vận hành từ khi tiếp nhận dữ liệu đến khi hoàn thành một chu kỳ học hỏi.

Bao gồm:

- Trình tự các tầng suy luận.
- Mối quan hệ giữa các tầng.
- Chu trình từ Thực tế đến Tri thức tích luỹ.
- Nguyên tắc vận hành của Hệ thống suy luận.

---

# Mối quan hệ với Trading

```text
Tri thức nền

├── Khái niệm

├── Quy ước

└── Luồng

        │

        ▼

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ
```

Trong đó:

- Khái niệm định nghĩa dữ liệu và tri thức.
- Quy ước chuẩn hóa cách biểu diễn.
- Luồng chuẩn hóa trình tự vận hành.

Ba nhóm này tạo thành nền tảng tri thức của Trading Domain.

---

# Nguyên tắc

Mỗi tài liệu chỉ mô tả một luồng.

Luồng chỉ mô tả quá trình vận hành.

Định nghĩa dữ liệu thuộc nhóm Khái niệm.

Quy tắc biểu diễn dữ liệu thuộc nhóm Quy ước.

---

# Vai trò

Luồng giúp:

- Chuẩn hóa quy trình vận hành.
- Chuẩn hóa trình tự xử lý.
- Duy trì tính nhất quán giữa các thành phần.
- Hỗ trợ Hệ thống suy luận và Tri thức tích luỹ phối hợp với nhau.

---

# Tóm tắt

```text
Luồng

↓

Chuẩn hóa

↓

Quy trình vận hành

↓

Trading Domain
```

Luồng định nghĩa trình tự vận hành của Trading Domain.

Mỗi luồng mô tả cách các thành phần phối hợp với nhau để hoàn thành một chu trình làm việc thống nhất.

---

---
title: Luồng suy luận
id: trading-reasoning-flow
version: 1.1
status: Stable
author: HTLH
language: vi
created: 2026-07-27
last_updated: 2026-07-27
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - reasoning
  - workflow
---

# Luồng suy luận

> Luồng suy luận mô tả toàn bộ quá trình Hệ thống suy luận vận hành từ khi tiếp nhận dữ liệu đến khi tích luỹ kinh nghiệm mới.

---

# Mục đích

Luồng suy luận mô tả cách Hệ thống suy luận vận hành từ khi quan sát Thực tế đến khi hoàn thành một chu kỳ suy luận.

Mỗi tầng có một vai trò riêng.

Đầu ra của tầng trước trở thành đầu vào của tầng sau.

Sau khi chu kỳ suy luận hoàn tất, Phản hồi thực tế cung cấp dữ liệu để Tri thức tích luỹ cập nhật tri thức cho các chu kỳ tiếp theo.

---

# Triết lý

Quan sát tạo ra dữ liệu.

Suy luận tạo ra khả năng.

Thực thi tạo ra hành động.

Thực tế kiểm chứng kết quả.

Tri thức tích luỹ chuẩn hóa kinh nghiệm thành tri thức.

Bộ nhớ lưu giữ tri thức cho những lần suy luận sau.

---

# Luồng suy luận

```text
01 · Hành vi
        │
        ▼
02 · Bối cảnh
        │
        ▼
03 · Động lượng
        │
        ▼
04 · Cấu trúc
        │
        ▼
05 · Chất lượng
        │
        ▼
06 · Quyết định
        │
        ▼
07 · Trọng số tín hiệu
        │
        ▼
Chữ ký tín hiệu
        │
        ▼
08 · Không gian kịch bản
        │
        ▼
09 · Kế hoạch thực thi
        │
        ▼
10 · Phản hồi thực tế
        │
        ▼
Tri thức tích luỹ
        │
        ▼
Bộ nhớ
        │
        ├── Trường hợp
        ├── Mẫu
        ├── Bài học tích luỹ
        └── Thống kê
```

---

# Chu trình

```text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

Đây là một chu trình vận hành liên tục.

Mỗi chu kỳ đều góp phần mở rộng Tri thức tích luỹ và hỗ trợ các chu kỳ suy luận tiếp theo.

---

# Nguyên tắc

Đầu ra của mỗi tầng là đầu vào của tầng kế tiếp.

Quá trình suy luận được thực hiện đầy đủ theo toàn bộ các tầng của Hệ thống suy luận.

Quá trình suy luận được thực hiện theo chiều từ dữ liệu đầu vào đến kết quả suy luận.

Chữ ký tín hiệu được hình thành sau tầng Trọng số tín hiệu.

Không gian kịch bản được hình thành sau khi Chữ ký tín hiệu đã hoàn tất.

Tri thức tích luỹ được tham khảo trong quá trình xây dựng Không gian kịch bản và Kế hoạch thực thi.

Thực tế là tiêu chuẩn kiểm chứng duy nhất của toàn bộ Hệ thống suy luận.

---

# Vai trò

Luồng suy luận chịu trách nhiệm điều phối toàn bộ chu trình vận hành của Hệ thống suy luận.

Trong Luồng suy luận:

Hệ thống suy luận chịu trách nhiệm:

- Quan sát dữ liệu.
- Phân tích dữ liệu.
- Đánh giá chất lượng tín hiệu.
- Xây dựng Không gian kịch bản.
- Lập Kế hoạch thực thi.
- Tiếp nhận Phản hồi thực tế.

Tri thức tích luỹ chịu trách nhiệm:

- Tra cứu Trường hợp.
- Nhận diện Mẫu.
- Rút ra Bài học tích luỹ.
- Cập nhật Thống kê.
- Chuẩn hóa và lưu giữ kinh nghiệm.

---

Luồng suy luận điều phối sự phối hợp giữa Hệ thống suy luận và Tri thức tích luỹ.

Hai thành phần này tạo thành một chu trình học hỏi liên tục từ Thực tế.

---

# Mối quan hệ với Trading

```text
                       Tri thức nền
               │
               │ tham chiếu
               ▼

Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

Trong đó:

- Tri thức nền cung cấp các khái niệm và quy ước làm nền tảng cho Luồng suy luận.
- Nguồn dữ liệu chuẩn hóa dữ liệu từ Thực tế.
- Hệ thống suy luận chuyển dữ liệu thành phương án thực thi.
- Tri thức tích luỹ học hỏi từ Thực tế và tái sử dụng kinh nghiệm trong các chu kỳ tiếp theo.

---

# Tóm tắt

```text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

Luồng suy luận chuẩn hóa:

- Thứ tự xử lý dữ liệu.
- Mối quan hệ giữa các tầng.
- Quá trình hình thành quyết định.
- Quá trình học hỏi từ Thực tế.

Luồng suy luận là khung vận hành của toàn bộ Trading Domain.