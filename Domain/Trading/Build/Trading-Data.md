---
title: Nguồn dữ liệu
id: trading-data-source
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-20
last_updated: 2026-07-27
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - data
---

# Nguồn dữ liệu

> Nguồn dữ liệu là thành phần tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

---

# Mục đích

Nguồn dữ liệu trả lời:

> Thực tế được ghi nhận như thế nào?

Nguồn dữ liệu ghi nhận và chuẩn hóa dữ liệu từ Thực tế để cung cấp đầu vào cho Hệ thống suy luận.

---

# Triết lý

Dữ liệu luôn đi trước suy luận.

Dữ liệu được chuẩn hóa trước khi tham gia Hệ thống suy luận.

---

# Kiến trúc

```text
Nguồn dữ liệu

├── README.md
├── ATS.md
└── Dữ liệu rời rạc.md
```

---

# Mối quan hệ với Trading

```text
             Tri thức nền
                    │
                    ▼

Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận
```

Trong đó:

- Thực tế là nguồn gốc của mọi dữ liệu.
- Nguồn dữ liệu tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.
- Tri thức nền cung cấp các khái niệm và quy ước để chuẩn hóa dữ liệu.
- Dữ liệu chuẩn hóa trở thành đầu vào của Hệ thống suy luận.

---

# Đầu vào

- Thực tế.

---

# Đầu ra

- Dữ liệu chuẩn hóa.

---

# Tham khảo

- Tri thức nền.

Nguồn dữ liệu sử dụng Tri thức nền để chuẩn hóa dữ liệu trước khi chuyển sang Hệ thống suy luận.

---

# Thành phần

## 01 · ATS

ATS là mẫu chuẩn để ghi nhận và chuẩn hóa dữ liệu từ Thực tế theo một cấu trúc thống nhất.

ATS giúp quan sát đồng thời nhiều khía cạnh của thị trường.

---

## 02 · Dữ liệu rời rạc

Dữ liệu rời rạc ghi nhận các dữ liệu từ Thực tế theo từng đơn vị quan sát độc lập.

Ví dụ:

- Funding Rate.
- Open Interest.
- CVD.
- VPIN.
- Fear & Greed.
- Long / Short Ratio.
- News.
- Macro.
- ...

Các dữ liệu này có thể:

* được ghi nhận trực tiếp;
* được tổ chức trong ATS;
* hoặc được kết hợp với ATS tùy theo ngữ cảnh quan sát.

---

# Nguyên tắc

Mọi dữ liệu đều phản ánh Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa theo các quy ước trong Tri thức nền trước khi được sử dụng.

ATS và Dữ liệu rời rạc đều là các nguồn dữ liệu của Hệ thống suy luận.

---

# Vai trò trong Trading

```text
Trading Domain

├── Tri thức nền
│      Chuẩn hóa ngôn ngữ và quy ước
│
├── Nguồn dữ liệu
│      Ghi nhận và chuẩn hóa dữ liệu
│
├── Hệ thống suy luận
│      Phân tích và xây dựng phương án
│
└── Tri thức tích luỹ
       Chuẩn hóa và lưu giữ kinh nghiệm
```

Nguồn dữ liệu là đầu vào của Hệ thống suy luận.

---

# Tóm tắt

```text
Thực tế

↓

Nguồn dữ liệu

↓

Dữ liệu chuẩn hóa

↓

Hệ thống suy luận
```

Nguồn dữ liệu chuẩn hóa:

- Cách tiếp nhận Thực tế.
- Cách ghi nhận dữ liệu.
- Cách chuẩn hóa dữ liệu.
- Cấu trúc dữ liệu đầu vào của Hệ thống suy luận.

---

---
title: ATS
id: trading-ats
version: 1.1
status: Stable
author: HTLH
language: vi
created: 2026-07-19
last_updated: 2026-07-27
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - ats
---

# ATS

> ATS là mẫu chuẩn để ghi nhận và chuẩn hóa dữ liệu từ Thực tế.

---

# Mục đích

ATS chuẩn hóa việc ghi nhận dữ liệu từ Thực tế theo một cấu trúc thống nhất, tạo ra dữ liệu đầu vào chuẩn hóa cho Hệ thống suy luận.

---

# Triết lý

ATS chuẩn hóa cách ghi nhận và biểu diễn dữ liệu từ Thực tế.

Dữ liệu được chuẩn hóa trước khi đi vào Hệ thống suy luận.

---

# Quy ước dữ liệu

Trong ATS, các ký hiệu được quy ước như sau.

## Auction Flow

- **VP1**: Chỉ số VP1 của indicator Auction Flow.
- **POC5**: Point of Control trên biểu đồ BTC khung 5m của indicator Auction Flow.
- **Auction Line**: Đường Auction Flow.
- **EMA20**: Đường EMA20 của Auction Flow.

