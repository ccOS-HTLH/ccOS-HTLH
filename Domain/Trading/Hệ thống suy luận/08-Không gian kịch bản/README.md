# 08 · Không gian kịch bản

> Biểu diễn sự bất định bằng các kịch bản.

---

# Mục đích

Không gian kịch bản là tầng thứ tám của Hệ thống suy luận.

Tầng này tổ chức các kịch bản hợp lý từ Trạng thái quyết định hiện tại.

Trọng số tín hiệu được sử dụng để hình thành các kịch bản và xác suất suy luận.

Sau khi các kịch bản được hình thành, Chữ ký tín hiệu được sử dụng để tham khảo Tri thức tích luỹ nhằm đánh giá và hiệu chỉnh mức độ tin cậy của từng kịch bản.

Mỗi kịch bản được mô tả thông qua:

- Suy luận.
- Điều kiện.
- Xác suất suy luận.
- Xác suất hiệu chỉnh.
- Điều kiện vô hiệu.

---

# Câu hỏi

## Theo kết quả suy luận hiện tại, những kịch bản nào có nhiều khả năng xảy ra?

→ Trọng số tín hiệu.

---

## Theo kinh nghiệm đã được tích luỹ, mức độ tin cậy của các kịch bản đó có thay đổi không?

→ Chữ ký tín hiệu + Tri thức tích luỹ.

---

# Đầu vào

- Trạng thái hành vi.
- Trạng thái bối cảnh.
- Trạng thái động lượng.
- Trạng thái cấu trúc.
- Trạng thái chất lượng.
- Trạng thái quyết định.
- Trọng số tín hiệu.
- Chữ ký tín hiệu.

---

# Đầu ra

Không gian kịch bản.

Mỗi kịch bản bao gồm:

- Xác suất suy luận.
- Xác suất hiệu chỉnh (nếu có).

Không gian kịch bản trở thành đầu vào của tầng Kế hoạch thực thi.

---

# Vai trò trong Hệ thống suy luận

```text
# Trọng số tín hiệu
        │
        ▼
# Không gian kịch bản
        │
        ├────────► Tham khảo # Tri thức tích luỹ
        ▼
# Kế hoạch thực thi
```

---

# Cấu trúc

```text
# 01 · Định nghĩa

↓

# 02 · Quan sát

↓

# 03 · Kịch bản

↓

# 04 · Hiệu chỉnh

↓

# 05 · Ví dụ
```

---

# Triết lý

Kết quả suy luận hiện tại hình thành các kịch bản.

Tri thức tích luỹ cung cấp kinh nghiệm để Không gian kịch bản tham khảo và hiệu chỉnh mức độ tin cậy của các kịch bản.