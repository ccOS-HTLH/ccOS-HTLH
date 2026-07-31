---
title: Tri thức nền
id: trading-knowledge
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-27
last_updated: 2026-07-27
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - knowledge
---

# Tri thức nền

> Tri thức nền là thành phần chuẩn hóa toàn bộ ngôn ngữ, khái niệm và quy ước của Trading Domain.

---

# Mục đích

Tri thức nền trả lời:

> Trading Domain hiểu dữ liệu theo cách nào?

Tri thức nền chuẩn hóa:

- Thuật ngữ.
- Khái niệm.
- Quy ước.
- Luồng suy luận.

Nhờ đó mọi thành phần trong Trading Domain sử dụng cùng một ngôn ngữ và cùng một quy ước.

---

# Triết lý

Một ngôn ngữ thống nhất tạo nên một hệ thống thống nhất.

Tri thức nền chuẩn hóa cách hiểu, cách biểu diễn và cách vận hành của Trading Domain.

---

# Kiến trúc

```text
Tri thức nền

├── README.md
│
├── Quy ước Chữ ký tín hiệu
│
├── Quy ước Trường hợp
├── Quy ước Mẫu
├── Quy ước Bài học tích luỹ
├── Quy ước Thống kê
│
├── Quy ước chỉ báo đa khung thời gian
│
└── Luồng suy luận
```

---

# Mối quan hệ với Trading

```text
Tri thức nền

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ
```

Trong đó:

- Nguồn dữ liệu tham khảo Tri thức nền để chuẩn hóa dữ liệu.
- Hệ thống suy luận tham khảo Tri thức nền để chuẩn hóa quá trình suy luận.
- Tri thức tích luỹ tham khảo Tri thức nền để chuẩn hóa Bộ nhớ.

---

# Thành phần

## Quy ước Chữ ký tín hiệu

Chuẩn hóa cấu trúc Chữ ký tín hiệu.

---

## Quy ước Trường hợp

Chuẩn hóa cấu trúc Trường hợp.

---

## Quy ước Mẫu

Chuẩn hóa cấu trúc Mẫu.

---

## Quy ước Bài học tích luỹ

Chuẩn hóa cấu trúc Bài học tích luỹ.

---

## Quy ước Thống kê

Chuẩn hóa cấu trúc Thống kê.

---

## Quy ước chỉ báo đa khung thời gian

Chuẩn hóa cách biểu diễn chỉ báo và khung thời gian.

---

## Luồng suy luận

Chuẩn hóa trình tự vận hành của Hệ thống suy luận.

---

# Nguyên tắc

Mọi thành phần của Trading Domain tham khảo cùng một Tri thức nền.

Mọi khái niệm, quy ước và luồng vận hành đều được chuẩn hóa trước khi được sử dụng.

---

# Vai trò trong Trading

```text
                Tri thức nền
                  │
      ┌───────────┼───────────┐
      ▼           ▼           ▼

Nguồn dữ liệu  Hệ thống   Tri thức
                suy luận   tích luỹ
```

Tri thức nền là nền tảng chuẩn hóa của toàn bộ Trading Domain.

---

# Tóm tắt

```text
Tri thức nền

↓

Chuẩn hóa

↓

Trading Domain
```

Tri thức nền là nền tảng thống nhất cho:

- Thuật ngữ.
- Khái niệm.
- Quy ước.
- Luồng suy luận.

---

---
title: Luồng suy luận
id: trading-reasoning-flow
version: 1.1
status: Stable
author: HTLH
language: vi
created: 2026-07-27
last_updated: 2026-07-27
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - reasoning
  - workflow
---

# Luồng suy luận

> Luồng suy luận mô tả toàn bộ quá trình Hệ thống suy luận vận hành từ khi tiếp nhận dữ liệu đến khi tích luỹ kinh nghiệm mới.

---

# Mục đích

Luồng suy luận mô tả cách Hệ thống suy luận vận hành từ khi quan sát Thực tế đến khi hoàn thành một chu kỳ suy luận.

Mỗi tầng có một vai trò riêng.

Đầu ra của tầng trước trở thành đầu vào của tầng sau.

Sau khi hoàn thành một vòng suy luận, Thực tế tạo ra dữ liệu mới để Tri thức tích luỹ cập nhật Bộ nhớ.

---

# Triết lý

Quan sát tạo ra dữ liệu.

Suy luận tạo ra khả năng.

Thực thi tạo ra hành động.

Thực tế kiểm chứng kết quả.

Tri thức tích luỹ chuẩn hóa kinh nghiệm thành tri thức.

Bộ nhớ lưu giữ tri thức cho những lần suy luận sau.

---

# Luồng suy luận

```text
01 · Hành vi
        │
        ▼
02 · Bối cảnh
        │
        ▼
03 · Động lượng
        │
        ▼
04 · Cấu trúc
        │
        ▼
05 · Chất lượng
        │
        ▼
06 · Quyết định
        │
        ▼
07 · Trọng số tín hiệu
        │
        ▼
Chữ ký tín hiệu
        │
        ▼
08 · Không gian kịch bản
        │
        ▼
09 · Kế hoạch thực thi
        │
        ▼
10 · Phản hồi thực tế
        │
        ▼
Tri thức tích luỹ
        │
        ├── Trường hợp
        ├── Mẫu
        ├── Bài học tích luỹ
        └── Thống kê
```

---

# Chu trình

```text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Không gian kịch bản

↓

Kế hoạch thực thi

↓

Phản hồi thực tế

↓

Tri thức tích luỹ

↓

Chu kỳ suy luận tiếp theo
```

Đây là một vòng lặp liên tục.

Mỗi chu kỳ đều có thể tạo ra kinh nghiệm mới.

---

# Nguyên tắc

Đầu ra của mỗi tầng là đầu vào của tầng kế tiếp.

Không được bỏ qua bất kỳ tầng nào trong quá trình suy luận.

Không được suy luận ngược từ kết quả về dữ liệu đầu vào.

Chữ ký tín hiệu được hình thành sau tầng Trọng số tín hiệu.

Không gian kịch bản chỉ được hình thành sau khi Chữ ký tín hiệu đã hoàn tất.

Tri thức tích luỹ chỉ được tham khảo sau khi Không gian kịch bản đã được xây dựng.

Thực tế là tiêu chuẩn kiểm chứng duy nhất của toàn bộ Hệ thống suy luận.

---

# Vai trò

Hệ thống suy luận chịu trách nhiệm:

- Quan sát dữ liệu.
- Phân tích dữ liệu.
- Đánh giá chất lượng tín hiệu.
- Xây dựng Không gian kịch bản.
- Lập Kế hoạch thực thi.
- Đánh giá kết quả từ Thực tế.

---

Tri thức tích luỹ chịu trách nhiệm:

- Tra cứu Trường hợp.
- Nhận diện Mẫu.
- Rút ra Bài học tích luỹ.
- Cập nhật Thống kê.
- Chuẩn hóa và lưu giữ kinh nghiệm.

---

Hai hệ thống phối hợp để giúp Trading Domain học hỏi liên tục từ Thực tế.

---

# Mối quan hệ với Trading

```text
             Tri thức nền
                    │
                    ▼

             Nguồn dữ liệu

                    │
                    ▼

          Hệ thống suy luận

                    │
                    ▼

          Tri thức tích luỹ

                    │
                    ▼

            Chu kỳ suy luận tiếp theo
```

