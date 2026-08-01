---
title: Nền tảng
id: trading-foundation
version: 1.0
status: Stable
author: HTLH
language: vi
created: 2026-07-27
last_updated: 2026-08-01
review_cycle: Monthly
confidence: 100%
tags:
  - trading
  - foundation
---

# Nền tảng

> Khởi tạo, định nghĩa và quản lý toàn bộ Trading Domain.

---

# Mục đích

Nền tảng là Module khởi tạo và quản lý Trading Domain.

Thư mục này tập hợp các tài liệu định nghĩa kiến trúc, nguyên tắc vận hành, điều hướng và vòng đời của toàn bộ hệ thống.

---

# Kiến trúc

```text
Nền tảng

├── Boot
├── System Instruction
├── Domain Manifest
├── AI Guide
├── Trading Navigation Pack
├── VERSION
├── CHANGELOG
├── ROADMAP
├── GLOSSARY
├── ACKNOWLEDGEMENTS
└── READY
```

---

# Vai trò

Nền tảng chịu trách nhiệm:

- Khởi tạo Trading Domain.
- Định nghĩa kiến trúc và nguyên tắc vận hành.
- Quản lý phiên bản và tài liệu.
- Chuẩn hóa tổ chức của toàn bộ Trading Domain.

---

# Luồng khởi tạo

```text
Nền tảng

↓

Boot

↓

Trading Domain

↓

READY
```

Sau khi Trading Domain được nạp hoàn chỉnh và xác nhận READY, các thành phần nghiệp vụ bắt đầu hoạt động theo quy trình chuẩn.

---

# Thành phần

## Boot

Khởi tạo quá trình nạp Trading Domain.

---

## System Instruction

Định nghĩa nguyên tắc làm việc của AI.

---

## Domain Manifest

Mô tả phạm vi và cấu trúc của Trading Domain.

---

## AI Guide

Hướng dẫn AI sử dụng Trading Domain.

---

## Trading Navigation Pack

Bản đồ điều hướng của Trading Domain.

---

## VERSION

Quản lý phiên bản hiện tại.

---

## CHANGELOG

Ghi nhận lịch sử thay đổi.

---

## ROADMAP

Định hướng phát triển của Trading Domain.

---

## GLOSSARY

Chuẩn hóa thuật ngữ.

---

## ACKNOWLEDGEMENTS

Ghi nhận các nguồn tham khảo và đóng góp.

---

## READY

Xác nhận Trading Domain đã được nạp hoàn chỉnh và sẵn sàng vận hành.

---

# Nguyên tắc

- Mỗi tài liệu đảm nhận một vai trò riêng.
- Các thành phần tuân theo cùng một kiến trúc và quy ước.
- Mọi thay đổi được quản lý theo phiên bản.

---

# Tóm tắt

```text
Nền tảng

↓

Trading Domain

↓

READY
```

Nền tảng cung cấp điểm khởi đầu và cơ sở tổ chức cho toàn bộ Trading Domain.

---

---
title: Boot
id: trading-boot
version: 1.3.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - boot
---

# Boot

> Điểm khởi động của Trading Domain.

---

# Mục đích

Boot định nghĩa quy trình khởi tạo Trading Domain.

Đây là điểm bắt đầu để AI nạp toàn bộ Trading Domain theo một trình tự thống nhất trước khi sử dụng.

---

# Luồng khởi tạo

Trading Domain được nạp theo thứ tự:

```text
Boot

↓

System Instruction

↓

Domain Manifest

↓

AI Guide

↓

Trading Navigation Pack

↓

Trading README

↓

README của các Module

↓

Các Module

↓

READY
```

Trình tự này đảm bảo toàn bộ Trading Domain được nạp đầy đủ trước khi vận hành.

---

# Quy tắc

## 01

Bắt đầu từ **Boot**.

---

## 02

Nạp Trading Domain theo đúng trình tự.

---

## 03

Chỉ sử dụng Trading Domain sau khi hoàn tất quá trình khởi tạo.

---

## 04

Trading Domain chuyển sang trạng thái **READY** sau khi toàn bộ tài liệu đã được nạp.

---

## 05

Mọi hoạt động đều tuân thủ kiến trúc và quy ước của Trading Domain.

---

## 06

Boot hỗ trợ các Boot Commands:

- `boot`
- `ready`
- `status`
- `reload`
- `update`
- `unload`

Chi tiết được định nghĩa trong **System Instruction**.

---

# Trạng thái

Sau khi hoàn tất quá trình khởi tạo:

```text
Trading Domain READY
```

Có thể kiểm tra trạng thái bất kỳ lúc nào bằng:

```text
status
```

---

# Chu kỳ làm việc

Sau khi READY:

