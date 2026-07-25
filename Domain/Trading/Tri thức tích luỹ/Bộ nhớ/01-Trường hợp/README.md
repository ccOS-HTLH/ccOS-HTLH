# Trường hợp

> Dữ liệu gốc của Bộ nhớ.

Trường hợp ghi lại một lần quan sát hoàn chỉnh của thị trường.

Mỗi Trường hợp phản ánh một diễn biến thực tế tại một thời điểm cụ thể.

Trường hợp không đại diện cho một quy luật.

Trường hợp chỉ lưu giữ dữ liệu đã được kiểm chứng từ Thực tế.

---

# Vai trò

Trường hợp là đơn vị dữ liệu cơ bản của Bộ nhớ.

Từ một hoặc nhiều Trường hợp, Tri thức tích luỹ có thể:

- Nhận diện Mẫu.
- Rút ra Bài học tích luỹ.
- Cập nhật Thống kê.

Mọi dữ liệu trong Bộ nhớ đều bắt nguồn từ Trường hợp.

---

# Khi nào tạo?

Một Trường hợp được tạo khi:

- Quá trình phân tích hoàn tất.
- Kế hoạch thực thi kết thúc.
- Kết quả thực tế đã rõ ràng.
- Tầng Phản hồi thực tế hoàn tất.

Không tạo Trường hợp khi diễn biến vẫn đang xảy ra.

---

# Vòng đời

```text
Thực tế

↓

Quan sát

↓

Phân tích

↓

Thực thi

↓

Phản hồi thực tế

↓

Tạo Trường hợp

↓

Nhận diện Mẫu

↓

Rút ra Bài học tích luỹ

↓

Cập nhật Thống kê
```

---

# Liên kết dữ liệu

Một Trường hợp có thể liên kết với:

- Chữ ký tín hiệu.
- Một hoặc nhiều Mẫu.
- Một hoặc nhiều Bài học tích luỹ.

Trường hợp không trực tiếp tạo Thống kê.

Thống kê được Tri thức tích luỹ cập nhật từ nhiều Trường hợp.

---

# Quy tắc

- Mỗi Trường hợp có một mã định danh duy nhất.
- Một tệp chỉ lưu một Trường hợp.
- Trường hợp là dữ liệu lịch sử.
- Không chỉnh sửa nội dung sau khi hoàn tất, ngoại trừ việc sửa lỗi ghi chép.
- Không bổ sung nhận định hoặc suy luận mới sau khi Trường hợp đã được lưu.

---

# Quy ước định danh

```text
TH-0001
TH-0002
TH-0003
...
```

---

# Triết lý

Một Trường hợp không chứng minh điều gì.

Nhiều Trường hợp mới có thể hình thành một Mẫu.

Mọi Mẫu đều bắt đầu từ Trường hợp.

Mọi kinh nghiệm đều bắt đầu từ Thực tế.