Trong đó:

- Tri thức nền chuẩn hóa toàn bộ quá trình vận hành.
- Nguồn dữ liệu chuẩn hóa dữ liệu từ Thực tế.
- Hệ thống suy luận chuyển dữ liệu thành phương án hành động.
- Tri thức tích luỹ học hỏi từ Thực tế và tái sử dụng kinh nghiệm trong các chu kỳ tiếp theo.

---

# Tóm tắt

```text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Không gian kịch bản

↓

Kế hoạch thực thi

↓

Phản hồi thực tế

↓

Tri thức tích luỹ

↓

Chu kỳ suy luận tiếp theo
```

Luồng suy luận chuẩn hóa:

- Thứ tự xử lý dữ liệu.
- Mối quan hệ giữa các tầng.
- Quá trình hình thành quyết định.
- Quá trình học hỏi từ Thực tế.

Luồng suy luận là xương sống của toàn bộ Trading Domain.

---

---
title: Quy ước chỉ báo đa khung thời gian
id: convention-multi-timeframe-indicators
version: 1.1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-25
last_updated: 2026-07-27
review_cycle: Monthly
confidence: 100%
tags:
  - convention
  - indicator
  - timeframe
---

# Quy ước chỉ báo đa khung thời gian

> Chuẩn hóa cách biểu diễn các chỉ báo và dữ liệu phụ thuộc khung thời gian trong Trading Domain.

---

# Mục đích

Quy ước này chuẩn hóa cách biểu diễn các chỉ báo và dữ liệu phụ thuộc khung thời gian trong Trading Domain.

Việc chuẩn hóa giúp:

- Xác định rõ ngữ cảnh.
- Thống nhất cách biểu diễn dữ liệu.
- Hỗ trợ Hệ thống suy luận.
- Hỗ trợ Tri thức tích luỹ.

---

# Triết lý

Chỉ báo luôn gắn với ngữ cảnh.

Khung thời gian là một phần của dữ liệu.

Dữ liệu được chuẩn hóa trước khi tham gia Hệ thống suy luận.

---

# Phạm vi áp dụng

Quy ước này được sử dụng thống nhất trong:

- Nguồn dữ liệu.
- Hệ thống suy luận.
- Tri thức nền.
- Tri thức tích luỹ.
- Bộ nhớ.

---

# Cấu trúc biểu diễn

Các chỉ báo được biểu diễn theo cấu trúc:

```text
<Tên chỉ báo> <Khung thời gian>
```

Ví dụ:

```text
EMA34 15m

RSI 1H

Volume 5m

CVD 5m
```

---

# Các nhóm dữ liệu

## Chỉ báo kỹ thuật

Ví dụ:

```text
EMA34 5m
EMA89 15m
EMA200 1H
EMA610 4H

RSI 5m
RSI 15m
RSI 1H
RSI 4H

Volume 5m
Volume 15m
Volume 1H
```

---

## Volume Profile

Ví dụ:

```text
POC30

VAH30

VAL30
```

Trong đó:

- POC30 = Point of Control khung 30 phút.
- VAH30 = Value Area High khung 30 phút.
- VAL30 = Value Area Low khung 30 phút.

---

## Auction Flow

Ví dụ:

```text
Auction Line

EMA20

POC5

VP1
```

Trong đó:

- Auction Line = Đường Auction Flow.
- EMA20 = EMA20 của Auction Flow.
- POC5 = Point of Control khung 5 phút.
- VP1 = Value Pivot của Auction Flow.

---

## Dữ liệu dòng tiền

Ví dụ:

```text
OI

Funding

CVD 5m

Delta 5m

Agg Liq 5m
```

Trong đó:

- OI = Open Interest hiện tại.
- Funding = Funding Rate hiện tại.
- CVD 5m = Cumulative Volume Delta khung 5 phút.
- Delta 5m = Delta khung 5 phút.
- Agg Liq 5m = Aggressive Liquidation khung 5 phút.

---

## Dữ liệu thị trường

Ví dụ:

```text
Long/Short Ratio 1H

Fear & Greed
```

Trong đó:

- Long/Short Ratio luôn đi kèm khung thời gian tương ứng.
- Fear & Greed sử dụng giá trị hiện tại.

---

# Ngoại lệ

Một số dữ liệu không phụ thuộc khung thời gian.

Ví dụ:

```text
OI

Funding

Fear & Greed

News

Macro
```

Các dữ liệu này được biểu diễn theo quy ước riêng của từng dữ liệu.

Không bổ sung khung thời gian nếu dữ liệu không phụ thuộc khung thời gian.

---

# Ví dụ

## EMA

Biểu diễn chuẩn:

```text
EMA200 4H đang là kháng cự.
```

Khung thời gian được biểu diễn cùng tên chỉ báo.

---

## RSI

Biểu diễn chuẩn:

```text
RSI 15m đang tiến vào vùng quá mua.
```

Khung thời gian phản ánh đúng ngữ cảnh của chỉ báo.

---

## EMA hỗ trợ

Biểu diễn chuẩn:

```text
Giá giữ trên EMA34 15m.
```

Mỗi EMA luôn đi kèm khung thời gian tương ứng.

---

## CVD

Biểu diễn chuẩn:

```text
CVD 5m đang tăng.
```

Khung thời gian giúp xác định đúng dữ liệu được quan sát.

---

## Long / Short Ratio

Biểu diễn chuẩn:

```text
Long/Short Ratio 1H nghiêng về phe Long.
```

Khung thời gian là một phần của dữ liệu.

---

## Funding

Biểu diễn chuẩn:

```text
Funding đang dương.
```

Funding sử dụng giá trị hiện tại.

---

## OI

Biểu diễn chuẩn:

```text
OI đang tăng.
```

OI sử dụng giá trị hiện tại.

---

# Nguyên tắc

Khung thời gian là một phần của dữ liệu.

Mọi chỉ báo được biểu diễn cùng khung thời gian tương ứng.

Mọi dữ liệu phụ thuộc khung thời gian sử dụng cùng một quy ước biểu diễn.

Các dữ liệu không phụ thuộc khung thời gian không bổ sung khung thời gian.

Mọi tài liệu trong Trading Domain sử dụng thống nhất quy ước này.

Mọi dữ liệu được chuẩn hóa trước khi tham gia Hệ thống suy luận.

---

# Vai trò

Quy ước này giúp:

- Chuẩn hóa dữ liệu.
- Chuẩn hóa tài liệu.
- Chuẩn hóa Hệ thống suy luận.
- Chuẩn hóa Tri thức tích luỹ.
- Chuẩn hóa Bộ nhớ.

Đây là quy ước chung của toàn bộ Trading Domain.

---

# Tóm tắt

Khung thời gian là một phần của dữ liệu.

Chỉ báo luôn đi cùng khung thời gian tương ứng.

Các dữ liệu không phụ thuộc khung thời gian sử dụng quy ước biểu diễn riêng.

Mọi thành phần trong Trading Domain sử dụng thống nhất quy ước này trước khi dữ liệu tham gia Hệ thống suy luận.

---

# Quy ước Chữ ký tín hiệu

> Quy ước chuẩn hóa quá trình suy luận thành một Chữ ký tín hiệu thống nhất.

---

# Mục đích