```text
Trading Domain READY

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

Trading Domain được duy trì cho đến khi thực hiện:

- `unload`
- `reload`
- `update` (khi cần nạp lại)
- Chuyển sang Domain khác.

---

# Nguyên tắc

- Boot là điểm bắt đầu của Trading Domain.
- Trading Domain được khởi tạo theo một trình tự thống nhất.
- READY đánh dấu trạng thái sẵn sàng vận hành.
- Mọi thành phần của Trading Domain tuân theo cùng một kiến trúc và quy ước.

---

# Tóm tắt

```text
Boot

↓

Trading Domain

↓

READY
```

Boot chuẩn hóa quá trình khởi tạo Trading Domain và đưa Domain vào trạng thái READY trước khi vận hành.

---

---
title: System Instruction
id: trading-system-instruction
version: 1.3.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
---

# System Instruction

> Quy định cách AI vận hành Trading Domain.

---

# Mục đích

System Instruction định nghĩa các nguyên tắc vận hành của Trading Domain.

Tài liệu này chuẩn hóa:

- Quy tắc vận hành.
- Thứ tự ưu tiên.
- Phạm vi áp dụng.
- Boot Commands.

Đây là tài liệu có mức ưu tiên cao nhất trong Trading Domain.

---

# Thứ tự ưu tiên

Trading Domain được vận hành theo trình tự:

```text
System Instruction

↓

Domain Manifest

↓

AI Guide

↓

Trading Navigation Pack

↓

Trading README

↓

README của các Module

↓

Các Module

↓

READY
```

Trình tự này được áp dụng thống nhất trong toàn bộ Domain.

---

# Quy tắc vận hành

## 01 · Bắt đầu từ Thực tế

Quá trình suy luận luôn bắt đầu từ Thực tế.

---

## 02 · Tuân thủ kiến trúc

Trading Domain vận hành theo kiến trúc:

```text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

---

## 03 · Hoàn thành Hệ thống suy luận

AI luôn thực hiện đầy đủ Hệ thống suy luận theo đúng trình tự đã được định nghĩa.

---

## 04 · Tri thức nền

Tri thức nền chuẩn hóa toàn bộ thuật ngữ, khái niệm và quy ước được sử dụng trong Trading Domain.

---

## 05 · Tri thức tích luỹ

Tri thức tích luỹ được tham khảo sau khi Hệ thống suy luận hoàn tất nhằm hỗ trợ:

- Đánh giá.
- Hiệu chỉnh.
- Tái sử dụng kinh nghiệm.

---

## 06 · Điều kiện dữ liệu

Quá trình suy luận được thực hiện trên tập dữ liệu đầy đủ và phù hợp với ngữ cảnh.

---

## 07 · Cập nhật kinh nghiệm

```text
Thực tế

↓

Tri thức tích luỹ

↓

Bộ nhớ
```

Tri thức tích luỹ cập nhật kinh nghiệm dựa trên kết quả đã được kiểm chứng.

---

## 08 · Thứ tự ưu tiên

Khi nhiều tài liệu cùng liên quan, áp dụng đúng thứ tự ưu tiên đã được định nghĩa.

---

# Boot Commands

## boot

Khởi tạo Trading Domain theo **Boot.md**.

Quy trình:

- Nạp Domain theo đúng trình tự.
- Cập nhật tiến trình sau mỗi bước.
- Kết thúc bằng:

```text
Trading Domain READY
```

---

## ready

Kiểm tra trạng thái hiện tại của Trading Domain.

Kết quả:

```text
Trading Domain READY
```

hoặc

```text
Trading Domain NOT READY
```

---

## status

Hiển thị trạng thái hiện tại.

Ví dụ:

```text
Trading Domain : READY

Version : 1.3.0

Status : Stable

Boot : Loaded

Core Documents : Loaded

Modules : Loaded

Current Domain : Trading
```

Nếu quá trình khởi tạo chưa hoàn tất:

```text
Trading Domain : NOT READY
```

---

## reload

Khởi tạo lại toàn bộ Trading Domain.

Quy trình:

```text
UNLOAD

↓

BOOT

↓

READY
```

---

## update

Nạp lại các tài liệu đã thay đổi.

Nếu thay đổi ảnh hưởng đến:

- Kiến trúc.
- Thứ tự nạp.
- Quy tắc vận hành.

Trading Domain thực hiện quy trình `reload`.

---

## unload

Kết thúc Trading Domain trong phiên làm việc hiện tại.

Kết quả:

```text
Trading Domain UNLOADED
```

Trạng thái sau đó:

```text
Trading Domain NOT READY
```

---

# Tiến trình Boot

Trong quá trình `boot`, AI cập nhật tiến trình sau mỗi bước.

```text
Boot.md                          ✅

System Instruction.md            ⏳

Domain Manifest.md               ⏳

AI Guide.md                      ⏳

Trading Navigation Pack.md        ⏳

Trading README.md                ⏳

README Modules                   ⏳

Modules                          ⏳

READY                            ⏳
```

Quy ước:

```text
⏳  Chưa nạp

🔄  Đang nạp

✅  Hoàn thành
```

Khi toàn bộ các bước hoàn tất:

```text
Trading Domain READY
```

---

# Session Scope

Sau khi:

```text
Trading Domain READY
```

Trading Domain trở thành ngữ cảnh làm việc hiện tại cho đến khi:

- `unload`
- `reload`
- `update` (khi cần nạp lại)
- Chuyển sang Domain khác.

---

# Domain Scope

Trading Domain áp dụng cho các tác vụ thuộc lĩnh vực Trading.

Các tác vụ ngoài phạm vi Trading sử dụng cơ chế mặc định của AI.

---

# Nguyên tắc

```text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

Mọi chu kỳ vận hành đều tuân theo cùng một kiến trúc.

---

# Tóm tắt

System Instruction là tài liệu điều phối toàn bộ Trading Domain.

Tài liệu này định nghĩa:

- Quy tắc vận hành.
- Thứ tự ưu tiên.
- Phạm vi áp dụng.
- Boot Commands.

Mọi thành phần của Trading Domain đều tuân theo các nguyên tắc được định nghĩa trong tài liệu này.

---

---
title: Trading Domain Manifest
id: trading-domain-manifest
version: 1.5.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
---

# Trading Domain Manifest

> Định nghĩa kiến trúc và mối quan hệ giữa các thành phần của Trading Domain.

---

# Domain

Trading

Version

```text
1.5.0
```

Status

```text
Stable
```

---

# Mục đích

Trading Domain Manifest mô tả:

- Kiến trúc của Trading Domain.
- Các Module và vai trò của từng Module.
- Mối quan hệ giữa các Module.
- Luồng vận hành tổng thể của Domain.

Manifest là tài liệu mô tả kiến trúc trung tâm của Trading Domain.

---

# Kiến trúc Trading

```text
Trading

├── README.md
│
├── Nền tảng
├── Tri thức nền
├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức tích luỹ
└── Build
```

---

# Vai trò các thành phần

## README

Điểm giới thiệu tổng quan của Trading Domain.

---

## Nền tảng

Chuẩn hóa và quản lý Trading Domain.

Bao gồm các tài liệu điều phối và quản lý toàn bộ Trading Domain.

---

## Tri thức nền

Chuẩn hóa:

- Thuật ngữ.
- Khái niệm.
- Quy ước.
- Kiến thức nền tảng.

---

## Nguồn dữ liệu

Chuẩn hóa dữ liệu đầu vào từ Thực tế.

---

## Hệ thống suy luận

Chuyển dữ liệu thành quyết định.

Bao gồm:

```text
01-Hành vi

02-Bối cảnh

03-Động lượng

04-Cấu trúc

05-Chất lượng

06-Quyết định

07-Trọng số tín hiệu

08-Không gian kịch bản

09-Kế hoạch thực thi

10-Phản hồi thực tế
```

---

## Tri thức tích luỹ

```text
README.md

├── Bộ nhớ
│
│   ├── README.md
│   ├── Quy ước Trường hợp
│   ├── Quy ước Mẫu
│   ├── Quy ước Bài học tích luỹ
│   └── Quy ước Thống kê
│
└── Cơ chế
    │
    ├── README.md
    ├── Tra cứu
    ├── Đối chiếu
    ├── Tổng hợp
    └── Cập nhật
```

Tri thức tích luỹ gồm:

- Bộ nhớ: chuẩn hóa và lưu giữ tri thức đã được kiểm chứng.
- Cơ chế: chuẩn hóa cách tra cứu, đối chiếu, tổng hợp và cập nhật Bộ nhớ.

---

## Build

Quản lý quá trình thiết kế, xây dựng và phát triển Trading Domain.

---

# Trách nhiệm tài liệu

| Tài liệu | Vai trò |
|----------|----------|
| Boot | Khởi tạo Trading Domain |
| System Instruction | Chuẩn hóa quy tắc vận hành |
| Domain Manifest | Chuẩn hóa kiến trúc Domain |
| AI Guide | Hướng dẫn AI sử dụng Domain |
| Trading Navigation Pack | Bản đồ điều hướng |
| README | Tổng quan Trading Domain |
| README của Module | Tổng quan từng Module |
| Module | Nội dung chuyên môn |

---

# Vai trò của các Module

| Module | Vai trò |
|---------|----------|
| Nền tảng | Chuẩn hóa Trading Domain |
| Tri thức nền | Chuẩn hóa ngôn ngữ và quy ước |
| Nguồn dữ liệu | Chuẩn hóa dữ liệu đầu vào |
| Hệ thống suy luận | Chuẩn hóa quá trình suy luận |
| Tri thức tích luỹ | Chuẩn hóa kinh nghiệm và cơ chế khai thác |
| Build | Quản lý quá trình xây dựng Domain |

---

# Tóm tắt

Kiến trúc:

```text
Trading

