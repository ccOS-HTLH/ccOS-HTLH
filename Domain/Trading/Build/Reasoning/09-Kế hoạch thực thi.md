# 09 · Kế hoạch thực thi

> Thiết kế, hiệu chỉnh và thực thi các phương án cho từng kịch bản.

---

# Mục đích

Kế hoạch thực thi là tầng thứ chín của Hệ thống suy luận.

Tầng này xây dựng các phương án thực thi cho từng kịch bản.

Không gian kịch bản cung cấp các kịch bản hiện tại.

Chữ ký tín hiệu được sử dụng để tra cứu Tri thức tích luỹ nhằm tham khảo các Trường hợp, Mẫu, Bài học tích luỹ và Thống kê liên quan, từ đó lựa chọn hoặc hiệu chỉnh phương án thực thi phù hợp (nếu có).

Sau khi các phương án được hình thành, các điều kiện thực tế được quan sát và Tri thức tích luỹ được tham khảo để hiệu chỉnh phương án phù hợp.

Khi các điều kiện thực thi được đáp ứng, phương án tương ứng được triển khai.

Mỗi phương án xác định:

- Điều kiện thực thi.
- Điều kiện xác nhận.
- Mức độ xác nhận.
- Điều kiện hủy bỏ.
- Quản trị rủi ro.
- Quản trị vị thế.

---

# Câu hỏi

## Nếu kịch bản này xảy ra, mình nên hành động như thế nào?

→ Không gian kịch bản.

---

## Theo kinh nghiệm đã được tích luỹ, phương án nào phù hợp hơn?

→ Chữ ký tín hiệu + Tri thức tích luỹ.

---

## Khi nào nên thực hiện phương án đã lựa chọn?

→ Điều kiện thực thi.

---

# Đầu vào

- Không gian kịch bản.
- Chữ ký tín hiệu.

---

# Đầu ra

Kế hoạch thực thi.

Kế hoạch thực thi bao gồm một hoặc nhiều phương án đã được hiệu chỉnh.

Mỗi phương án bao gồm:

- Điều kiện thực thi.
- Điều kiện xác nhận.
- Mức độ xác nhận.
- Điều kiện hủy bỏ.
- Quản trị rủi ro.
- Quản trị vị thế.

Khi các điều kiện thực thi được xác nhận, phương án tương ứng được thực hiện và trở thành đầu vào của tầng Phản hồi thực tế.

---

# Vai trò trong Hệ thống suy luận

```text
08 · Không gian kịch bản
        │
        ▼
07 · Chữ ký tín hiệu
        │
        ▼
# Tri thức tích luỹ
        │
        ▼
Tra cứu:
- Trường hợp
- Mẫu
- Bài học tích luỹ
- Thống kê
        │
        ▼
09 · Kế hoạch thực thi
        │
        ├── 03 · Phương án
        │
        ├── 03.1 · Mức độ xác nhận
        │
        ├── 04 · Hiệu chỉnh
        │
        └── 05 · Thực thi
        │
        ▼
Kế hoạch thực thi
        │
        ▼
10 · Phản hồi thực tế
```

---

# Cấu trúc

```text
01 · Định nghĩa

↓

02 · Quan sát

↓

03 · Phương án

↓

03.1 · Mức độ xác nhận

↓

04 · Hiệu chỉnh

↓

05 · Thực thi

↓

06 · Ví dụ
```

---

# Triết lý

Không gian kịch bản xác định các khả năng.

Tri thức tích luỹ giúp lựa chọn và hiệu chỉnh phương án phù hợp.

Khi các điều kiện của phương án được xác nhận, phương án tương ứng được thực thi.

Chỉ có Thực tế mới kiểm chứng được giá trị của một phương án.

---

# 01 · Định nghĩa

> Bản chất của Kế hoạch thực thi.

---

# Bản chất

Kế hoạch thực thi thiết kế các phương án thực thi cho từng kịch bản.

Kế hoạch thực thi không lựa chọn kịch bản.

Kế hoạch thực thi chuẩn bị các phương án thực thi cho những kịch bản có thể xảy ra.

Sau khi các phương án được hình thành, Tri thức tích luỹ được tham khảo để lựa chọn hoặc hiệu chỉnh phương án phù hợp hơn.

