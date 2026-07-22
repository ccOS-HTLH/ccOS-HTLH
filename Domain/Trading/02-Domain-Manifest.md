---
title: Trading Domain Manifest
id: trading-domain-manifest
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-07-22
review_cycle: Manual
confidence: 100%
---

# Trading Domain Manifest

> Định nghĩa cấu trúc và thứ tự nạp của Trading Domain.

---

# Domain

Trading

Version:

1.0

Status:

Stable

---

# Kiến trúc

```text
Trading

├── README.md

├── Nguồn dữ liệu
│
├── Hệ thống suy luận
│
├── Tri thức nền
│
└── Tri thức tích luỹ
```

---

# Thứ tự nạp

```text
01

Trading README

↓

02

Nguồn dữ liệu README

↓

03

Hệ thống suy luận README

↓

04

Tri thức nền README

↓

05

Tri thức tích luỹ README
```

Sau khi hoàn thành mới được đọc các module chi tiết.

---

# Luồng dữ liệu

```text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ
```

---

# Luồng tham khảo

```text
Tri thức nền

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận
```

---

# Module

## Nguồn dữ liệu

- ATS
- Dữ liệu rời rạc

---

## Hệ thống suy luận

01 Hành vi

02 Bối cảnh

03 Động lượng

04 Cấu trúc

05 Chất lượng

06 Quyết định

07 Trọng số tín hiệu

08 Không gian kịch bản

09 Kế hoạch thực thi

10 Phản hồi thực tế

---

## Tri thức tích luỹ

01 Định nghĩa

02 Quan sát

03 Thống kê

04 Tham khảo

05 Ví dụ

---

# Quy tắc

Không được:

- Bỏ qua module.
- Đảo thứ tự.
- Tạo suy luận ngoài kiến trúc.

Phải:

- Tuân thủ Manifest.
- Tuân thủ README của từng module.
- Tuân thủ Tri thức nền.

---

# Triết lý

Manifest định nghĩa kiến trúc.

README định nghĩa hành vi.

Module định nghĩa chi tiết.

Toàn bộ Trading Domain phải được vận hành theo đúng Manifest.