# 07 · Trọng số tín hiệu

> Giải thích mức độ ảnh hưởng của từng bằng chứng đến Trạng thái quyết định.

---

# Mục đích

Trọng số tín hiệu là tầng thứ bảy của Hệ thống suy luận.

Tầng này giải thích cách Trạng thái quyết định hiện tại được hình thành.

Tầng này lượng hóa mức độ ảnh hưởng của từng tầng suy luận đối với Trạng thái quyết định.

Đồng thời, tầng này chuẩn hóa toàn bộ kết quả suy luận thành một Chữ ký tín hiệu để phục vụ tầng Không gian kịch bản.

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

- Chữ ký tín hiệu.

Chữ ký tín hiệu trở thành đầu vào của tầng Không gian kịch bản.

---

# Vai trò trong Hệ thống suy luận

```text
Ra quyết định

↓

Trọng số tín hiệu

↓

Không gian kịch bản
```

---

# Cấu trúc

```text
01 · Định nghĩa

↓

02 · Quan sát

↓

03 · Chữ ký tín hiệu

↓

04 · Ví dụ
```

---

# Triết lý

Mọi Trạng thái quyết định đều có thể được giải thích.

Trọng số tín hiệu phản ánh mức độ đóng góp của từng tầng vào Trạng thái quyết định.

Chữ ký tín hiệu chuẩn hóa toàn bộ kết quả suy luận thành một dấu vết duy nhất.

---

# Định nghĩa

> Bản chất của Hành vi.

---

# Bản chất

Hành vi là sự biểu hiện của quá trình đấu giá giữa người mua và người bán.

Hành vi được phản ánh thông qua dữ liệu thị trường tại thời điểm quan sát.

---

# Thành phần

Hành vi được phản ánh thông qua:

- Giá
- Khối lượng
- Thời gian
- Lệnh chủ động
- Thanh khoản

Những thành phần này cùng phản ánh hành vi hiện tại của thị trường.

---

# Đầu ra

Tầng Hành vi tạo ra Trạng thái hành vi.

Trạng thái hành vi trở thành đầu vào của tầng Bối cảnh.

---

> Hành vi phản ánh điều đang thực sự diễn ra giữa người mua và người bán.

---

# Quan sát

> Quan sát sự thay đổi của lực thị trường.

---

# Mục đích

Quan sát sự thay đổi của lực thị trường.

Động lượng phản ánh sự thay đổi của lực thị trường.

---

# Quan sát

## Lực giao dịch

Quan sát phía đang chủ động tạo ra động lượng.

- Delta
- CVD
- Aggressive Orders
- Auction Flow

---

## Cường độ giao dịch

Quan sát mức độ mạnh hay yếu của lực thị trường.

- Volume
- VPIN

---

## Động lượng giá

Quan sát tốc độ thay đổi của giá.

- RSI
- Độ dốc EMA
- Price Velocity
- Momentum Divergence

---

# Nguyên tắc

Động lượng luôn được đánh giá theo sự thay đổi.

Sự thay đổi quan trọng hơn giá trị tuyệt đối.

Động lượng luôn được hiểu trong Bối cảnh hiện tại.

---

# Triết lý

Động lượng phản ánh sự thay đổi của lực.

---

# Trạng thái

> Mô tả trạng thái hiện tại của Bối cảnh.

---

# Mục đích

Trạng thái mô tả môi trường mà Hành vi đang diễn ra.

Mỗi trạng thái phản ánh điều kiện hiện tại của thị trường.

---

# Các trạng thái

## Cấu trúc thị trường

### Xu hướng tăng

Bối cảnh ưu tiên xu hướng tăng.

---

### Xu hướng giảm

Bối cảnh ưu tiên xu hướng giảm.

---

### Đi ngang

Thị trường đang ở trạng thái cân bằng.

---

## Trạng thái thị trường

### Mở rộng

Thị trường đang mở rộng khỏi vùng giá trị trước đó.

---

### Tích lũy

Thị trường đang vận động trong một vùng giá hẹp.

---

## Vùng rủi ro

### Rủi ro cao

Thị trường đang ở vùng có khả năng Chuyển đổi cao.

---

### Rủi ro thấp

Thị trường đang ở vùng thuận lợi cho xu hướng hiện tại tiếp diễn.

---

# Nguyên tắc

Trạng thái phản ánh bối cảnh hiện tại.

Trạng thái chỉ thay đổi khi bối cảnh thay đổi.

---

# Triết lý

Trạng thái phản ánh môi trường hiện tại của Hành vi.

---

# Ví dụ

---

# Ví dụ 01

## Trạng thái quyết định

- Định hướng tăng.

↓

## Trọng số tín hiệu

- Trọng số của Động lượng: **42%**
- Trọng số của Bối cảnh: **28%**
- Trọng số của Cấu trúc: **16%**
- Trọng số của Hành vi: **9%**
- Trọng số của Chất lượng: **5%**

↓

## Chữ ký tín hiệu

```text
SIG-8A24
```

---

# Ví dụ 02

## Trạng thái quyết định

- Trung lập.

↓

## Trọng số tín hiệu

- Trọng số của Bối cảnh: **31%**
- Trọng số của Cấu trúc: **24%**
- Trọng số của Động lượng: **22%**
- Trọng số của Hành vi: **14%**
- Trọng số của Chất lượng: **9%**

↓

## Chữ ký tín hiệu

```text
SIG-3F91
```

---

# Nguyên tắc

Trọng số tín hiệu phản ánh mức độ đóng góp của từng tầng.

Tổng các Trọng số tín hiệu phản ánh cách Trạng thái quyết định được hình thành.

Chữ ký tín hiệu chuẩn hóa toàn bộ kết quả suy luận thành một dấu vết duy nhất.

---

# Triết lý

Trọng số tín hiệu giải thích cách Trạng thái quyết định được hình thành.

Chữ ký tín hiệu chuẩn hóa toàn bộ quá trình suy luận để phục vụ Tri thức tích luỹ.