# Ví dụ

---

# Kịch bản 01 · Tiếp diễn xu hướng tăng

## Không gian kịch bản

- Xác suất suy luận: **72%**
- Xác suất hiệu chỉnh: **79%**

↓

## Phương án hiện tại

### Phương án A

- Vùng vào lệnh: Pullback về vùng POC.
- Điểm dừng lỗ: Dưới VAL.
- Điểm chốt lời: VAH.
- Tỷ lệ Lợi nhuận / Rủi ro: **2.8 : 1**
- Quy mô vị thế: **1.0R**

↓

### Tri thức tích luỹ

Tra cứu theo Chữ ký tín hiệu:

- Trường hợp: **43**
- Mẫu: **7**
- Bài học tích luỹ:
  - Các trường hợp tương tự thường hiệu quả hơn khi giảm quy mô vị thế.
- Thống kê:
  - Quy mô vị thế **0.8R** có kết quả ổn định hơn.

↓

### Sau hiệu chỉnh

- Phương án: **Giữ nguyên**
- Quy mô vị thế: **0.8R**

↓

### Quan sát

- Giá Pullback về vùng POC.
- Auction Flow cải thiện.
- CVD phục hồi.
- Chưa xuất hiện tín hiệu xác nhận cuối cùng.

↓

### Mức độ xác nhận

**PROBE**

↓

### Thực thi

Điều kiện thực thi được đáp ứng.

- Vào lệnh với quy mô **0.8R**.
- Quản trị vị thế theo kế hoạch.
- Khi các điều kiện xác nhận hoàn tất, tiếp tục quản trị theo phương án.
- Chốt lời tại VAH hoặc dừng lỗ nếu phương án mất hiệu lực.

---

# Kịch bản 02 · Mở rộng vùng tích luỹ

## Không gian kịch bản

- Xác suất suy luận: **24%**
- Xác suất hiệu chỉnh: **24%**

↓

## Phương án hiện tại

### Phương án A

- Chờ phá vỡ vùng giá trị.
- Chưa vào lệnh.

↓

### Tri thức tích luỹ

Tra cứu theo Chữ ký tín hiệu:

- Trường hợp: **0**
- Mẫu: **0**
- Bài học tích luỹ: **Chưa có**
- Thống kê: **Chưa có**

↓

### Sau hiệu chỉnh

- Phương án: **Giữ nguyên**

↓

### Quan sát

Các điều kiện thực thi chưa hình thành.

↓

### Mức độ xác nhận

**WATCH**

↓

### Thực thi

Tiếp tục theo dõi điều kiện thực thi.

Chưa thực hiện vào lệnh.

---

# Kịch bản 03 · Đảo chiều xu hướng giảm

## Không gian kịch bản

- Xác suất suy luận: **38%**
- Xác suất hiệu chỉnh: **29%**

↓

## Phương án hiện tại

### Phương án A

- Vào lệnh sau khi xác nhận phá vỡ.
- Điểm dừng lỗ: Trên đỉnh gần nhất.
- Quy mô vị thế: **1.0R**

↓

### Tri thức tích luỹ

Tra cứu theo Chữ ký tín hiệu:

- Trường hợp: **15**
- Mẫu: **3**
- Bài học tích luỹ:
  - Các trường hợp tương tự thường xuất hiện False Break.
- Thống kê:
  - Quy mô vị thế **0.5R** có kết quả ổn định hơn.

↓

### Sau hiệu chỉnh

- Quy mô vị thế: **0.5R**
- Phương án: **Giữ nguyên**

↓

### Quan sát

- Breakout đã được xác nhận.
- Volume mở rộng.
- Auction Flow xác nhận.
- Điều kiện thực thi đầy đủ.

↓

### Mức độ xác nhận

**CONFIRM**

↓

### Thực thi

Điều kiện thực thi và điều kiện xác nhận được đáp ứng.

- Vào lệnh với quy mô **0.5R**.
- Quản trị vị thế theo kế hoạch.
- Kết thúc phương án theo điểm chốt lời hoặc điều kiện vô hiệu.

---

# Nguyên tắc

Không gian kịch bản hình thành Xác suất suy luận.

Tri thức tích luỹ được tham khảo:

- Ở tầng Không gian kịch bản để hiệu chỉnh Xác suất suy luận.
- Ở tầng Kế hoạch thực thi để hiệu chỉnh các phương án đã tồn tại.

Nếu chưa có đủ dữ liệu, Xác suất hiệu chỉnh bằng Xác suất suy luận.

Mức độ xác nhận phản ánh chất lượng của các bằng chứng hiện tại.

Mức độ xác nhận được sử dụng để điều chỉnh mức độ cam kết và quy mô thực thi của cùng một phương án.

Khi các điều kiện thực thi và điều kiện xác nhận được đáp ứng, phương án tương ứng được thực hiện.

---

# Triết lý

Xác suất suy luận phản ánh kết quả của Hệ thống suy luận.

Xác suất hiệu chỉnh phản ánh kết quả sau khi tham khảo Tri thức tích luỹ.

Mức độ xác nhận phản ánh chất lượng của các bằng chứng hiện tại.

Thực thi biến phương án thành hành động.

Thực tế kiểm chứng giá trị của mọi hành động.