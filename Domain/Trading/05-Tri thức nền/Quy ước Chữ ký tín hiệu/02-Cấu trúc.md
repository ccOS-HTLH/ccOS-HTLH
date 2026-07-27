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
Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ
```

Trong đó:

- Hệ thống suy luận tạo Chữ ký tín hiệu sau khi hoàn thành quá trình suy luận.
- Chữ ký tín hiệu là đầu vào của Tri thức tích luỹ.
- Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tra cứu Bộ nhớ.

---

# Mô hình

```text
01 · Hành vi
        │
        ▼
02 · Bối cảnh
        │
        ▼
03 · Động lượng
        │
        ▼
04 · Cấu trúc
        │
        ▼
05 · Chất lượng
        │
        ▼
06 · Quyết định
        │
        ▼
07 · Trọng số tín hiệu
        │
        ▼
Chữ ký tín hiệu
        │
        ▼
Tri thức tích luỹ
        │
        ▼
08 · Không gian kịch bản
        │
        ▼
09 · Kế hoạch thực thi
```

---

# Đặc điểm

Mỗi thành phần phản ánh một phần của quá trình suy luận.

Mỗi thành phần đóng góp vào việc hình thành Chữ ký tín hiệu.

Toàn bộ trạng thái suy luận được phản ánh thông qua sự kết hợp của tất cả các thành phần.

Chữ ký tín hiệu phản ánh trạng thái của Hệ thống suy luận tại thời điểm được tạo.

---

# Nguyên tắc

Mọi Chữ ký tín hiệu đều sử dụng cùng một cấu trúc.

Cấu trúc của Chữ ký tín hiệu được sử dụng thống nhất trong toàn bộ Trading Domain.

Thay đổi ở bất kỳ thành phần nào của trạng thái suy luận đều có thể hình thành một Chữ ký tín hiệu mới.

Mỗi Chữ ký tín hiệu phản ánh trạng thái suy luận tại thời điểm được tạo.

Chữ ký tín hiệu chuẩn hóa trạng thái suy luận của Hệ thống suy luận.

Dữ liệu của Thực tế và kết quả kiểm chứng được quản lý thông qua Tri thức tích luỹ và Bộ nhớ.

---

# Tóm tắt

```text
01 · Hành vi
        │
02 · Bối cảnh
        │
03 · Động lượng
        │
04 · Cấu trúc
        │
05 · Chất lượng
        │
06 · Quyết định
        │
07 · Trọng số tín hiệu
        │
        ▼
Chữ ký tín hiệu
```

Chữ ký tín hiệu được hình thành từ toàn bộ trạng thái của Hệ thống suy luận.

Mỗi thành phần đóng góp một phần vào cấu trúc thống nhất của Chữ ký tín hiệu.

Cấu trúc thống nhất giúp Tri thức tích luỹ nhận diện, tra cứu và đối chiếu các trạng thái suy luận tương đồng.

---

# Triết lý

Toàn bộ trạng thái thị trường được quan sát thông qua nhiều tín hiệu.

Toàn bộ quá trình suy luận được hình thành từ nhiều tầng suy luận liên kết với nhau.

Chữ ký tín hiệu phản ánh trạng thái tổng thể của Hệ thống suy luận.

Chính trạng thái tổng thể đó giúp Tri thức tích luỹ nhận diện những lần suy luận tương đồng và tái sử dụng kinh nghiệm đã được Thực tế kiểm chứng.