├── Nền tảng
├── Tri thức nền
├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức tích luỹ
└── Build
```

Luồng vận hành:

```text
Tri thức nền

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

Trading Domain được tổ chức thành các Module chuyên trách.

Mỗi Module đảm nhiệm một vai trò riêng và cùng tham gia vào một kiến trúc thống nhất.

---

# Triết lý

Nền tảng định nghĩa Domain.

Tri thức nền chuẩn hóa cách hiểu.

Nguồn dữ liệu chuẩn hóa đầu vào.

Hệ thống suy luận chuyển dữ liệu thành quyết định.

Tri thức tích luỹ kế thừa kinh nghiệm đã được kiểm chứng.

Build quản lý quá trình phát triển Domain.

---

---
title: AI Guide
id: trading-ai-guide
version: 1.5.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
---

# AI Guide

> Hướng dẫn AI sử dụng Trading Domain.

---

# Mục đích

AI Guide hướng dẫn cách AI vận hành Trading Domain sau khi Domain ở trạng thái:

```text
Trading Domain READY
```

AI phối hợp các Module theo đúng kiến trúc của Trading Domain để xử lý dữ liệu, xây dựng suy luận và hỗ trợ quyết định.

---

# Quy trình làm việc

```text
Trading Domain READY

↓

Nguồn dữ liệu

↓

Chuẩn hóa dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

---

# 01 · Nguồn dữ liệu

Sau khi Trading Domain ở trạng thái READY, AI tiếp nhận dữ liệu đầu vào.

Nguồn dữ liệu có thể gồm:

- ATS
- Dữ liệu rời rạc
- Hoặc kết hợp nhiều nguồn

---

# 02 · Chuẩn hóa dữ liệu

AI diễn giải dữ liệu theo:

- Tri thức nền
- Quy ước của Trading Domain

Mọi thành phần sử dụng cùng hệ thuật ngữ và quy ước thống nhất.

---

# 03 · Hệ thống suy luận

AI thực hiện đầy đủ chu trình suy luận:

```text
01-Hành vi

↓

02-Bối cảnh

↓

03-Động lượng

↓

04-Cấu trúc

↓

05-Chất lượng

↓

06-Quyết định

↓

07-Trọng số tín hiệu

↓

08-Không gian kịch bản

↓

09-Kế hoạch thực thi

↓

10-Phản hồi thực tế
```

---

# 04 · Tri thức tích luỹ

```text
07-Trọng số tín hiệu
        │
        ├── tạo
        ▼
  Chữ ký tín hiệu

08-Không gian kịch bản
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

09-Kế hoạch thực thi
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Tham khảo Tri thức tích luỹ

10-Phản hồi thực tế
        │
        └── sử dụng Chữ ký tín hiệu
              │
              └── Cập nhật Tri thức tích luỹ
```

AI sử dụng Chữ ký tín hiệu để tham khảo và cập nhật Tri thức tích luỹ theo đúng quy ước của Trading Domain.

---

# 05 · Hệ thống suy luận tiếp theo

Sau khi tầng 10-Phản hồi thực tế hoàn tất, Tri thức tích luỹ cập nhật Bộ nhớ để hỗ trợ các Hệ thống suy luận tiếp theo.

---

# Vai trò của AI

- Tiếp nhận và chuẩn hóa Nguồn dữ liệu.
- Thực hiện đầy đủ Luồng suy luận.
- Tham khảo Tri thức tích luỹ qua Chữ ký tín hiệu.
- Cập nhật Tri thức tích luỹ sau khi Thực tế kiểm chứng.

---

# Điều kiện sử dụng

Trading Domain hoạt động khi ở trạng thái:

```text
Trading Domain READY
```

Sau khi READY:

- AI tiếp nhận Nguồn dữ liệu.
- AI tự động thực hiện toàn bộ chu trình của Trading Domain.
- AI trả về kết quả theo đúng cấu trúc của Domain.

---

# Tóm tắt

```text
Trading Domain READY

↓

Nguồn dữ liệu

↓

Chuẩn hóa dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

AI Guide mô tả cách AI phối hợp các Module của Trading Domain trong một chu kỳ vận hành hoàn chỉnh.

---

# Triết lý

Trading Domain cung cấp kiến trúc.

AI vận hành theo kiến trúc.

Tri thức tích luỹ đồng hành cùng từng chu kỳ suy luận để nâng cao chất lượng quyết định.

---

---
title: Trading Navigation Pack
id: trading-navigation-pack
version: 2.0.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - navigation
  - domain
---

# Trading Navigation Pack

> Bản đồ điều hướng của Trading Domain.

---

# Mục đích

Trading Navigation Pack là bản đồ điều hướng của Trading Domain.

Tài liệu này giúp AI:

- Định vị cấu trúc Domain.
- Xác định vai trò của từng Module.
- Điều hướng đến đúng tài liệu chuyên môn.

Navigation Pack không chứa tri thức chuyên môn.

---

# Kiến trúc

```text
Trading

├── 01 · Nền tảng
│
├── 02 · Tri thức nền
│
├── 03 · Nguồn dữ liệu
│
├── 04 · Hệ thống suy luận
│
├── 05 · Tri thức tích luỹ
│
└── 06 · Build
```

---

# Thành phần

## 01 · Nền tảng

Khởi tạo và quản lý Trading Domain.

---

## 02 · Tri thức nền

Chuẩn hóa thuật ngữ, khái niệm và quy ước.

---

## 03 · Nguồn dữ liệu

Tiếp nhận và chuẩn hóa dữ liệu đầu vào.

---

## 04 · Hệ thống suy luận

Chuyển dữ liệu thành quyết định.

---

## 05 · Tri thức tích luỹ

Quản lý kinh nghiệm đã được Thực tế kiểm chứng.

---

## 06 · Build

Đóng gói và quản lý tài liệu xây dựng Domain.

---

# Luồng kiến trúc

```text
Tri thức nền

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ

↓

Hệ thống suy luận tiếp theo
```

---

# Điều hướng

Trading Navigation Pack giúp AI xác định nhanh vị trí của từng Module trong Trading Domain.

Chi tiết của mỗi Module được định nghĩa trong README và các tài liệu tương ứng.

---

# Vai trò

Trading Navigation Pack giúp:

- Định vị Module.
- Điều hướng tài liệu.
- Kết nối kiến trúc của Trading Domain.

Navigation Pack không thay thế Tri thức nền và không chứa tri thức chuyên môn.

---

# Tóm tắt

```text
Trading Navigation Pack

↓

Điều hướng

↓

Trading Domain
```

Trading Navigation Pack là bản đồ điều hướng giúp AI xác định đúng Module và tài liệu trong Trading Domain.

---

---
title: VERSION
id: trading-version
version: 1.4.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - version
---

# VERSION

> Quản lý phiên bản của Trading Domain.

---

# Mục đích

VERSION xác định phiên bản và trạng thái phát hành hiện tại của Trading Domain.

Tài liệu này giúp:

- Xác định phiên bản hiện hành.
- Kiểm tra trạng thái phát hành.
- Đồng bộ toàn bộ Trading Domain.

---

# Trading Domain

## Phiên bản

```text
1.4.0
```

## Trạng thái

```text
Stable
```

## Ngày phát hành

```text
2026-07-27
```

---

# Phạm vi đồng bộ

## Tài liệu nền tảng

```text
Boot
System Instruction
Domain Manifest
AI Guide
Trading Navigation Pack
Trading README
VERSION
CHANGELOG
ROADMAP
GLOSSARY
ACKNOWLEDGEMENTS
READY
```

## Module

```text
README của các Module

↓

Các Module
```

---

# Semantic Versioning

Trading Domain sử dụng chuẩn:

```text
MAJOR.MINOR.PATCH
```

## Thay đổi lớn (MAJOR)

Thay đổi kiến trúc Trading Domain.

```text
1.x.x

↓

2.0.0
```

---

## Mở rộng (MINOR)

Mở rộng Trading Domain.

```text
1.3.0

↓

1.4.0
```

---

## Cập nhật nhỏ (PATCH)

Cập nhật nội dung hoặc tối ưu tài liệu.

```text
1.4.0

↓

1.4.1
```

---

# Quy trình cập nhật

```text
VERSION

↓

CHANGELOG

↓

ROADMAP (nếu cần)

↓

Tài liệu nền tảng

↓

Modules
```

Toàn bộ Trading Domain được xem là đồng bộ khi các tài liệu nền tảng và Module tương thích với phiên bản hiện hành.

---

# Vai trò

VERSION giúp:

- Quản lý phiên bản.
- Đồng bộ Trading Domain.
- Theo dõi trạng thái phát hành.

---

# Tóm tắt

```text
VERSION

↓

Trading Domain
```

VERSION là mốc tham chiếu chung về phiên bản và trạng thái phát hành của toàn bộ Trading Domain.

---

---
title: CHANGELOG
id: trading-changelog
version: 1.4.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - changelog
---

# CHANGELOG

> Ghi nhận lịch sử phát triển của Trading Domain.

---

# Mục đích

CHANGELOG ghi nhận các thay đổi giữa các phiên bản nhằm:

- Theo dõi quá trình phát triển.
- Xác định phạm vi thay đổi.
- Đồng bộ Trading Domain.

---

# Quy ước phiên bản

Trading Domain sử dụng chuẩn:

```text
MAJOR.MINOR.PATCH
```

