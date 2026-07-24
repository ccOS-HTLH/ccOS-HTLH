title: Hệ thống suy luận
id: trading-reasoning-system
version: 1.4.0
status: Stable
author: HTLH
language: vi
created: 2026-07-19
last_updated: 2026-07-23
review_cycle: Monthly
confidence: 100%
tags:

• trading
• reasoning

────────

Hệ thống suy luận

> Hệ thống suy luận là khuôn khổ chuyển dữ liệu quan sát thành quyết định có thể kiểm chứng bằng Thực tế.

────────

Mục đích

Hệ thống suy luận trả lời:

> Làm thế nào để chuyển dữ liệu quan sát thành một quyết định có căn cứ?

Hệ thống suy luận chuẩn hóa toàn bộ quá trình suy luận của Trading.

Mỗi tầng chỉ giải quyết một vấn đề.

Mỗi tầng kế thừa kết quả từ tầng trước.

Toàn bộ hệ thống hướng tới một quyết định có thể kiểm chứng bằng Thực tế.

────────

Triết lý

Quan sát luôn đi trước suy luận.

Mỗi tầng chỉ giải quyết một vấn đề.

Mỗi kết luận đều dựa trên bằng chứng.

Thực tế là tiêu chuẩn cuối cùng của mọi suy luận.

────────

Kiến trúc

```text
Hệ thống suy luận

├── README.md
├── 01-Hành vi
├── 02-Bối cảnh
├── 03-Động lượng
├── 04-Cấu trúc
├── 05-Chất lượng
├── 06-Quyết định
├── 07-Trọng số tín hiệu
├── 08-Không gian kịch bản
├── 09-Kế hoạch thực thi
└── 10-Phản hồi thực tế
```

────────

Đầu vào

Hệ thống suy luận tiếp nhận dữ liệu từ tầng Nguồn dữ liệu.

Nguồn dữ liệu có thể đến từ:

• ATS.
• Dữ liệu rời rạc.
• Các nguồn dữ liệu khác.

Mọi nguồn dữ liệu đều được xử lý theo cùng một Hệ thống suy luận.

────────

Đầu ra cuối cùng của toàn bộ Hệ thống suy luận:

• Quyết định.
• Không gian kịch bản.
• Kế hoạch thực thi.
• Phản hồi thực tế.

────────

Vị trí trong Trading

```text
Trading

├── Nguồn dữ liệu
│      ├── ATS
│      ├── Dữ liệu rời rạc
│      └── ...
│
└── Hệ thống suy luận
       Suy luận
```

ATS chỉ là một nguồn dữ liệu.

Dữ liệu rời rạc cũng là một nguồn dữ liệu.

Hệ thống suy luận không phụ thuộc vào bất kỳ nguồn dữ liệu cụ thể nào.

────────

Luồng hoạt động

```text
Nguồn dữ liệu

↓

01 · Hành vi

↓

02 · Bối cảnh

↓

03 · Động lượng

↓

04 · Cấu trúc

↓

05 · Chất lượng

↓

06 · Quyết định

↓

07 · Trọng số tín hiệu

↓

08 · Không gian kịch bản

↓

09 · Kế hoạch thực thi

↓

10 · Phản hồi thực tế
```

────────

Tóm tắt

```text
Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Quyết định

↓

Thực tế
```

Hệ thống suy luận định nghĩa:

• Kiến trúc suy luận.
• Mối quan hệ giữa các tầng.
• Cách chuyển dữ liệu quan sát thành quyết định.
• Cách kiểm chứng quyết định bằng Thực tế.

────────

01 · Hành vi

> Hiểu điều đang thực sự diễn ra giữa người mua và người bán.

────────

Mục đích

Hành vi là tầng đầu tiên của Hệ thống suy luận.

Tầng này chuyển dữ liệu quan sát thành sự hiểu biết về hành vi hiện tại của thị trường.

────────

Câu hỏi

> Điều gì đang thực sự diễn ra giữa người mua và người bán?

────────

Đầu vào

Dữ liệu quan sát từ Nguồn dữ liệu:

• Giá
• Khối lượng
• Delta
• CVD
• Open Interest
• Funding Rate
• Aggressive Orders
• Liquidation
• Volume Profile
• Heatmap
• Time

────────

Đầu ra

Trạng thái hành vi, làm đầu vào cho tầng Bối cảnh.

────────

Luồng

```text
Nguồn dữ liệu

↓

Hành vi

↓

Bối cảnh
```

────────

Cấu trúc

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

────────

Triết lý

Hiểu đúng hành vi là nền tảng của mọi suy luận tiếp theo.

────────

Định nghĩa

> Bản chất của Hành vi.

────────

Bản chất

Hành vi là sự biểu hiện của quá trình đấu giá giữa người mua và người bán.

Hành vi được nhận diện từ dữ liệu đã được Nguồn dữ liệu chuẩn hóa.

────────

Thành phần

Hành vi được phản ánh thông qua:

• Giá
• Khối lượng
• Thời gian
• Lệnh chủ động
• Thanh khoản

Những thành phần này cùng phản ánh hành vi hiện tại của thị trường.

────────

Đầu ra

Tầng Hành vi tạo ra Trạng thái hành vi.

Trạng thái hành vi trở thành đầu vào của tầng Bối cảnh.

────────

> Hành vi phản ánh điều đang thực sự diễn ra giữa người mua và người bán.

────────

Quan sát

> Xác định những khía cạnh của dữ liệu phản ánh hành vi thị trường.

────────

Mục đích

Tầng Hành vi tập trung vào những dữ liệu phản ánh trực tiếp hành vi giữa người mua và người bán.

────────

Khía cạnh quan sát

Hành vi giao dịch

• Sự chủ động của người mua và người bán.
• Sự thay đổi của Delta.
• Sự thay đổi của CVD.
• Sự thay đổi của Open Interest.
• Sự thay đổi của Funding Rate.
• Hoạt động thanh lý.

────────

Phản ứng thị trường

• Sự thay đổi của khối lượng.
• Sự thay đổi của thanh khoản.
• Phản ứng tại Volume Profile.
• Phản ứng tại Heatmap.

────────

Nguyên tắc

Quan sát nhất quán.

Mô tả khách quan.

Quan sát luôn đi trước suy luận.

────────

> Quan sát đúng tạo nên sự hiểu đúng về hành vi.

────────

Trạng thái

> Mô tả trạng thái hiện tại của Hành vi.

────────

Mục đích

Trạng thái tổng hợp kết quả quan sát hành vi tại thời điểm hiện tại.

────────

Trạng thái chính

Cân bằng

Người mua và người bán đạt trạng thái cân bằng.

────────

Người mua chiếm ưu thế

Người mua đang kiểm soát quá trình đấu giá.

────────

Người bán chiếm ưu thế

Người bán đang kiểm soát quá trình đấu giá.

────────

Hiện tượng hành vi

Chủ động

Một phía chủ động mở rộng vùng giá hiện tại.

────────

Hấp thụ

Một phía hấp thụ lực của phía còn lại nhưng giá chưa mở rộng tương ứng.

────────

Suy kiệt

Động lượng của một phía suy yếu rõ rệt.

────────

Phản ứng

Một phía phản ứng mạnh tại vùng giá quan trọng.

────────

Triết lý

Trạng thái phản ánh hành vi hiện tại của thị trường.

────────

Chuyển đổi

> Mô tả cách Hành vi thay đổi theo thời gian.

────────

Mục đích

Chuyển đổi mô tả sự thay đổi của hành vi thị trường giữa các trạng thái.

────────

Ví dụ

```text
Cân bằng

↓

Người mua chiếm ưu thế

↓

Suy kiệt

↓

Cân bằng
```

────────

```text
Cân bằng

↓

Người bán chiếm ưu thế

↓

Hấp thụ

↓

Người mua chiếm ưu thế
```

────────

Nguyên tắc

Mọi chuyển đổi đều bắt đầu từ quan sát mới.

Trạng thái chỉ chuyển đổi khi có đủ bằng chứng.

────────

Triết lý

Hành vi luôn vận động theo Thực tế.

────────

Ví dụ

────────

Ví dụ 01 · Người mua chiếm ưu thế

Quan sát

• Delta tăng mạnh.
• CVD tăng.
• Open Interest tăng.
• Lệnh mua chủ động áp đảo.

↓

Trạng thái

Người mua chiếm ưu thế.

────────

Ví dụ 02 · Người bán chiếm ưu thế

Quan sát

• Giá giảm.
• Delta âm.
• CVD giảm.
• Open Interest giảm.

↓

Trạng thái

Người bán chiếm ưu thế.

────────

Ví dụ 03 · Hấp thụ

Quan sát

• Delta tăng mạnh.
• Giá gần như đi ngang.
• Khối lượng lớn.

↓

Trạng thái

Hấp thụ.

────────

Nguyên tắc

Trạng thái được hình thành từ kết quả quan sát.

────────

Triết lý

Ví dụ giúp thống nhất cách hiểu về Hành vi.

────────

────────

02 · Bối cảnh

> Hiểu môi trường mà hành vi thị trường đang diễn ra.

────────

Mục đích

Bối cảnh là tầng thứ hai của Hệ thống suy luận.

Tầng này đặt Trạng thái hành vi vào đúng môi trường của thị trường.

────────

Câu hỏi

> Hành vi này đang diễn ra trong bối cảnh nào?

────────

Đầu vào

Trạng thái hành vi cùng các thông tin về môi trường thị trường, ví dụ:

• Xu hướng đa khung thời gian.
• Vị trí trong cấu trúc thị trường.
• Quan hệ giữa các khung thời gian.
• Bối cảnh thanh khoản.
• Bối cảnh vĩ mô (nếu có).

────────

Đầu ra

Trạng thái bối cảnh, làm đầu vào cho tầng Động lượng.

────────

Luồng

```text
Hành vi

↓

Bối cảnh

↓

Động lượng
```

────────

Cấu trúc

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

────────

Triết lý

Cùng một hành vi.

Khác bối cảnh.

Khác ý nghĩa.

────────

Định nghĩa

> Bản chất của Bối cảnh.

────────

Bản chất

Bối cảnh mô tả môi trường mà Hành vi đang diễn ra.

Bối cảnh giúp xác định ý nghĩa của Trạng thái hành vi.

────────

Thành phần

