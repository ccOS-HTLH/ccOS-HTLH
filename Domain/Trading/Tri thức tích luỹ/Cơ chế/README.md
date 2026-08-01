# Cơ chế

> Thành phần xử lý của Tri thức tích luỹ.

---

# Mục đích

Cơ chế chịu trách nhiệm khai thác và cập nhật Tri thức tích luỹ.

Thông qua Bộ nhớ, Cơ chế thực hiện:

- Tra cứu.
- Đối chiếu.
- Tổng hợp.
- Cập nhật.

Cơ chế giúp chuyển kinh nghiệm đã được kiểm chứng thành dữ liệu tham khảo cho các lần suy luận tiếp theo.

---

# Vai trò

Cơ chế là lớp xử lý của Tri thức tích luỹ.

Chịu trách nhiệm:

- Tra cứu dữ liệu liên quan.
- Đối chiếu với tình huống hiện tại.
- Tổng hợp kinh nghiệm.
- Cập nhật Bộ nhớ sau khi có Phản hồi thực tế.

---

# Khi hoạt động

Cơ chế được kích hoạt khi:

- Có Chữ ký tín hiệu cần tra cứu.
- Có Phản hồi thực tế cần cập nhật.

---

# Quy trình

```text
Chữ ký tín hiệu

↓

01-Tra cứu

↓

02-Đối chiếu

↓

03-Tổng hợp

↓

08-Không gian kịch bản

↓

09-Kế hoạch thực thi

↓

10-Phản hồi thực tế

↓

04-Cập nhật

↓

Bộ nhớ
```

---

# Thành phần

```text
01-Tra cứu

↓

02-Đối chiếu

↓

03-Tổng hợp

↓

04-Cập nhật
```

---

# Liên kết dữ liệu

```text
Bộ nhớ

↓

Cơ chế

↓

Hệ thống suy luận
```

Bộ nhớ lưu giữ kinh nghiệm.

Cơ chế khai thác và cập nhật kinh nghiệm.

---

# Triết lý

Bộ nhớ lưu giữ kinh nghiệm.

Cơ chế khai thác kinh nghiệm.

Tri thức tích luỹ kết nối kinh nghiệm với các lần suy luận tiếp theo.