---

## SonicR

- **Cụm EMA34**: Ba đường EMA34 màu xanh dương.
- **EMA89**: Đường EMA89 màu cam.
- **EMA200**: Đường EMA200 màu tím.
- **EMA610**: Đường EMA610 màu trắng.

---

## Volume Profile M30

- **POC30**: Point of Control của Volume Profile khung 30 phút.
- **VAH30**: Value Area High của Volume Profile khung 30 phút.
- **VAL30**: Value Area Low của Volume Profile khung 30 phút.

---

# Kiến trúc

```text
ATS

├── 01 · Đa khung thời gian
├── 02 · Auction Flow
├── 03 · Thực thi
└── 04 · Chỉ số bổ sung
```

---

# Thứ tự đọc

```text
01 · Đa khung thời gian

↓

02 · Auction Flow

↓

03 · Thực thi

↓

04 · Chỉ số bổ sung
```

---

# 01 · Đa khung thời gian

## Bố cục

```text
┌───────────────┬───────────────┐
│       D       │      4H       │
├───────────────┼───────────────┤
│      1H       │      15m      │
└───────────────┴───────────────┘
```

---

## Thứ tự đọc

```text
D

↓

4H

↓

1H

↓

15m
```

---

## Ghi nhận

- Giá.
- Cấu trúc.
- Cấu trúc SonicR.
- Khối lượng.
- RSI.

---

# 02 · Auction Flow

## Bố cục

```text
Biểu đồ BTC
(VP1 + POC5)

↓

RSI

↓

OI

↓

Auction Flow
(Auction Line + EMA20)
```

---

## Thứ tự đọc

```text
Biểu đồ BTC

↓

RSI

↓

OI

↓

Auction Flow
```

---

## Ghi nhận

### Biểu đồ BTC

- Giá.
- VP1.
- POC5.

### RSI

- RSI.

### OI

- Open Interest.

### Auction Flow

- Auction Line.
- EMA20.

---

# 03 · Thực thi

## Bố cục

```text
┌─────────────────────────┬─────────────────────────┐
│      5m + Delta         │ Heatmap Thanh khoản    │
├─────────────────────────┼─────────────────────────┤
│ Heatmap Sổ lệnh         │ Volume Profile M30     │
└─────────────────────────┴─────────────────────────┘
```

---

## Thứ tự đọc

```text
5m + Delta

↓

Heatmap Thanh khoản

↓

Heatmap Sổ lệnh

↓

Volume Profile M30
```

---

## Ghi nhận

### 5m + Delta

- Giá.
- Cấu trúc SonicR.
- Delta.
- Khối lượng.

### Heatmap Thanh khoản

- Các cụm thanh khoản còn tồn tại.

### Heatmap Sổ lệnh

- Tường mua.
- Tường bán.

### Volume Profile M30

Theo bảng thông tin của indicator:

- POC30.
- VAH30.
- VAL30.

---

# 04 · Chỉ số bổ sung

Được ghi nhận cùng ba ảnh.

## Dòng tiền

- Funding Rate.
- CVD.
- VPIN.
- Agg Liquidation.

---

## Tâm lý thị trường

- Fear & Greed.

---

## Vị thế thị trường

Long / Short Ratio (1H)

- Global.
- Top Accounts.
- Top Positions.

---

# Nguyên tắc

Mọi dữ liệu đều phản ánh Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa theo các quy ước trong Tri thức nền trước khi được sử dụng.

ATS chuẩn hóa dữ liệu trước khi dữ liệu tham gia Hệ thống suy luận.

ATS là một trong các nguồn dữ liệu của Trading Domain.

---

# Vai trò trong Nguồn dữ liệu

```text
Thực tế

↓

ATS

↓

Dữ liệu chuẩn hóa

↓

Hệ thống suy luận
```

ATS là mẫu chuẩn để ghi nhận và chuẩn hóa dữ liệu từ Thực tế.

ATS chuẩn hóa:

- Cấu trúc dữ liệu.
- Thứ tự quan sát.
- Quy ước dữ liệu.
- Đầu vào cho Hệ thống suy luận.

---

# Tóm tắt

```text
Thực tế

↓

ATS

↓

Dữ liệu chuẩn hóa

↓

Hệ thống suy luận
```

ATS chuẩn hóa:

- Cách ghi nhận Thực tế.
- Thứ tự quan sát.
- Cấu trúc dữ liệu.
- Quy ước dữ liệu.
- Dữ liệu đầu vào cho Hệ thống suy luận.

ATS là cầu nối giữa Thực tế và Hệ thống suy luận thông qua dữ liệu đã được chuẩn hóa.

---