Bối cảnh được phản ánh thông qua:

• Xu hướng đa khung thời gian.
• Cấu trúc thị trường.
• EMA.
• Hỗ trợ / Kháng cự.
• Fibonacci.
• Volume Profile.
• Thanh khoản.
• Môi trường vĩ mô.

Những thành phần này cùng mô tả môi trường hiện tại của thị trường.

────────

Đầu ra

Tầng Bối cảnh tạo ra Trạng thái bối cảnh.

Trạng thái bối cảnh trở thành đầu vào của tầng Động lượng.

────────

Triết lý

Bối cảnh tạo nên ý nghĩa.

────────

Quan sát

> Quan sát toàn bộ bối cảnh mà Hành vi đang diễn ra.

────────

Mục đích

Quan sát môi trường mà Hành vi đang diễn ra.

Bối cảnh phản ánh môi trường hiện tại của thị trường.

────────

Quan sát

Khung thời gian lớn

• Monthly
• Weekly
• Daily
• 4H

────────

Vị trí trong cấu trúc

• Vùng định giá cao
• Vùng cân bằng
• Vùng định giá thấp

────────

Cấu trúc thị trường

• Xu hướng tăng
• Xu hướng giảm
• Đi ngang

────────

Trạng thái thị trường

• Mở rộng
• Tích lũy

────────

Bối cảnh kỹ thuật

• EMA
• Support / Resistance
• Fibonacci
• Volume Profile (POC30 / VAH30 / VAL30)
• Liquidity

────────

Bối cảnh bên ngoài

• Funding Rate
• Fear & Greed
• DXY
• Gold
• Nasdaq
• News
• Macro Events

────────

Nguyên tắc

Bối cảnh được xây dựng từ khung thời gian lớn xuống khung thời gian nhỏ.

Khung lớn định nghĩa bối cảnh.

Khung nhỏ thể hiện Hành vi.

Thông thường, khung lớn dẫn dắt khung nhỏ.

Khi khung lớn tiếp cận vùng quyết định quan trọng, Hành vi trên khung nhỏ có thể tạo ra Chuyển đổi cho khung lớn.

────────

Triết lý

Bối cảnh là môi trường của Hành vi.

Hành vi luôn được hiểu trong bối cảnh của khung lớn.

────────

Trạng thái

> Mô tả trạng thái hiện tại của Bối cảnh.

────────

Mục đích

Trạng thái mô tả môi trường mà Hành vi đang diễn ra.

Mỗi trạng thái phản ánh điều kiện hiện tại của thị trường.

────────

Các trạng thái

Cấu trúc thị trường

Xu hướng tăng

Bối cảnh ưu tiên xu hướng tăng.

────────

Xu hướng giảm

Bối cảnh ưu tiên xu hướng giảm.

────────

Đi ngang

Thị trường đang ở trạng thái cân bằng.

────────

Trạng thái thị trường

Mở rộng

Thị trường đang mở rộng khỏi vùng giá trị trước đó.

────────

Tích lũy

Thị trường đang vận động trong một vùng giá hẹp.

────────

Vùng rủi ro

Rủi ro cao

Thị trường đang ở vùng có khả năng Chuyển đổi cao.

────────

Rủi ro thấp

Thị trường đang ở vùng thuận lợi cho xu hướng hiện tại tiếp diễn.

────────

Nguyên tắc

Trạng thái phản ánh bối cảnh hiện tại.

Trạng thái chỉ thay đổi khi bối cảnh thay đổi.

────────

Triết lý

Trạng thái phản ánh môi trường hiện tại của Hành vi.

────────

Chuyển đổi

> Mô tả cách Bối cảnh thay đổi theo thời gian.

────────

Mục đích

Chuyển đổi mô tả sự thay đổi của Bối cảnh thị trường.

Mỗi chuyển đổi phản ánh sự thay đổi của môi trường mà Hành vi đang diễn ra.

────────

Ví dụ

Chuyển đổi cấu trúc

```text
Đi ngang

↓

Xu hướng tăng
```

────────

```text
Xu hướng tăng

↓

Đi ngang
```

────────

```text
Xu hướng giảm

↓

Đi ngang
```

────────

Chuyển đổi trạng thái thị trường

```text
Tích lũy

↓

Mở rộng
```

────────

```text
Mở rộng

↓

Tích lũy
```

────────

Chuyển đổi vùng rủi ro

```text
Rủi ro thấp

↓

Rủi ro cao
```

────────

```text
Rủi ro cao

↓

Rủi ro thấp
```

────────

Nguyên tắc

Mọi chuyển đổi đều bắt đầu từ quan sát mới.

Trạng thái chỉ chuyển đổi khi có đủ bằng chứng.

Bối cảnh thay đổi chậm hơn Hành vi.

Bối cảnh định hướng Động lượng.

────────

Triết lý

Chuyển đổi phản ánh sự thay đổi của Bối cảnh.

────────

Ví dụ

────────

Ví dụ 01 · Xu hướng tăng

Quan sát

• Daily: Xu hướng tăng.
• 4H: Pullback.
• Giá chạm EMA89.
• Vùng định giá thấp.
• Thanh khoản phía dưới đã được quét.

↓

Trạng thái

Cấu trúc thị trường

• Xu hướng tăng.

Trạng thái thị trường

• Tích lũy.

Vùng rủi ro

• Rủi ro thấp.

────────

Ví dụ 02 · Xu hướng tăng

Quan sát

• Daily: Xu hướng tăng.
• 4H: Vùng định giá cao.
• Giá chạm Fibonacci 0.786.
• Kháng cự Weekly.
• Thanh khoản phía trên dày.

↓

Trạng thái

Cấu trúc thị trường

• Xu hướng tăng.

Trạng thái thị trường

• Mở rộng.

Vùng rủi ro

• Rủi ro cao.

────────

Ví dụ 03 · Đi ngang

Quan sát

• Weekly: Đi ngang.
• Daily: Biến động thu hẹp.
• Volume giảm.
• Thanh khoản cân bằng.

↓

Trạng thái

Cấu trúc thị trường

• Đi ngang.

Trạng thái thị trường

• Tích lũy.

Vùng rủi ro

• Rủi ro thấp.

────────

Nguyên tắc

Hành vi giống nhau có thể mang ý nghĩa khác nhau.

Bối cảnh quyết định cách hiểu Hành vi.

────────

Triết lý

Bối cảnh quyết định ý nghĩa của Hành vi.

────────

03 · Động lượng

> Hiểu sự thay đổi của lực thị trường.

────────

Mục đích

Động lượng là tầng thứ ba của Hệ thống suy luận.

Tầng này mô tả sự thay đổi của lực thị trường.

────────

Câu hỏi

> Lực đang mạnh lên, yếu đi hay đổi hướng?

────────

Đầu vào

• Trạng thái hành vi.
• Trạng thái bối cảnh.

────────

Đầu ra

Trạng thái động lượng, làm đầu vào cho tầng Cấu trúc.

────────

Luồng

```text
Hành vi

↓

Bối cảnh

↓

Động lượng

↓

Cấu trúc
```

────────

Cấu trúc

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

────────

Triết lý

Lực thay đổi trước.

Cấu trúc xác nhận sau.

────────

Định nghĩa

> Bản chất của Động lượng.

────────

Bản chất

Động lượng phản ánh sự thay đổi của lực thị trường.

Động lượng được hình thành từ ba nhóm tín hiệu.

────────

Thành phần

Lực giao dịch

Phản ánh phía đang chủ động tạo ra động lượng.

• Delta
• CVD
• Aggressive Orders
• Auction Flow

────────

Cường độ giao dịch

Phản ánh mức độ mạnh hay yếu của lực thị trường.

• Volume
• VPIN

────────

Động lượng giá

Phản ánh tốc độ thay đổi của giá.

• RSI
• Độ dốc EMA
• Velocity

────────

Ba nhóm tín hiệu này cùng phản ánh sự thay đổi của lực thị trường.

────────

Đầu ra

Tầng Động lượng tạo ra Trạng thái động lượng.

Trạng thái động lượng trở thành đầu vào của tầng Cấu trúc.

────────

Triết lý

Lực thay đổi trước.

Giá xác nhận sau.

────────

Quan sát

> Quan sát sự thay đổi của lực thị trường.

────────

Mục đích

Quan sát sự thay đổi của lực thị trường.

Động lượng phản ánh sự thay đổi của lực thị trường.

────────

Quan sát

Lực giao dịch

Quan sát phía đang chủ động tạo ra động lượng.

• Delta
• CVD
• Aggressive Orders
• Auction Flow

────────

Cường độ giao dịch

Quan sát mức độ mạnh hay yếu của lực thị trường.

• Volume
• VPIN

────────

Động lượng giá

Quan sát tốc độ thay đổi của giá.

• RSI
• Độ dốc EMA
• Price Velocity
• Momentum Divergence

────────

Nguyên tắc

Động lượng luôn được đánh giá theo sự thay đổi.

Sự thay đổi quan trọng hơn giá trị tuyệt đối.

Động lượng luôn được hiểu trong Bối cảnh hiện tại.

────────

Triết lý

Động lượng phản ánh sự thay đổi của lực.

────────

Trạng thái

> Mô tả trạng thái hiện tại của Động lượng.

────────

Mục đích

Trạng thái mô tả trạng thái hiện tại của Động lượng.

Mỗi trạng thái phản ánh sự thay đổi của lực thị trường.

────────

Các trạng thái

Hướng của lực

Ưu thế mua

Lực mua đang chiếm ưu thế.

────────

Ưu thế bán

Lực bán đang chiếm ưu thế.

────────

Cân bằng

Lực mua và lực bán tương đối cân bằng.

────────

Mức độ thay đổi

Gia tăng

Động lượng đang mạnh lên.

────────

Suy yếu

Động lượng đang yếu đi.

────────

Cạn dần

Động lượng đang mất dần sức mạnh.

────────

Quan hệ giữa lực và giá

Đồng thuận

Động lượng và giá cùng xác nhận một hướng.

────────

Phân kỳ

Động lượng và giá bắt đầu đi theo hai hướng khác nhau.

────────

Nguyên tắc

Trạng thái phản ánh Động lượng hiện tại.

Trạng thái chỉ thay đổi khi Động lượng thay đổi.

────────

Triết lý

Trạng thái phản ánh sức mạnh của lực thị trường.

