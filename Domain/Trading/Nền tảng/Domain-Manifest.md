---
title: Trading Domain Manifest
id: trading-domain-manifest
version: 1.4.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-07-22
review_cycle: Manual
confidence: 100%
---

# Trading Domain Manifest

> Định nghĩa kiến trúc và mối quan hệ giữa các thành phần của Trading Domain.

---

# Domain

Trading

Version

```text
1.4.0
```

Status

```text
Stable
```

---

# Kiến trúc

```text
Trading

├── README.md
├── Boot.md
├── System-Instruction.md
├── Domain-Manifest.md
├── AI-Guide.md
├── Trading-Knowledge-Pack.md
├── VERSION.md
├── CHANGELOG.md
├── ROADMAP.md
├── GLOSSARY.md
├── ACKNOWLEDGEMENTS.md
├── READY.md
│
├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích lũy
```

---

# Luồng Domain

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

Trong đó:

- Tri thức nền chuẩn hóa toàn bộ Trading Domain.
- Nguồn dữ liệu chuẩn hóa dữ liệu từ Thực tế.
- Hệ thống suy luận chuyển dữ liệu thành Quyết định.
- Quyết định được Thực tế kiểm chứng.
- Tri thức tích lũy lưu giữ kinh nghiệm đã được kiểm chứng và được tham khảo trong các chu kỳ suy luận tiếp theo.

---

# Module

## Nguồn dữ liệu

- ATS
- Dữ liệu rời rạc

---

## Hệ thống suy luận

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

## Tri thức nền

- Thuật ngữ
- Khái niệm
- Quy ước
- Kiến thức nền tảng

---

## Tri thức tích lũy

01 · Định nghĩa

02 · Quan sát

03 · Thống kê

04 · Tham khảo

05 · Ví dụ

---

# Trách nhiệm tài liệu

| Tài liệu | Vai trò |
|----------|----------|
| Boot | Thứ tự nạp Domain |
| System Instruction | Quy tắc vận hành |
| Domain Manifest | Kiến trúc Domain |
| AI Guide | Hướng dẫn AI sử dụng Domain |
| Trading Knowledge Pack | Chỉ mục tri thức |
| README | Tổng quan Domain |
| README của Module | Mô tả từng Module |
| Module | Tri thức chi tiết |
| READY | Xác nhận Domain sẵn sàng |

---

# Scope

Trading Domain Manifest chỉ mô tả:

- Kiến trúc Trading Domain
- Thành phần của Domain
- Quan hệ giữa các thành phần
- Luồng dữ liệu

Trading Domain Manifest không chứa:

- Quy tắc vận hành
- Logic suy luận
- Tri thức chuyên môn

---

# Triết lý

Boot định nghĩa cách khởi động.

Manifest định nghĩa kiến trúc.

System Instruction định nghĩa quy tắc vận hành.

AI Guide định nghĩa cách AI sử dụng Domain.

Knowledge Pack định vị tri thức.

README mô tả Domain.

Module chứa tri thức.

Tất cả cùng tạo nên Trading Domain.