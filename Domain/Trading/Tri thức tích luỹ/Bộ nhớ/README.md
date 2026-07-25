# Bộ nhớ

> Kho dữ liệu của Tri thức tích luỹ.

Bộ nhớ lưu giữ dữ liệu đã được kiểm chứng từ Thực tế.

Mọi thao tác đọc, ghi và cập nhật đều được thực hiện thông qua Tri thức tích luỹ.

Bộ nhớ không tham gia trực tiếp vào quá trình suy luận.

---

# Vai trò

Bộ nhớ lưu trữ và liên kết các dữ liệu đã được kiểm chứng để Tri thức tích luỹ:

- Tra cứu kinh nghiệm.
- Đối chiếu dữ liệu.
- Tổng hợp kết quả.
- Cập nhật tri thức.

---

# Cấu trúc

Bộ nhớ gồm bốn kho dữ liệu:

## 01 · Trường hợp

Lưu trữ các Trường hợp đã xảy ra.

## 02 · Mẫu

Lưu trữ các Mẫu đã được xác nhận.

## 03 · Bài học tích luỹ

Lưu trữ các Bài học tích luỹ đã được kiểm chứng.

## 04 · Thống kê

Lưu trữ các Thống kê lịch sử.

---

# Liên kết dữ liệu

Các thực thể được liên kết với nhau bằng tham chiếu.

## Trường hợp

- Chữ ký tín hiệu.
- Mẫu liên quan.
- Bài học tích luỹ liên quan.

## Mẫu

- Trường hợp liên quan.
- Bài học tích luỹ liên quan.
- Thống kê liên quan.

## Bài học tích luỹ

- Trường hợp liên quan.
- Mẫu liên quan.

## Thống kê

- Đối tượng liên quan.

---

# Quy tắc

- Chỉ lưu dữ liệu đã được kiểm chứng.
- Mỗi thực thể có một mã định danh duy nhất và bất biến.
- Các thực thể được liên kết bằng tham chiếu.
- Không chỉnh sửa dữ liệu lịch sử, ngoại trừ việc sửa lỗi ghi chép.

---

# Quy ước định danh

Mỗi loại thực thể sử dụng một tiền tố riêng.

Cấu trúc chung:

<Loại>-<Số thứ tự>

Ví dụ:

- TH-0001 · Trường hợp
- M-0001 · Mẫu
- BH-0001 · Bài học tích luỹ
- TK-0001 · Thống kê

---

# Triết lý

Thực tế tạo nên kinh nghiệm.

Bộ nhớ lưu giữ kinh nghiệm.

Tri thức tích luỹ học hỏi từ Bộ nhớ.

Hệ thống suy luận phát triển từ kinh nghiệm.