────────

Chuyển đổi

> Mô tả cách Động lượng thay đổi theo thời gian.

────────

Mục đích

Chuyển đổi mô tả sự thay đổi của Động lượng.

Mỗi chuyển đổi phản ánh sự thay đổi của lực thị trường.

────────

Ví dụ

Chuyển đổi hướng của lực

```text
Cân bằng

↓

Ưu thế mua
```

────────

```text
Ưu thế mua

↓

Cân bằng
```

────────

```text
Cân bằng

↓

Ưu thế bán
```

────────

Chuyển đổi mức độ thay đổi

```text
Gia tăng

↓

Suy yếu

↓

Cạn dần
```

────────

```text
Cạn dần

↓

Gia tăng
```

────────

Chuyển đổi quan hệ giữa lực và giá

```text
Đồng thuận

↓

Phân kỳ
```

────────

```text
Phân kỳ

↓

Đồng thuận
```

────────

Nguyên tắc

Mọi Chuyển đổi đều bắt đầu từ quan sát mới.

Trạng thái chỉ chuyển đổi khi có đủ bằng chứng.

Động lượng thay đổi trước.

Cấu trúc xác nhận sau.

────────

Triết lý

Chuyển đổi phản ánh sự thay đổi của Động lượng.

────────

Ví dụ

────────

Ví dụ 01 · Động lượng tăng mạnh

Quan sát

• Delta tăng.
• CVD tăng.
• Volume tăng.
• Auction Flow tăng.

↓

Trạng thái

Hướng của lực

• Ưu thế mua.

Mức độ thay đổi

• Gia tăng.

Quan hệ giữa lực và giá

• Đồng thuận.

────────

Ví dụ 02 · Phân kỳ

Quan sát

• Giá tăng.
• CVD giảm.
• RSI giảm.
• Volume giảm.

↓

Trạng thái

Hướng của lực

• Ưu thế mua.

Mức độ thay đổi

• Suy yếu.

Quan hệ giữa lực và giá

• Phân kỳ.

────────

Ví dụ 03 · Động lượng suy yếu

Quan sát

• Volume giảm.
• Delta giảm.
• Auction Flow suy yếu.
• RSI giảm.

↓

Trạng thái

Hướng của lực

• Cân bằng.

Mức độ thay đổi

• Cạn dần.

Quan hệ giữa lực và giá

• Đồng thuận.

────────

Nguyên tắc

Quan sát tạo nên Trạng thái.

Trạng thái phản ánh Động lượng hiện tại.

Động lượng mạnh chưa đồng nghĩa với Cấu trúc đã xác nhận.

Động lượng luôn được hiểu trong Bối cảnh hiện tại.

────────

Triết lý

Động lượng giúp hiểu nhịp vận động của lực.

────────

04 · Cấu trúc

> Hiểu cách thị trường thay đổi dưới tác động của lực.

────────

Mục đích

Cấu trúc là tầng thứ tư của Hệ thống suy luận.

Tầng này mô tả cách thị trường thay đổi dưới tác động của Động lượng.

Cấu trúc phản ánh kết quả mà lực thị trường tạo ra.

────────

Câu hỏi

> Sự thay đổi của lực đã tạo ra thay đổi nào trên cấu trúc?

────────

Đầu vào

• Trạng thái hành vi.
• Trạng thái bối cảnh.
• Trạng thái động lượng.

────────

Đầu ra

Trạng thái cấu trúc.

Đây là đầu vào của tầng Chất lượng.

────────

Luồng

```text
Động lượng

↓

Cấu trúc

↓

Chất lượng
```

────────

Cấu trúc

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

────────

Triết lý

Động lượng tạo nên chuyển động.

Cấu trúc xác nhận kết quả.

────────

Định nghĩa

> Bản chất của Cấu trúc.

────────

Bản chất

Cấu trúc phản ánh kết quả mà Động lượng tạo ra.

Cấu trúc xác nhận sự thay đổi của thị trường.

────────

Thành phần

Cấu trúc được xác định thông qua bốn nhóm thành phần.

────────

Hình thái cấu trúc

Phản ánh hình dạng hiện tại của cấu trúc thị trường.

• Swing High
• Swing Low

────────

Sự kiện trên cấu trúc

Phản ánh các thay đổi trực tiếp của cấu trúc.

• Break
• Retest
• Liquidity Sweep

────────

Phản ứng của cấu trúc

Phản ánh cách thị trường xác nhận cấu trúc mới.

• Acceptance
• Rejection

────────

Kết quả của cấu trúc

Phản ánh kết quả cuối cùng sau khi cấu trúc hình thành.

• Continuation
• Failure
• Range Development

────────

Bốn nhóm thành phần này cùng phản ánh sự thay đổi của cấu trúc thị trường.

────────

Đầu ra

Tầng Cấu trúc tạo ra Vector trạng thái cấu trúc.

Vector trạng thái cấu trúc trở thành đầu vào của tầng Chất lượng.

────────

Triết lý

Cấu trúc phản ánh kết quả của Động lượng.

────────

Quan sát

> Quan sát cách cấu trúc thị trường thay đổi dưới tác động của Động lượng.

────────

Mục đích

Quan sát sự thay đổi của cấu trúc thị trường.

Cấu trúc phản ánh kết quả mà Động lượng tạo ra.

────────

Quan sát

Hình thái cấu trúc

Quan sát hình dạng hiện tại của cấu trúc.

• Swing High
• Swing Low

────────

Sự kiện trên cấu trúc

Quan sát các thay đổi trực tiếp của cấu trúc.

• Break
• Retest
• Liquidity Sweep

────────

Phản ứng của cấu trúc

Quan sát cách thị trường xác nhận cấu trúc mới.

• Acceptance
• Rejection

────────

Kết quả của cấu trúc

Quan sát kết quả sau khi cấu trúc hình thành.

• Continuation
• Failure
• Range Development

────────

Nguyên tắc

Quan sát luôn bắt đầu từ cấu trúc hiện tại.

Cấu trúc được đánh giá theo kết quả tạo ra.

Cấu trúc luôn được hiểu trong Bối cảnh hiện tại.

────────

Triết lý

Động lượng tạo ra thay đổi.

Cấu trúc xác nhận kết quả.

────────

Trạng thái

> Mô tả trạng thái hiện tại của Cấu trúc.

────────

Mục đích

Trạng thái mô tả kết quả mà Động lượng tạo ra trên cấu trúc thị trường.

Mỗi trạng thái phản ánh hình thái hiện tại của Cấu trúc.

────────

Các trạng thái

Hình thái cấu trúc

Xu hướng tăng

Cấu trúc tăng được xác nhận.

────────

Xu hướng giảm

Cấu trúc giảm được xác nhận.

────────

Đi ngang

Cấu trúc cân bằng.

────────

Sự kiện trên cấu trúc

Mở rộng

Cấu trúc mở rộng sang một vùng giá mới.

────────

Tiếp diễn

Cấu trúc tiếp tục theo hướng hiện tại.

────────

Thất bại

Cấu trúc mới chưa được xác nhận.

────────

Phản ứng của cấu trúc

Acceptance

Thị trường chấp nhận vùng giá mới.

────────

Rejection

Thị trường từ chối vùng giá mới và quay trở lại vùng giá trước đó.

────────

Kết quả của cấu trúc

Continuation

Cấu trúc tiếp tục vận động theo hướng hiện tại.

────────

Failure

Cấu trúc không duy trì được hướng vận động.

────────

Range Development

Cấu trúc phát triển thành vùng cân bằng mới.

────────

Nguyên tắc

Trạng thái phản ánh Cấu trúc hiện tại.

Trạng thái chỉ thay đổi khi Cấu trúc thay đổi.

Mỗi nhóm trạng thái phản ánh một khía cạnh khác nhau của Cấu trúc.

────────

Triết lý

Trạng thái phản ánh kết quả của Động lượng.

────────

Chuyển đổi

> Mô tả cách Cấu trúc thay đổi theo thời gian.

────────

Mục đích

Chuyển đổi mô tả sự thay đổi của Cấu trúc.

Mỗi chuyển đổi phản ánh kết quả mà Động lượng tạo ra trên thị trường.

────────

Ví dụ

Chuyển đổi hình thái cấu trúc

```text
Đi ngang

↓

Xu hướng tăng
```

────────

```text
Xu hướng tăng

↓

Đi ngang
```

────────

```text
Đi ngang

↓

Xu hướng giảm
```

────────

Chuyển đổi sự kiện trên cấu trúc

```text
Mở rộng

↓

Tiếp diễn
```

────────

```text
Tiếp diễn

↓

Thất bại
```

────────

```text
Thất bại

↓

Mở rộng
```

────────

Chuyển đổi phản ứng của cấu trúc

```text
Acceptance

↓

Rejection
```

────────

```text
Rejection

↓

Acceptance
```

────────

Chuyển đổi kết quả của cấu trúc

```text
Continuation

↓

Failure
```

────────

```text
Failure

↓

Range Development
```

────────

```text
Range Development

↓

Continuation
```

────────

Nguyên tắc

Mọi Chuyển đổi đều bắt đầu từ Cấu trúc mới.

Trạng thái chỉ chuyển đổi khi có đủ bằng chứng.

Động lượng thay đổi trước.

Cấu trúc xác nhận sau.

────────

Triết lý

Chuyển đổi phản ánh sự thay đổi của Cấu trúc.

────────

Ví dụ

────────

Ví dụ 01 · Xu hướng tăng

Đầu vào

Trạng thái động lượng

• Hướng của lực: Ưu thế mua.
• Mức độ thay đổi: Gia tăng.
• Quan hệ giữa lực và giá: Đồng thuận.

↓

Quan sát

• Break.
• Acceptance.

↓

Trạng thái

Hình thái cấu trúc

• Xu hướng tăng.

Sự kiện trên cấu trúc

• Mở rộng.

Phản ứng của cấu trúc

• Acceptance.

Kết quả của cấu trúc

• Continuation.

────────

Ví dụ 02 · Đi ngang

Đầu vào

Trạng thái động lượng

• Hướng của lực: Ưu thế mua.
• Mức độ thay đổi: Suy yếu.
• Quan hệ giữa lực và giá: Phân kỳ.

↓

Quan sát

• Break.
• Failure.

↓

Trạng thái

