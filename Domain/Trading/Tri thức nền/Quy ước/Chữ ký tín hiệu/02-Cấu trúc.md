# 02 · Cấu trúc

> Thành phần cấu thành Chữ ký tín hiệu.

---

# Mục đích

Định nghĩa các thành phần tạo nên một Chữ ký tín hiệu.

Mọi Chữ ký tín hiệu đều được hình thành từ cùng một cấu trúc.

Cấu trúc thống nhất giúp Tri thức tích luỹ nhận diện, tra cứu và đối chiếu các trạng thái suy luận tương đồng.

---

# Triết lý

Chữ ký tín hiệu được hình thành từ toàn bộ trạng thái của quá trình suy luận.

Mỗi thành phần đóng góp một phần vào cấu trúc thống nhất của Chữ ký tín hiệu.

---

# Thành phần

Một Chữ ký tín hiệu được hình thành từ:

- Trạng thái hành vi.
- Trạng thái bối cảnh.
- Trạng thái động lượng.
- Trạng thái cấu trúc.
- Trạng thái chất lượng.
- Trạng thái quyết định.
- Trọng số tín hiệu.

Mỗi thành phần phản ánh một khía cạnh khác nhau của quá trình suy luận.

Toàn bộ các thành phần cùng tạo nên trạng thái suy luận được chuẩn hóa thành một Chữ ký tín hiệu.

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

# Mô hình

```text
01-Hành vi
      │
02-Bối cảnh
      │
03-Động lượng
      │
04-Cấu trúc
      │
05-Chất lượng
      │
06-Quyết định
      │
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

---

# Đặc điểm

Mỗi thành phần phản ánh một khía cạnh của trạng thái suy luận.

Sự kết hợp của các thành phần tạo nên một Chữ ký tín hiệu thống nhất.

Chữ ký tín hiệu phản ánh toàn bộ trạng thái suy luận tại thời điểm được tạo.

---

# Nguyên tắc

Mọi Chữ ký tín hiệu đều sử dụng cùng một cấu trúc.

Cấu trúc của Chữ ký tín hiệu được sử dụng thống nhất trong toàn bộ Trading Domain.

Thay đổi ở bất kỳ thành phần nào của trạng thái suy luận đều có thể hình thành một Chữ ký tín hiệu mới.

Mỗi Chữ ký tín hiệu phản ánh trạng thái suy luận tại thời điểm được tạo.

Chữ ký tín hiệu chuẩn hóa trạng thái suy luận của Hệ thống suy luận.

Chữ ký tín hiệu được sử dụng xuyên suốt các tầng Không gian kịch bản, Kế hoạch thực thi và Phản hồi thực tế để liên kết với Tri thức tích luỹ.

---

# Tóm tắt

Chữ ký tín hiệu được hình thành từ toàn bộ trạng thái suy luận sau tầng 07-Trọng số tín hiệu.

Cấu trúc thống nhất giúp Tri thức tích luỹ nhận diện, tra cứu và đối chiếu các trạng thái suy luận tương đồng.

Từ thời điểm được tạo, Chữ ký tín hiệu được sử dụng xuyên suốt các tầng 08-Không gian kịch bản, 09-Kế hoạch thực thi và 10-Phản hồi thực tế để tham khảo và cập nhật Tri thức tích luỹ.