Việc hiệu chỉnh không chỉ điều chỉnh phương án, mà còn điều chỉnh mức độ xác nhận và quy mô thực thi dựa trên chất lượng của các bằng chứng hiện tại.

Khi các điều kiện thực thi được đáp ứng, phương án đã được lựa chọn sẽ được thực hiện theo đúng kế hoạch.

---

# Thành phần

Một phương án thực thi bao gồm:

- Vùng vào lệnh.
- Điều kiện thực thi.
- Điều kiện xác nhận.
- Mức độ xác nhận.
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
- Hiệu chỉnh.
- Thực thi nhất quán.

---

# Đầu ra

Tầng Kế hoạch thực thi tạo ra các phương án thực thi đã được hiệu chỉnh.

Mỗi phương án bao gồm đầy đủ các điều kiện thực thi, điều kiện xác nhận, mức độ xác nhận, quản trị rủi ro và quản trị vị thế.

Khi các điều kiện thực thi được xác nhận, phương án tương ứng được thực hiện và trở thành đầu vào của tầng Phản hồi thực tế.

---

# Triết lý

Một phương án tốt giúp tạo nên một quá trình thực thi nhất quán.

Chất lượng của bằng chứng quyết định mức độ cam kết, không quyết định sự tồn tại của phương án.

Một quá trình thực thi nhất quán giúp Thực tế phản ánh chính xác chất lượng của phương án.

---

# 02 · Quan sát

> Quan sát các phương án thực thi của từng kịch bản.

---

# Mục đích

Quan sát các phương án thực thi được xây dựng cho từng kịch bản.

Quan sát các điều kiện thực thi của từng phương án.

Quan sát các yếu tố ảnh hưởng đến việc lựa chọn, hiệu chỉnh và thực thi phương án.

Quan sát quá trình hình thành các điều kiện để đánh giá mức độ xác nhận và xác định thời điểm thực thi phù hợp.

---

# Quan sát

Quan sát tập trung vào:

- Vùng vào lệnh.
- Điều kiện thực thi.
- Điều kiện xác nhận.
- Mức độ xác nhận.
- Vùng thanh khoản mục tiêu.
- Mức độ rủi ro.
- Mục tiêu lợi nhuận.
- Điều kiện vô hiệu.
- Thời điểm thực thi.
- Chi phí thực thi.

---

# Nguyên tắc

Mỗi kịch bản có thể có một hoặc nhiều phương án thực thi.

Mỗi phương án có các điều kiện thực thi riêng.

Tri thức tích luỹ được tham khảo để lựa chọn hoặc hiệu chỉnh phương án phù hợp hơn.

Mức độ xác nhận phản ánh chất lượng của các bằng chứng hiện tại và được sử dụng để hiệu chỉnh quy mô thực thi.

Khi các điều kiện thực thi và điều kiện xác nhận được đáp ứng, phương án tương ứng được thực hiện theo kế hoạch.

Trong quá trình thực thi, phương án được tuân thủ nhất quán.

---

# Triết lý

Phương án phản ánh cách thực thi của từng kịch bản.

Tri thức tích luỹ giúp lựa chọn và hiệu chỉnh phương án phù hợp hơn.

Mức độ xác nhận giúp điều chỉnh mức độ cam kết của cùng một phương án.

Chuẩn bị trước giúp quá trình thực thi nhất quán.

---

# 03 · Phương án

> Mô tả cấu trúc của một phương án thực thi.

---

# Mục đích

Phương án mô tả cách thực thi cho một kịch bản cụ thể.

Một kịch bản có thể có một hoặc nhiều phương án thực thi.

Các phương án được xây dựng trước khi tham khảo Tri thức tích luỹ để hiệu chỉnh và lựa chọn.

---

# Thành phần

Một phương án bao gồm:

- Vùng vào lệnh.
- Điều kiện thực thi.
- Điều kiện xác nhận.
- Mức độ xác nhận.
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

Sau khi được xây dựng, phương án có thể được hiệu chỉnh trước khi được lựa chọn để thực thi.

Trong quá trình hiệu chỉnh, quy mô vị thế và mức độ xác nhận có thể thay đổi theo chất lượng của các bằng chứng hiện tại.

---

# Vai trò

Phương án là đơn vị cơ bản của Kế hoạch thực thi.

Nhiều phương án kết hợp tạo thành Kế hoạch thực thi.

