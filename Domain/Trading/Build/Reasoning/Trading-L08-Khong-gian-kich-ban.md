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

---

# Định nghĩa

> Bản chất của Không gian kịch bản.

---

# Bản chất

Không gian kịch bản biểu diễn các khả năng đang tồn tại.

Mỗi kịch bản đại diện cho một khả năng phát triển hợp lý của thị trường.

Không gian kịch bản không khẳng định một tương lai duy nhất.

Không gian kịch bản tổ chức các khả năng hợp lý dựa trên kết quả suy luận hiện tại.

Sau khi các kịch bản được hình thành, Không gian kịch bản có thể tham khảo Tri thức tích luỹ để hiệu chỉnh mức độ tin cậy của từng kịch bản.

---

# Thành phần

Một kịch bản bao gồm:

- Suy luận.
- Điều kiện.
- Xác suất suy luận.
- Xác suất hiệu chỉnh.
- Điều kiện vô hiệu.
- Kết quả kỳ vọng.

---

# Mục tiêu

- Tổ chức.
- Ước lượng.
- Hiệu chỉnh.

---

# Đầu ra

Tầng Không gian kịch bản tạo ra tập các kịch bản hiện tại.

Mỗi kịch bản bao gồm:

- Xác suất suy luận.
- Xác suất hiệu chỉnh (nếu có).

Không gian kịch bản trở thành đầu vào của tầng Kế hoạch thực thi.

---

# Triết lý

Mỗi kịch bản là một khả năng được hình thành từ kết quả suy luận hiện tại.

Kinh nghiệm giúp đánh giá và hiệu chỉnh mức độ tin cậy của từng khả năng.

---

# Quan sát

> Quan sát toàn bộ các kịch bản hợp lý tại thời điểm hiện tại.

---

# Mục đích

Quan sát toàn bộ các kịch bản hợp lý được hình thành từ kết quả suy luận hiện tại.

Quan sát mức độ ưu tiên của từng kịch bản.

Quan sát mức độ tin cậy của từng kịch bản sau khi tham khảo Tri thức tích luỹ (nếu có).

---

# Quan sát

- Suy luận.
- Điều kiện.
- Xác suất suy luận.
- Xác suất hiệu chỉnh.
- Mức độ ưu tiên.
- Đồng thuận.
- Xung đột.
- Điều kiện vô hiệu.

---

# Nguyên tắc

Nhiều kịch bản có thể cùng tồn tại.

Mỗi kịch bản có Suy luận, Điều kiện và Xác suất suy luận riêng.

Mức độ ưu tiên của các kịch bản được hình thành từ kết quả suy luận hiện tại.

Không gian kịch bản có thể tham khảo Tri thức tích luỹ để hiệu chỉnh mức độ tin cậy của các kịch bản khi đã có đủ dữ liệu.

Không gian kịch bản thay đổi khi kết quả suy luận hoặc Tri thức tích luỹ thay đổi.

---

# Triết lý

Thị trường luôn tồn tại nhiều kịch bản đồng thời.

Kết quả suy luận hình thành các kịch bản.

Kinh nghiệm giúp đánh giá và hiệu chỉnh mức độ tin cậy của các kịch bản.

---

# Kịch bản

> Mô tả cấu trúc của một kịch bản.

---

# Mục đích

Kịch bản mô tả một khả năng phát triển hợp lý của thị trường.

Mỗi kịch bản được hình thành từ kết quả suy luận hiện tại.

---

# Thành phần

Một kịch bản bao gồm:

- Suy luận.
- Điều kiện.
- Xác suất suy luận.
- Xác suất hiệu chỉnh.
- Điều kiện vô hiệu.
- Kết quả kỳ vọng.

---

# Nguyên tắc

Mỗi kịch bản được hình thành từ cùng một kết quả suy luận.

Các kịch bản có thể cùng tồn tại.

Mỗi kịch bản có Suy luận, Điều kiện và Xác suất suy luận riêng.

Xác suất hiệu chỉnh chỉ xuất hiện khi có đủ dữ liệu tham khảo từ Tri thức tích luỹ.

Không có kịch bản nào được xem là chắc chắn.

---

# Vai trò

Kịch bản là đơn vị cơ bản của Không gian kịch bản.

Nhiều kịch bản kết hợp tạo thành Không gian kịch bản.

---

# Triết lý

