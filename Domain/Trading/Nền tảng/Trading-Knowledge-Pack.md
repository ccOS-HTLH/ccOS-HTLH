---
title: Trading Knowledge Pack
id: trading-knowledge-pack
version: 1.4.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-07-27
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

Tài liệu này giúp AI:

- Định vị cấu trúc Domain.
- Xác định vai trò của từng thành phần.
- Hiểu mối quan hệ giữa các Module.
- Điều hướng đến đúng tài liệu chuyên môn.

Knowledge Pack đóng vai trò chỉ mục, giúp toàn bộ Trading Domain được sử dụng nhất quán.

---

# Kiến trúc

```text
Trading

├── 01 · Nền tảng
│
├── 02 · Build
│
├── 03 · Nguồn dữ liệu
│
├── 04 · Hệ thống suy luận
│
├── 05 · Tri thức nền
│
└── 06 · Tri thức tích luỹ
```

---

# Thành phần

## 01 · Nền tảng

Vai trò:

Chuẩn hóa và quản lý Trading Domain.

Bao gồm:

- Boot
- System Instruction
- Domain Manifest
- AI Guide
- Trading Knowledge Pack
- VERSION
- CHANGELOG
- ROADMAP
- GLOSSARY
- ACKNOWLEDGEMENTS
- READY

---

## 02 · Build

Vai trò:

Đóng gói kiến trúc Trading Domain thành các tài liệu tổng hợp phục vụ triển khai, tham chiếu và bảo trì.

Bao gồm:

- Trading Core
- Trading Data
- Trading Reasoning
- Trading Knowledge
- Trading Memory
- Trading Domain Full
- Reasoning (01 → 10)

---

## 03 · Nguồn dữ liệu

Vai trò:

Chuẩn hóa dữ liệu đầu vào từ Thực tế.

Bao gồm:

- ATS
- Dữ liệu rời rạc

---

## 04 · Hệ thống suy luận

Vai trò:

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

## 05 · Tri thức nền

Vai trò:

Chuẩn hóa ngôn ngữ, quy ước và kiến trúc của Trading Domain.

Bao gồm:

- Quy ước Chữ ký tín hiệu
- Quy ước Trường hợp
- Quy ước Mẫu
- Quy ước Bài học tích luỹ
- Quy ước Thống kê
- Quy ước chỉ báo đa khung thời gian
- Luồng suy luận

---

## 06 · Tri thức tích luỹ

Vai trò:

Quản lý kinh nghiệm đã được Thực tế kiểm chứng và hỗ trợ các chu kỳ suy luận tiếp theo.

```text
Tri thức tích luỹ

├── README
│
├── Bộ nhớ
│   ├── README
│   ├── Trường hợp
│   ├── Mẫu
│   ├── Bài học tích luỹ
│   └── Thống kê
│
└── Cơ chế
    ├── README
    ├── Tra cứu
    ├── Đối chiếu
    ├── Tổng hợp
    └── Cập nhật
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

Tri thức tích luỹ

↓

Chu kỳ suy luận tiếp theo
```

---

# Điều hướng

Trading Knowledge Pack giúp AI định vị nhanh toàn bộ Trading Domain.

```text
01 · Nền tảng

↓

02 · Build

↓

03 · Nguồn dữ liệu

↓

04 · Hệ thống suy luận

↓

05 · Tri thức nền

↓

06 · Tri thức tích luỹ
```

Chi tiết của từng nhóm được định nghĩa trong README và các Module tương ứng.

---

# Vai trò

Trading Knowledge Pack giúp:

- Định vị tri thức.
- Điều hướng Module.
- Kết nối các thành phần của Trading Domain.
- Duy trì kiến trúc thống nhất trong toàn bộ Domain.

---

# Tóm tắt

```text
Trading Knowledge Pack

↓

Điều hướng

↓

Trading Domain
```

Trading Knowledge Pack là bản đồ tri thức của Trading Domain, giúp AI xác định đúng vị trí, vai trò và mối quan hệ của từng thành phần trước khi làm việc với các Module chuyên môn.