Phương án là đầu vào của bước Hiệu chỉnh và Thực thi.

---

# Triết lý

Một phương án chuẩn bị cách hành động phù hợp cho từng kịch bản.

Chất lượng của bằng chứng quyết định mức độ cam kết, không quyết định sự tồn tại của phương án.

Một phương án tốt luôn sẵn sàng được hiệu chỉnh trước khi được lựa chọn để thực thi.

---

# 03.1 · Mức độ xác nhận

> Đánh giá mức độ sẵn sàng để thực thi một phương án.

---

# Mục đích

Mức độ xác nhận phản ánh chất lượng của các bằng chứng hiện tại đối với một phương án.

Mức độ xác nhận giúp Kế hoạch thực thi xác định mức độ cam kết phù hợp trước khi thực hiện phương án.

Mức độ xác nhận được sử dụng để lựa chọn cách thực thi phù hợp cho cùng một phương án.

---

# Mức độ

## WATCH

Điều kiện thực thi đang được hình thành.

Phương án tiếp tục được quan sát.

Mục tiêu:

- Theo dõi.
- Thu thập thêm bằng chứng.
- Chờ điều kiện thực thi hoàn thiện.

---

## PROBE

Điều kiện thực thi bắt đầu hình thành.

Một phần các điều kiện xác nhận đã xuất hiện.

Phương án được thực hiện với mức độ cam kết thấp.

Ví dụ:

- Quy mô vị thế nhỏ hơn.
- Quản trị rủi ro chặt chẽ hơn.
- Tiếp tục quan sát trong quá trình thực thi.

---

## CONFIRM

Điều kiện thực thi và điều kiện xác nhận đã được đáp ứng.

Phương án được thực hiện theo kế hoạch đã xây dựng.

Quy mô vị thế và quản trị vị thế được triển khai theo phương án đã hiệu chỉnh.

---

# Nguyên tắc

Mức độ xác nhận phản ánh chất lượng của các bằng chứng hiện tại.

Mức độ xác nhận gắn với một phương án cụ thể.

Mức độ xác nhận giúp điều chỉnh:

- Quy mô vị thế.
- Mức độ cam kết.
- Cách triển khai phương án.

Trong quá trình quan sát, mức độ xác nhận được cập nhật khi các bằng chứng thay đổi.

---

# Vai trò

Mức độ xác nhận kết nối Quan sát với Thực thi.

Mức độ xác nhận giúp chuyển đổi từ chuẩn bị sang hành động một cách nhất quán.

---

# Triết lý

Cùng một phương án có thể được thực thi với nhiều mức độ cam kết khác nhau.

Mức độ xác nhận phản ánh mức độ hội tụ của các bằng chứng.

Mức độ xác nhận quyết định mức độ cam kết của cùng một phương án.

---

# 04 · Hiệu chỉnh

> Hiệu chỉnh các phương án bằng dữ liệu tham khảo từ Tri thức tích luỹ.

---

# Mục đích

Hiệu chỉnh giúp Kế hoạch thực thi tham khảo kinh nghiệm đã được tích luỹ.

Sau khi các phương án được xây dựng từ Không gian kịch bản, Chữ ký tín hiệu được sử dụng để tra cứu Tri thức tích luỹ.

Nếu tồn tại đủ dữ liệu tham khảo phù hợp, Kế hoạch thực thi có thể hiệu chỉnh các phương án và lựa chọn phương án phù hợp hơn để thực thi.

Hiệu chỉnh giúp phương án phản ánh tốt hơn chất lượng của các bằng chứng hiện tại trước khi được thực thi.

---

# Hiệu chỉnh

Kế hoạch thực thi có thể hiệu chỉnh:

- Mức độ ưu tiên của phương án.
- Mức độ phù hợp của phương án.
- Mức độ xác nhận.
- Quy mô vị thế.
- Quản trị vị thế.
- Tỷ lệ lợi nhuận / Rủi ro.

Trong quá trình hiệu chỉnh:

- Điều kiện thực thi được giữ nguyên.
- Điều kiện xác nhận được giữ nguyên.
- Điều kiện vô hiệu được giữ nguyên.

Hiệu chỉnh tập trung vào cách thực thi của phương án, không thay đổi bản chất của phương án.

---

# Nguyên tắc

Các phương án luôn được xây dựng từ Không gian kịch bản.

