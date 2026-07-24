# 06 · Ra quyết định

> Chuyển toàn bộ bằng chứng thành một kết luận duy nhất.

---

# Mục đích

Ra quyết định là tầng thứ sáu của Hệ thống suy luận.

Tầng này tổng hợp toàn bộ bằng chứng từ các tầng trước.

Tầng này tạo ra kết luận suy luận tại thời điểm hiện tại.

---

# Câu hỏi

Kết luận hợp lý nhất tại thời điểm hiện tại là gì?

---

# Đầu vào

- Trạng thái hành vi.
- Trạng thái bối cảnh.
- Trạng thái động lượng.
- Trạng thái cấu trúc.
- Trạng thái chất lượng.

---

# Đầu ra

Trạng thái quyết định.

Đây là đầu vào của tầng Trọng số tín hiệu.

---

# Luồng

```text
Chất lượng

↓

Ra quyết định

↓

Trọng số tín hiệu
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

Ra quyết định là điểm hội tụ của toàn bộ quá trình suy luận.

---

# Định nghĩa

> Bản chất của Ra quyết định.

---

# Bản chất

Ra quyết định là kết quả của toàn bộ quá trình suy luận.

Ra quyết định tổng hợp các bằng chứng hiện có thành một kết luận duy nhất.

Kết luận phản ánh phương án hợp lý nhất tại thời điểm hiện tại.

---

# Thành phần

Ra quyết định được hình thành từ:

- Trạng thái hành vi.
- Trạng thái bối cảnh.
- Trạng thái động lượng.
- Trạng thái cấu trúc.
- Trạng thái chất lượng.

Những thành phần này cùng tạo nên kết luận hiện tại.

---

# Đầu ra

Tầng Ra quyết định tạo ra **Trạng thái quyết định**.

Trạng thái quyết định trở thành đầu vào của tầng Trọng số tín hiệu.

---

# Triết lý

Ra quyết định phản ánh kết luận hiện tại của Hệ thống suy luận.

---

# Quan sát

> Quan sát toàn bộ kết quả suy luận trước khi tạo Ra quyết định.

---

# Mục đích

Quan sát toàn bộ kết quả từ các tầng suy luận trước đó.

Ra quyết định tổng hợp các trạng thái hiện có thành một kết luận duy nhất.

---

# Quan sát

- Trạng thái hành vi.
- Trạng thái bối cảnh.
- Trạng thái động lượng.
- Trạng thái cấu trúc.
- Trạng thái chất lượng.

---

# Nguyên tắc

Ra quyết định luôn kế thừa toàn bộ kết quả từ các tầng suy luận trước đó.

Ra quyết định không tạo thêm bằng chứng mới.

Ra quyết định phản ánh toàn bộ bằng chứng hiện có.

---

# Triết lý

Ra quyết định được xây dựng từ toàn bộ bằng chứng hiện có.

---

# Trạng thái

> Mô tả định hướng hiện tại của Hệ thống suy luận.

---

# Mục đích

Trạng thái phản ánh định hướng hiện tại của Hệ thống suy luận.

---

# Các trạng thái

### Định hướng tăng

Hệ thống suy luận ưu tiên kịch bản tăng.

---

### Định hướng giảm

Hệ thống suy luận ưu tiên kịch bản giảm.

---

### Trung lập

Hệ thống suy luận chưa ưu tiên kịch bản nào.

Tiếp tục quan sát.

---

### Chưa đủ cơ sở

Các bằng chứng hiện tại chưa đủ để hình thành một định hướng đáng tin cậy.

---

# Nguyên tắc

Ra quyết định chỉ có một trạng thái tại một thời điểm.

Trạng thái thay đổi khi bằng chứng thay đổi.

Ra quyết định luôn kế thừa toàn bộ kết quả từ các tầng suy luận trước đó.

---

# Triết lý

Trạng thái phản ánh định hướng hiện tại của Hệ thống suy luận.

---

# Chuyển đổi

> Mô tả sự thay đổi của Ra quyết định theo thời gian.

---

# Mục đích

Chuyển đổi mô tả sự thay đổi của định hướng khi hệ thống bằng chứng thay đổi.

---

# Ví dụ

```text
Trung lập

↓

Định hướng tăng
```

---

```text
Định hướng tăng

↓

Trung lập
```

---

```text
Định hướng tăng

↓

Định hướng giảm
```

---

```text
Chưa đủ cơ sở

↓

Trung lập

↓

Định hướng tăng
```

---

# Nguyên tắc

Ra quyết định thay đổi khi hệ thống bằng chứng thay đổi.

Trạng thái chỉ chuyển đổi khi kết luận của Hệ thống suy luận thay đổi.

Ra quyết định luôn kế thừa kết quả từ các tầng suy luận trước đó.

---

# Triết lý

Chuyển đổi phản ánh sự thay đổi của định hướng.

---

# Ví dụ

---

# Ví dụ 01

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
- Xác nhận cấu trúc: Acceptance.
- Kết quả vận động: Continuation.

### Trạng thái chất lượng

- Rất cao.

↓

## Trạng thái quyết định

- Định hướng tăng.

---

# Ví dụ 02

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
- Xác nhận cấu trúc: Acceptance.
- Kết quả vận động: Continuation.

### Trạng thái chất lượng

- Trung bình.

↓

## Trạng thái quyết định

- Trung lập.

---

# Ví dụ 03

## Đầu vào

### Trạng thái hành vi

- Người bán chiếm ưu thế.

### Trạng thái bối cảnh

- Xu hướng giảm.

### Trạng thái động lượng

- Hướng của lực: Ưu thế bán.
- Mức độ thay đổi: Gia tăng.
- Quan hệ giữa lực và giá: Đồng thuận.

### Trạng thái cấu trúc

- Hình thái cấu trúc: Xu hướng giảm.
- Xác nhận cấu trúc: Acceptance.
- Kết quả vận động: Continuation.

### Trạng thái chất lượng

- Rất cao.

↓

## Trạng thái quyết định

- Định hướng giảm.

---

# Ví dụ 04

## Đầu vào

### Trạng thái chất lượng

- Thấp.

↓

## Trạng thái quyết định

- Chưa đủ cơ sở.

---

# Nguyên tắc

Ra quyết định luôn được xây dựng từ toàn bộ kết quả của các tầng suy luận trước đó.

Ra quyết định chỉ phản ánh kết luận hợp lý nhất tại thời điểm hiện tại.

---

# Triết lý

Ra quyết định phản ánh kết luận hiện tại của Hệ thống suy luận.