| Thành phần | Ý nghĩa |
|------------|----------|
| **Thay đổi lớn (MAJOR)** | Thay đổi kiến trúc Trading Domain |
| **Mở rộng (MINOR)** | Mở rộng Module hoặc chức năng |
| **Cập nhật nhỏ (PATCH)** | Cập nhật nội dung hoặc tối ưu tài liệu |

---

# Quy ước thay đổi

| Loại | Ý nghĩa |
|------|----------|
| **Added** | Thêm mới |
| **Changed** | Điều chỉnh |
| **Fixed** | Sửa lỗi |
| **Docs** | Cập nhật tài liệu |

---

# Lịch sử phiên bản

## v1.4.0 • 2026-08-01

### Added

- Hoàn thiện kiến trúc **Nền tảng**, **Tri thức nền**, **Nguồn dữ liệu**, **Hệ thống suy luận**, **Tri thức tích luỹ** và **Build**.
- Bổ sung cấu trúc **Bộ nhớ** và **Cơ chế** trong Tri thức tích luỹ.
- Chuẩn hóa README cho toàn bộ Module.

### Changed

- Đồng bộ Trading Domain lên phiên bản **1.4.0**.
- Chuẩn hóa kiến trúc Domain.
- Chuẩn hóa luồng giữa Hệ thống suy luận và Tri thức tích luỹ.
- Tinh gọn toàn bộ Core Documents.
- Đồng bộ thuật ngữ và quy ước.

### Docs

- Cập nhật toàn bộ tài liệu nền tảng.
- Chuẩn hóa README các Module.
- Chuẩn hóa toàn bộ tài liệu Quy ước.

---

## v1.3.0 • 2026-07-22

### Added

- ROADMAP.
- Semantic Versioning.
- Compatibility.
- Boot Commands.
- Session Scope.
- Domain Scope.

### Changed

- Chuẩn hóa Core Documents.
- Chuẩn hóa quy trình Boot.
- Chuẩn hóa Trading Navigation Pack.
- Chuẩn hóa chu kỳ suy luận.

---

## v1.2.0 • 2026-07-22

### Added

- Boot.
- READY.
- Domain Manifest.
- AI Guide.
- Trading Navigation Pack.
- VERSION.
- CHANGELOG.
- GLOSSARY.
- ACKNOWLEDGEMENTS.

### Changed

- Chuẩn hóa Trading README.
- Hoàn thiện ranh giới giữa Hệ thống suy luận và Tri thức tích luỹ.

---

## v1.1.0 • 2026-07-22

### Added

- Không gian kịch bản.
- Kế hoạch thực thi.
- Phản hồi thực tế.

---

## v1.0.0 • 2026-07-19

### Added

Khởi tạo Trading Domain.

---

# Tóm tắt

```text
ROADMAP

↓

CHANGELOG

↓

VERSION
```

CHANGELOG ghi nhận lịch sử thay đổi của Trading Domain và là cơ sở đối chiếu giữa các phiên bản.

---

---
title: ROADMAP
id: trading-roadmap
version: 1.4.0
status: Planning
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - roadmap
  - planning
---

# ROADMAP

> Định hướng phát triển của Trading Domain.

---

# Mục đích

ROADMAP mô tả định hướng phát triển của Trading Domain.

Bao gồm:

- Mục tiêu.
- Kế hoạch.
- Các giai đoạn phát triển.

ROADMAP phản ánh định hướng tương lai, trong khi CHANGELOG ghi nhận những thay đổi đã hoàn thành.

---

# Chu kỳ phát triển

```text
📋 Kế hoạch

↓

🚧 Đang thực hiện

↓

✅ Hoàn thành

↓

CHANGELOG

↓

VERSION
```

Sau khi hoàn thành, các tài liệu liên quan được cập nhật và đồng bộ theo phiên bản mới.

---

# Lộ trình

## Giai đoạn 1 · Nền tảng

**Trạng thái**

```text
✅ Hoàn thành
```

### Mục tiêu

- Hoàn thiện hệ thống tài liệu nền tảng.
- Chuẩn hóa quy trình khởi tạo Trading Domain.
- Chuẩn hóa nguyên tắc vận hành.

---

## Giai đoạn 2 · Tri thức nền

**Trạng thái**

```text
🚧 Đang thực hiện
```

### Mục tiêu

- Hoàn thiện Quy ước.
- Hoàn thiện Luồng suy luận.
- Chuẩn hóa Trading Domain.

---

## Giai đoạn 3 · Nguồn dữ liệu

**Trạng thái**

```text
🚧 Đang thực hiện
```

### Mục tiêu

- Chuẩn hóa ATS.
- Chuẩn hóa Dữ liệu rời rạc.
- Chuẩn hóa quy trình tiếp nhận dữ liệu.

---

## Giai đoạn 4 · Hệ thống suy luận

**Trạng thái**

```text
📋 Kế hoạch
```

### Mục tiêu

