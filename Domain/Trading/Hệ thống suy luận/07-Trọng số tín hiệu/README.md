# 07 · Trọng số tín hiệu

> Giải thích mức độ ảnh hưởng của từng bằng chứng đến Trạng thái quyết định.

---

# Mục đích

Trọng số tín hiệu là tầng thứ bảy của Hệ thống suy luận.

Tầng này giải thích cách Trạng thái quyết định hiện tại được hình thành.

Tầng này lượng hóa mức độ ảnh hưởng của từng tầng suy luận đối với Trạng thái quyết định.

Đồng thời, tầng này chuẩn hóa toàn bộ kết quả suy luận thành một Chữ ký tín hiệu để phục vụ tầng Không gian kịch bản và Tri thức tích luỹ.

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
06 · Quyết định
        │
        ▼
07 · Trọng số tín hiệu
        │
        ▼
   Chữ ký tín hiệu
      │        │
      │        ├────────► 08 · Không gian kịch bản
      │
      └────────► Tri thức tích luỹ
                         │
                         ▼
                  Tra cứu Trường hợp
```

---

# Cấu trúc

```text
01 · Định nghĩa

↓

02 · Quan sát

↓

03 · Trọng số tín hiệu

↓

04 · Chữ ký tín hiệu

↓

05 · Ví dụ
```

---

# Triết lý

Mọi Trạng thái quyết định đều có thể được giải thích.

Trọng số tín hiệu phản ánh mức độ đóng góp của từng tầng vào Trạng thái quyết định.

Chữ ký tín hiệu chuẩn hóa toàn bộ kết quả suy luận thành một dấu vết duy nhất.

Dấu vết đó giúp Tri thức tích luỹ tra cứu các Trường hợp tương tự để tham khảo kinh nghiệm đã được tích luỹ.