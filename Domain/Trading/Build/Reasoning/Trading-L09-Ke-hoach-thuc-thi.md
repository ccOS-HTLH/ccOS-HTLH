# 09 · Kế hoạch thực thi

> Thiết kế các phương án thực thi cho từng kịch bản.

---

# Mục đích

Kế hoạch thực thi là tầng thứ chín của Hệ thống suy luận.

Tầng này xây dựng các phương án thực thi cho từng kịch bản.

Không gian kịch bản cung cấp các kịch bản hiện tại.

Chữ ký tín hiệu được sử dụng để tham khảo Tri thức tích luỹ nhằm lựa chọn những phương án đã được kiểm chứng (nếu có).

Mỗi phương án xác định:

- Điều kiện thực thi.
- Điều kiện xác nhận.
- Điều kiện hủy bỏ.
- Quản trị rủi ro.
- Quản trị vị thế.

---

# Câu hỏi

## Nếu kịch bản này xảy ra, mình nên hành động như thế nào?

→ Không gian kịch bản.

---

## Theo kinh nghiệm đã được tích luỹ, phương án nào đáng tin cậy hơn?

→ Chữ ký tín hiệu + Tri thức tích luỹ.

---

# Đầu vào

- Không gian kịch bản.
- Chữ ký tín hiệu.

---

# Đầu ra

Các phương án thực thi.

Các phương án thực thi trở thành đầu vào của tầng Phản hồi thực tế.

---

# Vai trò trong Hệ thống suy luận

```text
# Không gian kịch bản
        │
        ├────────► Tham khảo # Tri thức tích luỹ
        ▼
# Kế hoạch thực thi

↓

# Phản hồi thực tế
```

---

# Cấu trúc

```text
# 01 · Định nghĩa

↓

# 02 · Quan sát

↓

# 03 · Phương án

↓

# 04 · Hiệu chỉnh

↓

# 05 · Ví dụ
```

---

# Triết lý

Không gian kịch bản xác định khả năng.

Kinh nghiệm giúp lựa chọn phương án thực thi phù hợp nhất.

---

# Định nghĩa

> Bản chất của Kế hoạch thực thi.

---

# Bản chất

Kế hoạch thực thi thiết kế các phương án thực thi cho từng kịch bản.

Kế hoạch thực thi không lựa chọn kịch bản.

Kế hoạch thực thi chuẩn bị các phương án thực thi cho những kịch bản có thể xảy ra.

Sau khi các phương án được hình thành, Tri thức tích luỹ có thể được tham khảo để hiệu chỉnh mức độ phù hợp của từng phương án.

---

# Thành phần

Một phương án thực thi bao gồm:

- Vùng vào lệnh.
- Điều kiện xác nhận.
- Điều kiện vô hiệu.
- Điểm dừng lỗ.
- Điểm chốt lời.
- Quy mô vị thế.
- Tỷ lệ lợi nhuận / rủi ro.
- Quản trị vị thế.

---

# Mục tiêu

- Chuẩn bị.
- Chuẩn hóa.
- Lập phương án.

---

# Đầu ra

Tầng Kế hoạch thực thi tạo ra các phương án thực thi.

Các phương án thực thi trở thành đầu vào của tầng Phản hồi thực tế.

---

# Triết lý

Một phương án tốt tạo nên một quá trình thực thi nhất quán.

---

# Quan sát

> Quan sát các phương án thực thi của từng kịch bản.

---

# Mục đích

Quan sát các phương án thực thi được xây dựng cho từng kịch bản.

Quan sát những điều kiện cần có trước khi thực thi.

---

# Quan sát

- Vùng vào lệnh.
- Điều kiện xác nhận.
- Thanh khoản mục tiêu.
- Mức độ rủi ro.
- Mục tiêu lợi nhuận.
- Điều kiện vô hiệu.
- Thời điểm thực thi.
- Chi phí thực thi.

---

# Nguyên tắc

Mỗi kịch bản có thể có một hoặc nhiều phương án thực thi.

Mỗi phương án có các điều kiện thực thi riêng.

Tri thức tích luỹ có thể được tham khảo để đánh giá và hiệu chỉnh mức độ phù hợp của từng phương án.

Chỉ thực thi khi các điều kiện đã được xác nhận.

---

# Triết lý

Phương án phản ánh cách thực thi của từng kịch bản.

Chuẩn bị trước giúp quá trình thực thi nhất quán hơn.

---

# Phương án

> Mô tả cấu trúc của một phương án thực thi.

---

# Mục đích

Phương án mô tả cách thực thi cho một kịch bản cụ thể.

Một kịch bản có thể có một hoặc nhiều phương án thực thi.

---

# Thành phần

Một phương án bao gồm:

- Vùng vào lệnh.
- Điều kiện xác nhận.
- Điều kiện vô hiệu.
- Điểm dừng lỗ.
- Điểm chốt lời.
- Quy mô vị thế.
- Tỷ lệ lợi nhuận / rủi ro.
- Quản trị vị thế.