- Hoàn thiện Pipeline suy luận.
- Chuẩn hóa Không gian kịch bản.
- Chuẩn hóa Kế hoạch thực thi.
- Chuẩn hóa Phản hồi thực tế.

---

## Giai đoạn 5 · Tri thức tích luỹ

**Trạng thái**

```text
🚧 Đang thực hiện
```

### Mục tiêu

- Hoàn thiện Bộ nhớ.
- Hoàn thiện Cơ chế.
- Chuẩn hóa vòng đời tri thức.
- Hoàn thiện cơ chế học hỏi.

---

## Giai đoạn 6 · Build

**Trạng thái**

```text
🚧 Đang thực hiện
```

### Mục tiêu

- Hoàn thiện Build.
- Hoàn thiện các tài liệu tổng hợp.
- Chuẩn hóa tài liệu phục vụ triển khai và bảo trì.

---

## Giai đoạn 7 · AI & ccOS

**Trạng thái**

```text
📋 Kế hoạch
```

### Mục tiêu

- Tích hợp AI.
- Chuẩn hóa đa Domain.
- Tích hợp Trading Domain vào ccOS.

---

## Giai đoạn 8 · Trading Domain tự chủ

**Trạng thái**

```text
🔮 Tầm nhìn
```

### Mục tiêu

- Tri thức thích ứng.
- Bộ nhớ tiến hóa.
- Suy luận đa thị trường.
- Tri thức liên Domain.

---

# Lộ trình tổng thể

```text
01 · Nền tảng

↓

02 · Tri thức nền

↓

03 · Nguồn dữ liệu

↓

04 · Hệ thống suy luận

↓

05 · Tri thức tích luỹ

↓

06 · Build

↓

07 · AI & ccOS

↓

08 · Trading Domain tự chủ
```

---

# Vai trò

ROADMAP giúp:

- Xác định định hướng phát triển.
- Theo dõi tiến độ.
- Điều phối các giai đoạn.
- Đồng bộ kế hoạch phát triển của Trading Domain.

---

# Tóm tắt

```text
ROADMAP

↓

Kế hoạch

↓

CHANGELOG

↓

VERSION
```

ROADMAP là bản đồ phát triển của Trading Domain và định hướng các giai đoạn phát triển trong tương lai.

---

---
title: GLOSSARY
id: trading-glossary
version: 1.4.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - glossary
---

# GLOSSARY

> Chuẩn hóa thuật ngữ của Trading Domain.

---

# Mục đích

GLOSSARY là từ điển thuật ngữ thống nhất của Trading Domain.

Mỗi thuật ngữ chỉ có một định nghĩa và được sử dụng nhất quán trong toàn Domain.

---

# Thuật ngữ

## Trading Domain

Hệ thống tri thức và quy trình dành cho Trading.

---

## Domain

Hệ thống gồm kiến trúc, quy tắc và tri thức cho một lĩnh vực.

---

## Nền tảng

Khởi tạo và quản lý Trading Domain.

---

## Tri thức nền

Chuẩn hóa thuật ngữ, khái niệm và quy ước.

---

## Nguồn dữ liệu

Tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

---

## ATS

Mẫu chuẩn ghi nhận dữ liệu quan sát.

---

## Dữ liệu rời rạc

Dữ liệu bổ sung ngoài ATS.

---

## Hệ thống suy luận

Chuỗi xử lý chuyển dữ liệu thành Quyết định.

---

## Tri thức tích luỹ

Quản lý kinh nghiệm đã được Thực tế kiểm chứng.

---

## Bộ nhớ

Lưu giữ:

- Trường hợp
- Mẫu
- Bài học tích luỹ
- Thống kê

---

## Cơ chế

Khai thác và cập nhật Bộ nhớ.

---

## Chữ ký tín hiệu

Biểu diễn chuẩn của trạng thái suy luận.

---

## Trường hợp

Một lần vận hành hoàn chỉnh đã được Thực tế kiểm chứng.

---

## Mẫu

Tập hợp nhiều Trường hợp có đặc điểm tương đồng.

---

## Bài học tích luỹ

Kinh nghiệm tổng hợp từ nhiều Mẫu và Trường hợp.

---

## Thống kê

Kết quả định lượng được tổng hợp từ dữ liệu đã kiểm chứng.

---

## Module

Đơn vị tài liệu chuyên biệt của Trading Domain.

---

## Boot

Điểm khởi động Trading Domain.

---

## READY

Trạng thái Trading Domain sẵn sàng vận hành.

---

## Boot Commands

Các lệnh điều khiển Domain:

- boot
- ready
- status
- reload
- update
- unload

---

## Trading Navigation Pack

Bản đồ điều hướng của Trading Domain.

---

## Domain Manifest

Định nghĩa kiến trúc Trading Domain.

---

## AI Guide

Hướng dẫn AI sử dụng Trading Domain.

---

## System Instruction

Quy định cách AI vận hành Trading Domain.

---

## Tài liệu nền tảng

