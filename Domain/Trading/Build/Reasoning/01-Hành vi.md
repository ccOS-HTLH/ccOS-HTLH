# 01-Hành vi

> Hiểu điều đang thực sự diễn ra giữa người mua và người bán.

---

# Mục đích

Hành vi là tầng đầu tiên của Hệ thống suy luận.

Tầng này chuyển dữ liệu quan sát thành Trạng thái hành vi của thị trường.

---

# Câu hỏi

> Điều gì đang thực sự diễn ra giữa người mua và người bán?

---

# Đầu vào

Dữ liệu quan sát từ Nguồn dữ liệu:

- Giá
- Khối lượng
- Delta
- CVD
- Open Interest
- Funding Rate
- Aggressive Orders
- Liquidation
- Volume Profile
- Heatmap
- Time

---

# Đầu ra

Trạng thái hành vi, làm đầu vào cho tầng Bối cảnh.

---

# Luồng

```text
Nguồn dữ liệu

↓

Hành vi

↓

Bối cảnh
```

---

# Cấu trúc

```text
01-Định nghĩa

↓

02-Quan sát

↓

03-Trạng thái

↓

04-Chuyển đổi

↓

05-Ví dụ
```

---

# Triết lý

Hiểu đúng hành vi là nền tảng của mọi suy luận tiếp theo.

---

# Định nghĩa

> Bản chất của Hành vi.

---

# Bản chất

Hành vi là sự biểu hiện của quá trình đấu giá giữa người mua và người bán.

Hành vi được nhận diện từ dữ liệu đã được chuẩn hóa bởi Nguồn dữ liệu.

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

> Xác định những khía cạnh của dữ liệu phản ánh hành vi thị trường.

---

# Mục đích

Tầng Hành vi tập trung vào những dữ liệu phản ánh trực tiếp hành vi giữa người mua và người bán.

---

# Khía cạnh quan sát

## Hành vi giao dịch

- Sự chủ động của người mua và người bán.
- Sự thay đổi của Delta.
- Sự thay đổi của CVD.
- Sự thay đổi của Open Interest.
- Sự thay đổi của Funding Rate.
- Hoạt động thanh lý.

---

## Phản ứng thị trường

- Sự thay đổi của khối lượng.
- Sự thay đổi của thanh khoản.
- Phản ứng tại Volume Profile.
- Phản ứng tại Heatmap.

---

# Nguyên tắc

Quan sát nhất quán.

Mô tả khách quan.

Quan sát luôn đi trước suy luận.

---

> Quan sát đúng tạo nên sự hiểu đúng về hành vi.

---

# Trạng thái

> Mô tả trạng thái hiện tại của Hành vi.

---

# Mục đích

Trạng thái tổng hợp kết quả quan sát hành vi tại thời điểm hiện tại.

---

# Trạng thái chính

## Cân bằng

Người mua và người bán đạt trạng thái cân bằng.

---

## Người mua chiếm ưu thế

Người mua đang kiểm soát quá trình đấu giá.

---

## Người bán chiếm ưu thế

Người bán đang kiểm soát quá trình đấu giá.

---

# Hiện tượng hành vi

## Chủ động

Một phía chủ động mở rộng vùng giá hiện tại.

---

## Hấp thụ

Một phía hấp thụ lực của phía còn lại nhưng giá chưa mở rộng tương ứng.

---

## Suy kiệt

Động lượng của một phía suy yếu rõ rệt.

---

## Phản ứng

Một phía phản ứng mạnh tại vùng giá quan trọng.

---

# Triết lý

Trạng thái phản ánh hành vi hiện tại của thị trường.

---

# Chuyển đổi

> Mô tả cách Hành vi thay đổi theo thời gian.

---

# Mục đích

Chuyển đổi mô tả sự thay đổi của hành vi thị trường giữa các trạng thái.

---

# Ví dụ

```text
Cân bằng

↓

Người mua chiếm ưu thế

↓

Suy kiệt

↓

Cân bằng
```

---

```text
Cân bằng

↓

Người bán chiếm ưu thế

↓

Hấp thụ

↓

Người mua chiếm ưu thế
```

---

# Nguyên tắc

Mọi chuyển đổi đều bắt đầu từ quan sát mới.

Trạng thái chỉ chuyển đổi khi có đủ bằng chứng.

---

# Triết lý

Hành vi luôn vận động theo Thực tế.

---

# Ví dụ

---

# Ví dụ 01 · Người mua chiếm ưu thế

## Quan sát

- Delta tăng mạnh.
- CVD tăng.
- Open Interest tăng.
- Lệnh mua chủ động áp đảo.

↓

## Trạng thái

Người mua chiếm ưu thế.

---

# Ví dụ 02 · Người bán chiếm ưu thế

## Quan sát

- Giá giảm.
- Delta âm.
- CVD giảm.
- Open Interest giảm.

↓

## Trạng thái

Người bán chiếm ưu thế.

---

# Ví dụ 03 · Hấp thụ

## Quan sát

- Delta tăng mạnh.
- Giá gần như đi ngang.
- Khối lượng lớn.

↓

## Trạng thái

Hấp thụ.

---

# Nguyên tắc

Trạng thái được hình thành từ kết quả quan sát.

---

# Triết lý

Ví dụ giúp thống nhất cách hiểu về Hành vi.