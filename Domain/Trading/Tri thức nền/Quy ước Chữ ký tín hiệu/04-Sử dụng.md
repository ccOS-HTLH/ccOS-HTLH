# 04 · Sử dụng

> Cách Chữ ký tín hiệu được sử dụng trong Trading Domain.

---

# Mục đích

Quy định cách Chữ ký tín hiệu được sử dụng trong Hệ thống suy luận và Tri thức tích luỹ.

Chữ ký tín hiệu là cầu nối giữa quá trình suy luận và Bộ nhớ.

---

# Luồng sử dụng

```text
Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Tra cứu Bộ nhớ

↓

Đối chiếu

↓

Tổng hợp

↓

08 · Không gian kịch bản

09 · Kế hoạch thực thi

↓

10 · Phản hồi thực tế

↓

Cập nhật Bộ nhớ (nếu có)
```

---

# Vai trò

Trong Trading Domain:

- Tầng 07 tạo Chữ ký tín hiệu.
- Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tra cứu Bộ nhớ.
- Không gian kịch bản tham khảo kết quả từ Tri thức tích luỹ.
- Kế hoạch thực thi tham khảo kết quả từ Tri thức tích luỹ.
- Phản hồi thực tế cung cấp dữ liệu để Tri thức tích luỹ cập nhật Bộ nhớ.

---

# Nguyên tắc

- Chữ ký tín hiệu không trực tiếp truy cập Bộ nhớ.
- Chữ ký tín hiệu không trực tiếp tạo Trường hợp.
- Chữ ký tín hiệu không thay thế quá trình suy luận.
- Chữ ký tín hiệu chỉ đóng vai trò nhận diện và liên kết dữ liệu.

---

# Mối quan hệ

```text
Chữ ký tín hiệu
        │
        ▼
Tri thức tích luỹ
        │
        ▼
Bộ nhớ
   │
   ├── Trường hợp
   ├── Mẫu
   ├── Bài học tích luỹ
   └── Thống kê
```

---

# Triết lý

Chữ ký tín hiệu kết nối suy luận với kinh nghiệm.

Tri thức tích luỹ kết nối kinh nghiệm với quyết định.

Bộ nhớ lưu giữ những gì đã được Thực tế kiểm chứng.