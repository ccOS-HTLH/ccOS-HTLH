# 01-Định nghĩa

> Bản chất của Chữ ký tín hiệu.

---

# Bản chất

Chữ ký tín hiệu là biểu diễn chuẩn của một trạng thái suy luận.

Chữ ký tín hiệu chuẩn hóa toàn bộ trạng thái suy luận của Hệ thống suy luận thành một biểu diễn thống nhất.

Mỗi Chữ ký tín hiệu đại diện cho toàn bộ trạng thái suy luận tại thời điểm Hệ thống suy luận hoàn thành tầng 07-Trọng số tín hiệu.

---

# Vai trò

Chữ ký tín hiệu giúp:

- Chuẩn hóa trạng thái suy luận.
- Nhận diện các trạng thái suy luận tương đồng.
- Tra cứu Bộ nhớ thông qua Tri thức tích luỹ.
- Liên kết giữa Hệ thống suy luận và Tri thức tích luỹ.
- Đảm bảo tính nhất quán trong toàn bộ Trading Domain.

---

# Mối quan hệ với Trading

```text
07-Trọng số tín hiệu
        │
        ├── tạo
        ▼
  Chữ ký tín hiệu

08-Không gian kịch bản
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

09-Kế hoạch thực thi
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

10-Phản hồi thực tế
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Cập nhật Tri thức tích luỹ
```

Trong đó:

- Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.
- Từ tầng 08 đến tầng 10, Chữ ký tín hiệu được sử dụng thống nhất để tham khảo và cập nhật Tri thức tích luỹ.

---

# Đặc điểm

Chữ ký tín hiệu là biểu diễn chuẩn của trạng thái suy luận.

Một Chữ ký tín hiệu có thể được liên kết với nhiều Trường hợp có cùng trạng thái suy luận.

Thông qua các Trường hợp, Tri thức tích luỹ hình thành Mẫu, Bài học tích luỹ và Thống kê.

Tri thức được Tri thức tích luỹ quản lý trong Bộ nhớ.

---

# Mối quan hệ

Một Chữ ký tín hiệu có thể:

- Chưa được liên kết với Trường hợp nào.
- Liên kết với một Trường hợp.
- Liên kết với nhiều Trường hợp.

Một Trường hợp luôn liên kết với đúng một Chữ ký tín hiệu.

Một Chữ ký tín hiệu có thể được nhiều Trường hợp cùng sử dụng nếu chúng có cùng trạng thái suy luận.

---

# Mục tiêu

Chữ ký tín hiệu được tạo ra để:

- Chuẩn hóa trạng thái suy luận.
- Nhận diện các trạng thái suy luận tương đồng.
- Hỗ trợ Tri thức tích luỹ tra cứu Bộ nhớ.
- Chuẩn hóa điểm tham chiếu giữa Hệ thống suy luận và Tri thức tích luỹ.
- Hỗ trợ tái sử dụng kinh nghiệm trong các Hệ thống suy luận tiếp theo.

---

# Nguyên tắc

Một trạng thái suy luận tạo ra một Chữ ký tín hiệu.

Một Chữ ký tín hiệu có thể được nhiều Trường hợp cùng sử dụng khi chúng có cùng trạng thái suy luận.

Một Trường hợp luôn liên kết với đúng một Chữ ký tín hiệu.

Mỗi Chữ ký tín hiệu được cố định sau khi được tạo.

Tri thức tích luỹ sử dụng Chữ ký tín hiệu để nhận diện, tra cứu và cập nhật dữ liệu trong Bộ nhớ.

Chữ ký tín hiệu là cầu nối thống nhất giữa Hệ thống suy luận và Tri thức tích luỹ.

---

# Tóm tắt

Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.

Từ thời điểm đó, Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế để tham khảo và cập nhật Tri thức tích luỹ.