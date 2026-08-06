# 07-Trọng số tín hiệu

> Giải thích mức độ ảnh hưởng của từng bằng chứng đến Trạng thái quyết định.

---

# Mục đích

Trọng số tín hiệu là tầng thứ bảy của Hệ thống suy luận.

Tầng này giải thích cách Trạng thái quyết định hiện tại được hình thành.

Tầng này lượng hóa mức độ ảnh hưởng của từng tầng suy luận đối với Trạng thái quyết định.

Đồng thời, tầng này chuẩn hóa toàn bộ quá trình suy luận thành một Chữ ký tín hiệu để phục vụ tầng Không gian kịch bản và Tri thức tích luỹ.

---

# Câu hỏi

Điều gì ảnh hưởng nhiều nhất đến Trạng thái quyết định hiện tại?

---

# Đầu vào

- Trạng thái hành vi.
- Trạng thái bối cảnh.
- Trạng thái động lượng.
- Trạng thái cấu trúc.
- Trạng thái chất lượng.
- Trạng thái quyết định.

---

# Đầu ra

- Trọng số tín hiệu.
- Chữ ký tín hiệu.

Chữ ký tín hiệu trở thành đầu vào của tầng Không gian kịch bản, đồng thời là khóa tra cứu của Tri thức tích luỹ.

---

# Vai trò trong Hệ thống suy luận

```text
06-Quyết định
        │
        ▼
07-Trọng số tín hiệu
        │
        ▼
   Chữ ký tín hiệu
      │        │
      │        ├────────► 08-Không gian kịch bản
      │
      └────────► Tri thức tích luỹ
                         │
                         ▼
                  Tra cứu Trường hợp
```

---

# Cấu trúc

```text
01-Định nghĩa

↓

02-Quan sát

↓

03-Trọng số tín hiệu

↓

04-Chữ ký tín hiệu

↓

05-Ví dụ
```

---

# Triết lý

Mọi Trạng thái quyết định đều có thể được giải thích.

Trọng số tín hiệu phản ánh mức độ đóng góp của từng tầng vào Trạng thái quyết định.

Chữ ký tín hiệu chuẩn hóa toàn bộ quá trình suy luận thành một dấu vết duy nhất.

Dấu vết đó giúp Tri thức tích luỹ tra cứu các Trường hợp tương tự để tham khảo kinh nghiệm đã được tích luỹ.

---

# Định nghĩa

> Bản chất của Trọng số tín hiệu.

---

# Bản chất

Trọng số tín hiệu phản ánh mức độ đóng góp của từng tầng vào Trạng thái quyết định.

Trọng số tín hiệu không tạo ra Trạng thái quyết định.

Trọng số tín hiệu giải thích vì sao Trạng thái quyết định được hình thành.

Từ Trọng số tín hiệu, Hệ thống chuẩn hóa thành một Chữ ký tín hiệu để phục vụ các tầng tiếp theo.

---

# Thành phần

Trọng số tín hiệu được hình thành từ:

- Hành vi.
- Bối cảnh.
- Động lượng.
- Cấu trúc.
- Chất lượng.

Mỗi thành phần phản ánh mức độ đóng góp của một tầng suy luận vào Trạng thái quyết định.

Tổng hợp các thành phần tạo nên Trọng số tín hiệu của toàn bộ quá trình suy luận.

---

# Mục tiêu

- Giải thích.
- Lượng hóa.
- Chuẩn hóa.
- Truy vết.

---

# Đầu ra

Tầng Trọng số tín hiệu tạo ra:

- Trọng số tín hiệu.
- Chữ ký tín hiệu.

Trong đó:

- Trọng số tín hiệu giải thích cách Trạng thái quyết định được hình thành.
- Chữ ký tín hiệu chuẩn hóa toàn bộ quá trình suy luận thành một dấu vết duy nhất để Tri thức tích luỹ tra cứu các Trường hợp tương tự.

---

# Triết lý

Mỗi Trạng thái quyết định đều có thể được giải thích.

Trọng số tín hiệu lượng hóa mức độ đóng góp của từng tầng.

