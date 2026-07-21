---
title: Dữ liệu rời rạc
id: trading-discrete-data
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-20
last_updated: 2026-07-21
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - data
---

# Dữ liệu rời rạc

> Dữ liệu rời rạc ghi nhận một hoặc nhiều khía cạnh của Thực tế.

---

# Mục đích

Dữ liệu rời rạc ghi nhận những dữ liệu không nhất thiết phải nằm trong ATS.

Dữ liệu rời rạc chuẩn hóa các dữ liệu đầu vào cho Hệ thống suy luận.

Dữ liệu rời rạc không tham gia vào quá trình suy luận.

---

# Đặc điểm

Dữ liệu rời rạc có thể là:

- Một chỉ số.
- Một biểu đồ.
- Một sự kiện.
- Một tập dữ liệu.

Dữ liệu rời rạc có thể được sử dụng độc lập hoặc kết hợp với ATS.

---

# Ví dụ

## Chỉ số

- Funding Rate
- Open Interest
- CVD
- VPIN
- Fear & Greed
- Long / Short Ratio

---

## Dữ liệu

- News
- Macro
- On-chain
- Lịch kinh tế
- Dữ liệu khác

---

# Nguyên tắc

Mỗi dữ liệu phản ánh một phần của Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa trước khi được sử dụng.

ATS và Dữ liệu rời rạc đều là các nguồn dữ liệu của Hệ thống suy luận.

---

# Triết lý

Dữ liệu rời rạc không tạo ra suy luận.

Dữ liệu rời rạc chỉ cung cấp dữ liệu cho Hệ thống suy luận.

---

# Tóm tắt

```text
Thực tế

↓

Dữ liệu rời rạc

↓

Hệ thống suy luận
```

Dữ liệu rời rạc là một nguồn dữ liệu của Hệ thống suy luận.