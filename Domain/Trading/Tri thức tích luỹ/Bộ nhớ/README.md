# Bộ nhớ

> Kho lưu trữ kinh nghiệm của Tri thức tích luỹ.

---

# Mục đích

Bộ nhớ lưu giữ toàn bộ dữ liệu đã được Thực tế kiểm chứng.

Các dữ liệu này là cơ sở để Tri thức tích luỹ:

- Tra cứu.
- Đối chiếu.
- Tổng hợp.
- Cập nhật.

---

# Vai trò

Bộ nhớ là nơi lưu trữ và liên kết các thực thể của Tri thức tích luỹ.

Giúp:

- Quản lý dữ liệu lịch sử.
- Liên kết kinh nghiệm.
- Hỗ trợ tra cứu.
- Hỗ trợ cập nhật tri thức.

---

# Cấu trúc

```text
Bộ nhớ

├── Trường hợp
├── Mẫu
├── Bài học tích luỹ
└── Thống kê
```

---

# Thành phần

## 01-Trường hợp

Lưu trữ các Trường hợp đã được ghi nhận.

Mỗi Trường hợp ghi nhận một tình huống đã được Thực tế kiểm chứng.

---

## 02-Mẫu

Lưu trữ các Mẫu được hình thành từ nhiều Trường hợp.

Mỗi Mẫu phản ánh những đặc điểm lặp lại.

---

## 03-Bài học tích luỹ

Lưu trữ các kinh nghiệm được tổng hợp từ nhiều Mẫu và nhiều Trường hợp.

Mỗi Bài học bổ sung kinh nghiệm tham khảo cho Hệ thống suy luận tiếp theo.

---

## 04-Thống kê

Lưu trữ các kết quả thống kê được tổng hợp từ dữ liệu lịch sử.

Mỗi Thống kê giúp lượng hóa mức độ xuất hiện và hiệu quả của các trạng thái hoặc kinh nghiệm.

---

# Liên kết dữ liệu

Các thực thể được liên kết thông qua tham chiếu.

```text
Trường hợp
      │
      ▼
Mẫu
      │
      ▼
Bài học tích luỹ
      │
      ▼
Thống kê
```

Nhờ các liên kết này, Tri thức tích luỹ có thể truy vết toàn bộ quá trình hình thành kinh nghiệm.

---

# Quy ước định danh

Mỗi thực thể sử dụng một mã định danh duy nhất.

| Thực thể | Tiền tố |
|----------|---------|
| Trường hợp | TH-xxxx |
| Mẫu | M-xxxx |
| Bài học tích luỹ | BH-xxxx |
| Thống kê | TK-xxxx |

---

# Vai trò trong Tri thức tích luỹ

```text
Tra cứu

↓

Bộ nhớ

├── Trường hợp
├── Mẫu
├── Bài học tích luỹ
└── Thống kê

↓

Thông tin tham khảo
```

---

# Nguyên tắc

- Mỗi thực thể có một mã định danh duy nhất.
- Các thực thể được liên kết bằng tham chiếu.
- Dữ liệu được bổ sung theo thời gian để mở rộng kho kinh nghiệm.
- Bộ nhớ được mở rộng từ những kinh nghiệm đã được Thực tế kiểm chứng.

---

# Triết lý

Thực tế tạo nên kinh nghiệm.

Bộ nhớ lưu giữ kinh nghiệm.

Tri thức tích luỹ khai thác kinh nghiệm để hỗ trợ Hệ thống suy luận tiếp theo.