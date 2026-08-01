---
title: Nguồn dữ liệu
id: trading-data-source
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-20
last_updated: 2026-07-27
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

Nguồn dữ liệu ghi nhận và chuẩn hóa dữ liệu từ Thực tế để cung cấp đầu vào cho Hệ thống suy luận.

---

# Triết lý

Dữ liệu luôn đi trước suy luận.

Dữ liệu được chuẩn hóa trước khi tham gia Hệ thống suy luận.

---

# Kiến trúc

```text
Nguồn dữ liệu

├── README.md
├── ATS.md
└── Dữ liệu rời rạc.md
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

Trong đó:

- Thực tế là nguồn gốc của mọi dữ liệu.
- Nguồn dữ liệu tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.
- Tri thức nền cung cấp các khái niệm và quy ước để chuẩn hóa dữ liệu.
- Dữ liệu chuẩn hóa trở thành đầu vào của Hệ thống suy luận.

---

# Đầu vào

- Thực tế.

---

# Đầu ra

- Dữ liệu chuẩn hóa.

---

# Tham khảo

- Tri thức nền.

Nguồn dữ liệu sử dụng Tri thức nền để chuẩn hóa dữ liệu trước khi chuyển sang Hệ thống suy luận.

---

# Thành phần

## 01 · ATS

ATS là mẫu chuẩn để ghi nhận và chuẩn hóa dữ liệu từ Thực tế theo một cấu trúc thống nhất.

ATS giúp quan sát đồng thời nhiều khía cạnh của thị trường.

---

## 02 · Dữ liệu rời rạc

Dữ liệu rời rạc ghi nhận các dữ liệu từ Thực tế theo từng đơn vị quan sát độc lập.

Ví dụ:

- Funding Rate.
- Open Interest.
- CVD.
- VPIN.
- Fear & Greed.
- Long / Short Ratio.
- News.
- Macro.
- ...

Các dữ liệu này có thể:

* được ghi nhận trực tiếp;
* được tổ chức trong ATS;
* hoặc được kết hợp với ATS tùy theo ngữ cảnh quan sát.

---

# Nguyên tắc

Mọi dữ liệu đều phản ánh Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa theo các quy ước trong Tri thức nền trước khi được sử dụng.

ATS và Dữ liệu rời rạc đều là các nguồn dữ liệu của Hệ thống suy luận.

---

# Vai trò trong Trading

```text
Trading Domain

├── Tri thức nền
│      Chuẩn hóa ngôn ngữ và quy ước
│
├── Nguồn dữ liệu
│      Ghi nhận và chuẩn hóa dữ liệu
│
├── Hệ thống suy luận
│      Phân tích và xây dựng phương án
│
└── Tri thức tích luỹ
       Chuẩn hóa và lưu giữ kinh nghiệm
```

Nguồn dữ liệu là đầu vào của Hệ thống suy luận.

---

# Tóm tắt

```text
Thực tế

↓

Nguồn dữ liệu

↓

Dữ liệu chuẩn hóa

↓

Hệ thống suy luận
```

Nguồn dữ liệu chuẩn hóa:

- Cách tiếp nhận Thực tế.
- Cách ghi nhận dữ liệu.
- Cách chuẩn hóa dữ liệu.
- Cấu trúc dữ liệu đầu vào của Hệ thống suy luận.