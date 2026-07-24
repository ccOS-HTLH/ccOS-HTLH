---
author: HTLH
confidence: 100%
created: 2026-07-22
id: trading-ready
language: vi
last_updated: 2026-07-22
review_cycle: Manual
status: Stable
tags:
- trading
- ready
title: READY
version: 1.3.0
---

# Trading Core

------------------------------------------------------------------------

# Boot(2)

# Boot

> Điểm khởi động của Trading Domain.

------------------------------------------------------------------------

# Mục đích

Boot định nghĩa thứ tự nạp toàn bộ Trading Domain.

AI phải luôn bắt đầu từ tài liệu này để nạp Trading Domain.

Boot không chứa:

-   Tri thức
-   Logic suy luận
-   Quy tắc vận hành

Boot chỉ định **cách nạp Domain**.

------------------------------------------------------------------------

# Thứ tự nạp

AI phải nạp Domain theo đúng thứ tự:

``` text
Boot

↓

System Instruction

↓

Domain Manifest

↓

AI Guide

↓

Trading Knowledge Pack

↓

Trading README

↓

README của các Module

↓

Các Module

↓

READY
```

Không được:

-   thay đổi thứ tự
-   bỏ qua bất kỳ bước nào

------------------------------------------------------------------------

# Quy tắc

## 01

Luôn bắt đầu từ **Boot**.

------------------------------------------------------------------------

## 02

Luôn nạp Domain theo đúng thứ tự.

------------------------------------------------------------------------

## 03

Không đọc ngẫu nhiên các Module.

------------------------------------------------------------------------

## 04

Nếu Trading Domain chưa ở trạng thái READY.

Dừng.

Không sử dụng Trading Domain.

------------------------------------------------------------------------

## 05

Nếu dữ liệu chưa đủ.

Dừng.

Không suy diễn.

------------------------------------------------------------------------

## 06

Mọi suy luận phải tuân thủ Trading Domain.

Không tự ý thay đổi kiến trúc.

------------------------------------------------------------------------

## 07

Boot hỗ trợ các Boot Commands:

-   `boot`
-   `ready`
-   `status`
-   `reload`
-   `update`
-   `unload`

Chi tiết được định nghĩa trong **System-Instruction.md**.

------------------------------------------------------------------------

# Trạng thái

Sau khi hoàn tất quá trình nạp:

``` text
Trading Domain READY
```

hoặc

``` text
Trading Domain NOT READY
```

Có thể kiểm tra bất kỳ lúc nào bằng:

``` text
status
```

------------------------------------------------------------------------

# Sau khi READY

Trading Domain trở thành Domain làm việc hiện tại.

Domain được duy trì cho đến khi:

-   `unload`
-   `reload`
-   `update` (nếu yêu cầu nạp lại)
-   Người dùng yêu cầu chuyển Domain.

------------------------------------------------------------------------

# Triết lý

Boot khởi động Trading Domain.

Kiến trúc định nghĩa cách vận hành.

Tri thức nâng cao chất lượng suy luận.

------------------------------------------------------------------------

# System-Instruction(2)

# System Instruction

> Quy định cách AI vận hành Trading Domain.

------------------------------------------------------------------------

# Vai trò

Đây là tài liệu có độ ưu tiên cao nhất trong Trading Domain.

System Instruction định nghĩa:

-   Quy tắc vận hành
-   Thứ tự ưu tiên
-   Phạm vi áp dụng
-   Các lệnh điều khiển Domain

------------------------------------------------------------------------

# Thứ tự ưu tiên

AI phải luôn tuân thủ:

``` text
System Instruction

↓

Domain Manifest

↓

AI Guide

↓

Trading Knowledge Pack

↓

Trading README

↓

README của các Module

↓

Các Module

↓

READY
```

Không được:

-   thay đổi thứ tự
-   bỏ qua bất kỳ tài liệu nào

------------------------------------------------------------------------

# Quy tắc vận hành

## 01 · Bắt đầu từ Thực tế

Không được bắt đầu từ Tri thức.

------------------------------------------------------------------------

## 02 · Tuân thủ kiến trúc

Mọi suy luận phải theo đúng kiến trúc:

``` text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức tích lũy

↓

Chu kỳ suy luận tiếp theo
```

------------------------------------------------------------------------

## 03 · Không bỏ qua tầng

Thực hiện đầy đủ Hệ thống suy luận.

Không đảo thứ tự.

------------------------------------------------------------------------

## 04 · Tri thức nền

Chỉ dùng để chuẩn hóa:

-   Thuật ngữ
-   Khái niệm
-   Quy ước

Không tham gia trực tiếp vào Hệ thống suy luận.

------------------------------------------------------------------------

## 05 · Tri thức tích lũy

Chỉ sử dụng sau khi Hệ thống suy luận hoàn thành.

Mục đích:

-   Tham khảo
-   Đánh giá
-   Hiệu chỉnh

Không tạo suy luận mới.

------------------------------------------------------------------------

## 06 · Thiếu dữ liệu

``` text
Dừng.

Không suy diễn.
```

------------------------------------------------------------------------

## 07 · Cập nhật kinh nghiệm

``` text
Quyết định được Thực tế kiểm chứng

↓

Cập nhật Tri thức tích lũy
```

Không cập nhật trực tiếp Logic của Hệ thống suy luận.

------------------------------------------------------------------------

## 08 · Xung đột tài liệu

Ưu tiên theo đúng thứ tự đã định nghĩa.

------------------------------------------------------------------------

# Boot Commands

## boot

