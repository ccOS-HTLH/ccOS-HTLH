---
title: Trading
id: trading-domain
version: 1.6.0
status: Stable
author: HTLH
language: vi
created: 2026-07-19
last_updated: 2026-08-01
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - reasoning
  - knowledge
---

[ccOS](../../README.md) → [Domain](../README.md) → **Trading**

# Trading

> Trading là Domain của ccOS chuyên chuẩn hóa toàn bộ quá trình tiếp nhận Thực tế, suy luận, thực thi, kiểm chứng và tích luỹ tri thức trong giao dịch.

---

# Mục đích

Trading chuẩn hóa toàn bộ quá trình vận hành của Trading Domain.

Trading cung cấp một kiến trúc thống nhất để:

- Tiếp nhận Thực tế.
- Chuẩn hóa dữ liệu.
- Thực hiện suy luận.
- Lập kế hoạch thực thi.
- Kiểm chứng bằng Thực tế.
- Tích luỹ và tái sử dụng kinh nghiệm.

Mọi thành phần trong Trading đều được tổ chức theo cùng một kiến trúc và cùng một ngôn ngữ.

```text
Thực tế

↓

Nguồn dữ liệu
(chuẩn hóa theo Tri thức nền)

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

---

# Kiến trúc

```text
Trading

├── README.md
│
├── Nền tảng
├── Tri thức nền
├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức tích luỹ
└── Build
```

---

# Thành phần

## Nền tảng

Định nghĩa, chuẩn hóa và quản lý toàn bộ Trading Domain.

Bao gồm:

- Boot
- System Instruction
- Domain Manifest
- AI Guide
- Trading Navigation Pack
- VERSION
- CHANGELOG
- ROADMAP
- GLOSSARY
- ACKNOWLEDGEMENTS
- READY

---

## Tri thức nền

Chuẩn hóa toàn bộ tri thức nền của Trading Domain.

Bao gồm:

- Thuật ngữ.
- Khái niệm.
- Quy ước.
- Chỉ báo.
- Mô hình.
- Kiến thức nền tảng.
- Quy trình chuẩn.
- Quy ước dữ liệu.

Đây là nguồn tri thức tĩnh của Trading Domain.

---

## Nguồn dữ liệu

Tiếp nhận Thực tế và chuẩn hóa dữ liệu theo Tri thức nền.

Bao gồm:

- ATS.
- Dữ liệu rời rạc.
- Các nguồn dữ liệu khác.

---

## Hệ thống suy luận

Chuyển dữ liệu thành phương án hành động.

Bao gồm 10 tầng:

```text
01-Hành vi

↓

02-Bối cảnh

↓

03-Động lượng

↓

04-Cấu trúc

↓

05-Chất lượng

↓

06-Quyết định

↓

07-Trọng số tín hiệu

↓

08-Không gian kịch bản

↓

09-Kế hoạch thực thi

↓

10-Phản hồi thực tế
```

---

## Tri thức tích luỹ

Học hỏi từ Thực tế và tái sử dụng kinh nghiệm.

Tri thức tích luỹ:

- Tra cứu Trường hợp.
- Nhận diện Mẫu.
- Rút ra Bài học tích luỹ.
- Cập nhật Thống kê.
- Cung cấp dữ liệu tham khảo cho các Hệ thống suy luận tiếp theo.

Đây là nguồn tri thức động của Trading Domain.

---

## Build

Đóng gói Trading Domain thành các tài liệu sử dụng.

Bao gồm:

- Trading Core
- Trading Knowledge
- Trading Data
- Trading Reasoning
- Trading Memory
- Trading Domain Full

Đồng thời cung cấp các gói Build theo từng mô-đun của Trading Domain.

---

# Điều hướng

Trading Domain được nạp theo thứ tự:

```text
Boot

↓

System Instruction

↓

Domain Manifest

↓

AI Guide

↓

Trading Navigation Pack

↓

Trading README

↓

README của các thành phần

↓

Các thành phần

↓

READY
```

Chỉ sau khi:

```text
Trading Domain READY
```

AI mới được phép sử dụng Trading Domain.

---

# Tài liệu nền tảng

| Tài liệu | Vai trò |
|----------|----------|
| Boot | Khởi tạo Trading Domain |
| System Instruction | Chuẩn hóa quy tắc vận hành |
| Domain Manifest | Chuẩn hóa kiến trúc Domain |
| AI Guide | Hướng dẫn AI sử dụng Domain |
| Trading Navigation Pack | Bản đồ điều hướng |
| README | Tổng quan Trading Domain |
| VERSION | Phiên bản hiện tại |
| CHANGELOG | Lịch sử thay đổi |
| ROADMAP | Định hướng phát triển |
| GLOSSARY | Thuật ngữ |
| ACKNOWLEDGEMENTS | Ghi nhận nguồn tham khảo và đóng góp |
| READY | Xác nhận Trading Domain đã được nạp hoàn chỉnh |

---

# Vai trò của Build

Build chịu trách nhiệm đóng gói Trading Domain thành các tài liệu sử dụng.

Mọi gói Build đều được tạo từ tài liệu nguồn.

Build không phải là nơi chỉnh sửa nội dung.

Mọi thay đổi đều phải được thực hiện trên tài liệu nguồn trước khi Build.

---

# Triết lý

Trading Domain phát triển thông qua các chu kỳ học hỏi liên tục.

Tri thức nền chuẩn hóa cách hiểu của Trading Domain.

Nguồn dữ liệu chuẩn hóa Thực tế theo Tri thức nền.

Hệ thống suy luận sử dụng dữ liệu đã chuẩn hóa để tạo phương án hành động.

Thực tế kiểm chứng mọi kết quả.

Tri thức tích luỹ học hỏi từ Thực tế và tái sử dụng kinh nghiệm trong các Hệ thống suy luận tiếp theo.

---

# Tóm tắt

```text
Trading

├── Nền tảng
│      Định nghĩa Domain
│
├── Tri thức nền
│      Chuẩn hóa ngôn ngữ,
│      khái niệm và quy ước
│
├── Nguồn dữ liệu
│      Tiếp nhận Thực tế,
│      chuẩn hóa dữ liệu
│
├── Hệ thống suy luận
│      Chuyển dữ liệu
│      thành phương án hành động
│
├── Tri thức tích luỹ
│       Học hỏi từ Thực tế
│
└── Build
        Đóng gói Domain

```

Trading là Domain của ccOS dành cho giao dịch.

Trading chuẩn hóa:

- Tiếp nhận Thực tế.
- Chuẩn hóa dữ liệu.
- Chuẩn hóa tri thức.
- Chuẩn hóa suy luận.
- Xây dựng phương án hành động.
- Kiểm chứng bằng Thực tế.
- Học hỏi từ Thực tế.
- Tái sử dụng kinh nghiệm qua từng chu kỳ.
- Đóng gói Domain thành các tài liệu sử dụng.