Hình thái cấu trúc

• Đi ngang.

Sự kiện trên cấu trúc

• Thất bại.

Phản ứng của cấu trúc

• Rejection.

Kết quả của cấu trúc

• Failure.

────────

Ví dụ 03 · Xu hướng giảm

Đầu vào

Trạng thái động lượng

• Hướng của lực: Ưu thế bán.
• Mức độ thay đổi: Gia tăng.
• Quan hệ giữa lực và giá: Đồng thuận.

↓

Quan sát

• Liquidity Sweep.
• Acceptance.

↓

Trạng thái

Hình thái cấu trúc

• Xu hướng giảm.

Sự kiện trên cấu trúc

• Tiếp diễn.

Phản ứng của cấu trúc

• Acceptance.

Kết quả của cấu trúc

• Continuation.

────────

Nguyên tắc

Quan sát tạo nên Trạng thái.

Cấu trúc xác nhận kết quả của Động lượng.

Động lượng mạnh chưa đồng nghĩa với Cấu trúc đã xác nhận.

Cấu trúc luôn được hiểu trong Bối cảnh hiện tại.

────────

Triết lý

Cấu trúc xác nhận kết quả mà Động lượng tạo ra.

────────

05 · Chất lượng

> Đánh giá độ tin cậy của các bằng chứng suy luận.

────────

Mục đích

Chất lượng là tầng thứ năm của Hệ thống suy luận.

Tầng này đánh giá mức độ nhất quán giữa các bằng chứng đã được hình thành.

Tầng này không tạo thêm bằng chứng.

Tầng này đánh giá chất lượng của các bằng chứng hiện có.

────────

Câu hỏi

Các bằng chứng hiện tại đáng tin cậy đến mức nào?

────────

Đầu vào

• Trạng thái hành vi.
• Trạng thái bối cảnh.
• Trạng thái động lượng.
• Trạng thái cấu trúc.

────────

Đầu ra

Trạng thái chất lượng.

Đây là đầu vào của tầng Ra quyết định.

────────

Luồng

```text
Cấu trúc

↓

Chất lượng

↓

Ra quyết định
```

────────

Cấu trúc

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

────────

Triết lý

Chất lượng của quyết định bắt đầu từ chất lượng của bằng chứng.

────────

Định nghĩa

> Bản chất của Chất lượng.

────────

Bản chất

Chất lượng phản ánh mức độ tin cậy của các bằng chứng hiện có.

Chất lượng được hình thành từ mức độ đồng thuận giữa các tầng suy luận trước đó.

Chất lượng không tạo ra bằng chứng mới.

────────

Thành phần

Chất lượng được đánh giá thông qua:

• Mức độ đồng thuận của Hành vi.
• Mức độ đồng thuận của Bối cảnh.
• Mức độ đồng thuận của Động lượng.
• Mức độ đồng thuận của Cấu trúc.
• Mức độ đồng thuận đa khung thời gian.
• Môi trường rủi ro.

Những thành phần này cùng phản ánh độ tin cậy của hệ thống bằng chứng.

────────

Đầu ra

Tầng Chất lượng tạo ra Trạng thái chất lượng.

Trạng thái chất lượng trở thành đầu vào của tầng Ra quyết định.

────────

Triết lý

Chất lượng phản ánh độ tin cậy của các bằng chứng hiện có.

────────

Quan sát

> Quan sát mức độ nhất quán của hệ thống bằng chứng.

────────

Mục đích

Quan sát mức độ nhất quán giữa các bằng chứng hiện có.

Chất lượng phản ánh mức độ đồng thuận của toàn bộ hệ thống suy luận.

────────

Quan sát

Mức độ đồng thuận

• Đồng thuận của Hành vi.
• Đồng thuận của Bối cảnh.
• Đồng thuận của Động lượng.
• Đồng thuận của Cấu trúc.
• Đồng thuận đa khung thời gian.

────────

Môi trường

• Môi trường rủi ro.

────────

Quan hệ giữa các tầng

• Xác nhận.
• Xung đột.

────────

Nguyên tắc

Sự đồng thuận làm tăng độ tin cậy.

Sự xung đột làm giảm độ tin cậy.

Chất lượng luôn được đánh giá trên các bằng chứng hiện có.

────────

Triết lý

Chất lượng phản ánh mức độ tin cậy của hệ thống bằng chứng.

────────

Trạng thái

> Mô tả mức độ tin cậy hiện tại của hệ thống bằng chứng.

────────

Mục đích

Trạng thái phản ánh mức độ tin cậy hiện tại của hệ thống bằng chứng.

────────

Các trạng thái

Rất cao

Các bằng chứng đồng thuận rất mạnh.

────────

Cao

Các bằng chứng đồng thuận rõ ràng.

────────

Trung bình

Các bằng chứng đã hình thành sự đồng thuận nhưng vẫn còn thiếu xác nhận.

────────

Thấp

Các bằng chứng xuất hiện nhiều xung đột.

────────

Không hợp lệ

Các bằng chứng chưa đủ điều kiện để đưa ra quyết định.

────────

Nguyên tắc

Trạng thái phản ánh mức độ tin cậy hiện tại của hệ thống bằng chứng.

Trạng thái thay đổi khi mức độ đồng thuận giữa các bằng chứng thay đổi.

────────

Triết lý

Trạng thái phản ánh mức độ tin cậy của hệ thống bằng chứng.

────────

Chuyển đổi

> Mô tả sự thay đổi của Chất lượng theo thời gian.

────────

Mục đích

Chuyển đổi mô tả sự thay đổi của mức độ tin cậy của hệ thống bằng chứng.

────────

Ví dụ

```text
Trung bình

↓

Cao

↓

Rất cao
```

────────

```text
Rất cao

↓

Cao

↓

Trung bình
```

────────

```text
Trung bình

↓

Thấp

↓

Không hợp lệ
```

────────

Nguyên tắc

Chất lượng thay đổi khi mức độ đồng thuận giữa các bằng chứng thay đổi.

Trạng thái chỉ chuyển đổi khi chất lượng của hệ thống bằng chứng thay đổi.

Sự đồng thuận làm tăng độ tin cậy.

Sự xung đột làm giảm độ tin cậy.

────────

Triết lý

Chuyển đổi phản ánh sự thay đổi của Chất lượng.

────────

Ví dụ

────────

Ví dụ 01 · Rất cao

Đầu vào

Trạng thái hành vi

• Người mua chiếm ưu thế.

Trạng thái bối cảnh

• Xu hướng tăng.

Trạng thái động lượng

• Hướng của lực: Ưu thế mua.
• Mức độ thay đổi: Gia tăng.
• Quan hệ giữa lực và giá: Đồng thuận.

Trạng thái cấu trúc

• Hình thái cấu trúc: Xu hướng tăng.
• Sự kiện trên cấu trúc: Tiếp diễn.
• Phản ứng của cấu trúc: Acceptance.
• Kết quả của cấu trúc: Continuation.

↓

Trạng thái chất lượng

• Rất cao.

────────

Ví dụ 02 · Trung bình

Đầu vào

Trạng thái hành vi

• Người mua chiếm ưu thế.

Trạng thái bối cảnh

• Xu hướng tăng.

Trạng thái động lượng

• Hướng của lực: Ưu thế bán.
• Mức độ thay đổi: Gia tăng.
• Quan hệ giữa lực và giá: Phân kỳ.

Trạng thái cấu trúc

• Hình thái cấu trúc: Xu hướng tăng.
• Sự kiện trên cấu trúc: Tiếp diễn.
• Phản ứng của cấu trúc: Acceptance.
• Kết quả của cấu trúc: Continuation.

↓

Trạng thái chất lượng

• Trung bình.

────────

Ví dụ 03 · Thấp

Đầu vào

Trạng thái hành vi

• Người bán chiếm ưu thế.

Trạng thái bối cảnh

• Xu hướng tăng.

Trạng thái động lượng

• Hướng của lực: Ưu thế mua.
• Mức độ thay đổi: Gia tăng.
• Quan hệ giữa lực và giá: Đồng thuận.

Trạng thái cấu trúc

• Hình thái cấu trúc: Đi ngang.
• Sự kiện trên cấu trúc: Thất bại.
• Phản ứng của cấu trúc: Rejection.
• Kết quả của cấu trúc: Failure.

↓

Trạng thái chất lượng

• Thấp.

────────

Nguyên tắc

Chất lượng phản ánh mức độ đồng thuận giữa các bằng chứng.

Một tầng mạnh không đủ tạo nên Chất lượng cao.

Chất lượng cao chỉ xuất hiện khi các tầng cùng hướng tới một kết luận.

────────

Triết lý

Chất lượng phản ánh mức độ tin cậy của hệ thống bằng chứng.

────────

06 · Ra quyết định

> Chuyển toàn bộ bằng chứng thành một kết luận duy nhất.

────────

Mục đích

Ra quyết định là tầng thứ sáu của Hệ thống suy luận.

Tầng này tổng hợp toàn bộ bằng chứng từ các tầng trước.

Tầng này tạo ra kết luận suy luận tại thời điểm hiện tại.

────────

Câu hỏi

Kết luận hợp lý nhất tại thời điểm hiện tại là gì?

────────

Đầu vào

• Trạng thái hành vi.
• Trạng thái bối cảnh.
• Trạng thái động lượng.
• Trạng thái cấu trúc.
• Trạng thái chất lượng.

────────

Đầu ra

Trạng thái quyết định.

Đây là đầu vào của tầng Trọng số tín hiệu.

────────

Luồng

```text
Chất lượng

↓

Ra quyết định

↓

Trọng số tín hiệu
```

────────

Cấu trúc

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

────────

Triết lý

Ra quyết định là điểm hội tụ của toàn bộ quá trình suy luận.

────────

Định nghĩa

> Bản chất của Ra quyết định.

────────

Bản chất

Ra quyết định là kết quả của toàn bộ quá trình suy luận.

Ra quyết định tổng hợp các bằng chứng hiện có thành một kết luận duy nhất.

Kết luận phản ánh phương án hợp lý nhất tại thời điểm hiện tại.

────────

Thành phần

Ra quyết định được hình thành từ:

• Trạng thái hành vi.
• Trạng thái bối cảnh.
• Trạng thái động lượng.
• Trạng thái cấu trúc.
• Trạng thái chất lượng.