Quy ước Chữ ký tín hiệu định nghĩa cách Hệ thống suy luận tạo và sử dụng Chữ ký tín hiệu.

Chữ ký tín hiệu là định danh chuẩn của một trạng thái suy luận.

Mọi Chữ ký tín hiệu đều được tạo theo cùng một quy ước.

---

# Triết lý

Mỗi quá trình suy luận đều để lại một dấu vết.

Chữ ký tín hiệu là dấu vết chuẩn của quá trình suy luận.

Một quy ước thống nhất giúp Hệ thống suy luận và Tri thức tích luỹ sử dụng cùng một ngôn ngữ.

---

# Mối quan hệ với Trading

```text
Tri thức nền

↓

Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ
```

Trong đó:

- Tri thức nền chuẩn hóa quy ước tạo Chữ ký tín hiệu.
- Hệ thống suy luận tạo Chữ ký tín hiệu sau khi hoàn thành quá trình suy luận.
- Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tra cứu Bộ nhớ.
- Bộ nhớ cung cấp các kinh nghiệm đã được Thực tế kiểm chứng để hỗ trợ những chu kỳ suy luận tiếp theo.

---

# Vai trò

Quy ước này giúp:

- Chuẩn hóa trạng thái suy luận.
- Chuẩn hóa quá trình tra cứu.
- Liên kết Trường hợp.
- Nhận diện Mẫu.
- Tra cứu Bài học tích luỹ.
- Tham khảo Thống kê.
- Đảm bảo tính nhất quán trong toàn bộ Trading Domain.

---

# Phạm vi

Quy ước này được sử dụng thống nhất trong:

- Hệ thống suy luận.
- Tri thức tích luỹ.
- Bộ nhớ.

---

# Cấu trúc

```text
01 · Định nghĩa

↓

02 · Cấu trúc

↓

03 · Tạo Chữ ký

↓

04 · Sử dụng

↓

05 · Ví dụ
```

---

# Nguyên tắc

Mỗi quá trình suy luận tạo ra một Chữ ký tín hiệu.

Một Chữ ký tín hiệu phản ánh trạng thái của Hệ thống suy luận tại một thời điểm cụ thể.

Chữ ký tín hiệu chuẩn hóa trạng thái suy luận trước khi Tri thức tích luỹ thực hiện quá trình tra cứu.

Mọi Chữ ký tín hiệu đều được tạo theo cùng một quy ước.

---

# Tóm tắt

```text
Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ
```

Chữ ký tín hiệu chuẩn hóa:

- Trạng thái suy luận.
- Quá trình tra cứu.
- Mối liên kết giữa Hệ thống suy luận và Tri thức tích luỹ.

Chữ ký tín hiệu là cầu nối giữa Hệ thống suy luận và Bộ nhớ.

---

# Triết lý

Chữ ký tín hiệu chuẩn hóa trạng thái suy luận.

Tri thức tích luỹ chuẩn hóa kinh nghiệm.

Bộ nhớ lưu giữ những kinh nghiệm đã được Thực tế kiểm chứng.

Sự phối hợp giữa ba thành phần này giúp Trading Domain học hỏi và hoàn thiện qua từng chu kỳ suy luận.

---

# 01 · Định nghĩa

> Bản chất của Chữ ký tín hiệu.

---

# Bản chất

Chữ ký tín hiệu là định danh chuẩn của một trạng thái suy luận.

Chữ ký tín hiệu chuẩn hóa trạng thái suy luận của Hệ thống suy luận thành một định danh thống nhất.

Mỗi Chữ ký tín hiệu đại diện cho một trạng thái suy luận tại một thời điểm.

Chữ ký tín hiệu phản ánh trạng thái suy luận của Hệ thống tại thời điểm được tạo.

---

# Vai trò

Chữ ký tín hiệu giúp:

- Chuẩn hóa trạng thái suy luận.
- Nhận diện các quá trình suy luận tương đồng.
- Tra cứu Bộ nhớ thông qua Tri thức tích luỹ.
- Liên kết giữa Hệ thống suy luận và Bộ nhớ.
- Đảm bảo tính nhất quán trong toàn bộ Trading Domain.

---

# Mối quan hệ với Trading

```text
Tri thức nền

↓

Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ
```

Trong đó:

- Tri thức nền chuẩn hóa quy ước tạo Chữ ký tín hiệu.
- Hệ thống suy luận tạo Chữ ký tín hiệu sau khi hoàn thành quá trình suy luận.
- Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tra cứu Bộ nhớ.

---

# Đặc điểm

Chữ ký tín hiệu đóng vai trò định danh chuẩn của trạng thái suy luận.

Trường hợp lưu dữ liệu đã được Thực tế kiểm chứng.

Mẫu tổng hợp nhiều Trường hợp có trạng thái suy luận tương đồng.

Bài học tích luỹ chuẩn hóa kinh nghiệm được rút ra từ nhiều Trường hợp.

Thống kê phản ánh kết quả quan sát từ nhiều Trường hợp.

Chữ ký tín hiệu lưu trạng thái suy luận của Hệ thống suy luận.

Tri thức được tích luỹ và quản lý trong Bộ nhớ thông qua Tri thức tích luỹ.

---

# Mối quan hệ

Một Chữ ký tín hiệu có thể được liên kết với:

- Chưa có Trường hợp nào.
- Một Trường hợp.
- Nhiều Trường hợp.

Một Trường hợp luôn liên kết với đúng một Chữ ký tín hiệu.

Một Chữ ký tín hiệu có thể được nhiều Trường hợp cùng sử dụng nếu chúng có cùng trạng thái suy luận.

---

# Mục tiêu

Chữ ký tín hiệu được tạo ra để:

- Chuẩn hóa trạng thái suy luận.
- Nhận diện các trạng thái suy luận tương đồng.
- Hỗ trợ Tri thức tích luỹ tra cứu Bộ nhớ.
- Liên kết giữa Hệ thống suy luận và Tri thức tích luỹ.
- Tái sử dụng kinh nghiệm trong các chu kỳ suy luận tiếp theo.

---

# Nguyên tắc

Một trạng thái suy luận tạo ra một Chữ ký tín hiệu.

Một Chữ ký tín hiệu có thể được nhiều Trường hợp cùng sử dụng khi chúng có cùng trạng thái suy luận.

Một Trường hợp luôn liên kết với đúng một Chữ ký tín hiệu.

Mỗi Chữ ký tín hiệu được cố định sau khi được tạo.

Chữ ký tín hiệu được xác định từ trạng thái suy luận tại thời điểm được tạo.

Tri thức tích luỹ sử dụng Chữ ký tín hiệu để nhận diện và liên kết dữ liệu trong Bộ nhớ.

---

# Tóm tắt

```text
Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ
```

Chữ ký tín hiệu chuẩn hóa:

- Trạng thái suy luận.
- Quá trình nhận diện.
- Quá trình tra cứu.
- Mối liên kết giữa Hệ thống suy luận và Tri thức tích luỹ.

Chữ ký tín hiệu là cầu nối giữa Hệ thống suy luận và Tri thức tích luỹ.

---

# Triết lý

Mỗi quá trình suy luận đều để lại một dấu vết.

Chữ ký tín hiệu là dấu vết chuẩn của quá trình suy luận.

Những dấu vết tương đồng giúp Tri thức tích luỹ nhận diện các trạng thái suy luận gần giống nhau.

