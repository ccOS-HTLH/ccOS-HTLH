# 05 · Chất lượng

> Đánh giá độ tin cậy của các bằng chứng suy luận.

---

# Mục đích

Chất lượng là tầng thứ năm của Hệ thống suy luận.

Tầng này đánh giá mức độ nhất quán giữa các bằng chứng đã được hình thành.

Tầng này không tạo thêm bằng chứng.

Tầng này đánh giá chất lượng của các bằng chứng hiện có.

---

# Câu hỏi

Các bằng chứng hiện tại đáng tin cậy đến mức nào?

---

# Đầu vào

- Trạng thái hành vi.
- Trạng thái bối cảnh.
- Trạng thái động lượng.
- Trạng thái cấu trúc.

---

# Đầu ra

Trạng thái chất lượng.

Đây là đầu vào của tầng Ra quyết định.

---

# Luồng

```text
Cấu trúc

↓

Chất lượng

↓

Ra quyết định
```

---

# Cấu trúc

```text
01 · Định nghĩa

↓

02 · Quan sát

↓

03 · Trạng thái

↓

04 · Chuyển đổi

↓

05 · Ví dụ
```

---

# Triết lý

Chất lượng của quyết định bắt đầu từ chất lượng của bằng chứng.

---

# Định nghĩa

> Bản chất của Chất lượng.

---

# Bản chất

Chất lượng phản ánh mức độ tin cậy của các bằng chứng hiện có.

Chất lượng được hình thành từ mức độ đồng thuận giữa các tầng suy luận trước đó.

Chất lượng không tạo ra bằng chứng mới.

---

# Thành phần

Chất lượng được đánh giá thông qua:

- Mức độ đồng thuận của Hành vi.
- Mức độ đồng thuận của Bối cảnh.
- Mức độ đồng thuận của Động lượng.
- Mức độ đồng thuận của Cấu trúc.
- Mức độ đồng thuận đa khung thời gian.
- Môi trường rủi ro.

Những thành phần này cùng phản ánh độ tin cậy của hệ thống bằng chứng.

---

# Đầu ra

Tầng Chất lượng tạo ra **Trạng thái chất lượng**.

Trạng thái chất lượng trở thành đầu vào của tầng Ra quyết định.

---

# Triết lý

Chất lượng phản ánh độ tin cậy của các bằng chứng hiện có.

---

# Quan sát

> Quan sát mức độ nhất quán của hệ thống bằng chứng.

---

# Mục đích

Quan sát mức độ nhất quán giữa các bằng chứng hiện có.

Chất lượng phản ánh mức độ đồng thuận của toàn bộ hệ thống suy luận.

---

# Quan sát

## Mức độ đồng thuận

- Đồng thuận của Hành vi.
- Đồng thuận của Bối cảnh.
- Đồng thuận của Động lượng.
- Đồng thuận của Cấu trúc.
- Đồng thuận đa khung thời gian.

---

## Môi trường

- Môi trường rủi ro.

---

## Quan hệ giữa các tầng

- Xác nhận.
- Xung đột.

---

# Nguyên tắc

Sự đồng thuận làm tăng độ tin cậy.

Sự xung đột làm giảm độ tin cậy.

Chất lượng luôn được đánh giá trên các bằng chứng hiện có.

---

# Triết lý

Chất lượng phản ánh mức độ tin cậy của hệ thống bằng chứng.

---

# Trạng thái

> Mô tả mức độ tin cậy hiện tại của hệ thống bằng chứng.

---

# Mục đích

Trạng thái phản ánh mức độ tin cậy hiện tại của hệ thống bằng chứng.

---

# Các trạng thái

### Rất cao

Các bằng chứng đồng thuận rất mạnh.

---

### Cao

Các bằng chứng đồng thuận rõ ràng.

---

### Trung bình

Các bằng chứng đã hình thành sự đồng thuận nhưng vẫn còn thiếu xác nhận.

---

### Thấp

Các bằng chứng xuất hiện nhiều xung đột.