Những thành phần này cùng tạo nên kết luận hiện tại.

────────

Đầu ra

Tầng Ra quyết định tạo ra Trạng thái quyết định.

Trạng thái quyết định trở thành đầu vào của tầng Trọng số tín hiệu.

────────

Triết lý

Ra quyết định phản ánh kết luận hiện tại của Hệ thống suy luận.

────────

Quan sát

> Quan sát toàn bộ kết quả suy luận trước khi tạo Ra quyết định.

────────

Mục đích

Quan sát toàn bộ kết quả từ các tầng suy luận trước đó.

Ra quyết định tổng hợp các trạng thái hiện có thành một kết luận duy nhất.

────────

Quan sát

• Trạng thái hành vi.
• Trạng thái bối cảnh.
• Trạng thái động lượng.
• Trạng thái cấu trúc.
• Trạng thái chất lượng.

────────

Nguyên tắc

Ra quyết định luôn kế thừa toàn bộ kết quả từ các tầng suy luận trước đó.

Ra quyết định không tạo thêm bằng chứng mới.

Ra quyết định phản ánh toàn bộ bằng chứng hiện có.

────────

Triết lý

Ra quyết định được xây dựng từ toàn bộ bằng chứng hiện có.

────────

Trạng thái

> Mô tả định hướng hiện tại của Hệ thống suy luận.

────────

Mục đích

Trạng thái phản ánh định hướng hiện tại của Hệ thống suy luận.

────────

Các trạng thái

Định hướng tăng

Hệ thống suy luận ưu tiên kịch bản tăng.

────────

Định hướng giảm

Hệ thống suy luận ưu tiên kịch bản giảm.

────────

Trung lập

Hệ thống suy luận chưa ưu tiên kịch bản nào.

Tiếp tục quan sát.

────────

Chưa đủ cơ sở

Các bằng chứng hiện tại chưa đủ để hình thành một định hướng đáng tin cậy.

────────

Nguyên tắc

Ra quyết định chỉ có một trạng thái tại một thời điểm.

Trạng thái thay đổi khi bằng chứng thay đổi.

Ra quyết định luôn kế thừa toàn bộ kết quả từ các tầng suy luận trước đó.

────────

Triết lý

Trạng thái phản ánh định hướng hiện tại của Hệ thống suy luận.

────────

Chuyển đổi

> Mô tả sự thay đổi của Ra quyết định theo thời gian.

────────

Mục đích

Chuyển đổi mô tả sự thay đổi của định hướng khi hệ thống bằng chứng thay đổi.

────────

Ví dụ

```text
Trung lập

↓

Định hướng tăng
```

────────

```text
Định hướng tăng

↓

Trung lập
```

────────

```text
Định hướng tăng

↓

Định hướng giảm
```

────────

```text
Chưa đủ cơ sở

↓

Trung lập

↓

Định hướng tăng
```

────────

Nguyên tắc

Ra quyết định thay đổi khi hệ thống bằng chứng thay đổi.

Trạng thái chỉ chuyển đổi khi kết luận của Hệ thống suy luận thay đổi.

Ra quyết định luôn kế thừa kết quả từ các tầng suy luận trước đó.

────────

Triết lý

Chuyển đổi phản ánh sự thay đổi của định hướng.

────────

Ví dụ

────────

Ví dụ 01

Đầu vào

Trạng thái hành vi

• Người mua chiếm ưu thế.

Trạng thái bối cảnh

• Xu hướng tăng.

Trạng thái động lượng

• Hướng của lực: Ưu thế mua.
• Mức độ thay đổi: Gia tăng.
• Quan hệ giữa lực và giá: Đồng thuận.

Trạng thái cấu trúc

• Hình thái cấu trúc: Xu hướng tăng.
• Xác nhận cấu trúc: Acceptance.
• Kết quả vận động: Continuation.

Trạng thái chất lượng

• Rất cao.

↓

Trạng thái quyết định

• Định hướng tăng.

────────

Ví dụ 02

Đầu vào

Trạng thái hành vi

• Người mua chiếm ưu thế.

Trạng thái bối cảnh

• Xu hướng tăng.

Trạng thái động lượng

• Hướng của lực: Ưu thế bán.
• Mức độ thay đổi: Gia tăng.
• Quan hệ giữa lực và giá: Phân kỳ.

Trạng thái cấu trúc

• Hình thái cấu trúc: Xu hướng tăng.
• Xác nhận cấu trúc: Acceptance.
• Kết quả vận động: Continuation.

Trạng thái chất lượng

• Trung bình.

↓

Trạng thái quyết định

• Trung lập.

────────

Ví dụ 03

Đầu vào

Trạng thái hành vi

• Người bán chiếm ưu thế.

Trạng thái bối cảnh

• Xu hướng giảm.

Trạng thái động lượng

• Hướng của lực: Ưu thế bán.
• Mức độ thay đổi: Gia tăng.
• Quan hệ giữa lực và giá: Đồng thuận.

Trạng thái cấu trúc

• Hình thái cấu trúc: Xu hướng giảm.
• Xác nhận cấu trúc: Acceptance.
• Kết quả vận động: Continuation.

Trạng thái chất lượng

• Rất cao.

↓

Trạng thái quyết định

• Định hướng giảm.

────────

Ví dụ 04

Đầu vào

Trạng thái chất lượng

• Thấp.

↓

Trạng thái quyết định

• Chưa đủ cơ sở.

────────

Nguyên tắc

Ra quyết định luôn được xây dựng từ toàn bộ kết quả của các tầng suy luận trước đó.

Ra quyết định chỉ phản ánh kết luận hợp lý nhất tại thời điểm hiện tại.

────────

Triết lý

Ra quyết định phản ánh kết luận hiện tại của Hệ thống suy luận.

────────

07 · Trọng số tín hiệu

> Giải thích mức độ ảnh hưởng của từng bằng chứng đến Trạng thái quyết định.

────────

Mục đích

Trọng số tín hiệu là tầng thứ bảy của Hệ thống suy luận.

Tầng này giải thích cách Trạng thái quyết định hiện tại được hình thành.

Tầng này lượng hóa mức độ ảnh hưởng của từng tầng suy luận đối với Trạng thái quyết định.

Đồng thời, tầng này chuẩn hóa toàn bộ kết quả suy luận thành một Chữ ký tín hiệu để phục vụ tầng Không gian kịch bản.

────────

Câu hỏi

Điều gì ảnh hưởng nhiều nhất đến Trạng thái quyết định hiện tại?

────────

Đầu vào

• Trạng thái hành vi.
• Trạng thái bối cảnh.
• Trạng thái động lượng.
• Trạng thái cấu trúc.
• Trạng thái chất lượng.
• Trạng thái quyết định.

────────

Đầu ra

• Chữ ký tín hiệu.

Chữ ký tín hiệu trở thành đầu vào của tầng Không gian kịch bản.

────────

Vai trò trong Hệ thống suy luận

```text
Ra quyết định

↓

Trọng số tín hiệu

↓

Không gian kịch bản
```

────────

Cấu trúc

```text
01 · Định nghĩa

↓

02 · Quan sát

↓

03 · Chữ ký tín hiệu

↓

04 · Ví dụ
```

────────

Triết lý

Mọi Trạng thái quyết định đều có thể được giải thích.

Trọng số tín hiệu phản ánh mức độ đóng góp của từng tầng vào Trạng thái quyết định.

Chữ ký tín hiệu chuẩn hóa toàn bộ kết quả suy luận thành một dấu vết duy nhất.

────────

Định nghĩa

> Bản chất của Hành vi.

────────

Bản chất

Hành vi là sự biểu hiện của quá trình đấu giá giữa người mua và người bán.

Hành vi được phản ánh thông qua dữ liệu thị trường tại thời điểm quan sát.

────────

Thành phần

Hành vi được phản ánh thông qua:

• Giá
• Khối lượng
• Thời gian
• Lệnh chủ động
• Thanh khoản

Những thành phần này cùng phản ánh hành vi hiện tại của thị trường.

────────

Đầu ra

Tầng Hành vi tạo ra Trạng thái hành vi.

Trạng thái hành vi trở thành đầu vào của tầng Bối cảnh.

────────

> Hành vi phản ánh điều đang thực sự diễn ra giữa người mua và người bán.

────────

Quan sát

> Quan sát sự thay đổi của lực thị trường.

────────

Mục đích

Quan sát sự thay đổi của lực thị trường.

Động lượng phản ánh sự thay đổi của lực thị trường.

────────

Quan sát

Lực giao dịch

Quan sát phía đang chủ động tạo ra động lượng.

• Delta
• CVD
• Aggressive Orders
• Auction Flow

────────

Cường độ giao dịch

Quan sát mức độ mạnh hay yếu của lực thị trường.

• Volume
• VPIN

────────

Động lượng giá

Quan sát tốc độ thay đổi của giá.

• RSI
• Độ dốc EMA
• Price Velocity
• Momentum Divergence

────────

Nguyên tắc

Động lượng luôn được đánh giá theo sự thay đổi.

Sự thay đổi quan trọng hơn giá trị tuyệt đối.

Động lượng luôn được hiểu trong Bối cảnh hiện tại.

────────

Triết lý

Động lượng phản ánh sự thay đổi của lực.

────────

Trạng thái

> Mô tả trạng thái hiện tại của Bối cảnh.

────────

Mục đích

Trạng thái mô tả môi trường mà Hành vi đang diễn ra.

Mỗi trạng thái phản ánh điều kiện hiện tại của thị trường.

────────

Các trạng thái

Cấu trúc thị trường

Xu hướng tăng

Bối cảnh ưu tiên xu hướng tăng.

────────

Xu hướng giảm

Bối cảnh ưu tiên xu hướng giảm.

────────

Đi ngang

Thị trường đang ở trạng thái cân bằng.

────────

Trạng thái thị trường

Mở rộng

Thị trường đang mở rộng khỏi vùng giá trị trước đó.

────────

Tích lũy

Thị trường đang vận động trong một vùng giá hẹp.

────────

Vùng rủi ro

Rủi ro cao

Thị trường đang ở vùng có khả năng Chuyển đổi cao.

────────

Rủi ro thấp

Thị trường đang ở vùng thuận lợi cho xu hướng hiện tại tiếp diễn.

────────

Nguyên tắc

Trạng thái phản ánh bối cảnh hiện tại.

