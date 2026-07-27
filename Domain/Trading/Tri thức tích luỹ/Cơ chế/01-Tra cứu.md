# 01 · Tra cứu

> Tìm dữ liệu liên quan trong Bộ nhớ.

---

# Mục đích

Tra cứu là bước đầu tiên của Cơ chế.

Bước này tìm kiếm các dữ liệu liên quan trong Bộ nhớ dựa trên Chữ ký tín hiệu, tạo đầu vào cho bước Đối chiếu.

---

# Vai trò

Tra cứu giúp Tri thức tích luỹ:

- Tìm Trường hợp liên quan.
- Tìm Mẫu liên quan.
- Tìm Bài học tích luỹ liên quan.
- Tìm Thống kê liên quan.

Kết quả tra cứu cung cấp dữ liệu tham khảo cho các bước xử lý tiếp theo.

---

# Khi hoạt động

Tra cứu được kích hoạt khi Hệ thống suy luận tạo Chữ ký tín hiệu.

Quá trình tra cứu diễn ra trước bước Đối chiếu.

---

# Quy trình

```text
Chữ ký tín hiệu

↓

Tra cứu

↓

Trường hợp

↓

Mẫu

↓

Bài học tích luỹ

↓

Thống kê

↓

Đối chiếu
```

---

# Kết quả

Tra cứu trả về danh sách dữ liệu liên quan, có thể bao gồm:

- Trường hợp.
- Mẫu.
- Bài học tích luỹ.
- Thống kê.

Các dữ liệu này trở thành đầu vào của bước Đối chiếu.

---

# Phương thức

Tra cứu được thực hiện theo hai mức:

## 01 · Tra cứu trực tiếp

Tìm dữ liệu bằng Chữ ký tín hiệu.

## 02 · Tra cứu mở rộng

Mở rộng phạm vi tra cứu thông qua các liên kết giữa:

- Trường hợp.
- Mẫu.
- Bài học tích luỹ.
- Thống kê.

---

# Quy ước

Quá trình tra cứu sử dụng dữ liệu trong Bộ nhớ và giữ nguyên các liên kết giữa các thực thể.

---

# Triết lý

Tra cứu kết nối hiện tại với kinh nghiệm đã được lưu giữ.

Dữ liệu được tìm thấy tạo nền tảng cho bước Đối chiếu.