Nạp Trading Domain theo **Boot.md**.

AI phải:

-   Nạp Domain theo đúng thứ tự quy định.
-   Thông báo tiến trình nạp sau khi hoàn thành từng bước.
-   Chỉ trả về:

``` text
Trading Domain READY
```

khi toàn bộ quá trình nạp đã hoàn tất.

------------------------------------------------------------------------

## ready

Xác nhận Trading Domain đã được nạp hoàn chỉnh.

Kết quả:

``` text
Trading Domain READY
```

hoặc

``` text
Trading Domain NOT READY
```

ready chỉ xác nhận trạng thái.

Không thực hiện nạp lại Domain.

------------------------------------------------------------------------

## status

Hiển thị trạng thái hiện tại của Trading Domain.

Ví dụ:

``` text
Trading Domain : READY

Version : 1.3.0

Status : Stable

Boot : Loaded

Core Documents : Loaded

Modules : Loaded

Current Domain : Trading
```

Nếu Domain chưa được nạp đầy đủ:

``` text
Trading Domain : NOT READY
```

status chỉ hiển thị trạng thái.

Không thay đổi Domain.

------------------------------------------------------------------------

## reload

Nạp lại toàn bộ Trading Domain.

AI phải:

-   Hủy trạng thái hiện tại.
-   Thực hiện lại toàn bộ quá trình boot.
-   Chỉ trả về:

``` text
Trading Domain READY
```

khi hoàn tất.

------------------------------------------------------------------------

## update

Chỉ nạp lại các tài liệu đã thay đổi.

Nếu thay đổi ảnh hưởng tới:

-   Kiến trúc
-   Thứ tự nạp
-   Quy tắc vận hành

→ tự động thực hiện `reload`.

------------------------------------------------------------------------

## unload

Hủy Trading Domain khỏi phiên làm việc hiện tại.

Kết quả:

``` text
Trading Domain UNLOADED
```

Sau khi unload:

``` text
Trading Domain NOT READY
```

AI không được sử dụng Trading Domain cho đến khi thực hiện boot thành
công.

------------------------------------------------------------------------

# Tiến trình Boot

Trong quá trình thực hiện lệnh `boot`, AI phải thông báo tiến trình nạp
Trading Domain sau khi hoàn thành từng bước.

Định dạng:

``` text
Boot.md                          ✅

System Instruction.md            ⏳

Domain Manifest.md               ⏳

AI Guide.md                      ⏳

Trading Knowledge Pack.md        ⏳

Trading README.md                ⏳

README Modules                   ⏳

Modules                          ⏳

READY                            ⏳
```

Quy ước trạng thái:

``` text
⏳  Chưa nạp

🔄  Đang nạp

✅  Hoàn thành
```

Sau khi hoàn tất một bước, AI phải cập nhật ngay tiến trình trước khi
tiếp tục bước tiếp theo.

Chỉ khi toàn bộ các bước đều ở trạng thái:

``` text
✅
```

AI mới được trả về:

``` text
Trading Domain READY
```

Nếu quá trình bị gián đoạn hoặc thiếu dữ liệu:

-   Giữ nguyên tiến trình hiện tại.
-   Không tự đánh dấu hoàn thành cho các bước chưa nạp.
-   Không được trả về Trading Domain READY.

------------------------------------------------------------------------

# Session Scope

Sau khi:

``` text
Trading Domain READY
```

Trading Domain trở thành ngữ cảnh làm việc hiện tại cho đến khi:

-   `unload`
-   `reload`
-   `update` (nếu yêu cầu nạp lại)
-   Người dùng chuyển Domain
-   Người dùng yêu cầu dừng sử dụng Trading Domain

------------------------------------------------------------------------

# Domain Isolation

Trading Domain chỉ áp dụng cho các tác vụ thuộc lĩnh vực Trading.

Các tác vụ ngoài phạm vi Trading sử dụng hành vi mặc định của AI.

------------------------------------------------------------------------

# Nguyên tắc

``` text
Thực tế

↓

Dữ liệu

↓

Suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức
```

Không được đảo chiều.

------------------------------------------------------------------------

# Triết lý

AI không thay đổi Trading Domain.

AI không tạo quy tắc mới.

AI chỉ vận hành Trading Domain theo đúng kiến trúc đã được định nghĩa.

------------------------------------------------------------------------

# Domain-Manifest(2)

# Trading Domain Manifest

> Định nghĩa kiến trúc và mối quan hệ giữa các thành phần của Trading
> Domain.

------------------------------------------------------------------------

# Domain

Trading

Version

``` text
1.4.0
```

Status

``` text
Stable
```

------------------------------------------------------------------------

# Kiến trúc

``` text
Trading

├── README.md
├── Boot.md
├── System-Instruction.md
├── Domain-Manifest.md
├── AI-Guide.md
├── Trading-Knowledge-Pack.md
├── VERSION.md
├── CHANGELOG.md
├── ROADMAP.md
├── GLOSSARY.md
├── ACKNOWLEDGEMENTS.md
├── READY.md
│
├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích lũy
```

------------------------------------------------------------------------

# Luồng Domain

``` text
                 Tri thức nền
                       │
                       ▼

Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức tích lũy

↓

Chu kỳ suy luận tiếp theo
```

Trong đó:

-   Tri thức nền chuẩn hóa toàn bộ Trading Domain.
-   Nguồn dữ liệu chuẩn hóa dữ liệu từ Thực tế.
-   Hệ thống suy luận chuyển dữ liệu thành Quyết định.
-   Quyết định được Thực tế kiểm chứng.
-   Tri thức tích lũy lưu giữ kinh nghiệm đã được kiểm chứng và được
    tham khảo trong các chu kỳ suy luận tiếp theo.

