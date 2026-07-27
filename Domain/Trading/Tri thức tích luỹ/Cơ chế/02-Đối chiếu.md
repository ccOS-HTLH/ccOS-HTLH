# 02 · Đối chiếu

> Đánh giá mức độ liên quan giữa tình huống hiện tại và dữ liệu trong Bộ nhớ.

---

# Mục đích

Đối chiếu là bước thứ hai của Cơ chế.

Bước này so sánh tình huống hiện tại với các dữ liệu đã được Tra cứu để xác định những dữ liệu có giá trị tham khảo phù hợp.

---

# Vai trò

Đối chiếu giúp Tri thức tích luỹ:

- So sánh tình huống hiện tại với dữ liệu lịch sử.
- Đánh giá mức độ phù hợp giữa các Trường hợp.
- Nhận diện Mẫu phù hợp.
- Xác định Bài học tích luỹ và Thống kê có giá trị tham khảo.

Kết quả đối chiếu cung cấp đầu vào cho bước Tổng hợp.

---

# Khi hoạt động

Đối chiếu được thực hiện sau khi quá trình Tra cứu hoàn tất.

Quá trình này diễn ra trước bước Tổng hợp.

---

# Quy trình

```text
Tra cứu

↓

Đối chiếu

↓

Trường hợp phù hợp

↓

Mẫu phù hợp

↓

Bài học tích luỹ

↓

Thống kê

↓

Tổng hợp
```

---

# Kết quả

Đối chiếu trả về danh sách dữ liệu đã được đánh giá, có thể bao gồm:

- Trường hợp phù hợp.
- Mẫu phù hợp.
- Bài học tích luỹ liên quan.
- Thống kê liên quan.

Các dữ liệu này trở thành đầu vào của bước Tổng hợp.

---

# Tiêu chí

Việc đối chiếu có thể tham khảo:

- Chữ ký tín hiệu.
- Điều kiện thị trường.
- Mức độ tương đồng.
- Bối cảnh.
- Kết quả thực tế đã được kiểm chứng.

Mỗi dữ liệu có thể có mức độ phù hợp khác nhau.

---

# Quy ước

Đối chiếu sử dụng dữ liệu đã được Tra cứu và giữ nguyên các liên kết trong Bộ nhớ.

---

# Triết lý

Tra cứu tìm dữ liệu.

Đối chiếu đánh giá mức độ phù hợp.

Tổng hợp hình thành kết quả tham khảo.