Chữ ký tín hiệu chuẩn hóa toàn bộ quá trình suy luận thành một dấu vết có thể truy vết và tái sử dụng.

---

# Quan sát

> Quan sát mức độ đóng góp của từng tầng vào Trạng thái quyết định.

---

# Mục đích

Quan sát mức độ đóng góp của từng tầng suy luận vào Trạng thái quyết định.

Từ đó lượng hóa mức độ ảnh hưởng của từng tầng và hình thành Trọng số tín hiệu.

---

# Quan sát

Quan sát mức độ đóng góp của:

- Hành vi.
- Bối cảnh.
- Động lượng.
- Cấu trúc.
- Chất lượng.

Đồng thời quan sát Trạng thái quyết định được hình thành từ các tầng trên.

---

# Nguyên tắc

Mọi Trạng thái quyết định đều được hình thành từ nhiều tầng suy luận.

Mỗi tầng có một mức độ ảnh hưởng khác nhau.

Trọng số tín hiệu lượng hóa mức độ ảnh hưởng của từng tầng.

Tổng các Trọng số tín hiệu giải thích cách Trạng thái quyết định được hình thành.

---

# Đầu ra

Kết quả quan sát trở thành cơ sở để:

- Lượng hóa Trọng số tín hiệu.
- Chuẩn hóa thành Chữ ký tín hiệu.

---

# Triết lý

Quan sát đi trước lượng hóa.

Lượng hóa đi trước chuẩn hóa.

Trọng số tín hiệu giải thích cách Trạng thái quyết định được hình thành.

---

# Chữ ký tín hiệu

> Chuẩn hóa toàn bộ quá trình suy luận thành một dấu vết duy nhất.

---

# Mục đích

Chữ ký tín hiệu chuẩn hóa toàn bộ quá trình của Hệ thống suy luận thành một dấu vết duy nhất.

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

Những Chữ ký tín hiệu tương đồng đại diện cho những quá trình suy luận tương đồng.

Chữ ký tín hiệu không thay đổi nội dung của quá trình suy luận.

Chữ ký tín hiệu chỉ chuẩn hóa quá trình suy luận thành một dấu vết để Tri thức tích luỹ tra cứu các Trường hợp tương tự.

---

# Vai trò

```text
Kết quả suy luận

↓

Chữ ký tín hiệu

├────────► 08-Không gian kịch bản

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

---

# Ví dụ

---

# Ví dụ 01

## Trạng thái quyết định

- Định hướng tăng.

↓

## Trọng số tín hiệu

- Động lượng: **42%**
- Bối cảnh: **28%**
- Cấu trúc: **16%**
- Hành vi: **9%**
- Chất lượng: **5%**

↓

## Chữ ký tín hiệu

```text
SIG-8A24
```

↓

## Vai trò

```text
SIG-8A24

↓

08-Không gian kịch bản

↓

Tri thức tích luỹ

↓

Tra cứu các Trường hợp tương tự
```

---

# Ví dụ 02

## Trạng thái quyết định

- Trung lập.

↓

## Trọng số tín hiệu

- Bối cảnh: **31%**
- Cấu trúc: **24%**
- Động lượng: **22%**
- Hành vi: **14%**
- Chất lượng: **9%**

↓

## Chữ ký tín hiệu

```text
SIG-3F91
```

↓

## Vai trò

```text
SIG-3F91

↓

08-Không gian kịch bản

↓

Tri thức tích luỹ

↓

Tra cứu các Trường hợp tương tự
```

---

# Nguyên tắc

Trọng số tín hiệu phản ánh mức độ đóng góp của từng tầng suy luận.

Tổng các Trọng số tín hiệu giải thích cách Trạng thái quyết định được hình thành.

Chữ ký tín hiệu chuẩn hóa toàn bộ quá trình suy luận thành một dấu vết duy nhất.

Tri thức tích luỹ sử dụng Chữ ký tín hiệu làm khóa tra cứu các Trường hợp tương tự.

---

# Triết lý

Trọng số tín hiệu giải thích quá trình hình thành Trạng thái quyết định.

Chữ ký tín hiệu chuẩn hóa quá trình suy luận để kết nối với kinh nghiệm đã được tích luỹ.