Trạng thái chỉ thay đổi khi bối cảnh thay đổi.

────────

Triết lý

Trạng thái phản ánh môi trường hiện tại của Hành vi.

────────

Ví dụ

────────

Ví dụ 01

Trạng thái quyết định

• Định hướng tăng.

↓

Trọng số tín hiệu

• Trọng số của Động lượng: 42%
• Trọng số của Bối cảnh: 28%
• Trọng số của Cấu trúc: 16%
• Trọng số của Hành vi: 9%
• Trọng số của Chất lượng: 5%

↓

Chữ ký tín hiệu

```text
SIG-8A24
```

────────

Ví dụ 02

Trạng thái quyết định

• Trung lập.

↓

Trọng số tín hiệu

• Trọng số của Bối cảnh: 31%
• Trọng số của Cấu trúc: 24%
• Trọng số của Động lượng: 22%
• Trọng số của Hành vi: 14%
• Trọng số của Chất lượng: 9%

↓

Chữ ký tín hiệu

```text
SIG-3F91
```

────────

Nguyên tắc

Trọng số tín hiệu phản ánh mức độ đóng góp của từng tầng.

Tổng các Trọng số tín hiệu phản ánh cách Trạng thái quyết định được hình thành.

Chữ ký tín hiệu chuẩn hóa toàn bộ kết quả suy luận thành một dấu vết duy nhất.

────────

Triết lý

Trọng số tín hiệu giải thích cách Trạng thái quyết định được hình thành.

Chữ ký tín hiệu chuẩn hóa toàn bộ quá trình suy luận để phục vụ Tri thức tích luỹ.

────────

08 · Không gian kịch bản

> Biểu diễn sự bất định bằng các kịch bản.

────────

Mục đích

Không gian kịch bản là tầng thứ tám của Hệ thống suy luận.

Tầng này tổ chức các kịch bản hợp lý từ Trạng thái quyết định hiện tại.

Trọng số tín hiệu được sử dụng để hình thành các kịch bản và xác suất suy luận.

Sau khi các kịch bản được hình thành, Chữ ký tín hiệu được sử dụng để tham khảo Tri thức tích luỹ nhằm đánh giá và hiệu chỉnh mức độ tin cậy của từng kịch bản.

Mỗi kịch bản được mô tả thông qua:

• Suy luận.
• Điều kiện.
• Xác suất suy luận.
• Xác suất hiệu chỉnh.
• Điều kiện vô hiệu.

────────

Câu hỏi

Theo kết quả suy luận hiện tại, những kịch bản nào có nhiều khả năng xảy ra?

→ Trọng số tín hiệu.

────────

Theo kinh nghiệm đã được tích luỹ, mức độ tin cậy của các kịch bản đó có thay đổi không?

→ Chữ ký tín hiệu + Tri thức tích luỹ.

────────

Đầu vào

• Trạng thái hành vi.
• Trạng thái bối cảnh.
• Trạng thái động lượng.
• Trạng thái cấu trúc.
• Trạng thái chất lượng.
• Trạng thái quyết định.
• Trọng số tín hiệu.
• Chữ ký tín hiệu.

────────

Đầu ra

Không gian kịch bản.

Mỗi kịch bản bao gồm:

• Xác suất suy luận.
• Xác suất hiệu chỉnh (nếu có).

Không gian kịch bản trở thành đầu vào của tầng Kế hoạch thực thi.

────────

Vai trò trong Hệ thống suy luận

```text
# Trọng số tín hiệu
        │
        ▼
# Không gian kịch bản
        │
        ├────────► Tham khảo # Tri thức tích luỹ
        ▼
# Kế hoạch thực thi
```

────────

Cấu trúc

```text
# 01 · Định nghĩa

↓

# 02 · Quan sát

↓

# 03 · Kịch bản

↓

# 04 · Hiệu chỉnh

↓

# 05 · Ví dụ
```

────────

Triết lý

Kết quả suy luận hiện tại hình thành các kịch bản.

Tri thức tích luỹ cung cấp kinh nghiệm để Không gian kịch bản tham khảo và hiệu chỉnh mức độ tin cậy của các kịch bản.

────────

Định nghĩa

> Bản chất của Không gian kịch bản.

────────

Bản chất

Không gian kịch bản biểu diễn các khả năng đang tồn tại.

Mỗi kịch bản đại diện cho một khả năng phát triển hợp lý của thị trường.

Không gian kịch bản không khẳng định một tương lai duy nhất.

Không gian kịch bản tổ chức các khả năng hợp lý dựa trên kết quả suy luận hiện tại.

Sau khi các kịch bản được hình thành, Không gian kịch bản có thể tham khảo Tri thức tích luỹ để hiệu chỉnh mức độ tin cậy của từng kịch bản.

────────

Thành phần

Một kịch bản bao gồm:

• Suy luận.
• Điều kiện.
• Xác suất suy luận.
• Xác suất hiệu chỉnh.
• Điều kiện vô hiệu.
• Kết quả kỳ vọng.

────────

Mục tiêu

• Tổ chức.
• Ước lượng.
• Hiệu chỉnh.

────────

Đầu ra

Tầng Không gian kịch bản tạo ra tập các kịch bản hiện tại.

Mỗi kịch bản bao gồm:

• Xác suất suy luận.
• Xác suất hiệu chỉnh (nếu có).

Không gian kịch bản trở thành đầu vào của tầng Kế hoạch thực thi.

────────

Triết lý

Mỗi kịch bản là một khả năng được hình thành từ kết quả suy luận hiện tại.

Kinh nghiệm giúp đánh giá và hiệu chỉnh mức độ tin cậy của từng khả năng.

────────

Quan sát

> Quan sát toàn bộ các kịch bản hợp lý tại thời điểm hiện tại.

────────

Mục đích

Quan sát toàn bộ các kịch bản hợp lý được hình thành từ kết quả suy luận hiện tại.

Quan sát mức độ ưu tiên của từng kịch bản.

Quan sát mức độ tin cậy của từng kịch bản sau khi tham khảo Tri thức tích luỹ (nếu có).

────────

Quan sát

• Suy luận.
• Điều kiện.
• Xác suất suy luận.
• Xác suất hiệu chỉnh.
• Mức độ ưu tiên.
• Đồng thuận.
• Xung đột.
• Điều kiện vô hiệu.

────────

Nguyên tắc

Nhiều kịch bản có thể cùng tồn tại.

Mỗi kịch bản có Suy luận, Điều kiện và Xác suất suy luận riêng.

Mức độ ưu tiên của các kịch bản được hình thành từ kết quả suy luận hiện tại.

Không gian kịch bản có thể tham khảo Tri thức tích luỹ để hiệu chỉnh mức độ tin cậy của các kịch bản khi đã có đủ dữ liệu.

Không gian kịch bản thay đổi khi kết quả suy luận hoặc Tri thức tích luỹ thay đổi.

────────

Triết lý

Thị trường luôn tồn tại nhiều kịch bản đồng thời.

Kết quả suy luận hình thành các kịch bản.

Kinh nghiệm giúp đánh giá và hiệu chỉnh mức độ tin cậy của các kịch bản.

────────

Kịch bản

> Mô tả cấu trúc của một kịch bản.

────────

Mục đích

Kịch bản mô tả một khả năng phát triển hợp lý của thị trường.

Mỗi kịch bản được hình thành từ kết quả suy luận hiện tại.

────────

Thành phần

Một kịch bản bao gồm:

• Suy luận.
• Điều kiện.
• Xác suất suy luận.
• Xác suất hiệu chỉnh.
• Điều kiện vô hiệu.
• Kết quả kỳ vọng.

────────

Nguyên tắc

Mỗi kịch bản được hình thành từ cùng một kết quả suy luận.

Các kịch bản có thể cùng tồn tại.

Mỗi kịch bản có Suy luận, Điều kiện và Xác suất suy luận riêng.

Xác suất hiệu chỉnh chỉ xuất hiện khi có đủ dữ liệu tham khảo từ Tri thức tích luỹ.

Không có kịch bản nào được xem là chắc chắn.

────────

Vai trò

Kịch bản là đơn vị cơ bản của Không gian kịch bản.

Nhiều kịch bản kết hợp tạo thành Không gian kịch bản.

────────

Triết lý

Một kịch bản không dự đoán tương lai.

Một kịch bản chỉ biểu diễn một khả năng hợp lý.

────────

Hiệu chỉnh

> Hiệu chỉnh các kịch bản bằng dữ liệu tham khảo từ Tri thức tích luỹ.

────────

Mục đích

Hiệu chỉnh giúp Không gian kịch bản tham khảo kinh nghiệm đã được tích luỹ.

Sau khi các kịch bản được hình thành từ kết quả suy luận hiện tại, Chữ ký tín hiệu được sử dụng để tra cứu Tri thức tích luỹ.

Nếu tồn tại đủ dữ liệu đáng tin cậy, Không gian kịch bản có thể hiệu chỉnh mức độ tin cậy của các kịch bản.

────────

Hiệu chỉnh

Không gian kịch bản có thể hiệu chỉnh:

• Xác suất hiệu chỉnh.
• Mức độ ưu tiên.
• Kết quả kỳ vọng.

Suy luận không thay đổi.

Điều kiện không thay đổi.

Điều kiện vô hiệu không thay đổi.

────────

Nguyên tắc

Các kịch bản luôn được hình thành từ kết quả suy luận hiện tại.

Tri thức tích luỹ chỉ được tham khảo sau khi các kịch bản đã được hình thành.

Nếu chưa đủ dữ liệu, Không gian kịch bản giữ nguyên xác suất suy luận.

Nếu đã có đủ dữ liệu đáng tin cậy, Không gian kịch bản tham khảo Tri thức tích luỹ để hiệu chỉnh mức độ tin cậy của các kịch bản.

Tri thức tích luỹ không tạo ra kịch bản mới.

Tri thức tích luỹ chỉ cung cấp dữ liệu tham khảo.

────────

Triết lý

Kết quả suy luận hiện tại hình thành các kịch bản.

Kinh nghiệm giúp đánh giá và hiệu chỉnh mức độ tin cậy của các kịch bản.

────────

Ví dụ

────────

Kịch bản 01 · Tiếp diễn xu hướng tăng

Kết quả suy luận hiện tại

Xác suất suy luận

