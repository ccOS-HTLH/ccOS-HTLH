# Build

> Đóng gói Trading Domain thành các tài liệu sử dụng.

---

# Mục đích

Build chịu trách nhiệm đóng gói các tài liệu nguồn của Trading Domain thành các gói sử dụng.

Các gói Build giúp:

- Tập hợp đúng phạm vi tài liệu cần sử dụng.
- Giữ nguyên cấu trúc của tài liệu nguồn.
- Phân phối Trading Domain theo từng mục đích sử dụng.

Build không tạo tri thức mới và không phải là nơi chỉnh sửa nội dung.

Mọi thay đổi đều phải được thực hiện trên tài liệu nguồn trước khi Build.

---

# Câu hỏi

Cần sử dụng phần nào của Trading Domain?

Cần một gói chuyên biệt hay toàn bộ Domain?

---

# Thành phần

## Trading Core

Đóng gói các tài liệu nền tảng của Trading Domain.

## Trading Knowledge

Đóng gói toàn bộ Tri thức nền.

## Trading Data

Đóng gói toàn bộ tài liệu thuộc Nguồn dữ liệu.

## Trading Reasoning

Đóng gói toàn bộ Hệ thống suy luận.

## Trading Memory

Đóng gói toàn bộ Tri thức tích luỹ.

## Trading Domain Full

Đóng gói toàn bộ Trading Domain.

## Reasoning

Đóng gói riêng từng tầng của Hệ thống suy luận.

Mỗi tệp tương ứng với một tầng:

- 01-Hành vi
- 02-Bối cảnh
- ...
- 10-Phản hồi thực tế

---

# Vai trò trong Trading

```text
Tài liệu nguồn

↓

Build

↓

Các gói Build

├── Trading Core
├── Trading Knowledge
├── Trading Data
├── Trading Reasoning
├── Trading Memory
└── Trading Domain Full
```

---

# Nguyên tắc

- Không chỉnh sửa nội dung trong Build.
- Mọi Build đều được tạo từ tài liệu nguồn.
- Một tài liệu nguồn có thể xuất hiện trong nhiều gói Build.
- Các gói Build phải phản ánh đúng phiên bản hiện tại của Trading Domain.

---

# Triết lý

Tài liệu nguồn là nơi phát triển tri thức.

Build là nơi đóng gói tài liệu.

Một nguồn có thể tạo ra nhiều gói Build.

Mọi gói Build đều có thể truy xuất ngược về tài liệu nguồn.