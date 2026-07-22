---
title: GLOSSARY
id: trading-glossary
version: 1.4.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-07-22
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

GLOSSARY định nghĩa toàn bộ thuật ngữ được sử dụng trong Trading Domain.

Mỗi thuật ngữ chỉ có **một ý nghĩa duy nhất**.

Thuật ngữ mới phải được bổ sung vào GLOSSARY trước khi được sử dụng trong Domain.

---

# Thuật ngữ

## Trading Domain

Toàn bộ kiến trúc Trading Domain của ccOS.

Bao gồm:

- Nguồn dữ liệu
- Hệ thống suy luận
- Tri thức nền
- Tri thức tích lũy

---

## Domain

Một tập hợp kiến trúc, quy tắc và tri thức cho một lĩnh vực.

Trading là một Domain của ccOS.

---

## ATS

ATS là mẫu chuẩn ghi nhận Thực tế.

Chỉ chứa Quan sát.

Không chứa suy luận.

---

## Thực tế

Những gì thực sự xảy ra trên thị trường.

---

## Dữ liệu

Thông tin được ghi nhận từ Thực tế.

---

## Quan sát

Quá trình ghi nhận dữ liệu.

Không bao gồm suy luận.

---

## Nguồn dữ liệu

Thành phần tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

---

## Hệ thống suy luận

Quá trình chuyển dữ liệu thành Quyết định.

Bao gồm 10 tầng:

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

Chi tiết từng tầng được định nghĩa trong các Module tương ứng.

---

## Quyết định

Kết luận của Hệ thống suy luận.

---

## Chu kỳ suy luận

Chu kỳ suy luận là một vòng xử lý hoàn chỉnh của Trading Domain.

Chu kỳ này bắt đầu từ Thực tế và kết thúc khi Tri thức mới được hình thành sau khi Quyết định được Thực tế kiểm chứng.

```text
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

Tri thức
```

Trong Trading Domain:

- Dữ liệu được tiếp nhận và chuẩn hóa bởi **Nguồn dữ liệu**.
- Suy luận được thực hiện bởi **Hệ thống suy luận**.
- Tri thức mới được lưu vào Tri thức tích lũy sau khi Quyết định được Thực tế kiểm chứng.

---

## Chu kỳ học hỏi

Quá trình cập nhật Tri thức tích lũy sau khi Chu kỳ suy luận hoàn thành và Quyết định đã được Thực tế kiểm chứng.

---

## Tri thức

Kiến thức đã được kiểm chứng bởi Thực tế.

Bao gồm:

- Tri thức nền
- Tri thức tích lũy

---

## Tri thức nền

Chuẩn hóa:

- Thuật ngữ
- Khái niệm
- Quy ước
- Kiến thức nền tảng

Được tham khảo trong toàn bộ Domain.

---

## Tri thức tích lũy

Kinh nghiệm đã được kiểm chứng.

Được hình thành từ tầng **Phản hồi thực tế** của Hệ thống suy luận.

Chỉ dùng để:

- Tham khảo
- Đánh giá
- Hiệu chỉnh

Không tạo suy luận mới.

---

## Chữ ký tín hiệu

Dấu hiệu đặc trưng dùng để tra cứu Tri thức tích lũy.

---

## Module

Thành phần chuyên biệt của Trading Domain.

Mỗi Module định nghĩa tri thức và quy tắc chuyên môn trong phạm vi của chính nó.

Các Module cùng tạo nên Trading Domain.

---

## Boot

Điểm khởi động của Trading Domain.

Định nghĩa thứ tự nạp Domain.

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

## Status

Lệnh kiểm tra trạng thái hiện tại của Trading Domain.

Có thể trả về:

```text
Trading Domain READY
```

hoặc

```text
Trading Domain NOT READY
```

Status chỉ kiểm tra trạng thái.

Không nạp lại Domain.

---

## READY

Trạng thái xác nhận Trading Domain đã được nạp hoàn chỉnh.

---

## Knowledge Pack

Chỉ mục tri thức của Trading Domain.

Không chứa Logic suy luận.

---

## Manifest

Tài liệu mô tả kiến trúc và quan hệ giữa các thành phần của Domain.

---

## System Instruction

Tài liệu có độ ưu tiên cao nhất của Trading Domain.

Định nghĩa quy tắc vận hành.

---

## Core Documents

Tập hợp các tài liệu nền tảng của Trading Domain.

Bao gồm:

- Boot
- System Instruction
- Domain Manifest
- AI Guide
- Trading Knowledge Pack
- Trading README
- VERSION
- CHANGELOG
- ROADMAP
- GLOSSARY
- ACKNOWLEDGEMENTS
- READY

---

# Quy tắc

- Một thuật ngữ chỉ có một định nghĩa.
- Không tự tạo thuật ngữ mới.
- Thuật ngữ mới phải được bổ sung vào GLOSSARY.
- Mọi tài liệu trong Trading Domain phải sử dụng thống nhất các thuật ngữ tại đây.

---

# Triết lý

```text
Một ngôn ngữ

↓

Một kiến trúc

↓

Một hệ thống
```