---

# Nguyên tắc

Mỗi phương án được xây dựng cho một kịch bản cụ thể.

Một kịch bản có thể có nhiều phương án thực thi.

Các phương án có thể khác nhau về mức độ rủi ro, lợi nhuận kỳ vọng hoặc cách quản trị vị thế.

Không có phương án nào được xem là tuyệt đối.

---

# Vai trò

Phương án là đơn vị cơ bản của Kế hoạch thực thi.

Nhiều phương án kết hợp tạo thành Kế hoạch thực thi.

---

# Triết lý

Một phương án không đảm bảo kết quả.

Một phương án chỉ chuẩn bị cách hành động phù hợp cho từng kịch bản.

---

# Hiệu chỉnh

> Hiệu chỉnh các phương án bằng dữ liệu tham khảo từ Tri thức tích luỹ.

---

# Mục đích

Hiệu chỉnh giúp Kế hoạch thực thi tham khảo kinh nghiệm đã được tích luỹ.

Sau khi các phương án được xây dựng từ Không gian kịch bản, Chữ ký tín hiệu được sử dụng để tra cứu Tri thức tích luỹ.

Nếu tồn tại đủ dữ liệu đáng tin cậy, Kế hoạch thực thi có thể hiệu chỉnh mức độ phù hợp của từng phương án.

---

# Hiệu chỉnh

Kế hoạch thực thi có thể hiệu chỉnh:

- Mức độ ưu tiên của phương án.
- Mức độ phù hợp của phương án.
- Quy mô vị thế.
- Quản trị vị thế.
- Tỷ lệ lợi nhuận / rủi ro.

Điều kiện thực thi không thay đổi.

Điều kiện xác nhận không thay đổi.

Điều kiện vô hiệu không thay đổi.

---

# Nguyên tắc

Các phương án luôn được xây dựng từ Không gian kịch bản.

Tri thức tích luỹ chỉ được tham khảo sau khi các phương án đã được hình thành.

Nếu chưa đủ dữ liệu, Kế hoạch thực thi giữ nguyên phương án hiện tại.

Nếu đã có đủ dữ liệu đáng tin cậy, Kế hoạch thực thi tham khảo Tri thức tích luỹ để hiệu chỉnh mức độ phù hợp của từng phương án.

Tri thức tích luỹ không tạo ra phương án mới.

Tri thức tích luỹ chỉ cung cấp dữ liệu tham khảo.

---

# Triết lý

Không gian kịch bản hình thành các phương án.

Kinh nghiệm giúp lựa chọn và hiệu chỉnh phương án phù hợp hơn.

---

# Ví dụ

---

# Kịch bản 01 · Tiếp diễn xu hướng tăng

## Phương án hiện tại

### Phương án A

- Vùng vào lệnh: Pullback về vùng POC.
- Điểm dừng lỗ: Dưới VAL.
- Điểm chốt lời: VAH.
- Tỷ lệ Lợi nhuận / Rủi ro: **2.8 : 1**
- Quy mô vị thế: **1.0R**

↓

### Tri thức tích luỹ

- Chữ ký tín hiệu đã từng xuất hiện: **43** mẫu.
- Độ tin cậy: **Cao**.
- Quy mô vị thế tối ưu: **0.8R**.

↓

### Sau hiệu chỉnh

- Quy mô vị thế: **0.8R**
- Tỷ lệ Lợi nhuận / Rủi ro: **Giữ nguyên**
- Phương án: **Giữ nguyên**

---

# Kịch bản 02 · Mở rộng vùng tích luỹ

## Phương án hiện tại

### Phương án A

- Chờ phá vỡ vùng giá trị.
- Chưa vào lệnh.

↓

### Tri thức tích luỹ

- Chưa đủ dữ liệu.

↓

### Sau hiệu chỉnh

- Phương án giữ nguyên.

---

# Kịch bản 03 · Đảo chiều xu hướng giảm

## Phương án hiện tại

### Phương án A

- Vào lệnh sau khi xác nhận phá vỡ.
- Điểm dừng lỗ: Trên đỉnh gần nhất.
- Quy mô vị thế: **1.0R**

↓

### Tri thức tích luỹ

- Chữ ký tín hiệu đã từng xuất hiện: **15** mẫu.
- Độ tin cậy: **Trung bình**.
- Kế hoạch tương tự thường có tỷ lệ thất bại cao.

↓

### Sau hiệu chỉnh

- Quy mô vị thế: **0.5R**
- Chờ thêm xác nhận trước khi thực thi.

---

# Nguyên tắc

Các phương án luôn được xây dựng từ Không gian kịch bản.

Tri thức tích luỹ chỉ được tham khảo để hiệu chỉnh các phương án đã tồn tại.

Nếu chưa có đủ dữ liệu, Kế hoạch thực thi giữ nguyên phương án hiện tại.

---

# Triết lý

Không gian kịch bản tạo ra các phương án.

Kinh nghiệm giúp lựa chọn và hiệu chỉnh phương án phù hợp hơn.