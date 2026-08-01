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