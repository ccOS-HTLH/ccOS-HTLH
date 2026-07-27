# Cơ chế

> Thành phần xử lý của Tri thức tích luỹ.

---

# Mục đích

Cơ chế chịu trách nhiệm xử lý dữ liệu của Tri thức tích luỹ.

Thông qua Bộ nhớ, Cơ chế thực hiện:

- Tra cứu.
- Đối chiếu.
- Tổng hợp.
- Cập nhật.

Cơ chế giúp chuyển dữ liệu lịch sử thành thông tin tham khảo cho các chu kỳ suy luận tiếp theo.

---

# Vai trò

Cơ chế là lớp xử lý của Tri thức tích luỹ.

Tri thức tích luỹ sử dụng Cơ chế để:

- Tra cứu dữ liệu liên quan.
- Đối chiếu với tình huống hiện tại.
- Tổng hợp kinh nghiệm.
- Cập nhật Bộ nhớ sau khi có Phản hồi thực tế.

---

# Khi hoạt động

Cơ chế được kích hoạt khi:

- Có Chữ ký tín hiệu cần tra cứu.
- Có Phản hồi thực tế cần cập nhật.

Quá trình xử lý diễn ra xuyên suốt các chu kỳ suy luận.

---

# Quy trình

```text
Chữ ký tín hiệu

↓

Tra cứu

↓

Đối chiếu

↓

Tổng hợp

↓

Không gian kịch bản

↓

Kế hoạch thực thi

↓

Phản hồi thực tế

↓

Cập nhật Bộ nhớ
```

---

# Thành phần

```text
01 · Tra cứu

↓

02 · Đối chiếu

↓

03 · Tổng hợp

↓

04 · Cập nhật
```

---

# Liên kết dữ liệu

Cơ chế làm việc với Bộ nhớ để:

- Đọc dữ liệu.
- Đối chiếu dữ liệu.
- Tổng hợp kết quả.
- Ghi nhận dữ liệu mới.

Bộ nhớ lưu trữ dữ liệu.

Cơ chế xử lý dữ liệu.

---

# Quy ước

Chức năng và cách hoạt động của từng thành phần được định nghĩa trong:

```text
01 · Tra cứu

02 · Đối chiếu

03 · Tổng hợp

04 · Cập nhật
```

---

# Triết lý

Bộ nhớ lưu giữ kinh nghiệm.

Cơ chế sử dụng kinh nghiệm.

Tri thức tích luỹ kết nối kinh nghiệm với các chu kỳ suy luận tiếp theo.