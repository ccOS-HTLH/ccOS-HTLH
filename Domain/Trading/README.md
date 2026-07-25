---
title: Trading
id: trading-domain
version: 1.5.0
status: Stable
author: HTLH
language: vi
created: 2026-07-19
last_updated: 2026-07-25
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - reasoning
  - knowledge
---

# Trading

> Trading là Domain chuẩn hóa toàn bộ quá trình tiếp nhận Thực tế, suy luận, học hỏi và quản lý tri thức trong giao dịch.

---

# Mục đích

Trading chuẩn hóa toàn bộ chu trình từ Thực tế đến Quyết định.

Trading cung cấp một kiến trúc thống nhất để:

- Tiếp nhận dữ liệu.
- Chuẩn hóa tri thức.
- Thực hiện suy luận.
- Kiểm chứng bằng Thực tế.
- Tích luỹ và tái sử dụng kinh nghiệm.

Mọi thành phần trong Trading đều được tổ chức theo cùng một kiến trúc và cùng một ngôn ngữ.

---

# Kiến trúc

```text
Trading

├── README.md
├── LICENSE.md
│
├── Nền tảng
├── Build
├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích luỹ
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
- Trading Knowledge Pack
- VERSION
- CHANGELOG
- ROADMAP
- GLOSSARY
- ACKNOWLEDGEMENTS
- READY

---

## Build

Đóng gói Trading Domain thành các tài liệu sử dụng.

Bao gồm:

- Trading Core
- Trading Data
- Trading Reasoning
- Trading Memory
- Trading Domain Full

Đồng thời cung cấp các gói Build theo từng mô-đun của Hệ thống suy luận.

---

## Nguồn dữ liệu

Tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

Bao gồm:

- ATS.
- Dữ liệu rời rạc.
- Các nguồn dữ liệu khác.

---

## Hệ thống suy luận

Chuyển dữ liệu thành Quyết định.

Bao gồm 10 tầng:

```text
01 · Hành vi

↓

02 · Bối cảnh

↓

03 · Động lượng

↓

04 · Cấu trúc

↓

05 · Chất lượng

↓

06 · Quyết định

↓

07 · Trọng số tín hiệu

↓

08 · Không gian kịch bản

↓

09 · Kế hoạch thực thi

↓

10 · Phản hồi thực tế
```

---

## Tri thức nền

Chuẩn hóa:

- Thuật ngữ.
- Khái niệm.
- Quy ước.
- Kiến thức nền tảng.

Đây là nguồn tri thức tĩnh của Trading Domain.

---

## Tri thức tích luỹ

Học hỏi từ Thực tế và tái sử dụng kinh nghiệm.

Tri thức tích luỹ:

- Tra cứu kinh nghiệm.
- Đối chiếu dữ liệu.
- Tổng hợp tham khảo.
- Cập nhật Bộ nhớ.

Đây là nguồn tri thức động của Trading Domain.

---

# Chu trình hoạt động

```text
                  Tri thức nền
                        │
                        ▼

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

                        │
                        ▼

                Chu kỳ suy luận tiếp theo
```

Trong đó:

- Tri thức nền chuẩn hóa toàn bộ Trading Domain.
- Thực tế tạo ra dữ liệu.
- Nguồn dữ liệu chuẩn hóa dữ liệu đầu vào.
- Hệ thống suy luận chuyển dữ liệu thành Quyết định.
- Quyết định được Thực tế kiểm chứng.
- Tri thức tích luỹ học hỏi từ Thực tế và tái sử dụng kinh nghiệm trong các chu kỳ tiếp theo.

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

Trading Knowledge Pack

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
| System Instruction | Định nghĩa nguyên tắc làm việc của AI |
| Domain Manifest | Định nghĩa kiến trúc Domain |
| AI Guide | Hướng dẫn AI sử dụng Domain |
| Trading Knowledge Pack | Chỉ mục tri thức của Domain |
| README | Tổng quan Trading Domain |
| LICENSE | Giấy phép sử dụng |
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

```text
Tri thức nền

↓

Thực tế

↓

Dữ liệu

↓

Suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức tích luỹ

↓

Chu kỳ suy luận tiếp theo
```

Trading Domain phát triển thông qua các chu kỳ học hỏi liên tục.

Mọi tri thức đều được chuẩn hóa.

Mọi quyết định đều được kiểm chứng bằng Thực tế.

Mọi kinh nghiệm đều bắt nguồn từ Thực tế.

---

# Tóm tắt

```text
Trading

├── Nền tảng
│      Định nghĩa Domain
│
├── Build
│      Đóng gói Domain
│
├── Nguồn dữ liệu
│      Tiếp nhận dữ liệu
│
├── Hệ thống suy luận
│      Chuyển dữ liệu thành Quyết định
│
├── Tri thức nền
│      Chuẩn hóa tri thức
│
└── Tri thức tích luỹ
       Học hỏi từ Thực tế
```

Trading là Domain của ccOS dành cho giao dịch.

Trading chuẩn hóa:

- Tiếp nhận Thực tế.
- Chuẩn hóa dữ liệu.
- Chuẩn hóa tri thức.
- Chuẩn hóa suy luận.
- Chuyển dữ liệu thành Quyết định.
- Kiểm chứng Quyết định bằng Thực tế.
- Học hỏi từ Thực tế.
- Tái sử dụng kinh nghiệm qua từng chu kỳ.
- Đóng gói Domain thành các tài liệu sử dụng.