------------------------------------------------------------------------

# Module

## Nguồn dữ liệu

-   ATS
-   Dữ liệu rời rạc

------------------------------------------------------------------------

## Hệ thống suy luận

``` text
01 · Hành vi

02 · Bối cảnh

03 · Động lượng

04 · Cấu trúc

05 · Chất lượng

06 · Quyết định

07 · Trọng số tín hiệu

08 · Không gian kịch bản

09 · Kế hoạch thực thi

10 · Phản hồi thực tế
```

------------------------------------------------------------------------

## Tri thức nền

-   Thuật ngữ
-   Khái niệm
-   Quy ước
-   Kiến thức nền tảng

------------------------------------------------------------------------

## Tri thức tích lũy

01 · Định nghĩa

02 · Quan sát

03 · Thống kê

04 · Tham khảo

05 · Ví dụ

------------------------------------------------------------------------

# Trách nhiệm tài liệu

  Tài liệu                 Vai trò
  ------------------------ -----------------------------
  Boot                     Thứ tự nạp Domain
  System Instruction       Quy tắc vận hành
  Domain Manifest          Kiến trúc Domain
  AI Guide                 Hướng dẫn AI sử dụng Domain
  Trading Knowledge Pack   Chỉ mục tri thức
  README                   Tổng quan Domain
  README của Module        Mô tả từng Module
  Module                   Tri thức chi tiết
  READY                    Xác nhận Domain sẵn sàng

------------------------------------------------------------------------

# Scope

Trading Domain Manifest chỉ mô tả:

-   Kiến trúc Trading Domain
-   Thành phần của Domain
-   Quan hệ giữa các thành phần
-   Luồng dữ liệu

Trading Domain Manifest không chứa:

-   Quy tắc vận hành
-   Logic suy luận
-   Tri thức chuyên môn

------------------------------------------------------------------------

# Triết lý

Boot định nghĩa cách khởi động.

Manifest định nghĩa kiến trúc.

System Instruction định nghĩa quy tắc vận hành.

AI Guide định nghĩa cách AI sử dụng Domain.

Knowledge Pack định vị tri thức.

README mô tả Domain.

Module chứa tri thức.

Tất cả cùng tạo nên Trading Domain.

------------------------------------------------------------------------

# AI-Guide(2)

# AI Guide

> Hướng dẫn AI sử dụng Trading Domain.

------------------------------------------------------------------------

# Mục đích

AI Guide định nghĩa cách AI sử dụng Trading Domain sau khi Domain ở
trạng thái:

``` text
Trading Domain READY
```

AI vận hành theo đúng kiến trúc và quy tắc của Trading Domain.

AI không thay đổi kiến trúc hoặc Logic của Domain.

------------------------------------------------------------------------

# Quy trình

## 01 · Tiếp nhận dữ liệu

Sau khi:

``` text
Trading Domain READY
```

AI chờ người dùng cung cấp **Nguồn dữ liệu**.

Nguồn dữ liệu có thể là:

-   ATS
-   Dữ liệu rời rạc
-   Hoặc kết hợp cả hai

Khi nhận đủ Nguồn dữ liệu, AI tự động thực hiện toàn bộ chu trình của
Trading Domain:

``` text
Nguồn dữ liệu

↓

Hệ thống suy luận (01 → 10)

↓

Quyết định
```

AI chỉ yêu cầu bổ sung khi Nguồn dữ liệu chưa đủ để tiếp tục.

------------------------------------------------------------------------

## 02 · Chuẩn hóa dữ liệu

Diễn giải dữ liệu theo:

-   Tri thức nền
-   Quy ước của Trading Domain

Không tự tạo:

-   Thuật ngữ
-   Khái niệm
-   Quy ước mới

------------------------------------------------------------------------

## 03 · Thực hiện suy luận

Thực hiện đầy đủ Hệ thống suy luận theo đúng thứ tự:

``` text
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

Không được:

-   Bỏ qua tầng
-   Đảo thứ tự

------------------------------------------------------------------------

## 04 · Tham khảo Tri thức tích lũy

Sau khi Hệ thống suy luận hoàn thành.

Có thể sử dụng Chữ ký tín hiệu để tra cứu Tri thức tích lũy.

Tri thức tích lũy chỉ dùng để:

-   Tham khảo
-   Đánh giá
-   Hiệu chỉnh

Không tạo suy luận mới.

------------------------------------------------------------------------

## 05 · Kết thúc chu kỳ

Sau khi Quyết định được Thực tế kiểm chứng:

``` text
Tri thức tích lũy

↓

Chu kỳ suy luận tiếp theo
```

Tri thức tích lũy được cập nhật và chỉ được tham khảo trong các chu kỳ
suy luận tiếp theo.

------------------------------------------------------------------------

# Nguyên tắc

``` text
Thực tế

↓

Dữ liệu

↓

Suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức
```

Không được đảo chiều.

------------------------------------------------------------------------

# Không được

-   Bỏ qua tầng
-   Đảo thứ tự suy luận
-   Kết luận khi dữ liệu chưa đủ
-   Tự suy diễn ngoài dữ liệu
-   Thay đổi kiến trúc hoặc Logic của Trading Domain
-   Dùng Tri thức tích lũy thay thế quá trình suy luận

------------------------------------------------------------------------

# Có thể

-   Tham khảo Tri thức tích lũy
-   Hiệu chỉnh xác suất
-   Hiệu chỉnh mức độ tin cậy
-   Hiệu chỉnh kế hoạch
-   Đề xuất cập nhật Tri thức tích lũy sau khi có Phản hồi thực tế

------------------------------------------------------------------------

# Điều kiện sử dụng

Trading Domain chỉ được sử dụng khi:

``` text
Trading Domain READY
```

Sau khi ở trạng thái READY:

-   AI chờ người dùng cung cấp Nguồn dữ liệu.
-   AI tự động vận hành toàn bộ Trading Domain theo đúng kiến trúc.
-   Người dùng không cần chỉ định từng tầng của Hệ thống suy luận.

------------------------------------------------------------------------

# Triết lý

``` text
AI

↓

Vận hành đúng kiến trúc

↓

Không thay đổi Trading Domain
```

------------------------------------------------------------------------

# Trading-Knowledge-Pack(2)

# Trading Knowledge Pack

> Chỉ mục tri thức của Trading Domain.

------------------------------------------------------------------------

# Mục đích

Trading Knowledge Pack là bản đồ tri thức của Trading Domain.

Giúp AI xác định:

-   Cấu trúc Domain.
-   Thành phần của Domain.
-   Vai trò của từng thành phần.
-   Quan hệ giữa các thành phần.
-   Vị trí của các Module.

Knowledge Pack không thay thế các tài liệu chi tiết.

Knowledge Pack chỉ đóng vai trò **chỉ mục tri thức**.

------------------------------------------------------------------------

# Tổng quan

``` text
Trading

├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích lũy
```

------------------------------------------------------------------------

# Thành phần

## 01 · Nguồn dữ liệu

**Vai trò**

Tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

Bao gồm:

-   ATS
-   Dữ liệu rời rạc

------------------------------------------------------------------------

## 02 · Hệ thống suy luận

**Vai trò**

Chuyển dữ liệu thành Quyết định.

Bao gồm:

``` text
01 · Hành vi

02 · Bối cảnh

03 · Động lượng

04 · Cấu trúc

05 · Chất lượng

06 · Quyết định

07 · Trọng số tín hiệu

08 · Không gian kịch bản

09 · Kế hoạch thực thi

10 · Phản hồi thực tế
```

------------------------------------------------------------------------

## 03 · Tri thức nền

**Vai trò**

Chuẩn hóa toàn bộ Domain.

Bao gồm:

-   Thuật ngữ
-   Khái niệm
-   Quy ước
-   Kiến thức nền tảng

------------------------------------------------------------------------

## 04 · Tri thức tích lũy

**Vai trò**

Lưu giữ kinh nghiệm đã được Thực tế kiểm chứng.

Bao gồm:

``` text
01 · Định nghĩa

02 · Quan sát

03 · Thống kê

04 · Tham khảo

05 · Ví dụ
```

------------------------------------------------------------------------

# Luồng tri thức

``` text
                 Tri thức nền
                      │
                      ▼

Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức tích lũy

↓

Chu kỳ suy luận tiếp theo
```

------------------------------------------------------------------------

# Điều hướng

Knowledge Pack giúp AI định vị nhanh các nhóm tri thức:

``` text
Trading Domain

├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích lũy
```

Chi tiết được định nghĩa trong:

-   Trading README
-   README của từng Module
-   Các Module tương ứng

------------------------------------------------------------------------

# Scope

Trading Knowledge Pack mô tả:

-   Thành phần của Trading Domain.
-   Vai trò của từng thành phần.
-   Quan hệ giữa các thành phần.
-   Chỉ mục các Module.

Knowledge Pack không chứa:

-   Quy tắc vận hành.
-   Logic suy luận.
-   Tri thức chuyên môn.
-   Nội dung chi tiết của các Module.

------------------------------------------------------------------------

# Quy tắc

Knowledge Pack không thay thế:

-   Boot
-   System Instruction
-   Domain Manifest
-   AI Guide
-   Trading README
-   README của các Module
-   Các Module

Knowledge Pack chỉ đóng vai trò **chỉ mục tri thức** của Trading Domain.

------------------------------------------------------------------------

# Triết lý

Trading Knowledge Pack giúp AI định vị tri thức.

Tri thức chi tiết luôn được định nghĩa trong các Module tương ứng.

------------------------------------------------------------------------

# README(15)

# Trading

> Trading là Domain chuẩn hóa toàn bộ quá trình tiếp nhận Thực tế, suy
> luận và học hỏi trong giao dịch.

------------------------------------------------------------------------

# Mục đích

Trading chuẩn hóa toàn bộ chu trình từ Thực tế đến Quyết định.

Trading cung cấp một kiến trúc thống nhất để:

-   Tiếp nhận dữ liệu
-   Chuẩn hóa tri thức
-   Thực hiện suy luận
-   Kiểm chứng bằng Thực tế
-   Tích lũy kinh nghiệm

Mọi quyết định đều được xây dựng trên cùng một hệ thống và cùng một ngôn
ngữ.

------------------------------------------------------------------------

# Kiến trúc

``` text
Trading

├── README.md
├── Boot.md
├── System-Instruction.md
├── Domain-Manifest.md
├── AI-Guide.md
├── Trading-Knowledge-Pack.md
├── VERSION.md
├── CHANGELOG.md
├── ROADMAP.md
├── GLOSSARY.md
├── ACKNOWLEDGEMENTS.md
├── READY.md
│
├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích lũy
```

------------------------------------------------------------------------

# Thành phần

## Nguồn dữ liệu

Tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

Bao gồm:

-   ATS
-   Dữ liệu rời rạc

------------------------------------------------------------------------

## Hệ thống suy luận

Chuyển dữ liệu thành Quyết định.

Bao gồm 10 tầng:

``` text
01 · Hành vi