Một kịch bản không dự đoán tương lai.

Một kịch bản chỉ biểu diễn một khả năng hợp lý.

---

# Hiệu chỉnh

> Hiệu chỉnh các kịch bản bằng dữ liệu tham khảo từ Tri thức tích luỹ.

---

# Mục đích

Hiệu chỉnh giúp Không gian kịch bản tham khảo kinh nghiệm đã được tích luỹ.

Sau khi các kịch bản được hình thành từ kết quả suy luận hiện tại, Chữ ký tín hiệu được sử dụng để tra cứu Tri thức tích luỹ.

Nếu tồn tại đủ dữ liệu đáng tin cậy, Không gian kịch bản có thể hiệu chỉnh mức độ tin cậy của các kịch bản.

---

# Hiệu chỉnh

Không gian kịch bản có thể hiệu chỉnh:

- Xác suất hiệu chỉnh.
- Mức độ ưu tiên.
- Kết quả kỳ vọng.

Suy luận không thay đổi.

Điều kiện không thay đổi.

Điều kiện vô hiệu không thay đổi.

---

# Nguyên tắc

Các kịch bản luôn được hình thành từ kết quả suy luận hiện tại.

Tri thức tích luỹ chỉ được tham khảo sau khi các kịch bản đã được hình thành.

Nếu chưa đủ dữ liệu, Không gian kịch bản giữ nguyên xác suất suy luận.

Nếu đã có đủ dữ liệu đáng tin cậy, Không gian kịch bản tham khảo Tri thức tích luỹ để hiệu chỉnh mức độ tin cậy của các kịch bản.

Tri thức tích luỹ không tạo ra kịch bản mới.

Tri thức tích luỹ chỉ cung cấp dữ liệu tham khảo.

---

# Triết lý

Kết quả suy luận hiện tại hình thành các kịch bản.

Kinh nghiệm giúp đánh giá và hiệu chỉnh mức độ tin cậy của các kịch bản.

---

# Ví dụ

---

# Kịch bản 01 · Tiếp diễn xu hướng tăng

## Kết quả suy luận hiện tại

### Xác suất suy luận

**72%**

### Điều kiện

- Hành vi: Người mua chiếm ưu thế.
- Động lượng: Gia tăng.
- Cấu trúc: Tiếp diễn xu hướng tăng.

### Điều kiện vô hiệu

- Giá mất vùng POC.

↓

### Tri thức tích luỹ

- Chữ ký tín hiệu đã từng xuất hiện: **43** mẫu.
- Độ tin cậy: **Cao**.

↓

### Sau hiệu chỉnh

#### Xác suất hiệu chỉnh

**76%**

---

# Kịch bản 02 · Mở rộng vùng tích luỹ

## Kết quả suy luận hiện tại

### Xác suất suy luận

**18%**

### Điều kiện

- Động lượng suy yếu.
- Khối lượng cân bằng.

### Điều kiện vô hiệu

- Giá phá vỡ hoàn toàn khỏi vùng giá trị.

↓

### Tri thức tích luỹ

- Chưa đủ dữ liệu.

↓

### Sau hiệu chỉnh

#### Xác suất hiệu chỉnh

Không thay đổi.

---

# Kịch bản 03 · Đảo chiều xu hướng giảm

## Kết quả suy luận hiện tại

### Xác suất suy luận

**10%**

### Điều kiện

- Động lượng đảo chiều.
- Cấu trúc: Xác nhận xu hướng giảm.

### Điều kiện vô hiệu

- Giá tạo đỉnh cao hơn mới.

↓

### Tri thức tích luỹ

- Chữ ký tín hiệu đã từng xuất hiện: **15** mẫu.
- Độ tin cậy: **Trung bình**.

↓

### Sau hiệu chỉnh

#### Xác suất hiệu chỉnh

**6%**

---

# Nguyên tắc

Các kịch bản luôn được hình thành từ kết quả suy luận hiện tại.

Không gian kịch bản chỉ tham khảo Tri thức tích luỹ sau khi các kịch bản đã được hình thành.

Nếu chưa có đủ dữ liệu, Xác suất hiệu chỉnh giữ nguyên Xác suất suy luận.

---

# Triết lý

Kết quả suy luận hiện tại hình thành các kịch bản.

Kinh nghiệm giúp đánh giá và hiệu chỉnh mức độ tin cậy của các kịch bản.