Tri thức tích luỹ được tham khảo sau khi các phương án đã được hình thành.

Nếu chưa có đủ dữ liệu tham khảo phù hợp, Kế hoạch thực thi giữ nguyên các phương án hiện tại.

Nếu đã có đủ dữ liệu tham khảo phù hợp, Kế hoạch thực thi tham khảo Tri thức tích luỹ để hiệu chỉnh các phương án trước khi lựa chọn phương án phù hợp để thực thi.

Tri thức tích luỹ cung cấp dữ liệu tham khảo để hiệu chỉnh phương án hiện có.

---

# Vai trò

Hiệu chỉnh kết nối Tri thức tích luỹ với Kế hoạch thực thi.

Hiệu chỉnh giúp cùng một phương án có thể được thực thi với mức độ cam kết phù hợp với chất lượng của các bằng chứng hiện tại.

---

# Triết lý

Không gian kịch bản hình thành các phương án.

Tri thức tích luỹ giúp hiệu chỉnh các phương án.

Chất lượng của bằng chứng quyết định mức độ cam kết của cùng một phương án.

Kế hoạch thực thi lựa chọn phương án phù hợp để thực thi.

---

# 05 · Thực thi

> Thực hiện phương án đã được lựa chọn và hiệu chỉnh.

---

# Mục đích

Thực thi chịu trách nhiệm triển khai phương án đã được lựa chọn.

Thực thi bắt đầu khi các điều kiện thực thi và điều kiện xác nhận của phương án được đáp ứng.

Trong quá trình thực thi, phương án được triển khai nhất quán theo kế hoạch đã được xây dựng và hiệu chỉnh.

Mức độ xác nhận của phương án được sử dụng để xác định mức độ cam kết và quy mô thực thi.

---

# Thực thi

Quá trình thực thi bao gồm:

- Theo dõi điều kiện thực thi.
- Xác nhận điều kiện vào lệnh.
- Xác định mức độ xác nhận.
- Thực hiện vào lệnh.
- Quản trị vị thế.
- Thực hiện điểm dừng lỗ.
- Thực hiện điểm chốt lời.
- Kết thúc phương án.

Kết thúc phương án có thể xảy ra khi:

- Hoàn thành mục tiêu.
- Điều kiện vô hiệu xuất hiện.
- Điểm dừng lỗ được kích hoạt.
- Điểm chốt lời được hoàn thành.

---

# Nguyên tắc

Khi các điều kiện thực thi và điều kiện xác nhận được đáp ứng, phương án được triển khai theo kế hoạch.

Mức độ xác nhận được sử dụng để xác định mức độ cam kết và quy mô vị thế phù hợp.

Trong quá trình thực thi, phương án được giữ nguyên.

Nếu phương án mất hiệu lực theo các điều kiện đã xác định, quá trình thực thi được kết thúc.

Mọi hành động được thực hiện theo phương án đã được lựa chọn và hiệu chỉnh.

Kết quả của quá trình thực thi được chuyển sang tầng Phản hồi thực tế để đánh giá.

---

# Vai trò

Thực thi là bước chuyển từ kế hoạch sang hành động.

Thực thi kết nối Kế hoạch thực thi với Phản hồi thực tế.

Mọi kết quả thực tế đều bắt đầu từ quá trình thực thi.

---

# Triết lý

Phương án xác định cách hành động.

Mức độ xác nhận quyết định mức độ cam kết của cùng một phương án.

Thực thi biến phương án thành hành động.

Thực tế kiểm chứng giá trị của mọi hành động.

---

# 06 · Ví dụ

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

Mức độ xác nhận phản ánh mức độ hội tụ của các bằng chứng hiện tại.

Mức độ xác nhận được sử dụng để điều chỉnh mức độ cam kết và quy mô thực thi của cùng một phương án.

Khi các điều kiện thực thi và điều kiện xác nhận được đáp ứng, phương án tương ứng được thực hiện.

---

# Triết lý

Xác suất suy luận phản ánh kết quả của Hệ thống suy luận.

Xác suất hiệu chỉnh phản ánh kết quả sau khi tham khảo Tri thức tích luỹ.

Mức độ xác nhận phản ánh mức độ hội tụ của các bằng chứng hiện tại.

Thực thi biến phương án thành hành động.

Thực tế kiểm chứng giá trị của mọi hành động.