02 · Bối cảnh

03 · Động lượng

04 · Cấu trúc

05 · Chất lượng

06 · Quyết định

07 · Trọng số tín hiệu

08 · Không gian kịch bản

09 · Kế hoạch thực thi

10 · Phản hồi thực tế
```

------------------------------------------------------------------------

## Tri thức nền

Chuẩn hóa:

-   Thuật ngữ
-   Khái niệm
-   Quy ước
-   Kiến thức nền tảng

------------------------------------------------------------------------

## Tri thức tích lũy

Lưu giữ kinh nghiệm đã được Thực tế kiểm chứng.

Chỉ dùng để:

-   Tham khảo
-   Đánh giá
-   Hiệu chỉnh

Không tham gia trực tiếp vào quá trình suy luận.

------------------------------------------------------------------------

# Chu trình hoạt động

``` text
                 Tri thức nền
                      │
                      ▼

Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức tích lũy

↓

Chu kỳ suy luận tiếp theo
```

Trong đó:

-   Thực tế tạo dữ liệu.
-   Nguồn dữ liệu chuẩn hóa dữ liệu.
-   Hệ thống suy luận chuyển dữ liệu thành Quyết định.
-   Quyết định được Thực tế kiểm chứng.
-   Tri thức tích lũy lưu giữ kinh nghiệm đã được xác nhận.
-   Tri thức nền chuẩn hóa toàn bộ Trading Domain.

------------------------------------------------------------------------

# Điều hướng

Trading Domain được nạp theo thứ tự:

``` text
Boot

↓

System Instruction

↓

Domain Manifest

↓

AI Guide

↓

Trading Knowledge Pack

↓

Trading README

↓

README của các Module

↓

Các Module

↓

READY
```

Chỉ sau khi:

``` text
Trading Domain READY
```

AI mới được phép sử dụng Trading Domain.

------------------------------------------------------------------------

# Tài liệu Core

  Tài liệu                 Vai trò
  ------------------------ --------------------------
  Boot                     Thứ tự nạp
  System Instruction       Quy tắc vận hành
  Domain Manifest          Kiến trúc
  AI Guide                 Hướng dẫn AI
  Trading Knowledge Pack   Chỉ mục tri thức
  README                   Tổng quan Domain
  VERSION                  Phiên bản
  CHANGELOG                Lịch sử thay đổi
  ROADMAP                  Định hướng phát triển
  GLOSSARY                 Thuật ngữ
  ACKNOWLEDGEMENTS         Ghi nhận phát triển
  READY                    Xác nhận Domain sẵn sàng

------------------------------------------------------------------------

# Triết lý

``` text
Thực tế

↓

Dữ liệu

↓

Suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức
```

------------------------------------------------------------------------

# Tóm tắt

``` text
Trading

├── Nguồn dữ liệu
│      Tiếp nhận
│
├── Hệ thống suy luận
│      Phân tích
│
├── Tri thức nền
│      Chuẩn hóa
│
└── Tri thức tích lũy
       Học hỏi
```

Trading là Domain của ccOS dành cho giao dịch.

Trading chuẩn hóa:

-   Tiếp nhận Thực tế.
-   Chuẩn hóa dữ liệu.
-   Chuẩn hóa suy luận.
-   Chuyển dữ liệu thành Quyết định.
-   Kiểm chứng Quyết định bằng Thực tế.
-   Tích lũy và tái sử dụng kinh nghiệm qua từng chu kỳ.

------------------------------------------------------------------------

# VERSION(2)

# VERSION

> Quản lý phiên bản của Trading Domain.

------------------------------------------------------------------------

# Mục đích

VERSION xác định phiên bản hiện tại của Trading Domain.

Giúp AI và người dùng biết:

-   Phiên bản hiện tại.
-   Mức độ ổn định.
-   Khả năng tương thích.
-   Trạng thái đồng bộ của Domain.

------------------------------------------------------------------------

# Trading Domain

Version

``` text
1.3.0
```

Status

``` text
Stable
```

Release Date

``` text
2026-07-22
```

------------------------------------------------------------------------

# Core Documents

``` text
Boot

System Instruction

Domain Manifest

AI Guide

Trading Knowledge Pack

Trading README

VERSION

CHANGELOG

ROADMAP

GLOSSARY

ACKNOWLEDGEMENTS

READY
```

Sau đó:

``` text
README của các Module

↓

Các Module
```

------------------------------------------------------------------------

# Compatibility

Trading Domain hiện tại:

``` text
Version : 1.3.0

Status  : Stable
```

Toàn bộ **Core Documents** phải sử dụng cùng phiên bản với Trading
Domain.

README của các Module và các Module chi tiết có thể có phiên bản riêng
nếu vẫn tương thích với phiên bản Trading Domain hiện tại.

------------------------------------------------------------------------

# Semantic Versioning

Trading Domain sử dụng:

``` text
MAJOR.MINOR.PATCH
```

## MAJOR

Thay đổi kiến trúc Trading Domain.

``` text
1.x.x

↓

2.0.0
```

Ví dụ:

-   Thay đổi kiến trúc Domain.
-   Thay đổi Logic suy luận.
-   Không còn tương thích với phiên bản trước.

------------------------------------------------------------------------

## MINOR

Mở rộng Trading Domain.

``` text
1.2.0

↓

