# Thống kê

> Dữ liệu định lượng của Bộ nhớ.

Thống kê tổng hợp dữ liệu lịch sử từ các Trường hợp đã được kiểm chứng.

Thống kê mô tả tần suất, xác suất và xu hướng của các đối tượng trong Bộ nhớ.

Thống kê không tạo ra quy luật.

Thống kê chỉ phản ánh dữ liệu lịch sử.

---

# Vai trò

Thống kê cung cấp góc nhìn định lượng cho Tri thức tích luỹ.

Từ Thống kê, Tri thức tích luỹ có thể:

- Đánh giá tần suất xuất hiện.
- Ước lượng xác suất lịch sử.
- So sánh hiệu quả giữa các phương án.
- Theo dõi sự thay đổi theo thời gian.

Thống kê hỗ trợ Hệ thống suy luận tham khảo dữ liệu lịch sử.

---

# Khi nào tạo?

Một Thống kê được tạo khi:

- Đã có đủ Trường hợp được kiểm chứng.
- Có dữ liệu cần tổng hợp hoặc định lượng.
- Có đối tượng cần theo dõi theo thời gian.

Thống kê được cập nhật khi xuất hiện thêm dữ liệu mới.

---

# Vòng đời

```text
Nhiều Trường hợp

↓

Tổng hợp dữ liệu

↓

Tính toán

↓

Cập nhật Thống kê

↓

Tham khảo trong các lần suy luận sau
```

---

# Liên kết dữ liệu

Một Thống kê có thể liên kết với:

- Một hoặc nhiều Trường hợp.
- Một hoặc nhiều Mẫu.

Thống kê không trực tiếp tạo Bài học tích luỹ.

Mọi Thống kê đều phải truy xuất được về các Trường hợp đã sử dụng để tính toán.

---

# Quy tắc

- Mỗi Thống kê có một mã định danh duy nhất.
- Một tệp chỉ lưu một Thống kê.
- Mọi Thống kê đều phải có dữ liệu nguồn.
- Thống kê có thể được cập nhật khi xuất hiện thêm dữ liệu mới.
- Không sử dụng Thống kê để thay thế Thực tế.

---

# Quy ước định danh

```text
TK-0001
TK-0002
TK-0003
...
```

---

# Triết lý

Thống kê phản ánh lịch sử.

Lịch sử không đảm bảo tương lai.

Thống kê hỗ trợ đánh giá xác suất.

Mọi Thống kê đều phải truy xuất được về Thực tế.