---

### Không hợp lệ

Các bằng chứng chưa đủ điều kiện để đưa ra quyết định.

---

# Nguyên tắc

Trạng thái phản ánh mức độ tin cậy hiện tại của hệ thống bằng chứng.

Trạng thái thay đổi khi mức độ đồng thuận giữa các bằng chứng thay đổi.

---

# Triết lý

Trạng thái phản ánh mức độ tin cậy của hệ thống bằng chứng.

---

# Chuyển đổi

> Mô tả sự thay đổi của Chất lượng theo thời gian.

---

# Mục đích

Chuyển đổi mô tả sự thay đổi của mức độ tin cậy của hệ thống bằng chứng.

---

# Ví dụ

```text
Trung bình

↓

Cao

↓

Rất cao
```

---

```text
Rất cao

↓

Cao

↓

Trung bình
```

---

```text
Trung bình

↓

Thấp

↓

Không hợp lệ
```

---

# Nguyên tắc

Chất lượng thay đổi khi mức độ đồng thuận giữa các bằng chứng thay đổi.

Trạng thái chỉ chuyển đổi khi chất lượng của hệ thống bằng chứng thay đổi.

Sự đồng thuận làm tăng độ tin cậy.

Sự xung đột làm giảm độ tin cậy.

---

# Triết lý

Chuyển đổi phản ánh sự thay đổi của Chất lượng.

---

# Ví dụ

---

# Ví dụ 01 · Rất cao

## Đầu vào

### Trạng thái hành vi

- Người mua chiếm ưu thế.

### Trạng thái bối cảnh

- Xu hướng tăng.

### Trạng thái động lượng

- Hướng của lực: Ưu thế mua.
- Mức độ thay đổi: Gia tăng.
- Quan hệ giữa lực và giá: Đồng thuận.

### Trạng thái cấu trúc

- Hình thái cấu trúc: Xu hướng tăng.
- Sự kiện trên cấu trúc: Tiếp diễn.
- Phản ứng của cấu trúc: Acceptance.
- Kết quả của cấu trúc: Continuation.

↓

## Trạng thái chất lượng

- Rất cao.

---

# Ví dụ 02 · Trung bình

## Đầu vào

### Trạng thái hành vi

- Người mua chiếm ưu thế.

### Trạng thái bối cảnh

- Xu hướng tăng.

### Trạng thái động lượng

- Hướng của lực: Ưu thế bán.
- Mức độ thay đổi: Gia tăng.
- Quan hệ giữa lực và giá: Phân kỳ.

### Trạng thái cấu trúc

- Hình thái cấu trúc: Xu hướng tăng.
- Sự kiện trên cấu trúc: Tiếp diễn.
- Phản ứng của cấu trúc: Acceptance.
- Kết quả của cấu trúc: Continuation.

↓

## Trạng thái chất lượng

- Trung bình.

---

# Ví dụ 03 · Thấp

## Đầu vào

### Trạng thái hành vi

- Người bán chiếm ưu thế.

### Trạng thái bối cảnh

- Xu hướng tăng.

### Trạng thái động lượng

- Hướng của lực: Ưu thế mua.
- Mức độ thay đổi: Gia tăng.
- Quan hệ giữa lực và giá: Đồng thuận.

### Trạng thái cấu trúc

- Hình thái cấu trúc: Đi ngang.
- Sự kiện trên cấu trúc: Thất bại.
- Phản ứng của cấu trúc: Rejection.
- Kết quả của cấu trúc: Failure.

↓

## Trạng thái chất lượng

- Thấp.

---

# Nguyên tắc

Chất lượng phản ánh mức độ đồng thuận giữa các bằng chứng.

Một tầng mạnh không đủ tạo nên Chất lượng cao.

Chất lượng cao chỉ xuất hiện khi các tầng cùng hướng tới một kết luận.

---

# Triết lý

Chất lượng phản ánh mức độ tin cậy của hệ thống bằng chứng.