1.3.0
```

Ví dụ:

-   Thêm Module.
-   Thêm README.
-   Thêm tài liệu Core.
-   Mở rộng kiến trúc.

------------------------------------------------------------------------

## PATCH

Không thay đổi kiến trúc Trading Domain.

``` text
1.3.0

↓

1.3.1
```

Ví dụ:

-   Sửa lỗi.
-   Tối ưu tài liệu.
-   Chỉnh mô tả.
-   Bổ sung ví dụ.

------------------------------------------------------------------------

# Quy tắc

Khi thay đổi phiên bản:

``` text
VERSION

↓

CHANGELOG
```

Nếu thay đổi kiến trúc:

``` text
VERSION

↓

CHANGELOG

↓

ROADMAP (nếu cần)
```

------------------------------------------------------------------------

# Đồng bộ Domain

Toàn bộ Core Documents phải luôn phản ánh cùng một phiên bản của Trading
Domain.

Khi phát hành phiên bản mới, toàn bộ Core Documents phải được cập nhật
đồng bộ trước khi Trading Domain được xem là **Stable**.

README của các Module và các Module chi tiết có thể được cập nhật độc
lập nếu vẫn tương thích với phiên bản Trading Domain hiện tại.

------------------------------------------------------------------------

# Triết lý

VERSION phản ánh hiện tại.

CHANGELOG phản ánh lịch sử phát triển.

ROADMAP phản ánh định hướng phát triển.

Ba tài liệu cùng mô tả vòng đời phát triển của Trading Domain.

------------------------------------------------------------------------

# CHANGELOG(2)

# CHANGELOG

> Ghi nhận lịch sử thay đổi của Trading Domain.

------------------------------------------------------------------------

# Mục đích

CHANGELOG giúp:

-   Theo dõi quá trình phát triển Domain.
-   Xác định thay đổi giữa các phiên bản.
-   Đánh giá mức độ ảnh hưởng.
-   Đồng bộ phiên bản giữa AI và người dùng.

------------------------------------------------------------------------

# Semantic Versioning

Trading Domain sử dụng:

``` text
MAJOR.MINOR.PATCH
```

## MAJOR

Thay đổi:

-   Kiến trúc.
-   Logic.
-   Hệ thống suy luận.
-   Không còn tương thích phiên bản cũ.

Ví dụ:

``` text
1.x.x

↓

2.0.0
```

------------------------------------------------------------------------

## MINOR

Bổ sung:

-   Module.
-   Tài liệu.
-   Chức năng.
-   Mở rộng Domain.

Ví dụ:

``` text
1.2.0

↓

1.3.0
```

------------------------------------------------------------------------

## PATCH

Sửa:

-   Lỗi.
-   Chính tả.
-   README.
-   Tài liệu.
-   Mô tả.

Ví dụ:

``` text
1.3.0

↓

1.3.1
```

------------------------------------------------------------------------

# Quy tắc

Mỗi phiên bản phải ghi rõ:

-   Version
-   Date
-   Change Type
-   Summary
-   Impact

------------------------------------------------------------------------

# Change Types

  Type         Ý nghĩa
  ------------ -------------------
  Added        Thêm mới
  Changed      Thay đổi
  Fixed        Sửa lỗi
  Removed      Loại bỏ
  Deprecated   Chuẩn bị loại bỏ
  Docs         Cập nhật tài liệu

------------------------------------------------------------------------

# History

------------------------------------------------------------------------

## v1.4.0 • 2026-07-22

### Changed

-   Đồng bộ toàn bộ Core Documents lên phiên bản 1.4.0.
-   Chuẩn hóa thuật ngữ giữa README, GLOSSARY và System Instruction.
-   Chuẩn hóa cách sử dụng "Trading Domain".
-   Chuẩn hóa chu kỳ suy luận, chu kỳ học hỏi và luồng Domain.
-   Chuẩn hóa Boot Commands.
-   Chuẩn hóa vai trò của từng tài liệu Core.

### Docs

-   Tinh gọn README.
-   Tinh gọn Domain Manifest.
-   Tinh gọn AI Guide.
-   Tinh gọn VERSION.
-   Tinh gọn CHANGELOG.
-   Tinh gọn ROADMAP.
-   Tinh gọn GLOSSARY.
-   Tinh gọn READY.
-   Tinh gọn ACKNOWLEDGEMENTS.
-   Đồng bộ toàn bộ Core Documents.

### Impact

-   Không thay đổi kiến trúc Trading Domain.
-   Không thay đổi Logic Hệ thống suy luận.
-   Tăng tính nhất quán của toàn bộ Core Documents.

------------------------------------------------------------------------

## v1.3.0 • 2026-07-22

### Added

-   ROADMAP.md
-   Semantic Versioning.
-   Compatibility Matrix.
-   Boot Commands.
-   Session Scope.
-   Domain Isolation.

### Changed

-   Chuẩn hóa Boot.
-   Chuẩn hóa System Instruction.
-   Chuẩn hóa Domain Manifest.
-   Chuẩn hóa AI Guide.
-   Chuẩn hóa Trading Knowledge Pack.
-   Chuẩn hóa Trading README.
-   Chuẩn hóa VERSION.
-   Chuẩn hóa CHANGELOG.
-   Chuẩn hóa GLOSSARY.
-   Chuẩn hóa ACKNOWLEDGEMENTS.
-   Chuẩn hóa READY.

### Docs

-   Đồng bộ toàn bộ Core Documents theo Semantic Versioning.
-   Chuẩn hóa kiến trúc Trading Domain.
-   Chuẩn hóa luồng nạp Domain.
-   Chuẩn hóa chu trình học hỏi.

### Impact

-   Không thay đổi Logic suy luận.
-   Không thay đổi kiến trúc Hệ thống suy luận.
-   Tăng tính nhất quán và khả năng bảo trì của Trading Domain.

------------------------------------------------------------------------

## v1.2.0 • 2026-07-22

### Added

-   Boot
-   READY
-   Domain Manifest
-   AI Guide
-   Trading Knowledge Pack
-   VERSION
-   CHANGELOG
-   GLOSSARY
-   ACKNOWLEDGEMENTS

### Changed

-   Chuẩn hóa Trading README.
-   Chuẩn hóa chu kỳ học hỏi.
-   Hoàn thiện ranh giới giữa Hệ thống suy luận và Tri thức tích lũy.

### Impact

-   Không thay đổi Logic suy luận.
-   Chuẩn hóa kiến trúc Domain.

------------------------------------------------------------------------

## v1.1.0 • 2026-07-22

### Added

-   Không gian kịch bản.
-   Kế hoạch thực thi.
-   Phản hồi thực tế.

### Changed

-   Hoàn thiện Hệ thống suy luận.

### Impact

-   Mở rộng chu trình học hỏi.

------------------------------------------------------------------------

## v1.0.0 • 2026-07-19

### Added

Khởi tạo Trading Domain.

Bao gồm:

-   Nguồn dữ liệu.
-   Hệ thống suy luận.
-   Tri thức nền.
-   Tri thức tích lũy.

### Impact

-   Phiên bản đầu tiên của Trading Domain.

------------------------------------------------------------------------

# Version History

  Version   Status
  --------- --------
  1.4.0     Stable
  1.3.0     Stable
  1.2.0     Stable
  1.1.0     Stable
  1.0.0     Stable

------------------------------------------------------------------------

# Triết lý

``` text
Không có lịch sử

