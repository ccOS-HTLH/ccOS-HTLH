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