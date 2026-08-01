# Quy ước Chữ ký tín hiệu

> Quy ước chuẩn hóa cách tạo và sử dụng Chữ ký tín hiệu trong Trading Domain.

---

# Mục đích

Quy ước Chữ ký tín hiệu định nghĩa cách Hệ thống suy luận tạo và sử dụng Chữ ký tín hiệu.

Chữ ký tín hiệu là biểu diễn chuẩn của toàn bộ trạng thái suy luận tại thời điểm Hệ thống suy luận hoàn thành tầng 07-Trọng số tín hiệu. Từ thời điểm đó, Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế để tham khảo và cập nhật Tri thức tích luỹ.

Mọi Chữ ký tín hiệu đều được tạo theo cùng một quy ước.

---

# Triết lý

Mỗi quá trình suy luận đều để lại một dấu vết.

Chữ ký tín hiệu là dấu vết chuẩn của quá trình suy luận.

Một quy ước thống nhất giúp Hệ thống suy luận và Tri thức tích luỹ sử dụng cùng một ngôn ngữ.

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

# Vai trò

Quy ước này giúp:

- Chuẩn hóa trạng thái suy luận.
- Chuẩn hóa quá trình tra cứu.
- Nhận diện Trường hợp.
- Nhận diện Mẫu.
- Tham khảo Bài học tích luỹ.
- Tham khảo Thống kê.
- Đảm bảo tính nhất quán trong toàn bộ Trading Domain.

---

# Phạm vi

Quy ước này được sử dụng thống nhất trong:

- Hệ thống suy luận.
- Tri thức tích luỹ.

---

# Cấu trúc

```text
README

↓

01-Định nghĩa

↓

02-Cấu trúc

↓

03-Tạo Chữ ký

↓

04-Sử dụng

↓

05-Ví dụ
```

---

# Nguyên tắc

Mỗi quá trình suy luận tạo ra một Chữ ký tín hiệu.

Một Chữ ký tín hiệu phản ánh trạng thái của Hệ thống suy luận tại thời điểm hoàn thành tầng 07-Trọng số tín hiệu.

Mỗi Chữ ký tín hiệu được tạo theo cùng một quy ước và được sử dụng thống nhất trong các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế.

Cùng một trạng thái suy luận tạo ra cùng một Chữ ký tín hiệu.

---

# Tóm tắt

Chữ ký tín hiệu được tạo sau tầng 07-Trọng số tín hiệu.

Từ thời điểm đó, Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế để tham khảo và cập nhật Tri thức tích luỹ.