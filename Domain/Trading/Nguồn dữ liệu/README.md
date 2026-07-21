---
title: Nguồn dữ liệu
id: trading-data-source
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-20
last_updated: 2026-07-21
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - data
---

# Nguồn dữ liệu

> Nguồn dữ liệu là thành phần tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

---

# Mục đích

Nguồn dữ liệu trả lời:

> Thực tế được ghi nhận như thế nào?

Nguồn dữ liệu chuẩn hóa dữ liệu từ Thực tế để cung cấp đầu vào cho Hệ thống suy luận.

---

# Triết lý

Dữ liệu luôn đi trước suy luận.

Không có dữ liệu.

Không có suy luận.

---

# Kiến trúc

```text
Nguồn dữ liệu

├── README.md
├── 01-ATS
└── 02-Dữ liệu rời rạc
```

---

# Mối quan hệ với Trading

```text
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

---

# Đầu vào

- Thực tế.
- Tri thức nền.

---

# Đầu ra

Dữ liệu chuẩn hóa.

---

# Thành phần

## 01 · ATS

ATS là một mẫu ghi nhận Thực tế theo cấu trúc thống nhất.

ATS giúp quan sát đồng thời nhiều khía cạnh của thị trường.

---

## 02 · Dữ liệu rời rạc

Dữ liệu rời rạc ghi nhận một hoặc nhiều khía cạnh của Thực tế.

Ví dụ:

- Funding Rate
- Open Interest
- CVD
- VPIN
- Fear & Greed
- Long / Short Ratio
- News
- Macro
- ...

Dữ liệu rời rạc có thể được sử dụng độc lập hoặc kết hợp với ATS.

---

# Nguyên tắc

Mọi dữ liệu đều phản ánh Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa theo Tri thức nền trước khi được sử dụng.

ATS và Dữ liệu rời rạc đều là các nguồn dữ liệu của Hệ thống suy luận.

---

# Vai trò trong Trading

```text
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

---

# Tóm tắt

```text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận
```

Nguồn dữ liệu định nghĩa:

- Cách tiếp nhận Thực tế.
- Cách chuẩn hóa dữ liệu.
- Cấu trúc dữ liệu đầu vào của Hệ thống suy luận.