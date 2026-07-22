---
title: AI Guide
id: trading-ai-guide
version: 1.4.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-07-22
review_cycle: Manual
confidence: 100%
---

# AI Guide

> Hướng dẫn AI sử dụng Trading Domain.

---

# Mục đích

AI Guide định nghĩa cách AI sử dụng Trading Domain sau khi Domain ở trạng thái:

```text
Trading Domain READY
```

AI vận hành theo đúng kiến trúc và quy tắc của Trading Domain.

AI không thay đổi kiến trúc hoặc Logic của Domain.

---

# Quy trình

## 01 · Tiếp nhận dữ liệu

Sau khi:

```text
Trading Domain READY
```

AI chờ người dùng cung cấp **Nguồn dữ liệu**.

Nguồn dữ liệu có thể là:

- ATS
- Dữ liệu rời rạc
- Hoặc kết hợp cả hai

Khi nhận đủ Nguồn dữ liệu, AI tự động thực hiện toàn bộ chu trình của Trading Domain:

```text
Nguồn dữ liệu

↓

Hệ thống suy luận (01 → 10)

↓

Quyết định
```

AI chỉ yêu cầu bổ sung khi Nguồn dữ liệu chưa đủ để tiếp tục.

---

## 02 · Chuẩn hóa dữ liệu

Diễn giải dữ liệu theo:

- Tri thức nền
- Quy ước của Trading Domain

Không tự tạo:

- Thuật ngữ
- Khái niệm
- Quy ước mới

---

## 03 · Thực hiện suy luận

Thực hiện đầy đủ Hệ thống suy luận theo đúng thứ tự:

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

Không được:

- Bỏ qua tầng
- Đảo thứ tự

---

## 04 · Tham khảo Tri thức tích lũy

Sau khi Hệ thống suy luận hoàn thành.

Có thể sử dụng Chữ ký tín hiệu để tra cứu Tri thức tích lũy.

Tri thức tích lũy chỉ dùng để:

- Tham khảo
- Đánh giá
- Hiệu chỉnh

Không tạo suy luận mới.

---

## 05 · Kết thúc chu kỳ

Sau khi Quyết định được Thực tế kiểm chứng:

```text
Tri thức tích lũy

↓

Chu kỳ suy luận tiếp theo
```

Tri thức tích lũy được cập nhật và chỉ được tham khảo trong các chu kỳ suy luận tiếp theo.

---

# Nguyên tắc

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

Không được đảo chiều.

---

# Không được

- Bỏ qua tầng
- Đảo thứ tự suy luận
- Kết luận khi dữ liệu chưa đủ
- Tự suy diễn ngoài dữ liệu
- Thay đổi kiến trúc hoặc Logic của Trading Domain
- Dùng Tri thức tích lũy thay thế quá trình suy luận

---

# Có thể

- Tham khảo Tri thức tích lũy
- Hiệu chỉnh xác suất
- Hiệu chỉnh mức độ tin cậy
- Hiệu chỉnh kế hoạch
- Đề xuất cập nhật Tri thức tích lũy sau khi có Phản hồi thực tế

---

# Điều kiện sử dụng

Trading Domain chỉ được sử dụng khi:

```text
Trading Domain READY
```

Sau khi ở trạng thái READY:

- AI chờ người dùng cung cấp Nguồn dữ liệu.
- AI tự động vận hành toàn bộ Trading Domain theo đúng kiến trúc.
- Người dùng không cần chỉ định từng tầng của Hệ thống suy luận.

---

# Triết lý

```text
AI

↓

Vận hành đúng kiến trúc

↓

Không thay đổi Trading Domain
```