Kinh nghiệm được tích luỹ từ nhiều lần suy luận đã được Thực tế kiểm chứng.

Tri thức được hình thành khi nhiều Trường hợp cùng chia sẻ một Chữ ký tín hiệu và được Thực tế kiểm chứng.

---

# 02 · Cấu trúc

> Thành phần cấu thành Chữ ký tín hiệu.

---

# Mục đích

Định nghĩa các thành phần tạo nên một Chữ ký tín hiệu.

Mọi Chữ ký tín hiệu đều được hình thành từ cùng một cấu trúc.

Cấu trúc thống nhất giúp Tri thức tích luỹ nhận diện, tra cứu và đối chiếu các trạng thái suy luận tương đồng.

---

# Triết lý

Chữ ký tín hiệu được hình thành từ toàn bộ trạng thái của quá trình suy luận.

Mỗi thành phần đóng góp một phần vào cấu trúc thống nhất của Chữ ký tín hiệu.

---

# Thành phần

Một Chữ ký tín hiệu được hình thành từ:

- Trạng thái hành vi.
- Trạng thái bối cảnh.
- Trạng thái động lượng.
- Trạng thái cấu trúc.
- Trạng thái chất lượng.
- Trạng thái quyết định.
- Trọng số tín hiệu.

Mỗi thành phần phản ánh một khía cạnh khác nhau của quá trình suy luận.

Toàn bộ các thành phần cùng tạo nên trạng thái suy luận được chuẩn hóa thành một Chữ ký tín hiệu.

---

# Mối quan hệ với Trading

```text
Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ
```

Trong đó:

- Hệ thống suy luận tạo Chữ ký tín hiệu sau khi hoàn thành quá trình suy luận.
- Chữ ký tín hiệu là đầu vào của Tri thức tích luỹ.
- Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tra cứu Bộ nhớ.

---

# Mô hình

```text
01 · Hành vi
        │
        ▼
02 · Bối cảnh
        │
        ▼
03 · Động lượng
        │
        ▼
04 · Cấu trúc
        │
        ▼
05 · Chất lượng
        │
        ▼
06 · Quyết định
        │
        ▼
07 · Trọng số tín hiệu
        │
        ▼
Chữ ký tín hiệu
        │
        ▼
Tri thức tích luỹ
        │
        ▼
08 · Không gian kịch bản
        │
        ▼
09 · Kế hoạch thực thi
```

---

# Đặc điểm

Mỗi thành phần phản ánh một phần của quá trình suy luận.

Mỗi thành phần đóng góp vào việc hình thành Chữ ký tín hiệu.

Toàn bộ trạng thái suy luận được phản ánh thông qua sự kết hợp của tất cả các thành phần.

Chữ ký tín hiệu phản ánh trạng thái của Hệ thống suy luận tại thời điểm được tạo.

---

# Nguyên tắc

Mọi Chữ ký tín hiệu đều sử dụng cùng một cấu trúc.

Cấu trúc của Chữ ký tín hiệu được sử dụng thống nhất trong toàn bộ Trading Domain.

Thay đổi ở bất kỳ thành phần nào của trạng thái suy luận đều có thể hình thành một Chữ ký tín hiệu mới.

Mỗi Chữ ký tín hiệu phản ánh trạng thái suy luận tại thời điểm được tạo.

Chữ ký tín hiệu chuẩn hóa trạng thái suy luận của Hệ thống suy luận.

Dữ liệu của Thực tế và kết quả kiểm chứng được quản lý thông qua Tri thức tích luỹ và Bộ nhớ.

---

# Tóm tắt

```text
01 · Hành vi
        │
02 · Bối cảnh
        │
03 · Động lượng
        │
04 · Cấu trúc
        │
05 · Chất lượng
        │
06 · Quyết định
        │
07 · Trọng số tín hiệu
        │
        ▼
Chữ ký tín hiệu
```

Chữ ký tín hiệu được hình thành từ toàn bộ trạng thái của Hệ thống suy luận.

Mỗi thành phần đóng góp một phần vào cấu trúc thống nhất của Chữ ký tín hiệu.

Cấu trúc thống nhất giúp Tri thức tích luỹ nhận diện, tra cứu và đối chiếu các trạng thái suy luận tương đồng.

---

# Triết lý

Toàn bộ trạng thái thị trường được quan sát thông qua nhiều tín hiệu.

Toàn bộ quá trình suy luận được hình thành từ nhiều tầng suy luận liên kết với nhau.

Chữ ký tín hiệu phản ánh trạng thái tổng thể của Hệ thống suy luận.

Chính trạng thái tổng thể đó giúp Tri thức tích luỹ nhận diện những lần suy luận tương đồng và tái sử dụng kinh nghiệm đã được Thực tế kiểm chứng.

---

# 03 · Tạo Chữ ký

> Quy tắc tạo Chữ ký tín hiệu.

---

# Mục đích

Quy định thời điểm và nguyên tắc tạo Chữ ký tín hiệu.

Mỗi quá trình suy luận tạo ra một Chữ ký tín hiệu.

Việc tạo Chữ ký tín hiệu đánh dấu thời điểm Hệ thống suy luận hoàn thành một trạng thái suy luận thống nhất.

---

# Triết lý

Chữ ký tín hiệu được tạo từ quá trình suy luận.

Kinh nghiệm được hình thành từ Thực tế.

Tri thức tích luỹ là cầu nối giữa suy luận và kinh nghiệm.

---

# Khi nào tạo?

Chữ ký tín hiệu được tạo sau khi:

- Hệ thống suy luận hoàn tất.
- Trạng thái quyết định đã được xác định.
- Trọng số tín hiệu đã được lượng hóa.

Đây là đầu ra cuối cùng của Hệ thống suy luận trước khi hình thành Không gian kịch bản.

---

# Vai trò

Việc tạo Chữ ký tín hiệu giúp:

- Chuẩn hóa trạng thái suy luận.
- Chuẩn hóa quá trình nhận diện.
- Liên kết Hệ thống suy luận với Tri thức tích luỹ.
- Đảm bảo mọi chu kỳ suy luận sử dụng cùng một cơ chế nhận diện.
- Tạo điểm bắt đầu cho quá trình tra cứu Bộ nhớ.

---

# Mối quan hệ với Trading

```text
Hệ thống suy luận

↓

Trọng số tín hiệu

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

08 · Không gian kịch bản

↓

09 · Kế hoạch thực thi
```

Trong đó:

- Hệ thống suy luận tạo Chữ ký tín hiệu sau khi hoàn thành quá trình suy luận.
- Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tham khảo Bộ nhớ.
- Không gian kịch bản và Kế hoạch thực thi được xây dựng dựa trên kết quả tham khảo từ Tri thức tích luỹ.

---

# Nguyên tắc

Mỗi quá trình suy luận tạo ra một Chữ ký tín hiệu.

Cùng một trạng thái suy luận tạo ra cùng một Chữ ký tín hiệu.

Thay đổi ở bất kỳ thành phần nào của trạng thái suy luận đều có thể hình thành một Chữ ký tín hiệu mới.

Chữ ký tín hiệu được tạo theo một quy ước thống nhất từ trạng thái suy luận.

Chữ ký tín hiệu được xác định từ trạng thái suy luận tại thời điểm được tạo.

---

# Mối quan hệ với Tri thức tích luỹ

Sau khi được tạo:

```text
Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ
```