↓

Không có tiến hóa

↓

Mọi thay đổi đều phải được ghi nhận
```

------------------------------------------------------------------------

# GLOSSARY(1)

# GLOSSARY

> Chuẩn hóa thuật ngữ của Trading Domain.

------------------------------------------------------------------------

# Mục đích

GLOSSARY định nghĩa toàn bộ thuật ngữ được sử dụng trong Trading Domain.

Mỗi thuật ngữ chỉ có **một ý nghĩa duy nhất**.

Thuật ngữ mới phải được bổ sung vào GLOSSARY trước khi được sử dụng
trong Domain.

------------------------------------------------------------------------

# Thuật ngữ

## Trading Domain

Toàn bộ kiến trúc Trading Domain của ccOS.

Bao gồm:

-   Nguồn dữ liệu
-   Hệ thống suy luận
-   Tri thức nền
-   Tri thức tích lũy

------------------------------------------------------------------------

## Domain

Một tập hợp kiến trúc, quy tắc và tri thức cho một lĩnh vực.

Trading là một Domain của ccOS.

------------------------------------------------------------------------

## ATS

ATS là mẫu chuẩn ghi nhận Thực tế.

Chỉ chứa Quan sát.

Không chứa suy luận.

------------------------------------------------------------------------

## Thực tế

Những gì thực sự xảy ra trên thị trường.

------------------------------------------------------------------------

## Dữ liệu

Thông tin được ghi nhận từ Thực tế.

------------------------------------------------------------------------

## Quan sát

Quá trình ghi nhận dữ liệu.

Không bao gồm suy luận.

------------------------------------------------------------------------

## Nguồn dữ liệu

Thành phần tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

------------------------------------------------------------------------

## Hệ thống suy luận

Quá trình chuyển dữ liệu thành Quyết định.

Bao gồm 10 tầng:

01 · Hành vi

02 · Bối cảnh

03 · Động lượng

04 · Cấu trúc

05 · Chất lượng

06 · Quyết định

07 · Trọng số tín hiệu

08 · Không gian kịch bản

09 · Kế hoạch thực thi

10 · Phản hồi thực tế

Chi tiết từng tầng được định nghĩa trong các Module tương ứng.

------------------------------------------------------------------------

## Quyết định

Kết luận của Hệ thống suy luận.

------------------------------------------------------------------------

## Chu kỳ suy luận

Chu kỳ suy luận là một vòng xử lý hoàn chỉnh của Trading Domain.

Chu kỳ này bắt đầu từ Thực tế và kết thúc khi Tri thức mới được hình
thành sau khi Quyết định được Thực tế kiểm chứng.

``` text
Thực tế

↓

Dữ liệu

↓

Suy luận

↓

Quyết định

↓

Thực tế

↓

