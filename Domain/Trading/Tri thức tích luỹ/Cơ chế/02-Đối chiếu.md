# 02 · Đối chiếu

> Đánh giá mức độ liên quan giữa tình huống hiện tại và dữ liệu trong Bộ nhớ.

---

# Mục đích

Đối chiếu là bước thứ hai của Cơ chế.

Bước này chịu trách nhiệm so sánh tình huống hiện tại với các dữ liệu đã được Tra cứu.

Đối chiếu đánh giá mức độ liên quan.

Đối chiếu không tạo dữ liệu mới.

Đối chiếu không cập nhật Bộ nhớ.

---

# Câu hỏi

Trong các dữ liệu đã Tra cứu:

- Trường hợp nào tương đồng nhất?
- Mẫu nào phù hợp nhất?
- Bài học nào có thể áp dụng?
- Thống kê nào có giá trị tham khảo?

---

# Đầu vào

- Tình huống hiện tại.
- Kết quả Tra cứu.

---

# Đầu ra

Danh sách dữ liệu đã được đối chiếu, có thể bao gồm:

- Trường hợp liên quan.
- Mẫu phù hợp.
- Bài học tích luỹ phù hợp.
- Thống kê liên quan.

Các kết quả này trở thành đầu vào của bước Tổng hợp.

---

# Vai trò trong Cơ chế

```text
Tra cứu

↓

Đối chiếu

↓

Trường hợp phù hợp

Mẫu phù hợp

Bài học tích luỹ phù hợp

Thống kê liên quan

↓

Tổng hợp
```

---

# Nguyên tắc

- Chỉ đánh giá các dữ liệu đã được Tra cứu.
- Không tạo dữ liệu mới.
- Không cập nhật Bộ nhớ.
- Không đưa ra quyết định.
- Không loại bỏ dữ liệu lịch sử.

---

# Tiêu chí đối chiếu

Việc đối chiếu có thể dựa trên:

- Chữ ký tín hiệu.
- Điều kiện thị trường.
- Mức độ tương đồng.
- Bối cảnh.
- Kết quả thực tế đã được kiểm chứng.

Mỗi dữ liệu có thể có mức độ phù hợp khác nhau.

---

# Triết lý

Tra cứu tìm dữ liệu.

Đối chiếu đánh giá dữ liệu.

Tổng hợp mới hình thành kết quả tham khảo.