Tri thức tích luỹ sử dụng Chữ ký tín hiệu để:

- Tra cứu Trường hợp.
- Nhận diện Mẫu.
- Tổng hợp Bài học tích luỹ.
- Tham khảo Thống kê.
- Hỗ trợ xây dựng Không gian kịch bản.
- Hỗ trợ xây dựng Kế hoạch thực thi.

---

# Sau khi được Thực tế kiểm chứng

Sau khi phương án được Thực tế kiểm chứng và Tầng Phản hồi thực tế hoàn tất:

```text
Chữ ký tín hiệu

↓

Trường hợp

↓

Mẫu

↓

Bài học tích luỹ

↓

Thống kê
```

Trong đó:

- Trường hợp lưu dữ liệu đã được kiểm chứng.
- Mẫu tổng hợp nhiều Trường hợp có trạng thái suy luận tương đồng.
- Bài học tích luỹ chuẩn hóa kinh nghiệm.
- Thống kê phản ánh kết quả quan sát từ nhiều Trường hợp.

---

# Tóm tắt

```text
Hệ thống suy luận

↓

Trọng số tín hiệu

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

08 · Không gian kịch bản

↓

09 · Kế hoạch thực thi
```

Chữ ký tín hiệu được tạo sau khi toàn bộ Hệ thống suy luận hoàn tất.

Việc tạo Chữ ký tín hiệu đánh dấu sự kết thúc của quá trình suy luận và là điểm khởi đầu cho quá trình tham khảo Tri thức tích luỹ.

---

# Triết lý

Chữ ký tín hiệu được tạo từ quá trình suy luận.

Kinh nghiệm được hình thành từ Thực tế.

Tri thức tích luỹ là cầu nối giữa suy luận và kinh nghiệm.

Tri thức được tích luỹ từ nhiều Trường hợp cùng chia sẻ một Chữ ký tín hiệu và được Thực tế kiểm chứng.

Chính quá trình tích luỹ đó giúp Trading Domain ngày càng nhận diện chính xác hơn các trạng thái suy luận tương đồng.

---

# 04 · Sử dụng

> Cách Chữ ký tín hiệu được sử dụng trong Trading Domain.

---

# Mục đích

Quy định cách Chữ ký tín hiệu được sử dụng trong Hệ thống suy luận và Tri thức tích luỹ.

Chữ ký tín hiệu là cầu nối giữa quá trình suy luận và Bộ nhớ.

---

# Triết lý

Chữ ký tín hiệu kết nối suy luận với kinh nghiệm.

Tri thức tích luỹ kết nối kinh nghiệm với quyết định.

Bộ nhớ lưu giữ những kinh nghiệm đã được Thực tế kiểm chứng.

---

# Luồng sử dụng

```text
Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ

↓

Tra cứu

↓

Đối chiếu

↓

Tổng hợp

↓

08 · Không gian kịch bản

↓

09 · Kế hoạch thực thi

↓

10 · Phản hồi thực tế

↓

Cập nhật Bộ nhớ
```

---

# Vai trò

Trong Trading Domain:

- Tầng 07 tạo Chữ ký tín hiệu.
- Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tra cứu Bộ nhớ.
- Không gian kịch bản được xây dựng dựa trên kết quả tham khảo từ Tri thức tích luỹ.
- Kế hoạch thực thi được xây dựng dựa trên kết quả tham khảo từ Tri thức tích luỹ.
- Phản hồi thực tế cung cấp dữ liệu để Tri thức tích luỹ cập nhật Bộ nhớ.

---

# Nguyên tắc

Chữ ký tín hiệu là định danh chuẩn của trạng thái suy luận.

Tri thức tích luỹ sử dụng Chữ ký tín hiệu để nhận diện và liên kết dữ liệu trong Bộ nhớ.

Quá trình hình thành Trường hợp được thực hiện sau khi Thực tế kiểm chứng hoàn tất.

Chữ ký tín hiệu được sử dụng sau khi Hệ thống suy luận hoàn tất.

---

# Mối quan hệ

```text
Chữ ký tín hiệu
        │
        ▼
Tri thức tích luỹ
        │
        ▼
Bộ nhớ
        │
        ▼
08 · Không gian kịch bản
        │
        ▼
09 · Kế hoạch thực thi
```

Trong đó:

- Chữ ký tín hiệu chuẩn hóa trạng thái suy luận.
- Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tra cứu Bộ nhớ.
- Bộ nhớ cung cấp các Trường hợp, Mẫu, Bài học tích luỹ và Thống kê liên quan.
- Không gian kịch bản và Kế hoạch thực thi được xây dựng từ kết quả tổng hợp của Tri thức tích luỹ.

---

# Tóm tắt

```text
Hệ thống suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ

↓

Không gian kịch bản

↓

Kế hoạch thực thi
```

Chữ ký tín hiệu chuẩn hóa điểm kết nối giữa Hệ thống suy luận và Tri thức tích luỹ.

Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tra cứu, đối chiếu và tổng hợp kinh nghiệm trong Bộ nhớ.

Kết quả tổng hợp hỗ trợ xây dựng Không gian kịch bản và Kế hoạch thực thi.

---

# Triết lý

Chữ ký tín hiệu kết nối suy luận với kinh nghiệm.

Tri thức tích luỹ kết nối kinh nghiệm với quyết định.

Bộ nhớ lưu giữ những kinh nghiệm đã được Thực tế kiểm chứng.

Những kinh nghiệm đó tiếp tục hỗ trợ các chu kỳ suy luận sau thông qua Tri thức tích luỹ.

---

# 05 · Ví dụ

> Minh họa cách Chữ ký tín hiệu được tạo và sử dụng trong Trading Domain.

---

# Mục đích

Minh họa cách Chữ ký tín hiệu được tạo và sử dụng trong Trading Domain.

Các ví dụ minh họa quy trình tạo, sử dụng và tra cứu Chữ ký tín hiệu.

Các ví dụ sử dụng dữ liệu minh họa để làm rõ quy trình vận hành của Trading Domain.

---

# Triết lý

Ví dụ giúp chuyển quy ước thành cách sử dụng cụ thể.

Nhiều ví dụ giúp làm rõ cách Hệ thống suy luận và Tri thức tích luỹ phối hợp trong thực tế.

---

# Mẫu chuẩn

```text
Quá trình suy luận

↓

Trạng thái hành vi

Trạng thái bối cảnh

Trạng thái động lượng

Trạng thái cấu trúc

Trạng thái chất lượng

Trạng thái quyết định

Trọng số tín hiệu

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ
```

---

# Ví dụ 01

## Quá trình suy luận

- Hành vi: Tăng.
- Bối cảnh: Thuận lợi.
- Động lượng: Mạnh.
- Cấu trúc: Tiếp diễn.
- Chất lượng: Cao.
- Quyết định: Ưu tiên Long.

↓

## Chữ ký tín hiệu

```text
SIG-EX01
```

↓

## Tri thức tích luỹ

```text
TH-0012
TH-0038

↓

M-0004

↓

BH-0007

↓

TK-0002
```

↓

## Kết quả

Tri thức tích luỹ trả về các Trường hợp, Mẫu, Bài học tích luỹ và Thống kê liên quan để Hệ thống suy luận tham khảo trước khi xây dựng Không gian kịch bản và Kế hoạch thực thi.

---

# Ví dụ 02

## Quá trình suy luận

