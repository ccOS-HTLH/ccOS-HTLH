# 01 · Tra cứu

> Tìm dữ liệu liên quan trong Bộ nhớ.

---

# Mục đích

Tra cứu là bước đầu tiên của Cơ chế.

Bước này chịu trách nhiệm tìm kiếm các dữ liệu đã được lưu trong Bộ nhớ dựa trên tình huống hiện tại.

Tra cứu không đánh giá.

Tra cứu không kết luận.

Tra cứu chỉ trả về những dữ liệu có khả năng liên quan.

---

# Câu hỏi

Tình huống hiện tại đã từng xuất hiện chưa?

Nếu đã từng xuất hiện:

- Có Trường hợp nào liên quan?
- Có Mẫu nào liên quan?
- Có Bài học tích luỹ nào liên quan?
- Có Thống kê nào liên quan?

---

# Đầu vào

- Chữ ký tín hiệu.

---

# Đầu ra

Danh sách dữ liệu liên quan, có thể bao gồm:

- Trường hợp.
- Mẫu.
- Bài học tích luỹ.
- Thống kê.

Các kết quả này trở thành đầu vào của bước Đối chiếu.

---

# Vai trò trong Cơ chế

```text
Chữ ký tín hiệu

↓

Tra cứu

↓

Trường hợp
Mẫu
Bài học tích luỹ
Thống kê

↓

Đối chiếu
```

---

# Nguyên tắc

- Chỉ tra cứu dữ liệu trong Bộ nhớ.
- Không đánh giá mức độ tương đồng.
- Không loại bỏ dữ liệu.
- Không tạo dữ liệu mới.
- Không cập nhật Bộ nhớ.

---

# Cách tra cứu

Tra cứu được thực hiện theo hai bước:

## 01 · Tra cứu trực tiếp

Sử dụng Chữ ký tín hiệu để tìm các dữ liệu liên quan trong Bộ nhớ.

Đây là phương thức tra cứu ưu tiên.

## 02 · Tra cứu mở rộng

Nếu kết quả chưa đủ để tham khảo, tiếp tục mở rộng phạm vi tra cứu dựa trên:

- Liên kết giữa các thực thể.
- Điều kiện đã được lưu.
- Các dữ liệu liên quan khác trong Bộ nhớ.

Việc đánh giá mức độ liên quan được thực hiện ở bước Đối chiếu.

---

# Triết lý

Tra cứu chỉ tìm dữ liệu.

Đối chiếu mới đánh giá dữ liệu.

Mọi kết quả tra cứu đều là dữ liệu tham khảo.