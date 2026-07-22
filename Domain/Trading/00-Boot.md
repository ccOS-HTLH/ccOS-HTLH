---
title: Boot
id: trading-boot
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-07-22
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - boot
  - loader
---

# Boot

> Điểm khởi động của Trading Domain.

---

# Mục đích

Boot định nghĩa thứ tự nạp toàn bộ Trading Domain.

AI phải luôn bắt đầu từ tài liệu này trước khi sử dụng Domain.

Boot không chứa Tri thức.

Boot chỉ định cách nạp Tri thức.

---

# Thứ tự nạp

AI phải đọc theo đúng thứ tự sau:

```text
01

System Instruction

↓

02

Domain Manifest

↓

03

AI Guide

↓

04

Trading Knowledge Pack

↓

05

Trading README

↓

06

Nguồn dữ liệu README

↓

07

Hệ thống suy luận README

↓

08

Tri thức nền README

↓

09

Tri thức tích lũy README

↓

10

Các Module
```

Không được thay đổi thứ tự.

Không được bỏ qua bất kỳ tầng nào.

---

# Quy tắc

## 01

Luôn bắt đầu từ Boot.

---

## 02

Luôn nạp Domain theo đúng thứ tự.

---

## 03

Không đọc ngẫu nhiên các Module.

---

## 04

Không sử dụng Tri thức tích lũy trước khi Hệ thống suy luận hoàn thành quá trình suy luận hiện tại.

---

## 05

Tri thức tích lũy chỉ được sử dụng để:

- Tham khảo.
- Đánh giá.
- Hiệu chỉnh.

Không được sử dụng để tạo suy luận mới.

---

## 06

Nếu dữ liệu chưa đủ.

Dừng.

Không suy diễn.

---

## 07

Mọi Logic phải tuân thủ Trading Domain.

Không được tự ý thay đổi kiến trúc.

---

# Luồng khởi động

```text
Boot

↓

System Instruction

↓

Domain Manifest

↓

AI Guide

↓

Trading Knowledge Pack

↓

Trading README

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức nền

↓

Tri thức tích lũy

↓

Ready
```

---

# Trạng thái

Sau khi hoàn thành toàn bộ thứ tự nạp:

```text
Trading Domain

Status

READY
```

AI có thể bắt đầu sử dụng Trading Domain.

---

# Triết lý

Boot chỉ định cách khởi động.

Kiến trúc quyết định cách vận hành.

Tri thức quyết định chất lượng suy luận.