- Hành vi: Đi ngang.
- Bối cảnh: Không rõ xu hướng.
- Động lượng: Yếu.
- Cấu trúc: Tích lũy.
- Chất lượng: Trung bình.
- Quyết định: Quan sát.

↓

## Chữ ký tín hiệu

```text
SIG-EX02
```

↓

## Tri thức tích luỹ

Tri thức tích luỹ chưa tìm thấy Trường hợp có trạng thái suy luận tương đồng.

↓

## Kết quả

Hệ thống suy luận tiếp tục đánh giá dựa trên dữ liệu hiện tại.

Sau khi xuất hiện các Trường hợp đã được Thực tế kiểm chứng, Tri thức tích luỹ sẽ cập nhật Bộ nhớ và tiếp tục hỗ trợ các chu kỳ suy luận sau.

---

# Nguyên tắc

Mỗi ví dụ minh họa một quá trình suy luận hoàn chỉnh.

Chữ ký tín hiệu được hình thành sau khi Hệ thống suy luận hoàn tất.

Tri thức tích luỹ sử dụng Chữ ký tín hiệu để tra cứu và liên kết dữ liệu trong Bộ nhớ.

Không gian kịch bản và Kế hoạch thực thi được xây dựng dựa trên kết quả tham khảo từ Tri thức tích luỹ.

Bộ nhớ được cập nhật sau khi Thực tế kiểm chứng hoàn tất.

---

# Mối quan hệ

```text
Quá trình suy luận
        │
        ▼
Chữ ký tín hiệu
        │
        ▼
Tri thức tích luỹ
        │
        ▼
Bộ nhớ
   │
   ├── Trường hợp
   ├── Mẫu
   ├── Bài học tích luỹ
   └── Thống kê
        │
        ▼
08 · Không gian kịch bản
        │
        ▼
09 · Kế hoạch thực thi
```

Các ví dụ minh họa toàn bộ chu trình sử dụng Chữ ký tín hiệu trong Trading Domain.

---

# Tóm tắt

```text
Quá trình suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ

↓

08 · Không gian kịch bản

↓

09 · Kế hoạch thực thi
```

Ví dụ minh họa cách Chữ ký tín hiệu vận hành trong Trading Domain.

Mỗi ví dụ phản ánh sự phối hợp giữa Hệ thống suy luận, Tri thức tích luỹ và Bộ nhớ trong một chu kỳ suy luận hoàn chỉnh.

---

# Triết lý

Mỗi quá trình suy luận đều tạo ra một Chữ ký tín hiệu.

Mỗi Chữ ký tín hiệu đều có thể trở thành cầu nối đến những kinh nghiệm đã được Thực tế kiểm chứng.

Tri thức được tích luỹ từ nhiều Trường hợp cùng chia sẻ một Chữ ký tín hiệu và được Thực tế kiểm chứng.

Những kinh nghiệm đã được tích luỹ tiếp tục hỗ trợ các chu kỳ suy luận sau thông qua Tri thức tích luỹ.

---

# Chu trình

```text
Quá trình suy luận

↓

Chữ ký tín hiệu

↓

Tri thức tích luỹ

↓

Bộ nhớ

↓

08 · Không gian kịch bản

↓

09 · Kế hoạch thực thi

↓

10 · Phản hồi thực tế

↓

Cập nhật Bộ nhớ

↓

Chu kỳ suy luận tiếp theo
```

Chữ ký tín hiệu kết nối Hệ thống suy luận với Tri thức tích luỹ.

Tri thức tích luỹ kết nối kinh nghiệm với quyết định.

Mỗi chu kỳ suy luận đều góp phần mở rộng và hoàn thiện Bộ nhớ của Trading Domain.

---

# Quy ước Trường hợp

> Quy định cấu trúc chuẩn khi ghi nhận một Trường hợp.

---

# Mục đích

Quy ước này chuẩn hóa cách ghi nhận Trường hợp.

Mọi Trường hợp sử dụng cùng một cấu trúc để Tri thức tích luỹ có thể tra cứu, đối chiếu và tổng hợp thống nhất.

---

# Triết lý

Một Trường hợp lưu giữ một lần vận hành hoàn chỉnh của Hệ thống suy luận đã được Thực tế kiểm chứng.

Cấu trúc thống nhất giúp kinh nghiệm được tích luỹ và tái sử dụng qua nhiều chu kỳ suy luận.

---

# Cấu trúc

```text
TH-xxxx

↓

Loại

↓

Bối cảnh

↓

Quan sát

- Hành vi giá
- Thanh khoản
- Dòng tiền

↓

Suy luận

↓

Thực thi

↓

Kết quả

↓

Nhận xét

↓

Từ khóa
```

---

# Nội dung

## Loại

Phân loại bản chất của Trường hợp.

Ví dụ:

- Tiếp diễn xu hướng.
- Đảo chiều xu hướng.
- Mở rộng vùng tích luỹ.
- Phá vỡ thất bại.

---

## Bối cảnh

Mô tả trạng thái thị trường tại thời điểm Trường hợp được hình thành.

---

## Quan sát

Ghi nhận dữ liệu đã được quan sát từ Thực tế.

Bao gồm:

- Hành vi giá.
- Thanh khoản.
- Dòng tiền.

---

## Suy luận

Tóm tắt kết quả của Hệ thống suy luận tại thời điểm xây dựng phương án hoặc kịch bản.

---

## Thực thi

Mô tả quá trình thực hiện phương án.

Có thể bao gồm:

- Điều kiện thực thi.
- Entry.
- Stop Loss.
- Take Profit.
- Quản trị vị thế.

---

## Kết quả

Ghi nhận kết quả sau khi Thực tế kiểm chứng.

Ví dụ:

- Đạt TP.
- Dừng lỗ.
- Không vào lệnh.
- Phương án mất hiệu lực.

---

## Nhận xét

Tổng hợp những kinh nghiệm rút ra từ Trường hợp sau khi hoàn tất.

---

## Từ khóa

Liệt kê các từ khóa phục vụ tra cứu.

Ví dụ:

- Trend Continuation.
- POC Pullback.
- EMA89 1H.
- Positive CVD.
- OI Increase.

---

# Nguyên tắc

Mỗi Trường hợp được lưu trong một tệp riêng.

Mọi Trường hợp sử dụng cùng một cấu trúc.

Các mục được sắp xếp theo cùng một thứ tự.

Nội dung phản ánh dữ liệu và kết quả đã được Thực tế kiểm chứng.

---

# Vai trò

Quy ước này giúp Tri thức tích luỹ:

- Tra cứu Trường hợp.
- Đối chiếu Trường hợp.
- Nhận diện Mẫu.
- Tổng hợp Bài học tích luỹ.
- Cập nhật Thống kê.

---

# Tóm tắt

```text
Thực tế

↓

Trường hợp

↓

Tri thức tích luỹ
```

Trường hợp chuẩn hóa việc ghi nhận một lần vận hành hoàn chỉnh của Hệ thống suy luận.

Đây là đơn vị tri thức cơ sở để hình thành Mẫu, Bài học tích luỹ và Thống kê.

---

# Quy ước Mẫu

> Quy định cấu trúc chuẩn khi ghi nhận một Mẫu.

---

# Mục đích

Quy ước này chuẩn hóa cách ghi nhận Mẫu trong Trading Domain.