Nhóm tài liệu quản lý Trading Domain:

- Boot
- System Instruction
- Domain Manifest
- AI Guide
- Trading Navigation Pack
- README
- VERSION
- CHANGELOG
- ROADMAP
- GLOSSARY
- ACKNOWLEDGEMENTS
- READY

---

# Nguyên tắc

- Mỗi thuật ngữ chỉ có một định nghĩa.
- Thuật ngữ mới được bổ sung vào GLOSSARY trước khi sử dụng.
- Toàn bộ Trading Domain sử dụng thống nhất các thuật ngữ tại đây.

---

# Tóm tắt

```text
GLOSSARY

↓

Thuật ngữ

↓

Ngôn ngữ thống nhất

↓

Trading Domain
```

GLOSSARY chuẩn hóa thuật ngữ và tạo nền tảng ngôn ngữ chung cho toàn bộ Trading Domain.

---

---
title: ACKNOWLEDGEMENTS
id: trading-acknowledgements
version: 1.5.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - acknowledgements
---

# ACKNOWLEDGEMENTS

> Ghi nhận quá trình hình thành và phát triển của Trading Domain.

---

# Mục đích

ACKNOWLEDGEMENTS ghi nhận:

- Người xây dựng.
- Đóng góp trong quá trình phát triển.
- Nguyên tắc thiết kế.
- Định hướng phát triển.

---

# Người xây dựng

## HTLH

Thiết kế và phát triển:

- Trading Domain.
- Kiến trúc Trading.
- Tri thức nền.
- Nguồn dữ liệu.
- Hệ thống suy luận.
- Tri thức tích luỹ.

---

# AI đồng hành

## ChatGPT (OpenAI)

Hỗ trợ:

- Chuẩn hóa tài liệu.
- Rà soát tính nhất quán.
- Hoàn thiện cấu trúc Domain.
- Đề xuất cải tiến kiến trúc.

---

# Nguyên tắc thiết kế

Trading Domain được xây dựng theo kiến trúc:

```text
Tri thức nền

↓

Nguồn dữ liệu

↓

Hệ thống suy luận

↓

Tri thức tích luỹ
```

Tri thức được hình thành từ dữ liệu đã được Thực tế kiểm chứng và được tích luỹ để hỗ trợ các chu kỳ suy luận tiếp theo.

---

# Định hướng phát triển

Trading Domain hướng tới:

- Chuẩn hóa.
- Nhất quán.
- Kiểm chứng được.
- Mở rộng được.
- Phát triển bền vững.

---

# Ghi nhận

Trading Domain được hình thành từ quá trình:

- Quan sát.
- Thực hành.
- Kiểm chứng.
- Chuẩn hóa.

Những kinh nghiệm đã được kiểm chứng trở thành nền tảng để Trading Domain tiếp tục phát triển.

---

# Tóm tắt

```text
Quan sát

↓

Thực hành

↓

Kiểm chứng

↓

Chuẩn hóa

↓

Trading Domain
```

ACKNOWLEDGEMENTS ghi nhận quá trình hình thành và những đóng góp giúp Trading Domain phát triển theo một kiến trúc thống nhất.

---

---
title: READY
id: trading-ready
version: 1.4.0
status: Stable
author: HTLH
language: vi
created: 2026-07-22
last_updated: 2026-08-01
review_cycle: Manual
confidence: 100%
tags:
  - trading
  - ready
---

# READY

> Xác nhận Trading Domain đã sẵn sàng vận hành.

---

# Mục đích

READY đánh dấu Trading Domain đã được nạp hoàn chỉnh và trở thành ngữ cảnh làm việc hiện tại.

Sau khi READY, AI có thể sử dụng toàn bộ Trading Domain cho các tác vụ thuộc lĩnh vực Trading.

---

# Điều kiện

Trading Domain đạt trạng thái READY sau khi hoàn tất:

```text
Boot

↓

System Instruction

↓

Domain Manifest

↓

AI Guide

↓

Trading Navigation Pack

↓

Trading README

↓

README các Module

↓

Các Module

↓

READY
```

---

# Trạng thái

```text
Trading Domain READY
```

hoặc

```text
Trading Domain NOT READY
```

---

# Sau khi READY

Trading Domain được duy trì cho đến khi:

- unload
- reload
- update (khi cần nạp lại)
- Chuyển sang Domain khác

Có thể kiểm tra bằng:

```text
status
```

---

# Vai trò

READY xác nhận:

- Core Documents đã được nạp.
- Các Module đã sẵn sàng.
- Trading Domain có thể được sử dụng.

READY không chứa tri thức hay quy tắc vận hành.

---

# Tóm tắt

```text
Boot

↓

Trading Domain READY

↓

Sẵn sàng vận hành
```

READY là điểm kết thúc của quá trình khởi tạo và là điểm bắt đầu sử dụng Trading Domain.