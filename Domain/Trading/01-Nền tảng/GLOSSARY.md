---
title: GLOSSARY
id: trading-glossary
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
  - glossary
---

# GLOSSARY

> Chuẩn hóa thuật ngữ của Trading Domain.

---

# Mục đích

GLOSSARY là từ điển thuật ngữ thống nhất của Trading Domain.

Mỗi thuật ngữ có một định nghĩa duy nhất và được sử dụng nhất quán trong toàn Domain.

---

# Thuật ngữ

## Trading Domain

Hệ thống tri thức và quy trình dành cho lĩnh vực Trading.

Bao gồm:

- Nền tảng
- Build
- Nguồn dữ liệu
- Hệ thống suy luận
- Tri thức nền
- Tri thức tích luỹ

---

## Domain

Một hệ thống gồm kiến trúc, quy tắc và tri thức cho một lĩnh vực.

---

## Nền tảng

Nhóm tài liệu quản lý và định nghĩa Trading Domain.

---

## Build

Nhóm tài liệu xây dựng và mô tả kiến trúc vận hành của Trading Domain.

---

## Nguồn dữ liệu

Thành phần tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

---

## ATS

Mẫu chuẩn ghi nhận dữ liệu quan sát.

---

## Dữ liệu rời rạc

Các dữ liệu bổ sung ngoài ATS được chuẩn hóa để phục vụ suy luận.

---

## Thực tế

Những gì xảy ra trên thị trường.

---

## Dữ liệu

Thông tin được ghi nhận từ Thực tế.

---

## Quan sát

Quá trình ghi nhận dữ liệu.

---

## Hệ thống suy luận

Chuỗi xử lý chuyển dữ liệu thành Quyết định.

Gồm 10 tầng từ Hành vi đến Phản hồi thực tế.

---

## Quyết định

Kết quả của Hệ thống suy luận.

---

## Chu kỳ suy luận

Một vòng xử lý hoàn chỉnh:

```text
Thực tế
    │
    ▼
Nguồn dữ liệu
    │
    ▼
Hệ thống suy luận
    │
    ▼
Quyết định
    │
    ▼
Thực tế
    │
    ▼
Tri thức tích luỹ
```

---

## Tri thức nền

Tập hợp thuật ngữ, khái niệm và quy ước chuẩn hóa Trading Domain.

---

## Tri thức tích luỹ

Kinh nghiệm được hình thành sau khi Quyết định được Thực tế kiểm chứng.

Bao gồm:

- Bộ nhớ
- Cơ chế

---

## Bộ nhớ

Kho lưu giữ:

- Trường hợp
- Mẫu
- Bài học tích luỹ
- Thống kê

---

## Cơ chế

Các quy trình làm việc với Bộ nhớ:

- Tra cứu
- Đối chiếu
- Tổng hợp
- Cập nhật

---

## Chữ ký tín hiệu

Định danh chuẩn của một trạng thái suy luận.

---

## Trường hợp

Một lần vận hành hoàn chỉnh đã được Thực tế kiểm chứng.

---

## Mẫu

Tập hợp nhiều Trường hợp có đặc điểm tương đồng.

---

## Bài học tích luỹ

Kinh nghiệm được tổng hợp từ nhiều Mẫu và Trường hợp.

---

## Thống kê

Kết quả định lượng được tổng hợp từ nhiều Trường hợp.

---

## Module

Đơn vị tài liệu chuyên biệt của Trading Domain.

---

## Boot

Điểm khởi động Trading Domain.

---

## READY

Trạng thái xác nhận Trading Domain đã sẵn sàng sử dụng.

---

## Boot Commands

Các lệnh điều khiển Domain:

- boot
- ready
- status
- reload
- update
- unload

---

## Trading Knowledge Pack

Chỉ mục tri thức của Trading Domain.

---

## Domain Manifest

Tài liệu mô tả kiến trúc Trading Domain.

---

## AI Guide

Hướng dẫn AI sử dụng Trading Domain.

---

## System Instruction

Tài liệu quy định cách AI vận hành Trading Domain.

---

## Core Documents

Các tài liệu nền tảng của Trading Domain:

- Boot
- System Instruction
- Domain Manifest
- AI Guide
- Trading Knowledge Pack
- README
- VERSION
- CHANGELOG
- ROADMAP
- GLOSSARY
- ACKNOWLEDGEMENTS
- READY

---

# Quy tắc

- Một thuật ngữ chỉ có một định nghĩa.
- Thuật ngữ mới được bổ sung vào GLOSSARY trước khi sử dụng.
- Toàn bộ Trading Domain sử dụng thống nhất các thuật ngữ tại đây.

---

# Tóm tắt

```text
GLOSSARY

↓

Thuật ngữ

↓

Khái niệm

↓

Ngôn ngữ thống nhất

↓

Trading Domain
```

GLOSSARY là nền tảng ngôn ngữ chung của toàn bộ Trading Domain.