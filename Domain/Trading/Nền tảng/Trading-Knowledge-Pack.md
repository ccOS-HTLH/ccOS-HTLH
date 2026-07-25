---
title: Trading Knowledge Pack
id: trading-knowledge-pack
version: 1.3.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-07-22
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - knowledge-pack
---

# Trading Knowledge Pack

> Chỉ mục tri thức của Trading Domain.

---

# Mục đích

Trading Knowledge Pack là bản đồ tri thức của Trading Domain.

Giúp AI xác định:

- Cấu trúc Domain.
- Thành phần của Domain.
- Vai trò của từng thành phần.
- Quan hệ giữa các thành phần.
- Vị trí của các Module.

Knowledge Pack không thay thế các tài liệu chi tiết.

Knowledge Pack chỉ đóng vai trò **chỉ mục tri thức**.

---

# Tổng quan

```text
Trading

├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích lũy
```

---

# Thành phần

## 01 · Nguồn dữ liệu

**Vai trò**

Tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

Bao gồm:

- ATS
- Dữ liệu rời rạc

---

## 02 · Hệ thống suy luận

**Vai trò**

Chuyển dữ liệu thành Quyết định.

Bao gồm:

```text
01 · Hành vi

02 · Bối cảnh

03 · Động lượng

04 · Cấu trúc

05 · Chất lượng

06 · Quyết định

07 · Trọng số tín hiệu

08 · Không gian kịch bản

09 · Kế hoạch thực thi

10 · Phản hồi thực tế
```

---

## 03 · Tri thức nền

**Vai trò**

Chuẩn hóa toàn bộ Domain.

Bao gồm:

- Thuật ngữ
- Khái niệm
- Quy ước
- Kiến thức nền tảng

---

## 04 · Tri thức tích lũy

**Vai trò**

Lưu giữ kinh nghiệm đã được Thực tế kiểm chứng.

Bao gồm:

```text
01 · Định nghĩa

02 · Quan sát

03 · Thống kê

04 · Tham khảo

05 · Ví dụ
```

---

# Luồng tri thức

```text
                 Tri thức nền
                      │
                      ▼

Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức tích lũy

↓

Chu kỳ suy luận tiếp theo
```

---

# Điều hướng

Knowledge Pack giúp AI định vị nhanh các nhóm tri thức:

```text
Trading Domain

├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích lũy
```

Chi tiết được định nghĩa trong:

- Trading README
- README của từng Module
- Các Module tương ứng

---

# Scope

Trading Knowledge Pack mô tả:

- Thành phần của Trading Domain.
- Vai trò của từng thành phần.
- Quan hệ giữa các thành phần.
- Chỉ mục các Module.

Knowledge Pack không chứa:

- Quy tắc vận hành.
- Logic suy luận.
- Tri thức chuyên môn.
- Nội dung chi tiết của các Module.

---

# Quy tắc

Knowledge Pack không thay thế:

- Boot
- System Instruction
- Domain Manifest
- AI Guide
- Trading README
- README của các Module
- Các Module

Knowledge Pack chỉ đóng vai trò **chỉ mục tri thức** của Trading Domain.

---

# Triết lý

Trading Knowledge Pack giúp AI định vị tri thức.

Tri thức chi tiết luôn được định nghĩa trong các Module tương ứng.