---
title: Dữ liệu rời rạc
id: trading-discrete-data
version: 1.1
status: Stable
author: HTLH
language: vi
created: 2026-07-20
last_updated: 2026-07-31
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - data
---

# Dữ liệu rời rạc

> Dữ liệu rời rạc ghi nhận một hoặc nhiều khía cạnh của Thực tế.

---

# Mục đích

Dữ liệu rời rạc ghi nhận các dữ liệu từ Thực tế theo từng đơn vị quan sát độc lập.

Dữ liệu rời rạc có thể được ghi nhận trong ATS hoặc độc lập tùy theo ngữ cảnh sử dụng.

Dữ liệu rời rạc chuẩn hóa và bổ sung dữ liệu đầu vào cho Hệ thống suy luận.

---

# Triết lý

Dữ liệu rời rạc mở rộng khả năng quan sát Thực tế.

Dữ liệu rời rạc bổ sung dữ liệu đầu vào cho Hệ thống suy luận.

---

# Kiến trúc

```text
Dữ liệu rời rạc

├── Chỉ số
├── Biểu đồ
├── Sự kiện
└── Tập dữ liệu
```

---

# Mối quan hệ với Trading

```text
             Tri thức nền
                    │
                    ▼

Thực tế

↓

Dữ liệu rời rạc

↓

Hệ thống suy luận
```

Trong đó:

- Thực tế là nguồn gốc của mọi dữ liệu.
- Dữ liệu rời rạc ghi nhận một hoặc nhiều dữ liệu từ Thực tế.
- Dữ liệu rời rạc có thể được tổ chức trong ATS hoặc được ghi nhận độc lập tùy theo ngữ cảnh.
- Tri thức nền cung cấp các khái niệm và quy ước để chuẩn hóa dữ liệu.
- Dữ liệu sau khi được chuẩn hóa trở thành đầu vào của Hệ thống suy luận.

---

# Đầu vào

- Thực tế.

---

# Đầu ra

- Dữ liệu chuẩn hóa.

---

# Tham khảo

- Tri thức nền.

Dữ liệu rời rạc sử dụng Tri thức nền để chuẩn hóa dữ liệu trước khi chuyển sang Hệ thống suy luận.

---

# Thành phần

## Chỉ số

Ví dụ:

- Funding Rate.
- Open Interest.
- CVD.
- VPIN.
- Fear & Greed.
- Long / Short Ratio.
- Chỉ số khác.

---

## Biểu đồ

Ví dụ:

- On-chain.
- Dominance.
- Macro Chart.
- Biểu đồ khác.

---

## Sự kiện

Ví dụ:

- News.
- Lịch kinh tế.
- Sự kiện vĩ mô.
- Sự kiện doanh nghiệp.
- Sự kiện khác.

---

## Tập dữ liệu

Ví dụ:

- Macro.
- On-chain.
- Dữ liệu thống kê.
- Bộ dữ liệu khác.

---

# Đặc điểm

Dữ liệu rời rạc có thể là:

- Một chỉ số.
- Một biểu đồ.
- Một sự kiện.
- Một tập dữ liệu.

Dữ liệu rời rạc có thể:

- Được ghi nhận trong ATS.
- Được ghi nhận độc lập.
- Được kết hợp với ATS tùy theo ngữ cảnh quan sát.

---

# Nguyên tắc

Mỗi dữ liệu phản ánh một phần của Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa theo các quy ước trong Tri thức nền trước khi được sử dụng.

ATS và Dữ liệu rời rạc đều là các nguồn dữ liệu của Hệ thống suy luận.

---

# Vai trò trong Nguồn dữ liệu

```text
Thực tế
        │
        ▼
   Dữ liệu rời rạc
        │
   ┌────┴────┐
   ▼         ▼
 ATS      Độc lập
   └────┬────┘
        ▼
Dữ liệu chuẩn hóa
        ▼
Hệ thống suy luận
```

Dữ liệu rời rạc mở rộng khả năng ghi nhận Thực tế.

Các dữ liệu rời rạc có thể được sử dụng độc lập hoặc được tổ chức trong ATS trước khi chuyển sang Hệ thống suy luận.

---

# Tóm tắt

```text
Thực tế

↓

Dữ liệu rời rạc

↓

Dữ liệu chuẩn hóa

↓

Hệ thống suy luận
```

Dữ liệu rời rạc chuẩn hóa:

- Các chỉ số.
- Các biểu đồ.
- Các sự kiện.
- Các tập dữ liệu.

Dữ liệu rời rạc bổ sung dữ liệu đầu vào cho Hệ thống suy luận.

Dữ liệu rời rạc có thể được ghi nhận trong ATS hoặc độc lập tùy theo ngữ cảnh sử dụng.