Mỗi Mẫu được hình thành từ nhiều Trường hợp đã được Thực tế kiểm chứng.

Nhờ cấu trúc thống nhất, Tri thức tích luỹ có thể nhận diện các trạng thái và hành vi lặp lại để hỗ trợ những chu kỳ suy luận tiếp theo.

---

# Cấu trúc

```text
M-xxxx

↓

Tên Mẫu

↓

Nguồn hình thành

- Các Trường hợp liên quan

↓

Điều kiện xuất hiện

↓

Đặc điểm chung

↓

Điều kiện vô hiệu

↓

Mức độ xuất hiện

↓

Nhận xét

↓

Từ khóa
```

---

# Nội dung

## Tên Mẫu

Tên ngắn gọn phản ánh đặc điểm chung của Mẫu.

Ví dụ:

- POC Pullback
- EMA Multi-Timeframe Pullback
- Failed Breakout
- Trend Continuation

---

## Nguồn hình thành

Liệt kê các Trường hợp tạo nên Mẫu.

Ví dụ:

- TH-0001
- TH-0004
- TH-0012

Nguồn hình thành giúp truy ngược về dữ liệu gốc và theo dõi quá trình phát triển của Mẫu.

---

## Điều kiện xuất hiện

Mô tả các điều kiện thường xuất hiện trước khi Mẫu hình thành.

Ví dụ:

- Giá giữ POC.
- OI tăng.
- CVD tăng.
- Delta dương.
- Auction Flow đồng thuận.

Điều kiện xuất hiện phản ánh những yếu tố lặp lại giữa các Trường hợp.

---

## Đặc điểm chung

Tóm tắt các đặc điểm xuất hiện phổ biến trong những Trường hợp thuộc Mẫu.

Ví dụ:

- Giá thường Pullback trước khi tiếp diễn.
- POC thường dịch lên.
- Delta thường đồng thuận với CVD.

Đây là phần mô tả bản chất của Mẫu.

---

## Điều kiện vô hiệu

Mô tả những điều kiện làm Mẫu không còn phù hợp.

Ví dụ:

- Giá mất POC.
- CVD đảo chiều mạnh.
- Auction Flow suy yếu.
- Cấu trúc thị trường thay đổi.

---

## Mức độ xuất hiện

Phản ánh mức độ lặp lại của Mẫu qua các Trường hợp.

Ví dụ:

- Mới xuất hiện.
- Xuất hiện thường xuyên.
- Xuất hiện ổn định.

Mức độ xuất hiện giúp đánh giá độ trưởng thành của Mẫu.

---

## Nhận xét

Tổng hợp những điểm đáng chú ý sau khi đối chiếu các Trường hợp.

Phần này làm rõ những đặc điểm nổi bật của Mẫu và hỗ trợ quá trình tích luỹ tri thức.

---

## Từ khóa

Liệt kê các từ khóa phục vụ tra cứu.

Ví dụ:

- Trend Continuation
- POC Pullback
- EMA34 1H
- EMA89 15M
- Positive CVD
- OI Increase
- Auction Flow

---

# Nguyên tắc

- Mỗi tệp lưu một Mẫu.
- Một Mẫu được hình thành từ nhiều Trường hợp.
- Mẫu phản ánh những đặc điểm lặp lại đã được Thực tế kiểm chứng.
- Có thể mở rộng khi xuất hiện thêm Trường hợp phù hợp.
- Nguồn hình thành luôn duy trì khả năng truy ngược về các Trường hợp liên quan.

---

# Vai trò

Quy ước này giúp mọi Mẫu có cùng cấu trúc và cách biểu diễn.

Tri thức tích luỹ dựa trên Mẫu để:

- Nhận diện sự lặp lại.
- So sánh các Mẫu.
- Hình thành Bài học tích luỹ.
- Hỗ trợ cập nhật Thống kê.
- Hiệu chỉnh Không gian kịch bản và Kế hoạch thực thi.

---

# Tóm tắt

```text
Nhiều Trường hợp

↓

Mẫu

↓

Tri thức tích luỹ

↓

Bài học tích luỹ

↓

Thống kê
```

Mẫu là tầng tổng hợp đầu tiên trong Tri thức tích luỹ, giúp chuyển nhiều Trường hợp riêng lẻ thành một tri thức có thể tái sử dụng.

---

# Triết lý

Một Mẫu phản ánh những đặc điểm lặp lại đã được quan sát qua nhiều Trường hợp.

Sự lặp lại tạo nên Mẫu.

Mẫu tạo nền tảng cho quá trình tích luỹ tri thức.

---

# Quy ước Bài học tích luỹ

> Quy định cấu trúc chuẩn khi ghi nhận một Bài học tích luỹ.

---

# Mục đích

Quy ước này chuẩn hóa cách ghi nhận Bài học tích luỹ.

Mỗi Bài học tích luỹ được hình thành từ nhiều Mẫu và nhiều Trường hợp đã được Thực tế kiểm chứng.

Bài học tích luỹ giúp Tri thức tích luỹ tổng hợp kinh nghiệm để tham khảo trong quá trình suy luận và thực thi.

---

# Cấu trúc

```text
BH-xxxx

↓

Tên Bài học

↓

Nguồn hình thành

- Các Mẫu liên quan
- Các Trường hợp liên quan

↓

Bài học

↓

Điều kiện áp dụng

↓

Điều kiện chuyển ngữ cảnh

↓

Mức độ tin cậy

↓

Nhận xét

↓

Từ khóa
```

---

# Nội dung

## Tên Bài học

Tên ngắn gọn phản ánh nội dung kinh nghiệm được tích luỹ.

Ví dụ:

- Pullback tại POC có xác suất tiếp diễn cao.
- EMA đa khung thời gian giúp xác nhận hỗ trợ.
- Auction Flow đồng thuận giúp giảm False Break.

---

## Nguồn hình thành

Liệt kê các Mẫu và Trường hợp tạo nên Bài học.

Ví dụ:

Mẫu:

- M-0001
- M-0004

Trường hợp:

- TH-0001
- TH-0008
- TH-0016

Nguồn hình thành giúp truy ngược toàn bộ quá trình hình thành Bài học.

---

## Bài học

Tóm tắt kinh nghiệm được rút ra.

Ví dụ:

- Pullback tại POC thường hiệu quả hơn khi OI, CVD và Delta cùng đồng thuận.
- EMA đa khung thời gian giúp xác nhận vùng hỗ trợ động.
- Auction Flow đồng thuận giúp tăng xác suất tiếp diễn.

Bài học phản ánh kinh nghiệm đã được Thực tế kiểm chứng và phạm vi áp dụng của kinh nghiệm đó.

---

## Điều kiện áp dụng

Mô tả những điều kiện phù hợp để tham khảo Bài học.

Ví dụ:

- Xu hướng tăng.
- POC được giữ.
- OI tăng.
- CVD đồng thuận.
- Auction Flow đồng thuận.

---

## Điều kiện chuyển ngữ cảnh

Mô tả những điều kiện cho thấy nên tham khảo Bài học khác phù hợp hơn với trạng thái thị trường.

Ví dụ:

- Thị trường đi ngang.
- Cấu trúc xu hướng thay đổi.
- Thanh khoản biến động mạnh.
- Tin tức làm thay đổi hành vi thị trường.

---

## Mức độ tin cậy

Đánh giá mức độ tin cậy của Bài học.

