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