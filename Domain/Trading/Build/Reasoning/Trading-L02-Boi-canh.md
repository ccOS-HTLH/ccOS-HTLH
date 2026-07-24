# 02 · Bối cảnh

> Hiểu môi trường mà hành vi thị trường đang diễn ra.

---

# Mục đích

Bối cảnh là tầng thứ hai của Hệ thống suy luận.

Tầng này đặt Trạng thái hành vi vào đúng môi trường của thị trường.

---

# Câu hỏi

> Hành vi này đang diễn ra trong bối cảnh nào?

---

# Đầu vào

Trạng thái hành vi cùng các thông tin về môi trường thị trường, ví dụ:

- Xu hướng đa khung thời gian.
- Vị trí trong cấu trúc thị trường.
- Quan hệ giữa các khung thời gian.
- Bối cảnh thanh khoản.
- Bối cảnh vĩ mô (nếu có).

---

# Đầu ra

Trạng thái bối cảnh, làm đầu vào cho tầng Động lượng.

---

# Luồng

```text
Hành vi

↓

Bối cảnh

↓

Động lượng
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

Cùng một hành vi.

Khác bối cảnh.

Khác ý nghĩa.

---

# Định nghĩa

> Bản chất của Bối cảnh.

---

# Bản chất

Bối cảnh mô tả môi trường mà Hành vi đang diễn ra.

Bối cảnh giúp xác định ý nghĩa của Trạng thái hành vi.

---

# Thành phần

Bối cảnh được phản ánh thông qua:

- Xu hướng đa khung thời gian.
- Cấu trúc thị trường.
- EMA.
- Hỗ trợ / Kháng cự.
- Fibonacci.
- Volume Profile.
- Thanh khoản.
- Môi trường vĩ mô.

Những thành phần này cùng mô tả môi trường hiện tại của thị trường.

---

# Đầu ra

Tầng Bối cảnh tạo ra Trạng thái bối cảnh.

Trạng thái bối cảnh trở thành đầu vào của tầng Động lượng.

---

# Triết lý

Bối cảnh tạo nên ý nghĩa.

---

# Quan sát

> Quan sát toàn bộ bối cảnh mà Hành vi đang diễn ra.

---

# Mục đích

Quan sát môi trường mà Hành vi đang diễn ra.

Bối cảnh phản ánh môi trường hiện tại của thị trường.

---

# Quan sát

## Khung thời gian lớn

- Monthly
- Weekly
- Daily
- 4H

---

## Vị trí trong cấu trúc

- Vùng định giá cao
- Vùng cân bằng
- Vùng định giá thấp

---

## Cấu trúc thị trường

- Xu hướng tăng
- Xu hướng giảm
- Đi ngang

---

## Trạng thái thị trường

- Mở rộng
- Tích lũy

---

## Bối cảnh kỹ thuật

- EMA
- Support / Resistance
- Fibonacci
- Volume Profile (POC30 / VAH30 / VAL30)
- Liquidity

---

## Bối cảnh bên ngoài

- Funding Rate
- Fear & Greed
- DXY
- Gold
- Nasdaq
- News
- Macro Events

---

# Nguyên tắc

Bối cảnh được xây dựng từ khung thời gian lớn xuống khung thời gian nhỏ.

Khung lớn định nghĩa bối cảnh.

Khung nhỏ thể hiện Hành vi.

Thông thường, khung lớn dẫn dắt khung nhỏ.

Khi khung lớn tiếp cận vùng quyết định quan trọng, Hành vi trên khung nhỏ có thể tạo ra Chuyển đổi cho khung lớn.

---

# Triết lý

Bối cảnh là môi trường của Hành vi.

Hành vi luôn được hiểu trong bối cảnh của khung lớn.

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

# Chuyển đổi

> Mô tả cách Bối cảnh thay đổi theo thời gian.

---

# Mục đích

Chuyển đổi mô tả sự thay đổi của Bối cảnh thị trường.

Mỗi chuyển đổi phản ánh sự thay đổi của môi trường mà Hành vi đang diễn ra.

---

# Ví dụ

## Chuyển đổi cấu trúc

```text
Đi ngang

↓

Xu hướng tăng
```

---

```text
Xu hướng tăng

↓

Đi ngang
```

---

```text
Xu hướng giảm

↓

Đi ngang
```

---

## Chuyển đổi trạng thái thị trường

```text
Tích lũy

↓

Mở rộng
```

---

```text
Mở rộng

↓

Tích lũy
```

---

## Chuyển đổi vùng rủi ro

```text
Rủi ro thấp

↓

Rủi ro cao
```

---

```text
Rủi ro cao

↓

Rủi ro thấp
```

---

# Nguyên tắc

Mọi chuyển đổi đều bắt đầu từ quan sát mới.

Trạng thái chỉ chuyển đổi khi có đủ bằng chứng.

Bối cảnh thay đổi chậm hơn Hành vi.

Bối cảnh định hướng Động lượng.

---

# Triết lý

Chuyển đổi phản ánh sự thay đổi của Bối cảnh.

---

# Ví dụ

---

# Ví dụ 01 · Xu hướng tăng

## Quan sát

- Daily: Xu hướng tăng.
- 4H: Pullback.
- Giá chạm EMA89.
- Vùng định giá thấp.
- Thanh khoản phía dưới đã được quét.

↓

## Trạng thái

### Cấu trúc thị trường

- Xu hướng tăng.

### Trạng thái thị trường

- Tích lũy.

### Vùng rủi ro

- Rủi ro thấp.

---

# Ví dụ 02 · Xu hướng tăng

## Quan sát

- Daily: Xu hướng tăng.
- 4H: Vùng định giá cao.
- Giá chạm Fibonacci 0.786.
- Kháng cự Weekly.
- Thanh khoản phía trên dày.

↓

## Trạng thái

### Cấu trúc thị trường

- Xu hướng tăng.

### Trạng thái thị trường

- Mở rộng.

### Vùng rủi ro

- Rủi ro cao.

---

# Ví dụ 03 · Đi ngang

## Quan sát

- Weekly: Đi ngang.
- Daily: Biến động thu hẹp.
- Volume giảm.
- Thanh khoản cân bằng.

↓

## Trạng thái

### Cấu trúc thị trường

- Đi ngang.

### Trạng thái thị trường

- Tích lũy.

### Vùng rủi ro

- Rủi ro thấp.

---

# Nguyên tắc

Hành vi giống nhau có thể mang ý nghĩa khác nhau.

Bối cảnh quyết định cách hiểu Hành vi.

---

# Triết lý

Bối cảnh quyết định ý nghĩa của Hành vi.