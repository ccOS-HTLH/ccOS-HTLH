---
title: Boot
id: trading-boot
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
  - boot
---

# Boot

> Điểm khởi động của Trading Domain.

---

# Mục đích

Boot định nghĩa thứ tự nạp toàn bộ Trading Domain.

AI phải luôn bắt đầu từ tài liệu này để nạp Trading Domain.

Boot không chứa:

- Tri thức
- Logic suy luận
- Quy tắc vận hành

Boot chỉ định **cách nạp Domain**.

---

# Thứ tự nạp

AI phải nạp Domain theo đúng thứ tự:

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

README của các Module

↓

Các Module

↓

READY
```

Không được:

- thay đổi thứ tự
- bỏ qua bất kỳ bước nào

---

# Quy tắc

## 01

Luôn bắt đầu từ **Boot**.

---

## 02

Luôn nạp Domain theo đúng thứ tự.

---

## 03

Không đọc ngẫu nhiên các Module.

---

## 04

Nếu Trading Domain chưa ở trạng thái READY.

Dừng.

Không sử dụng Trading Domain.

---

## 05

Nếu dữ liệu chưa đủ.

Dừng.

Không suy diễn.

---

## 06

Mọi suy luận phải tuân thủ Trading Domain.

Không tự ý thay đổi kiến trúc.

---

## 07

Boot hỗ trợ các Boot Commands:

- `boot`
- `ready`
- `status`
- `reload`
- `update`
- `unload`

Chi tiết được định nghĩa trong **System-Instruction.md**.

---

# Trạng thái

Sau khi hoàn tất quá trình nạp:

```text
Trading Domain READY
```
hoặc

```text
Trading Domain NOT READY
```

Có thể kiểm tra bất kỳ lúc nào bằng:

```text
status
```

---

# Sau khi READY

Trading Domain trở thành Domain làm việc hiện tại.

Domain được duy trì cho đến khi:

- `unload`
- `reload`
- `update` (nếu yêu cầu nạp lại)
- Người dùng yêu cầu chuyển Domain.

---

# Triết lý

Boot khởi động Trading Domain.

Kiến trúc định nghĩa cách vận hành.

Tri thức nâng cao chất lượng suy luận.