Ví dụ:

- Thấp.
- Trung bình.
- Cao.

Mức độ tin cậy phản ánh mức độ kiểm chứng của Bài học qua các Trường hợp và Mẫu liên quan.

---

## Nhận xét

Tổng hợp những điểm đáng chú ý sau khi tổng hợp các Mẫu và Trường hợp.

Nhận xét giúp làm rõ phạm vi sử dụng và giá trị tham khảo của Bài học.

---

## Từ khóa

Liệt kê các từ khóa phục vụ tra cứu.

Ví dụ:

- Trend Continuation.
- POC Pullback.
- EMA Multi-Timeframe.
- Auction Flow.
- Positive CVD.
- OI Increase.

---

# Nguyên tắc

- Mỗi tệp lưu một Bài học tích luỹ.
- Một Bài học được hình thành từ nhiều Mẫu và nhiều Trường hợp.
- Bài học được xây dựng trên các dữ liệu đã được Thực tế kiểm chứng.
- Bài học có thể được cập nhật khi xuất hiện thêm Mẫu hoặc Trường hợp mới.
- Mỗi lần cập nhật đều dựa trên dữ liệu bổ sung từ Thực tế.

---

# Vai trò

Quy ước này giúp mọi Bài học tích luỹ có cấu trúc thống nhất.

Nhờ đó Tri thức tích luỹ có thể:

- Tham khảo kinh nghiệm.
- Hiệu chỉnh Không gian kịch bản.
- Hiệu chỉnh Kế hoạch thực thi.
- Hỗ trợ cập nhật Thống kê.

---

# Tóm tắt

```text
Nhiều Trường hợp

↓

Nhiều Mẫu

↓

Bài học tích luỹ

↓

Tri thức tích luỹ

↓

Không gian kịch bản

↓

Kế hoạch thực thi
```

Bài học tích luỹ chuẩn hóa:

- Kinh nghiệm đã được kiểm chứng.
- Điều kiện áp dụng.
- Điều kiện chuyển ngữ cảnh.
- Mức độ tin cậy.
- Giá trị tham khảo cho các chu kỳ suy luận tiếp theo.

---

# Triết lý

Mỗi Bài học phản ánh một kinh nghiệm đã được tích luỹ từ nhiều lần quan sát.

Những kinh nghiệm được kiểm chứng nhiều lần sẽ trở thành nền tảng tham khảo cho các chu kỳ suy luận tiếp theo.

---

# Quy ước Thống kê

> Quy định cấu trúc chuẩn khi ghi nhận một Thống kê.

---

# Mục đích

Quy ước này chuẩn hóa cách ghi nhận Thống kê.

Mọi Thống kê đều được tổng hợp từ nhiều Trường hợp đã được Thực tế kiểm chứng.

Thống kê giúp Tri thức tích luỹ định lượng mức độ xuất hiện và hiệu quả của các trạng thái, Mẫu hoặc Bài học.

---

# Cấu trúc

```text
TK-xxxx

↓

Tên Thống kê

↓

Nguồn dữ liệu

- Trường hợp
- Mẫu
- Bài học

↓

Phạm vi thống kê

↓

Chỉ số

↓

Kết quả

↓

Điều kiện áp dụng

↓

Nhận xét

↓

Từ khóa
```

---

# Nội dung

## Tên Thống kê

Tên ngắn gọn phản ánh nội dung được thống kê.

Ví dụ:

- Hiệu quả Pullback tại POC.
- Tỷ lệ thành công Trend Continuation.
- Hiệu quả EMA đa khung thời gian.
- Phân bố Reward / Risk.

---

## Nguồn dữ liệu

Liệt kê nguồn dữ liệu sử dụng để tạo Thống kê.

Có thể bao gồm:

### Trường hợp

- TH-0001
- TH-0005
- TH-0018

### Mẫu

- M-0002
- M-0004

### Bài học

- BH-0001

Nguồn dữ liệu giúp truy ngược toàn bộ quá trình hình thành Thống kê.

---

## Phạm vi thống kê

Mô tả phạm vi của Thống kê.

Ví dụ:

- Trend Continuation.
- BTC.
- Khung thời gian 15M–4H.
- POC Pullback.

Phạm vi giúp sử dụng Thống kê đúng ngữ cảnh.

---

## Chỉ số

Liệt kê các chỉ số được thống kê.

Ví dụ:

- Số Trường hợp.
- Tỷ lệ thành công.
- Tỷ lệ thất bại.
- Reward / Risk trung bình.
- Holding Time trung bình.
- Drawdown trung bình.
- Win Rate.
- Expectancy.

Các chỉ số phản ánh kết quả định lượng của nguồn dữ liệu.

---

## Kết quả

Trình bày kết quả thống kê.

Ví dụ:

- 52 Trường hợp.
- Win Rate: 71%.
- RR trung bình: 2.6.
- Holding Time trung bình: 7 giờ.

Kết quả phản ánh dữ liệu lịch sử đã được tổng hợp và kiểm chứng.

---

## Điều kiện áp dụng

Mô tả điều kiện phù hợp để tham khảo Thống kê.

Ví dụ:

- Xu hướng tăng.
- POC được giữ.
- OI đồng thuận.
- CVD đồng thuận.
- Delta đồng thuận.

---

## Nhận xét

Tóm tắt những điểm đáng chú ý.

Ví dụ:

- Win Rate tăng khi Auction Flow đồng thuận.
- Reward / Risk giảm trong thị trường Sideway.
- Delta đồng thuận giúp giảm False Break.

Nhận xét làm rõ ý nghĩa của kết quả thống kê trong phạm vi đã quan sát.

---

## Từ khóa

Liệt kê các từ khóa phục vụ tra cứu.

Ví dụ:

- Trend Continuation.
- POC Pullback.
- EMA Multi-Timeframe.
- Positive Delta.
- Positive CVD.
- Auction Flow.
- Statistics.

---

# Nguyên tắc

- Mỗi tệp lưu một Thống kê.
- Một Thống kê được tổng hợp từ nhiều Trường hợp và có thể tham khảo thêm Mẫu hoặc Bài học.
- Mọi số liệu đều dựa trên dữ liệu đã được Thực tế kiểm chứng.
- Thống kê được cập nhật khi có thêm dữ liệu phù hợp.
- Mọi số liệu đều truy ngược được nguồn dữ liệu.

---

# Vai trò

Quy ước này giúp mọi Thống kê có cấu trúc thống nhất.

Nhờ đó Tri thức tích luỹ có thể:

- Định lượng mức độ tin cậy.
- So sánh hiệu quả giữa các phương án.
- Hiệu chỉnh Không gian kịch bản.
- Hiệu chỉnh Kế hoạch thực thi.

---

# Tóm tắt

```text
Trường hợp

↓

Mẫu

↓

Bài học

↓

Thống kê
```

Thống kê chuẩn hóa:

- Nguồn dữ liệu.
- Phạm vi quan sát.
- Các chỉ số định lượng.
- Kết quả tổng hợp.

Thống kê cung cấp cơ sở định lượng để Tri thức tích luỹ hỗ trợ quá trình suy luận.

---

# Triết lý

Thống kê lượng hóa những gì Thực tế đã ghi nhận.

Dữ liệu được tổng hợp theo cùng một quy ước giúp Tri thức tích luỹ đánh giá kinh nghiệm một cách nhất quán.