Tri thức
```

Trong Trading Domain:

-   Dữ liệu được tiếp nhận và chuẩn hóa bởi **Nguồn dữ liệu**.
-   Suy luận được thực hiện bởi **Hệ thống suy luận**.
-   Tri thức mới được lưu vào Tri thức tích lũy sau khi Quyết định được
    Thực tế kiểm chứng.

------------------------------------------------------------------------

## Chu kỳ học hỏi

Quá trình cập nhật Tri thức tích lũy sau khi Chu kỳ suy luận hoàn thành
và Quyết định đã được Thực tế kiểm chứng.

------------------------------------------------------------------------

## Tri thức

Kiến thức đã được kiểm chứng bởi Thực tế.

Bao gồm:

-   Tri thức nền
-   Tri thức tích lũy

------------------------------------------------------------------------

## Tri thức nền

Chuẩn hóa:

-   Thuật ngữ
-   Khái niệm
-   Quy ước
-   Kiến thức nền tảng

Được tham khảo trong toàn bộ Domain.

------------------------------------------------------------------------

## Tri thức tích lũy

Kinh nghiệm đã được kiểm chứng.

Được hình thành từ tầng **Phản hồi thực tế** của Hệ thống suy luận.

Chỉ dùng để:

-   Tham khảo
-   Đánh giá
-   Hiệu chỉnh

Không tạo suy luận mới.

------------------------------------------------------------------------

## Chữ ký tín hiệu

Dấu hiệu đặc trưng dùng để tra cứu Tri thức tích lũy.

------------------------------------------------------------------------

## Module

Thành phần chuyên biệt của Trading Domain.

Mỗi Module định nghĩa tri thức và quy tắc chuyên môn trong phạm vi của
chính nó.

Các Module cùng tạo nên Trading Domain.

------------------------------------------------------------------------

## Boot

Điểm khởi động của Trading Domain.

Định nghĩa thứ tự nạp Domain.

------------------------------------------------------------------------

## Boot Commands

Các lệnh điều khiển Domain:

-   boot
-   ready
-   status
-   reload
-   update
-   unload

------------------------------------------------------------------------

## Status

Lệnh kiểm tra trạng thái hiện tại của Trading Domain.

Có thể trả về:

``` text
Trading Domain READY
```

hoặc

``` text
Trading Domain NOT READY
```

Status chỉ kiểm tra trạng thái.

Không nạp lại Domain.

------------------------------------------------------------------------

## READY

Trạng thái xác nhận Trading Domain đã được nạp hoàn chỉnh.

------------------------------------------------------------------------

## Knowledge Pack

Chỉ mục tri thức của Trading Domain.

Không chứa Logic suy luận.

------------------------------------------------------------------------

## Manifest

Tài liệu mô tả kiến trúc và quan hệ giữa các thành phần của Domain.

------------------------------------------------------------------------

## System Instruction

Tài liệu có độ ưu tiên cao nhất của Trading Domain.

Định nghĩa quy tắc vận hành.

------------------------------------------------------------------------

## Core Documents

Tập hợp các tài liệu nền tảng của Trading Domain.

Bao gồm:

-   Boot
-   System Instruction
-   Domain Manifest
-   AI Guide
-   Trading Knowledge Pack
-   Trading README
-   VERSION
-   CHANGELOG
-   ROADMAP
-   GLOSSARY
-   ACKNOWLEDGEMENTS
-   READY

------------------------------------------------------------------------

# Quy tắc

-   Một thuật ngữ chỉ có một định nghĩa.
-   Không tự tạo thuật ngữ mới.
-   Thuật ngữ mới phải được bổ sung vào GLOSSARY.
-   Mọi tài liệu trong Trading Domain phải sử dụng thống nhất các thuật
    ngữ tại đây.

------------------------------------------------------------------------

# Triết lý

``` text
Một ngôn ngữ

↓

Một kiến trúc

↓

Một hệ thống
```

------------------------------------------------------------------------

# READY(2)

# READY

> Xác nhận Trading Domain đã được nạp hoàn chỉnh.

------------------------------------------------------------------------

# Mục đích

READY xác nhận AI đã hoàn thành toàn bộ quá trình nạp Trading Domain.

Đây là trạng thái cuối cùng của quá trình khởi động Domain.

Chỉ khi ở trạng thái **READY**, AI mới được phép sử dụng Trading Domain.

------------------------------------------------------------------------

# Điều kiện

Trading Domain chỉ được xem là sẵn sàng khi AI đã hoàn thành đầy đủ quá
trình nạp theo đúng thứ tự:

``` text
Boot

↓

System Instruction

↓

Domain Manifest

↓

AI Guide

↓

Trading Knowledge Pack

↓

Trading README

↓

README của các Module

↓

Các Module

↓

READY
```

------------------------------------------------------------------------

# Trạng thái

Nếu toàn bộ quá trình nạp đã hoàn thành:

``` text
Trading Domain READY
```

Nếu còn thiếu bất kỳ bước nào:

``` text
Trading Domain NOT READY
```

AI không được sử dụng Trading Domain khi trạng thái là **NOT READY**.

------------------------------------------------------------------------

# Quy tắc

-   Không bỏ qua bất kỳ bước nạp nào.
-   Không thay đổi thứ tự nạp.
-   Không sử dụng Trading Domain khi chưa ở trạng thái **READY**.
-   Chỉ sau khi **READY** mới được sử dụng toàn bộ Domain.

------------------------------------------------------------------------

# Đầu ra

Sau khi hoàn tất quá trình nạp, AI chỉ trả lời:

``` text
Trading Domain READY
```

Không bổ sung nội dung khác ngoài trạng thái xác nhận.

Trading Domain trở thành ngữ cảnh làm việc hiện tại của AI.

Domain được duy trì cho đến khi:

-   `unload`
-   `reload`
-   `update` (nếu yêu cầu nạp lại)
-   Người dùng chuyển sang Domain khác.

Lệnh `status` chỉ kiểm tra trạng thái hiện tại và không làm thay đổi
Trading Domain.

------------------------------------------------------------------------

# Vai trò

READY không chứa:

-   Tri thức
-   Logic suy luận
-   Quy tắc vận hành

READY chỉ xác nhận trạng thái của Trading Domain.

------------------------------------------------------------------------

# Triết lý

``` text
Khởi động đúng.

↓

Nạp đúng.

↓

READY.

↓

Vận hành nhất quán.
```
