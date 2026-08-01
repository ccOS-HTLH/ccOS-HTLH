# 01-Trường hợp

> Đơn vị tri thức cơ bản của Bộ nhớ.

---

# Mục đích

Trường hợp ghi nhận một Hệ thống suy luận đã được Thực tế kiểm chứng.

Mỗi Trường hợp lưu giữ:

- Bối cảnh.
- Diễn biến chính.
- Kết quả.
- Các ghi nhận.
- Liên kết tới Mẫu, Bài học tích luỹ và Thống kê.

Các dữ liệu chi tiết được lưu trong Phụ lục của Trường hợp.

---

# Vai trò

Trường hợp là đơn vị dữ liệu nhỏ nhất của Bộ nhớ.

Thông qua Trường hợp, Tri thức tích luỹ có thể:

- Tra cứu kinh nghiệm.
- Nhận diện Mẫu.
- Tổng hợp Bài học tích luỹ.
- Cập nhật Thống kê.

Mọi tri thức trong Bộ nhớ đều bắt đầu từ Trường hợp.

---

# Khi tạo

Một Trường hợp được ghi nhận sau khi:

```text
Hệ thống suy luận

↓

Hoàn tất

↓

Trường hợp
```

---

# Vòng đời

```text
Hệ thống suy luận

↓

Trường hợp

↓

Mẫu

↓

Bài học tích luỹ

↓

Thống kê
```

---

# Liên kết

Một Trường hợp có thể liên kết với:

- Chữ ký tín hiệu.
- Mẫu.
- Bài học tích luỹ.
- Thống kê.
- Phụ lục của Trường hợp.

Nhiều Trường hợp tạo nên Thống kê.

---

# Tra cứu

Quá trình tham khảo kinh nghiệm luôn bắt đầu từ Chữ ký tín hiệu.

```text
Chữ ký tín hiệu

↓

Trường hợp

↓

Mẫu

↓

Bài học tích luỹ

↓

Thống kê
```

---

# Định danh

```text
TH-0001
TH-0002
TH-0003
...
```

---

# Quy ước

Cấu trúc và cách ghi nhận Trường hợp được định nghĩa trong:

```text
Example.md
```

---

# Triết lý

Một Trường hợp lưu giữ một kinh nghiệm đã được Thực tế kiểm chứng.

Nhiều Trường hợp hình thành Mẫu.

Nhiều Mẫu hình thành Bài học tích luỹ.

Nhiều Bài học được tích lũy thành Tri thức tích luỹ.