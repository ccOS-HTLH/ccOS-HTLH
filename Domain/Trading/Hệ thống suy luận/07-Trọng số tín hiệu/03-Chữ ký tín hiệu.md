# Chữ ký tín hiệu

> Chuẩn hóa toàn bộ kết quả suy luận thành một dấu vết duy nhất.

---

# Mục đích

Chữ ký tín hiệu chuẩn hóa toàn bộ kết quả của Hệ thống suy luận thành một dấu vết duy nhất.

Chữ ký tín hiệu giúp Tri thức tích luỹ tra cứu các Trường hợp có trạng thái suy luận tương đồng.

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

---

# Đầu ra

Một Chữ ký tín hiệu duy nhất.

Chữ ký tín hiệu trở thành:

- Đầu vào của tầng Không gian kịch bản.
- Khóa tra cứu của Tri thức tích luỹ.

---

# Nguyên tắc

Mỗi Trạng thái quyết định chỉ tạo ra một Chữ ký tín hiệu.

Hai quá trình suy luận giống nhau phải tạo ra cùng một Chữ ký tín hiệu.

Khi bất kỳ thành phần nào của quá trình suy luận thay đổi, Chữ ký tín hiệu phải thay đổi.

Chữ ký tín hiệu được tạo theo một quy ước thống nhất của Hệ thống suy luận.

Chữ ký tín hiệu không được tạo ngẫu nhiên.

Những Chữ ký tín hiệu tương đồng đại diện cho những trạng thái suy luận tương đồng.

Chữ ký tín hiệu không thay đổi nội dung của quá trình suy luận.

Chữ ký tín hiệu chỉ chuẩn hóa quá trình suy luận thành một dấu vết để Tri thức tích luỹ tra cứu các Trường hợp tương tự.

---

# Vai trò

```text
Kết quả suy luận

↓

Chữ ký tín hiệu

├────────► 08 · Không gian kịch bản

└────────► Tri thức tích luỹ
                 │
                 ▼
          Tra cứu Trường hợp
```

---

# Triết lý

Mỗi quá trình suy luận đều để lại một dấu vết.

Mỗi dấu vết đều có một Chữ ký tín hiệu.

Chữ ký tín hiệu giúp Hệ thống suy luận kết nối hiện tại với kinh nghiệm từ Thực tế.