72%

Điều kiện

• Hành vi: Người mua chiếm ưu thế.
• Động lượng: Gia tăng.
• Cấu trúc: Tiếp diễn xu hướng tăng.

Điều kiện vô hiệu

• Giá mất vùng POC.

↓

Tri thức tích luỹ

• Chữ ký tín hiệu đã từng xuất hiện: 43 mẫu.
• Độ tin cậy: Cao.

↓

Sau hiệu chỉnh

Xác suất hiệu chỉnh

76%

────────

Kịch bản 02 · Mở rộng vùng tích luỹ

Kết quả suy luận hiện tại

Xác suất suy luận

18%

Điều kiện

• Động lượng suy yếu.
• Khối lượng cân bằng.

Điều kiện vô hiệu

• Giá phá vỡ hoàn toàn khỏi vùng giá trị.

↓

Tri thức tích luỹ

• Chưa đủ dữ liệu.

↓

Sau hiệu chỉnh

Xác suất hiệu chỉnh

Không thay đổi.

────────

Kịch bản 03 · Đảo chiều xu hướng giảm

Kết quả suy luận hiện tại

Xác suất suy luận

10%

Điều kiện

• Động lượng đảo chiều.
• Cấu trúc: Xác nhận xu hướng giảm.

Điều kiện vô hiệu

• Giá tạo đỉnh cao hơn mới.

↓

Tri thức tích luỹ

• Chữ ký tín hiệu đã từng xuất hiện: 15 mẫu.
• Độ tin cậy: Trung bình.

↓

Sau hiệu chỉnh

Xác suất hiệu chỉnh

6%

────────

Nguyên tắc

Các kịch bản luôn được hình thành từ kết quả suy luận hiện tại.

Không gian kịch bản chỉ tham khảo Tri thức tích luỹ sau khi các kịch bản đã được hình thành.

Nếu chưa có đủ dữ liệu, Xác suất hiệu chỉnh giữ nguyên Xác suất suy luận.

────────

Triết lý

Kết quả suy luận hiện tại hình thành các kịch bản.

Kinh nghiệm giúp đánh giá và hiệu chỉnh mức độ tin cậy của các kịch bản.

────────

09 · Kế hoạch thực thi

> Thiết kế các phương án thực thi cho từng kịch bản.

────────

Mục đích

Kế hoạch thực thi là tầng thứ chín của Hệ thống suy luận.

Tầng này xây dựng các phương án thực thi cho từng kịch bản.

Không gian kịch bản cung cấp các kịch bản hiện tại.

Chữ ký tín hiệu được sử dụng để tham khảo Tri thức tích luỹ nhằm lựa chọn những phương án đã được kiểm chứng (nếu có).

Mỗi phương án xác định:

• Điều kiện thực thi.
• Điều kiện xác nhận.
• Điều kiện hủy bỏ.
• Quản trị rủi ro.
• Quản trị vị thế.

────────

Câu hỏi

Nếu kịch bản này xảy ra, mình nên hành động như thế nào?

→ Không gian kịch bản.

────────

Theo kinh nghiệm đã được tích luỹ, phương án nào đáng tin cậy hơn?

→ Chữ ký tín hiệu + Tri thức tích luỹ.

────────

Đầu vào

• Không gian kịch bản.
• Chữ ký tín hiệu.

────────

Đầu ra

Các phương án thực thi.

Các phương án thực thi trở thành đầu vào của tầng Phản hồi thực tế.

────────

Vai trò trong Hệ thống suy luận

```text
# Không gian kịch bản
        │
        ├────────► Tham khảo # Tri thức tích luỹ
        ▼
# Kế hoạch thực thi

↓

# Phản hồi thực tế
```

────────

Cấu trúc

```text
# 01 · Định nghĩa

↓

# 02 · Quan sát

↓

# 03 · Phương án

↓

# 04 · Hiệu chỉnh

↓

# 05 · Ví dụ
```

────────

Triết lý

Không gian kịch bản xác định khả năng.

Kinh nghiệm giúp lựa chọn phương án thực thi phù hợp nhất.

────────

Định nghĩa

> Bản chất của Kế hoạch thực thi.

────────

Bản chất

Kế hoạch thực thi thiết kế các phương án thực thi cho từng kịch bản.

Kế hoạch thực thi không lựa chọn kịch bản.

Kế hoạch thực thi chuẩn bị các phương án thực thi cho những kịch bản có thể xảy ra.

Sau khi các phương án được hình thành, Tri thức tích luỹ có thể được tham khảo để hiệu chỉnh mức độ phù hợp của từng phương án.

────────

Thành phần

Một phương án thực thi bao gồm:

• Vùng vào lệnh.
• Điều kiện xác nhận.
• Điều kiện vô hiệu.
• Điểm dừng lỗ.
• Điểm chốt lời.
• Quy mô vị thế.
• Tỷ lệ lợi nhuận / rủi ro.
• Quản trị vị thế.

────────

Mục tiêu

• Chuẩn bị.
• Chuẩn hóa.
• Lập phương án.

────────

Đầu ra

Tầng Kế hoạch thực thi tạo ra các phương án thực thi.

Các phương án thực thi trở thành đầu vào của tầng Phản hồi thực tế.

────────

Triết lý

Một phương án tốt tạo nên một quá trình thực thi nhất quán.

────────

Quan sát

> Quan sát các phương án thực thi của từng kịch bản.

────────

Mục đích

Quan sát các phương án thực thi được xây dựng cho từng kịch bản.

Quan sát những điều kiện cần có trước khi thực thi.

────────

Quan sát

• Vùng vào lệnh.
• Điều kiện xác nhận.
• Thanh khoản mục tiêu.
• Mức độ rủi ro.
• Mục tiêu lợi nhuận.
• Điều kiện vô hiệu.
• Thời điểm thực thi.
• Chi phí thực thi.

────────

Nguyên tắc

Mỗi kịch bản có thể có một hoặc nhiều phương án thực thi.

Mỗi phương án có các điều kiện thực thi riêng.

Tri thức tích luỹ có thể được tham khảo để đánh giá và hiệu chỉnh mức độ phù hợp của từng phương án.

Chỉ thực thi khi các điều kiện đã được xác nhận.

────────

Triết lý

Phương án phản ánh cách thực thi của từng kịch bản.

Chuẩn bị trước giúp quá trình thực thi nhất quán hơn.

────────

Phương án

> Mô tả cấu trúc của một phương án thực thi.

────────

Mục đích

Phương án mô tả cách thực thi cho một kịch bản cụ thể.

Một kịch bản có thể có một hoặc nhiều phương án thực thi.

────────

Thành phần

Một phương án bao gồm:

• Vùng vào lệnh.
• Điều kiện xác nhận.
• Điều kiện vô hiệu.
• Điểm dừng lỗ.
• Điểm chốt lời.
• Quy mô vị thế.
• Tỷ lệ lợi nhuận / rủi ro.
• Quản trị vị thế.

────────

Nguyên tắc

Mỗi phương án được xây dựng cho một kịch bản cụ thể.

Một kịch bản có thể có nhiều phương án thực thi.

Các phương án có thể khác nhau về mức độ rủi ro, lợi nhuận kỳ vọng hoặc cách quản trị vị thế.

Không có phương án nào được xem là tuyệt đối.

────────

Vai trò

Phương án là đơn vị cơ bản của Kế hoạch thực thi.

Nhiều phương án kết hợp tạo thành Kế hoạch thực thi.

────────

Triết lý

Một phương án không đảm bảo kết quả.

Một phương án chỉ chuẩn bị cách hành động phù hợp cho từng kịch bản.

────────

Hiệu chỉnh

> Hiệu chỉnh các phương án bằng dữ liệu tham khảo từ Tri thức tích luỹ.

────────

Mục đích

Hiệu chỉnh giúp Kế hoạch thực thi tham khảo kinh nghiệm đã được tích luỹ.

Sau khi các phương án được xây dựng từ Không gian kịch bản, Chữ ký tín hiệu được sử dụng để tra cứu Tri thức tích luỹ.

Nếu tồn tại đủ dữ liệu đáng tin cậy, Kế hoạch thực thi có thể hiệu chỉnh mức độ phù hợp của từng phương án.

────────

Hiệu chỉnh

Kế hoạch thực thi có thể hiệu chỉnh:

• Mức độ ưu tiên của phương án.
• Mức độ phù hợp của phương án.
• Quy mô vị thế.
• Quản trị vị thế.
• Tỷ lệ lợi nhuận / rủi ro.

Điều kiện thực thi không thay đổi.

Điều kiện xác nhận không thay đổi.

Điều kiện vô hiệu không thay đổi.

────────

Nguyên tắc

Các phương án luôn được xây dựng từ Không gian kịch bản.

Tri thức tích luỹ chỉ được tham khảo sau khi các phương án đã được hình thành.

Nếu chưa đủ dữ liệu, Kế hoạch thực thi giữ nguyên phương án hiện tại.

Nếu đã có đủ dữ liệu đáng tin cậy, Kế hoạch thực thi tham khảo Tri thức tích luỹ để hiệu chỉnh mức độ phù hợp của từng phương án.

Tri thức tích luỹ không tạo ra phương án mới.

Tri thức tích luỹ chỉ cung cấp dữ liệu tham khảo.

────────

Triết lý

Không gian kịch bản hình thành các phương án.

Kinh nghiệm giúp lựa chọn và hiệu chỉnh phương án phù hợp hơn.

────────

Ví dụ

────────

Kịch bản 01 · Tiếp diễn xu hướng tăng

Phương án hiện tại

Phương án A

• Vùng vào lệnh: Pullback về vùng POC.
• Điểm dừng lỗ: Dưới VAL.
• Điểm chốt lời: VAH.
• Tỷ lệ Lợi nhuận / Rủi ro: 2.8 : 1
• Quy mô vị thế: 1.0R

↓

Tri thức tích luỹ

• Chữ ký tín hiệu đã từng xuất hiện: 43 mẫu.
• Độ tin cậy: Cao.
• Quy mô vị thế tối ưu: 0.8R.

↓

Sau hiệu chỉnh

• Quy mô vị thế: 0.8R
• Tỷ lệ Lợi nhuận / Rủi ro: Giữ nguyên
• Phương án: Giữ nguyên

────────

Kịch bản 02 · Mở rộng vùng tích luỹ

Phương án hiện tại

Phương án A

• Chờ phá vỡ vùng giá trị.
• Chưa vào lệnh.

↓

Tri thức tích luỹ

• Chưa đủ dữ liệu.

↓

Sau hiệu chỉnh

• Phương án giữ nguyên.

────────

Kịch bản 03 · Đảo chiều xu hướng giảm

Phương án hiện tại

Phương án A

• Vào lệnh sau khi xác nhận phá vỡ.
• Điểm dừng lỗ: Trên đỉnh gần nhất.
• Quy mô vị thế: 1.0R

↓

Tri thức tích luỹ

• Chữ ký tín hiệu đã từng xuất hiện: 15 mẫu.
• Độ tin cậy: Trung bình.
• Kế hoạch tương tự thường có tỷ lệ thất bại cao.

↓

Sau hiệu chỉnh

• Quy mô vị thế: 0.5R
• Chờ thêm xác nhận trước khi thực thi.

────────

Nguyên tắc

Các phương án luôn được xây dựng từ Không gian kịch bản.

Tri thức tích luỹ chỉ được tham khảo để hiệu chỉnh các phương án đã tồn tại.

Nếu chưa có đủ dữ liệu, Kế hoạch thực thi giữ nguyên phương án hiện tại.

────────

Triết lý

Không gian kịch bản tạo ra các phương án.

Kinh nghiệm giúp lựa chọn và hiệu chỉnh phương án phù hợp hơn.

────────

10 · Phản hồi thực tế

> Đánh giá kết quả thực tế sau khi Kế hoạch thực thi được thực hiện.

────────

Mục đích

Phản hồi thực tế là tầng thứ mười của Hệ thống suy luận.

Tầng này quan sát kết quả thực tế sau khi Kế hoạch thực thi được thực hiện.

Tầng này đánh giá sự phù hợp giữa:

• Không gian kịch bản.
• Kế hoạch thực thi.
• Thực tế.

Phản hồi thực tế tạo ra dữ liệu để Tri thức tích luỹ cập nhật kinh nghiệm của Hệ thống suy luận.

────────

Câu hỏi

Thực tế đã diễn ra như thế nào?

→ Phản hồi thực tế.

────────

Có xuất hiện bằng chứng mới cần được tích luỹ không?

→ Tri thức tích luỹ.

────────

Đầu vào

• Kế hoạch thực thi.
• Thực tế.

────────

Đầu ra

• Phản hồi thực tế.
• Bằng chứng mới (nếu có).

Phản hồi thực tế trở thành đầu vào của Tri thức tích luỹ.

────────

Vai trò trong Hệ thống suy luận

```text
# Kế hoạch thực thi

↓

# Thực tế

↓

# Phản hồi thực tế

↓

# Tri thức tích luỹ
```

────────

Cấu trúc

```text
# 01 · Định nghĩa

↓

# 02 · Quan sát

↓

# 03 · Phản hồi

↓

# 04 · Cập nhật

↓

# 05 · Ví dụ
```

────────

Triết lý

Thực tế là tiêu chuẩn cuối cùng của mọi suy luận.

Mỗi phản hồi thực tế đều có thể trở thành kinh nghiệm cho những lần suy luận sau.

────────

Định nghĩa

> Bản chất của Phản hồi thực tế.

────────

Bản chất

Phản hồi thực tế so sánh:

```text
Không gian kịch bản

↓

Kế hoạch thực thi

↓

Thực tế
```

Phản hồi thực tế ghi nhận kết quả thực tế.

Phản hồi thực tế đánh giá mức độ phù hợp giữa Không gian kịch bản, Kế hoạch thực thi và Thực tế.

Phản hồi thực tế cung cấp bằng chứng từ Thực tế cho Hệ thống suy luận.

────────

Thành phần

Phản hồi thực tế bao gồm:

• Kết quả kỳ vọng.
• Kết quả thực tế.
• Xác nhận kịch bản.
• Vô hiệu kịch bản.
• Chất lượng thực thi.
• Hành vi ngoài kỳ vọng.
• Bằng chứng thực tế.

────────

Mục tiêu

• Quan sát.
• So sánh.
• Đánh giá.

────────

Đầu ra

Tầng Phản hồi thực tế tạo ra Phản hồi thực tế.

Phản hồi thực tế trở thành đầu vào của Tri thức tích luỹ.

Tri thức tích luỹ sử dụng Phản hồi thực tế để cập nhật kinh nghiệm của Hệ thống suy luận.

────────

Triết lý

Thực tế là tiêu chuẩn cuối cùng của mọi suy luận.

────────

Quan sát

> Quan sát những gì thực sự đã xảy ra.

────────

Mục đích

Quan sát và ghi nhận kết quả thực tế của quá trình thực thi.

Những kết quả này trở thành bằng chứng cho Hệ thống suy luận và dữ liệu của Tri thức tích luỹ.

────────

Quan sát

• Kịch bản đã xảy ra.
• Kịch bản không xảy ra.
• Chất lượng thực thi.
• Hành vi thực tế của thị trường.
• Hành vi ngoài kỳ vọng.
• Kết quả thực tế.

────────

Nguyên tắc

Thực tế luôn có độ ưu tiên cao nhất.

Phản hồi thực tế chỉ ghi nhận những gì đã được xác nhận bởi Thực tế.

Mọi bằng chứng đều bắt nguồn từ Thực tế.

────────

Triết lý

Thực tế là tiêu chuẩn cuối cùng của mọi suy luận.

Mọi kinh nghiệm đều bắt đầu từ Thực tế.

────────

Phản hồi

> Mô tả cấu trúc của một Phản hồi thực tế.

────────

Mục đích

Phản hồi ghi nhận kết quả thực tế sau khi phương án được thực thi.

Phản hồi đánh giá mức độ phù hợp giữa:

• Kịch bản.
• Phương án thực thi.
• Thực tế.

────────

Thành phần

Một Phản hồi bao gồm:

• Kết quả kỳ vọng.
• Kết quả thực tế.
• Kịch bản đã xảy ra.
• Kịch bản không xảy ra.
• Chất lượng thực thi.
• Hành vi ngoài kỳ vọng.
• Bằng chứng thực tế.

────────

Nguyên tắc

Mỗi phương án thực thi tạo ra một Phản hồi thực tế.

Phản hồi chỉ được hình thành sau khi có kết quả thực tế.

Mỗi Phản hồi phản ánh đúng những gì đã xảy ra.

Phản hồi không thay đổi quá khứ.

────────

Vai trò

Phản hồi là đơn vị cơ bản của tầng Phản hồi thực tế.

Nhiều Phản hồi được tích luỹ thành kinh nghiệm trong Tri thức tích luỹ.

────────

Triết lý

Phản hồi không tạo ra sự thật.

Phản hồi chỉ ghi nhận sự thật đã xảy ra.

────────

Cập nhật

> Cập nhật kết quả thực tế thành dữ liệu của Tri thức tích luỹ.

────────

Mục đích

Cập nhật giúp chuyển kết quả thực tế thành dữ liệu của Tri thức tích luỹ.

Sau khi Phản hồi thực tế được hình thành, những thông tin cần thiết được chuyển sang Tri thức tích luỹ để thống kê và tích luỹ kinh nghiệm.

────────

Cập nhật

Phản hồi thực tế có thể cập nhật:

• Chữ ký tín hiệu.
• Kịch bản đã xảy ra.
• Phương án đã thực thi.
• Kết quả thực tế.
• Bài học tích luỹ.

────────

Ví dụ

```text
Kịch bản

↓

Được xác nhận

↓

Tri thức tích luỹ ghi nhận
```

────────

```text
Kịch bản

↓

Bị vô hiệu

↓

Tri thức tích luỹ ghi nhận
```

────────

```text
Ngoài dự kiến

↓

Tri thức tích luỹ ghi nhận trường hợp mới
```

────────

Nguyên tắc

Chỉ những kết quả đã được xác nhận bởi Thực tế mới được cập nhật.

Mỗi Phản hồi thực tế chỉ được cập nhật một lần.

Phản hồi thực tế không trực tiếp tạo ra Tri thức.

Tri thức tích luỹ sử dụng Phản hồi thực tế để thống kê và tích luỹ kinh nghiệm.

────────

Triết lý

Phản hồi thực tế ghi nhận những gì đã xảy ra.

Tri thức tích luỹ lưu giữ những gì đã được xác nhận.

────────

Ví dụ

────────

Ví dụ 01

Kịch bản

Tiếp diễn xu hướng tăng.

↓

Phương án thực thi

Mua theo xu hướng.

↓

Thực tế

Tiếp diễn xu hướng tăng.

↓

Phản hồi thực tế

• Kịch bản được xác nhận.
• Phương án thực thi hiệu quả.

↓

Tri thức tích luỹ

• Ghi nhận Chữ ký tín hiệu.
• Tăng số lượng mẫu.
• Cập nhật bài học tích luỹ.

────────

Ví dụ 02

Kịch bản

Tiếp diễn xu hướng tăng.

↓

Phương án thực thi

Mua theo xu hướng.

↓

Thực tế

Đảo chiều xu hướng giảm.

↓

Phản hồi thực tế

• Kịch bản bị vô hiệu.
• Phương án thực thi không hiệu quả.

↓

Tri thức tích luỹ

• Ghi nhận Chữ ký tín hiệu.
• Tăng số lượng mẫu.
• Cập nhật bài học tích luỹ.

────────

Ví dụ 03

Kịch bản

Đi ngang.

↓

Phương án thực thi

Giao dịch trong vùng tích luỹ.

↓

Thực tế

Biến động mở rộng ngoài dự kiến.

↓

Phản hồi thực tế

• Hành vi ngoài kỳ vọng.
• Xuất hiện bằng chứng mới.

↓

Tri thức tích luỹ

• Ghi nhận trường hợp mới.
• Khởi tạo dữ liệu cho Chữ ký tín hiệu mới.

────────

Nguyên tắc

Mọi kết quả thực tế đều được ghi nhận bởi Phản hồi thực tế.

Tri thức tích luỹ sử dụng các Phản hồi thực tế để thống kê và tích luỹ kinh nghiệm.

────────

Triết lý

Thực tế tạo ra Phản hồi.

Phản hồi tạo ra dữ liệu cho Tri thức tích luỹ.