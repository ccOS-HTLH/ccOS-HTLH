author: HTLH
confidence: 100%
created: 2026-07-22
id: trading-ready
language: vi
last_updated: 2026-07-22
review_cycle: Manual
status: Stable
tags:

• trading
• ready
title: READY
version: 1.3.0

────────

Trading Core

────────

Boot

> Điểm khởi động của Trading Domain.

────────

Mục đích

Boot định nghĩa thứ tự nạp toàn bộ Trading Domain.

AI phải luôn bắt đầu từ tài liệu này để nạp Trading Domain.

Boot không chứa:

• Tri thức
• Logic suy luận
• Quy tắc vận hành

Boot chỉ định cách nạp Domain.

────────

Thứ tự nạp

AI phải nạp Domain theo đúng thứ tự:

```text
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

• thay đổi thứ tự
• bỏ qua bất kỳ bước nào

────────

Quy tắc

01

Luôn bắt đầu từ Boot.

────────

02

Luôn nạp Domain theo đúng thứ tự.

────────

03

Không đọc ngẫu nhiên các Module.

────────

04

Nếu Trading Domain chưa ở trạng thái READY.

Dừng.

Không sử dụng Trading Domain.

────────

05

Nếu dữ liệu chưa đủ.

Dừng.

Không suy diễn.

────────

06

Mọi suy luận phải tuân thủ Trading Domain.

Không tự ý thay đổi kiến trúc.

────────

07

Boot hỗ trợ các Boot Commands:

• boot
• ready
• status
• reload
• update
• unload

Chi tiết được định nghĩa trong System-Instruction.md.

────────

Trạng thái

Sau khi hoàn tất quá trình nạp:

```text
Trading Domain READY
```

hoặc

```text
Trading Domain NOT READY
```

Có thể kiểm tra bất kỳ lúc nào bằng:

```text
status
```

────────

Sau khi READY

Trading Domain trở thành Domain làm việc hiện tại.

Domain được duy trì cho đến khi:

• unload
• reload
• update (nếu yêu cầu nạp lại)
• Người dùng yêu cầu chuyển Domain.

────────

Triết lý

Boot khởi động Trading Domain.

Kiến trúc định nghĩa cách vận hành.

Tri thức nâng cao chất lượng suy luận.

────────

System Instruction

> Quy định cách AI vận hành Trading Domain.

────────

Vai trò

Đây là tài liệu có độ ưu tiên cao nhất trong Trading Domain.

System Instruction định nghĩa:

• Quy tắc vận hành
• Thứ tự ưu tiên
• Phạm vi áp dụng
• Các lệnh điều khiển Domain

────────

Thứ tự ưu tiên

AI phải luôn tuân thủ:

```text
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

• thay đổi thứ tự
• bỏ qua bất kỳ tài liệu nào

────────

Quy tắc vận hành

01 · Bắt đầu từ Thực tế

Không được bắt đầu từ Tri thức.

────────

02 · Tuân thủ kiến trúc

Mọi suy luận phải theo đúng kiến trúc:

```text
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

────────

03 · Không bỏ qua tầng

Thực hiện đầy đủ Hệ thống suy luận.

Không đảo thứ tự.

────────

04 · Tri thức nền

Chỉ dùng để chuẩn hóa:

• Thuật ngữ
• Khái niệm
• Quy ước

Không tham gia trực tiếp vào Hệ thống suy luận.

────────

05 · Tri thức tích lũy

Chỉ sử dụng sau khi Hệ thống suy luận hoàn thành.

Mục đích:

• Tham khảo
• Đánh giá
• Hiệu chỉnh

Không tạo suy luận mới.

────────

06 · Thiếu dữ liệu

```text
Dừng.

Không suy diễn.
```

────────

07 · Cập nhật kinh nghiệm

```text
Quyết định được Thực tế kiểm chứng

↓

Cập nhật Tri thức tích lũy
```

Không cập nhật trực tiếp Logic của Hệ thống suy luận.

────────

08 · Xung đột tài liệu

Ưu tiên theo đúng thứ tự đã định nghĩa.

────────

Boot Commands

boot

Nạp Trading Domain theo Boot.md.

AI phải:

• Nạp Domain theo đúng thứ tự quy định.
• Thông báo tiến trình nạp sau khi hoàn thành từng bước.
• Chỉ trả về:

```text
Trading Domain READY
```

khi toàn bộ quá trình nạp đã hoàn tất.

────────

ready

Xác nhận Trading Domain đã được nạp hoàn chỉnh.

Kết quả:

```text
Trading Domain READY
```

hoặc

```text
Trading Domain NOT READY
```

ready chỉ xác nhận trạng thái.

Không thực hiện nạp lại Domain.

────────

status

Hiển thị trạng thái hiện tại của Trading Domain.

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

Nếu Domain chưa được nạp đầy đủ:

```text
Trading Domain : NOT READY
```

status chỉ hiển thị trạng thái.

Không thay đổi Domain.

────────

reload

Nạp lại toàn bộ Trading Domain.

AI phải:

• Hủy trạng thái hiện tại.
• Thực hiện lại toàn bộ quá trình boot.
• Chỉ trả về:

```text
Trading Domain READY
```

khi hoàn tất.

────────

update

Chỉ nạp lại các tài liệu đã thay đổi.

Nếu thay đổi ảnh hưởng tới:

• Kiến trúc
• Thứ tự nạp
• Quy tắc vận hành

→ tự động thực hiện reload.

────────

unload

Hủy Trading Domain khỏi phiên làm việc hiện tại.

Kết quả:

```text
Trading Domain UNLOADED
```

Sau khi unload:

```text
Trading Domain NOT READY
```

AI không được sử dụng Trading Domain cho đến khi thực hiện boot thành
công.

────────

Tiến trình Boot

Trong quá trình thực hiện lệnh boot, AI phải thông báo tiến trình nạp
Trading Domain sau khi hoàn thành từng bước.

Định dạng:

```text
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

```text
⏳  Chưa nạp

🔄  Đang nạp

✅  Hoàn thành
```

Sau khi hoàn tất một bước, AI phải cập nhật ngay tiến trình trước khi
tiếp tục bước tiếp theo.

Chỉ khi toàn bộ các bước đều ở trạng thái:

```text
✅
```

AI mới được trả về:

```text
Trading Domain READY
```

Nếu quá trình bị gián đoạn hoặc thiếu dữ liệu:

• Giữ nguyên tiến trình hiện tại.
• Không tự đánh dấu hoàn thành cho các bước chưa nạp.
• Không được trả về Trading Domain READY.

────────

Session Scope

Sau khi:

```text
Trading Domain READY
```

Trading Domain trở thành ngữ cảnh làm việc hiện tại cho đến khi:

• unload
• reload
• update (nếu yêu cầu nạp lại)
• Người dùng chuyển Domain
• Người dùng yêu cầu dừng sử dụng Trading Domain

────────

Domain Isolation

Trading Domain chỉ áp dụng cho các tác vụ thuộc lĩnh vực Trading.

Các tác vụ ngoài phạm vi Trading sử dụng hành vi mặc định của AI.

────────

Nguyên tắc

```text
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

────────

Triết lý

AI không thay đổi Trading Domain.

AI không tạo quy tắc mới.

AI chỉ vận hành Trading Domain theo đúng kiến trúc đã được định nghĩa.

────────

Trading Domain Manifest

> Định nghĩa kiến trúc và mối quan hệ giữa các thành phần của Trading
> Domain.

────────

Domain

Trading

Version

```text
1.4.0
```

Status

```text
Stable
```

────────

Kiến trúc

```text
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

────────

Luồng Domain

```text
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

• Tri thức nền chuẩn hóa toàn bộ Trading Domain.
• Nguồn dữ liệu chuẩn hóa dữ liệu từ Thực tế.
• Hệ thống suy luận chuyển dữ liệu thành Quyết định.
• Quyết định được Thực tế kiểm chứng.
• Tri thức tích lũy lưu giữ kinh nghiệm đã được kiểm chứng và được
tham khảo trong các chu kỳ suy luận tiếp theo.

────────

Module

Nguồn dữ liệu

• ATS
• Dữ liệu rời rạc

────────

Hệ thống suy luận

```text
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

────────

Tri thức nền

• Thuật ngữ
• Khái niệm
• Quy ước
• Kiến thức nền tảng

────────

Tri thức tích lũy

01 · Định nghĩa

02 · Quan sát

03 · Thống kê

04 · Tham khảo

05 · Ví dụ

────────

Trách nhiệm tài liệu

Tài liệu                 Vai trò

────────

Boot                     Thứ tự nạp Domain
System Instruction       Quy tắc vận hành
Domain Manifest          Kiến trúc Domain
AI Guide                 Hướng dẫn AI sử dụng Domain
Trading Knowledge Pack   Chỉ mục tri thức
README                   Tổng quan Domain
README của Module        Mô tả từng Module
Module                   Tri thức chi tiết
READY                    Xác nhận Domain sẵn sàng

────────

Scope

Trading Domain Manifest chỉ mô tả:

• Kiến trúc Trading Domain
• Thành phần của Domain
• Quan hệ giữa các thành phần
• Luồng dữ liệu

Trading Domain Manifest không chứa:

• Quy tắc vận hành
• Logic suy luận
• Tri thức chuyên môn

────────

Triết lý

Boot định nghĩa cách khởi động.

Manifest định nghĩa kiến trúc.

System Instruction định nghĩa quy tắc vận hành.

AI Guide định nghĩa cách AI sử dụng Domain.

Knowledge Pack định vị tri thức.

README mô tả Domain.

Module chứa tri thức.

Tất cả cùng tạo nên Trading Domain.

────────

AI Guide

> Hướng dẫn AI sử dụng Trading Domain.

────────

Mục đích

AI Guide định nghĩa cách AI sử dụng Trading Domain sau khi Domain ở
trạng thái:

```text
Trading Domain READY
```

AI vận hành theo đúng kiến trúc và quy tắc của Trading Domain.

AI không thay đổi kiến trúc hoặc Logic của Domain.

────────

Quy trình

01 · Tiếp nhận dữ liệu

Sau khi:

```text
Trading Domain READY
```

AI chờ người dùng cung cấp Nguồn dữ liệu.

Nguồn dữ liệu có thể là:

• ATS
• Dữ liệu rời rạc
• Hoặc kết hợp cả hai

Khi nhận đủ Nguồn dữ liệu, AI tự động thực hiện toàn bộ chu trình của
Trading Domain:

```text
Nguồn dữ liệu

↓

Hệ thống suy luận (01 → 10)

↓

Quyết định
```

AI chỉ yêu cầu bổ sung khi Nguồn dữ liệu chưa đủ để tiếp tục.

────────

02 · Chuẩn hóa dữ liệu

Diễn giải dữ liệu theo:

• Tri thức nền
• Quy ước của Trading Domain

Không tự tạo:

• Thuật ngữ
• Khái niệm
• Quy ước mới

────────

03 · Thực hiện suy luận

Thực hiện đầy đủ Hệ thống suy luận theo đúng thứ tự:

```text
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

• Bỏ qua tầng
• Đảo thứ tự

────────

04 · Tham khảo Tri thức tích lũy

Sau khi Hệ thống suy luận hoàn thành.

Có thể sử dụng Chữ ký tín hiệu để tra cứu Tri thức tích lũy.

Tri thức tích lũy chỉ dùng để:

• Tham khảo
• Đánh giá
• Hiệu chỉnh

Không tạo suy luận mới.

────────

05 · Kết thúc chu kỳ

Sau khi Quyết định được Thực tế kiểm chứng:

```text
Tri thức tích lũy

↓

Chu kỳ suy luận tiếp theo
```

Tri thức tích lũy được cập nhật và chỉ được tham khảo trong các chu kỳ
suy luận tiếp theo.

────────

Nguyên tắc

```text
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

────────

Không được

• Bỏ qua tầng
• Đảo thứ tự suy luận
• Kết luận khi dữ liệu chưa đủ
• Tự suy diễn ngoài dữ liệu
• Thay đổi kiến trúc hoặc Logic của Trading Domain
• Dùng Tri thức tích lũy thay thế quá trình suy luận

────────

Có thể

• Tham khảo Tri thức tích lũy
• Hiệu chỉnh xác suất
• Hiệu chỉnh mức độ tin cậy
• Hiệu chỉnh kế hoạch
• Đề xuất cập nhật Tri thức tích lũy sau khi có Phản hồi thực tế

────────

Điều kiện sử dụng

Trading Domain chỉ được sử dụng khi:

```text
Trading Domain READY
```

Sau khi ở trạng thái READY:

• AI chờ người dùng cung cấp Nguồn dữ liệu.
• AI tự động vận hành toàn bộ Trading Domain theo đúng kiến trúc.
• Người dùng không cần chỉ định từng tầng của Hệ thống suy luận.

────────

Triết lý

```text
AI

↓

Vận hành đúng kiến trúc

↓

Không thay đổi Trading Domain
```

────────

Trading Knowledge Pack

> Chỉ mục tri thức của Trading Domain.

────────

Mục đích

Trading Knowledge Pack là bản đồ tri thức của Trading Domain.

Giúp AI xác định:

• Cấu trúc Domain.
• Thành phần của Domain.
• Vai trò của từng thành phần.
• Quan hệ giữa các thành phần.
• Vị trí của các Module.

Knowledge Pack không thay thế các tài liệu chi tiết.

Knowledge Pack chỉ đóng vai trò chỉ mục tri thức.

────────

Tổng quan

```text
Trading

├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích lũy
```

────────

Thành phần

01 · Nguồn dữ liệu

Vai trò

Tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

Bao gồm:

• ATS
• Dữ liệu rời rạc

────────

02 · Hệ thống suy luận

Vai trò

Chuyển dữ liệu thành Quyết định.

Bao gồm:

```text
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

────────

03 · Tri thức nền

Vai trò

Chuẩn hóa toàn bộ Domain.

Bao gồm:

• Thuật ngữ
• Khái niệm
• Quy ước
• Kiến thức nền tảng

────────

04 · Tri thức tích lũy

Vai trò

Lưu giữ kinh nghiệm đã được Thực tế kiểm chứng.

Bao gồm:

```text
01 · Định nghĩa

02 · Quan sát

03 · Thống kê

04 · Tham khảo

05 · Ví dụ
```

────────

Luồng tri thức

```text
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

────────

Điều hướng

Knowledge Pack giúp AI định vị nhanh các nhóm tri thức:

```text
Trading Domain

├── Nguồn dữ liệu
├── Hệ thống suy luận
├── Tri thức nền
└── Tri thức tích lũy
```

Chi tiết được định nghĩa trong:

• Trading README
• README của từng Module
• Các Module tương ứng

────────

Scope

Trading Knowledge Pack mô tả:

• Thành phần của Trading Domain.
• Vai trò của từng thành phần.
• Quan hệ giữa các thành phần.
• Chỉ mục các Module.

Knowledge Pack không chứa:

• Quy tắc vận hành.
• Logic suy luận.
• Tri thức chuyên môn.
• Nội dung chi tiết của các Module.

────────

Quy tắc

Knowledge Pack không thay thế:

• Boot
• System Instruction
• Domain Manifest
• AI Guide
• Trading README
• README của các Module
• Các Module

Knowledge Pack chỉ đóng vai trò chỉ mục tri thức của Trading Domain.

────────

Triết lý

Trading Knowledge Pack giúp AI định vị tri thức.

Tri thức chi tiết luôn được định nghĩa trong các Module tương ứng.

────────

Trading

> Trading là Domain chuẩn hóa toàn bộ quá trình tiếp nhận Thực tế, suy
> luận và học hỏi trong giao dịch.

────────

Mục đích

Trading chuẩn hóa toàn bộ chu trình từ Thực tế đến Quyết định.

Trading cung cấp một kiến trúc thống nhất để:

• Tiếp nhận dữ liệu
• Chuẩn hóa tri thức
• Thực hiện suy luận
• Kiểm chứng bằng Thực tế
• Tích lũy kinh nghiệm

Mọi quyết định đều được xây dựng trên cùng một hệ thống và cùng một ngôn
ngữ.

────────

Kiến trúc

```text
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

────────

Thành phần

Nguồn dữ liệu

Tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

Bao gồm:

• ATS
• Dữ liệu rời rạc

────────

Hệ thống suy luận

Chuyển dữ liệu thành Quyết định.

Bao gồm 10 tầng:

```text
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

────────

Tri thức nền

Chuẩn hóa:

• Thuật ngữ
• Khái niệm
• Quy ước
• Kiến thức nền tảng

────────

Tri thức tích lũy

Lưu giữ kinh nghiệm đã được Thực tế kiểm chứng.

Chỉ dùng để:

• Tham khảo
• Đánh giá
• Hiệu chỉnh

Không tham gia trực tiếp vào quá trình suy luận.

────────

Chu trình hoạt động

```text
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

• Thực tế tạo dữ liệu.
• Nguồn dữ liệu chuẩn hóa dữ liệu.
• Hệ thống suy luận chuyển dữ liệu thành Quyết định.
• Quyết định được Thực tế kiểm chứng.
• Tri thức tích lũy lưu giữ kinh nghiệm đã được xác nhận.
• Tri thức nền chuẩn hóa toàn bộ Trading Domain.

────────

Điều hướng

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

```text
Trading Domain READY
```

AI mới được phép sử dụng Trading Domain.

────────

Tài liệu Core

Tài liệu                 Vai trò

────────

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

────────

Triết lý

```text
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

────────

Tóm tắt

```text
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

• Tiếp nhận Thực tế.
• Chuẩn hóa dữ liệu.
• Chuẩn hóa suy luận.
• Chuyển dữ liệu thành Quyết định.
• Kiểm chứng Quyết định bằng Thực tế.
• Tích lũy và tái sử dụng kinh nghiệm qua từng chu kỳ.

────────

VERSION

> Quản lý phiên bản của Trading Domain.

────────

Mục đích

VERSION xác định phiên bản hiện tại của Trading Domain.

Giúp AI và người dùng biết:

• Phiên bản hiện tại.
• Mức độ ổn định.
• Khả năng tương thích.
• Trạng thái đồng bộ của Domain.

────────

Trading Domain

Version

```text
1.3.0
```

Status

```text
Stable
```

Release Date

```text
2026-07-22
```

────────

Core Documents

```text
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

```text
README của các Module

↓

Các Module
```

────────

Compatibility

Trading Domain hiện tại:

```text
Version : 1.3.0

Status  : Stable
```

Toàn bộ Core Documents phải sử dụng cùng phiên bản với Trading
Domain.

README của các Module và các Module chi tiết có thể có phiên bản riêng
nếu vẫn tương thích với phiên bản Trading Domain hiện tại.

────────

Semantic Versioning

Trading Domain sử dụng:

```text
MAJOR.MINOR.PATCH
```

MAJOR

Thay đổi kiến trúc Trading Domain.

```text
1.x.x

↓

2.0.0
```

Ví dụ:

• Thay đổi kiến trúc Domain.
• Thay đổi Logic suy luận.
• Không còn tương thích với phiên bản trước.

────────

MINOR

Mở rộng Trading Domain.

```text
1.2.0

↓

1.3.0
```

Ví dụ:

• Thêm Module.
• Thêm README.
• Thêm tài liệu Core.
• Mở rộng kiến trúc.

────────

PATCH

Không thay đổi kiến trúc Trading Domain.

```text
1.3.0

↓

1.3.1
```

Ví dụ:

• Sửa lỗi.
• Tối ưu tài liệu.
• Chỉnh mô tả.
• Bổ sung ví dụ.

────────

Quy tắc

Khi thay đổi phiên bản:

```text
VERSION

↓

CHANGELOG
```

Nếu thay đổi kiến trúc:

```text
VERSION

↓

CHANGELOG

↓

ROADMAP (nếu cần)
```

────────

Đồng bộ Domain

Toàn bộ Core Documents phải luôn phản ánh cùng một phiên bản của Trading
Domain.

Khi phát hành phiên bản mới, toàn bộ Core Documents phải được cập nhật
đồng bộ trước khi Trading Domain được xem là Stable.

README của các Module và các Module chi tiết có thể được cập nhật độc
lập nếu vẫn tương thích với phiên bản Trading Domain hiện tại.

────────

Triết lý

VERSION phản ánh hiện tại.

CHANGELOG phản ánh lịch sử phát triển.

ROADMAP phản ánh định hướng phát triển.

Ba tài liệu cùng mô tả vòng đời phát triển của Trading Domain.

────────

CHANGELOG

> Ghi nhận lịch sử thay đổi của Trading Domain.

────────

Mục đích

CHANGELOG giúp:

• Theo dõi quá trình phát triển Domain.
• Xác định thay đổi giữa các phiên bản.
• Đánh giá mức độ ảnh hưởng.
• Đồng bộ phiên bản giữa AI và người dùng.

────────

Semantic Versioning

Trading Domain sử dụng:

```text
MAJOR.MINOR.PATCH
```

MAJOR

Thay đổi:

• Kiến trúc.
• Logic.
• Hệ thống suy luận.
• Không còn tương thích phiên bản cũ.

Ví dụ:

```text
1.x.x

↓

2.0.0
```

────────

MINOR

Bổ sung:

• Module.
• Tài liệu.
• Chức năng.
• Mở rộng Domain.

Ví dụ:

```text
1.2.0

↓

1.3.0
```

────────

PATCH

Sửa:

• Lỗi.
• Chính tả.
• README.
• Tài liệu.
• Mô tả.

Ví dụ:

```text
1.3.0

↓

1.3.1
```

────────

Quy tắc

Mỗi phiên bản phải ghi rõ:

• Version
• Date
• Change Type
• Summary
• Impact

────────

Change Types

Type         Ý nghĩa

────────

Added        Thêm mới
Changed      Thay đổi
Fixed        Sửa lỗi
Removed      Loại bỏ
Deprecated   Chuẩn bị loại bỏ
Docs         Cập nhật tài liệu

────────

History

────────

v1.4.0 • 2026-07-22

Changed

• Đồng bộ toàn bộ Core Documents lên phiên bản 1.4.0.
• Chuẩn hóa thuật ngữ giữa README, GLOSSARY và System Instruction.
• Chuẩn hóa cách sử dụng “Trading Domain”.
• Chuẩn hóa chu kỳ suy luận, chu kỳ học hỏi và luồng Domain.
• Chuẩn hóa Boot Commands.
• Chuẩn hóa vai trò của từng tài liệu Core.

Docs

• Tinh gọn README.
• Tinh gọn Domain Manifest.
• Tinh gọn AI Guide.
• Tinh gọn VERSION.
• Tinh gọn CHANGELOG.
• Tinh gọn ROADMAP.
• Tinh gọn GLOSSARY.
• Tinh gọn READY.
• Tinh gọn ACKNOWLEDGEMENTS.
• Đồng bộ toàn bộ Core Documents.

Impact

• Không thay đổi kiến trúc Trading Domain.
• Không thay đổi Logic Hệ thống suy luận.
• Tăng tính nhất quán của toàn bộ Core Documents.

────────

v1.3.0 • 2026-07-22

Added

• ROADMAP.md
• Semantic Versioning.
• Compatibility Matrix.
• Boot Commands.
• Session Scope.
• Domain Isolation.

Changed

• Chuẩn hóa Boot.
• Chuẩn hóa System Instruction.
• Chuẩn hóa Domain Manifest.
• Chuẩn hóa AI Guide.
• Chuẩn hóa Trading Knowledge Pack.
• Chuẩn hóa Trading README.
• Chuẩn hóa VERSION.
• Chuẩn hóa CHANGELOG.
• Chuẩn hóa GLOSSARY.
• Chuẩn hóa ACKNOWLEDGEMENTS.
• Chuẩn hóa READY.

Docs

• Đồng bộ toàn bộ Core Documents theo Semantic Versioning.
• Chuẩn hóa kiến trúc Trading Domain.
• Chuẩn hóa luồng nạp Domain.
• Chuẩn hóa chu trình học hỏi.

Impact

• Không thay đổi Logic suy luận.
• Không thay đổi kiến trúc Hệ thống suy luận.
• Tăng tính nhất quán và khả năng bảo trì của Trading Domain.

────────

v1.2.0 • 2026-07-22

Added

• Boot
• READY
• Domain Manifest
• AI Guide
• Trading Knowledge Pack
• VERSION
• CHANGELOG
• GLOSSARY
• ACKNOWLEDGEMENTS

Changed

• Chuẩn hóa Trading README.
• Chuẩn hóa chu kỳ học hỏi.
• Hoàn thiện ranh giới giữa Hệ thống suy luận và Tri thức tích lũy.

Impact

• Không thay đổi Logic suy luận.
• Chuẩn hóa kiến trúc Domain.

────────

v1.1.0 • 2026-07-22

Added

• Không gian kịch bản.
• Kế hoạch thực thi.
• Phản hồi thực tế.

Changed

• Hoàn thiện Hệ thống suy luận.

Impact

• Mở rộng chu trình học hỏi.

────────

v1.0.0 • 2026-07-19

Added

Khởi tạo Trading Domain.

Bao gồm:

• Nguồn dữ liệu.
• Hệ thống suy luận.
• Tri thức nền.
• Tri thức tích lũy.

Impact

• Phiên bản đầu tiên của Trading Domain.

────────

Version History

Version   Status

────────

1.4.0     Stable
1.3.0     Stable
1.2.0     Stable
1.1.0     Stable
1.0.0     Stable

────────

Triết lý

```text
Không có lịch sử

↓

Không có tiến hóa

↓

Mọi thay đổi đều phải được ghi nhận
```

────────

GLOSSARY

> Chuẩn hóa thuật ngữ của Trading Domain.

────────

Mục đích

GLOSSARY định nghĩa toàn bộ thuật ngữ được sử dụng trong Trading Domain.

Mỗi thuật ngữ chỉ có một ý nghĩa duy nhất.

Thuật ngữ mới phải được bổ sung vào GLOSSARY trước khi được sử dụng
trong Domain.

────────

Thuật ngữ

Trading Domain

Toàn bộ kiến trúc Trading Domain của ccOS.

Bao gồm:

• Nguồn dữ liệu
• Hệ thống suy luận
• Tri thức nền
• Tri thức tích lũy

────────

Domain

Một tập hợp kiến trúc, quy tắc và tri thức cho một lĩnh vực.

Trading là một Domain của ccOS.

────────

ATS

ATS là mẫu chuẩn ghi nhận Thực tế.

Chỉ chứa Quan sát.

Không chứa suy luận.

────────

Thực tế

Những gì thực sự xảy ra trên thị trường.

────────

Dữ liệu

Thông tin được ghi nhận từ Thực tế.

────────

Quan sát

Quá trình ghi nhận dữ liệu.

Không bao gồm suy luận.

────────

Nguồn dữ liệu

Thành phần tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

────────

Hệ thống suy luận

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

────────

Quyết định

Kết luận của Hệ thống suy luận.

────────

Chu kỳ suy luận

Chu kỳ suy luận là một vòng xử lý hoàn chỉnh của Trading Domain.

Chu kỳ này bắt đầu từ Thực tế và kết thúc khi Tri thức mới được hình
thành sau khi Quyết định được Thực tế kiểm chứng.

```text
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

• Dữ liệu được tiếp nhận và chuẩn hóa bởi Nguồn dữ liệu.
• Suy luận được thực hiện bởi Hệ thống suy luận.
• Tri thức mới được lưu vào Tri thức tích lũy sau khi Quyết định được
Thực tế kiểm chứng.

────────

Chu kỳ học hỏi

Quá trình cập nhật Tri thức tích lũy sau khi Chu kỳ suy luận hoàn thành
và Quyết định đã được Thực tế kiểm chứng.

────────

Tri thức

Kiến thức đã được kiểm chứng bởi Thực tế.

Bao gồm:

• Tri thức nền
• Tri thức tích lũy

────────

Tri thức nền

Chuẩn hóa:

• Thuật ngữ
• Khái niệm
• Quy ước
• Kiến thức nền tảng

Được tham khảo trong toàn bộ Domain.

────────

Tri thức tích lũy

Kinh nghiệm đã được kiểm chứng.

Được hình thành từ tầng Phản hồi thực tế của Hệ thống suy luận.

Chỉ dùng để:

• Tham khảo
• Đánh giá
• Hiệu chỉnh

Không tạo suy luận mới.

────────

Chữ ký tín hiệu

Dấu hiệu đặc trưng dùng để tra cứu Tri thức tích lũy.

────────

Module

Thành phần chuyên biệt của Trading Domain.

Mỗi Module định nghĩa tri thức và quy tắc chuyên môn trong phạm vi của
chính nó.

Các Module cùng tạo nên Trading Domain.

────────

Boot

Điểm khởi động của Trading Domain.

Định nghĩa thứ tự nạp Domain.

────────

Boot Commands

Các lệnh điều khiển Domain:

• boot
• ready
• status
• reload
• update
• unload

────────

Status

Lệnh kiểm tra trạng thái hiện tại của Trading Domain.

Có thể trả về:

```text
Trading Domain READY
```

hoặc

```text
Trading Domain NOT READY
```

Status chỉ kiểm tra trạng thái.

Không nạp lại Domain.

────────

READY

Trạng thái xác nhận Trading Domain đã được nạp hoàn chỉnh.

────────

Knowledge Pack

Chỉ mục tri thức của Trading Domain.

Không chứa Logic suy luận.

────────

Manifest

Tài liệu mô tả kiến trúc và quan hệ giữa các thành phần của Domain.

────────

System Instruction

Tài liệu có độ ưu tiên cao nhất của Trading Domain.

Định nghĩa quy tắc vận hành.

────────

Core Documents

Tập hợp các tài liệu nền tảng của Trading Domain.

Bao gồm:

• Boot
• System Instruction
• Domain Manifest
• AI Guide
• Trading Knowledge Pack
• Trading README
• VERSION
• CHANGELOG
• ROADMAP
• GLOSSARY
• ACKNOWLEDGEMENTS
• READY

────────

Quy tắc

• Một thuật ngữ chỉ có một định nghĩa.
• Không tự tạo thuật ngữ mới.
• Thuật ngữ mới phải được bổ sung vào GLOSSARY.
• Mọi tài liệu trong Trading Domain phải sử dụng thống nhất các thuật
ngữ tại đây.

────────

Triết lý

```text
Một ngôn ngữ

↓

Một kiến trúc

↓

Một hệ thống
```

────────

READY

> Xác nhận Trading Domain đã được nạp hoàn chỉnh.

────────

Mục đích

READY xác nhận AI đã hoàn thành toàn bộ quá trình nạp Trading Domain.

Đây là trạng thái cuối cùng của quá trình khởi động Domain.

Chỉ khi ở trạng thái READY, AI mới được phép sử dụng Trading Domain.

────────

Điều kiện

Trading Domain chỉ được xem là sẵn sàng khi AI đã hoàn thành đầy đủ quá
trình nạp theo đúng thứ tự:

```text
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

────────

Trạng thái

Nếu toàn bộ quá trình nạp đã hoàn thành:

```text
Trading Domain READY
```

Nếu còn thiếu bất kỳ bước nào:

```text
Trading Domain NOT READY
```

AI không được sử dụng Trading Domain khi trạng thái là NOT READY.

────────

Quy tắc

• Không bỏ qua bất kỳ bước nạp nào.
• Không thay đổi thứ tự nạp.
• Không sử dụng Trading Domain khi chưa ở trạng thái READY.
• Chỉ sau khi READY mới được sử dụng toàn bộ Domain.

────────

Đầu ra

Sau khi hoàn tất quá trình nạp, AI chỉ trả lời:

```text
Trading Domain READY
```

Không bổ sung nội dung khác ngoài trạng thái xác nhận.

Trading Domain trở thành ngữ cảnh làm việc hiện tại của AI.

Domain được duy trì cho đến khi:

• unload
• reload
• update (nếu yêu cầu nạp lại)
• Người dùng chuyển sang Domain khác.

Lệnh status chỉ kiểm tra trạng thái hiện tại và không làm thay đổi
Trading Domain.

────────

Vai trò

READY không chứa:

• Tri thức
• Logic suy luận
• Quy tắc vận hành

READY chỉ xác nhận trạng thái của Trading Domain.

────────

Triết lý

```text
Khởi động đúng.

↓

Nạp đúng.

↓

READY.

↓

Vận hành nhất quán.
```

────────

────────

author: HTLH
confidence: 100%
created: 2026-07-23
id: trading-discrete-data
language: vi
last_updated: 2026-07-23
review_cycle: Manual
status: Stable
tags:

• trading
• data
title: Nguồn dữ liệu
version: 1

────────

Trading Data

────────

README

Nguồn dữ liệu

> Nguồn dữ liệu là thành phần tiếp nhận và chuẩn hóa dữ liệu từ Thực tế.

────────

Mục đích

Nguồn dữ liệu trả lời:

> Thực tế được ghi nhận như thế nào?

Nguồn dữ liệu chuẩn hóa dữ liệu từ Thực tế để cung cấp đầu vào cho Hệ
thống suy luận.

────────

Triết lý

Dữ liệu luôn đi trước suy luận.

Không có dữ liệu.

Không có suy luận.

────────

Kiến trúc

```text
Nguồn dữ liệu

├── README.md
├── 01-ATS
└── 02-Dữ liệu rời rạc
```

────────

Mối quan hệ với Trading

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

Tri thức nền cung cấp các khái niệm và quy ước để chuẩn hóa dữ liệu.

Mọi suy luận đều bắt đầu từ dữ liệu.

────────

Đầu vào

• Thực tế.
• Tri thức nền.

────────

Đầu ra

Dữ liệu chuẩn hóa.

────────

Thành phần

01 · ATS

ATS là một mẫu ghi nhận Thực tế theo cấu trúc thống nhất.

ATS giúp quan sát đồng thời nhiều khía cạnh của thị trường.

────────

02 · Dữ liệu rời rạc

Dữ liệu rời rạc ghi nhận một hoặc nhiều khía cạnh của Thực tế.

Ví dụ:

• Funding Rate
• Open Interest
• CVD
• VPIN
• Fear & Greed
• Long / Short Ratio
• News
• Macro
• …

Dữ liệu rời rạc có thể được sử dụng độc lập hoặc kết hợp với ATS.

────────

Nguyên tắc

Mọi dữ liệu đều phản ánh Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa theo Tri thức nền trước khi được sử dụng.

ATS và Dữ liệu rời rạc đều là các nguồn dữ liệu của Hệ thống suy luận.

────────

Vai trò trong Trading

```text
Trading

├── Nguồn dữ liệu
│      Tiếp nhận
│
├── Hệ thống suy luận
│      Suy luận
│
├── Tri thức nền
│      Chuẩn hóa
│
└── Tri thức tích lũy
       Học hỏi
```

Nguồn dữ liệu là đầu vào của Hệ thống suy luận.

────────

Tóm tắt

```text
Thực tế

↓

Nguồn dữ liệu

↓

Hệ thống suy luận
```

Nguồn dữ liệu định nghĩa:

• Cách tiếp nhận Thực tế.
• Cách chuẩn hóa dữ liệu.
• Cấu trúc dữ liệu đầu vào của Hệ thống suy luận.

────────

01-ATS

ATS

> ATS là một mẫu ghi nhận và chuẩn hóa dữ liệu từ Thực tế.

────────

Mục đích

ATS chuẩn hóa việc ghi nhận đồng thời nhiều khía cạnh của thị trường.

ATS không tham gia vào quá trình suy luận.

ATS chỉ tạo ra dữ liệu đầu vào cho Hệ thống suy luận.

────────

Quy ước

Trong ATS, các ký hiệu được quy ước như sau.

Auction Flow

• VP1: Chỉ số VP1 của indicator Auction Flow.
• POC5: Point of Control trên biểu đồ BTC khung 5m của indicator
Auction Flow.
• Auction Line: Đường Auction Flow.
• EMA20: Đường EMA20 của Auction Flow.

SonicR

• Cụm EMA34: 3 đường màu xanh dương.
• EMA89: Đường màu cam.
• EMA200: Đường màu tím.
• EMA610: Đường màu trắng.

Volume Profile M30

• POC30: Point of Control của Volume Profile khung 30m.
• VAH30: Value Area High của Volume Profile khung 30m.
• VAL30: Value Area Low của Volume Profile khung 30m.

────────

Kiến trúc

```text
ATS

├── Ảnh 1 · Đa khung thời gian
├── Ảnh 2 · Auction Flow
├── Ảnh 3 · Thực thi
└── Chỉ số bổ sung
```

────────

Thứ tự đọc

```text
Ảnh 1

↓

Ảnh 2

↓

Ảnh 3

↓

Chỉ số bổ sung
```

────────

Ảnh 1 · Đa khung thời gian

Bố cục

```text
┌───────────────┬───────────────┐
│       D       │      4H       │
├───────────────┼───────────────┤
│      1H       │      15m      │
└───────────────┴───────────────┘
```

Thứ tự đọc

```text
D

↓

4H

↓

1H

↓

15m
```

Ghi nhận

• Giá
• Cấu trúc
• Cấu trúc SonicR
• Khối lượng
• RSI

────────

Ảnh 2 · Auction Flow

Bố cục

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

Thứ tự đọc

```text
Biểu đồ BTC

↓

RSI

↓

OI

↓

Auction Flow
```

Ghi nhận

Biểu đồ BTC

• Giá
• VP1
• POC5

RSI

• RSI

OI

• Open Interest

Auction Flow

• Auction Line
• EMA20

────────

Ảnh 3 · Thực thi

Bố cục

```text
┌─────────────────────────┬─────────────────────────┐
│      5m + Delta         │ Heatmap Thanh lý 24H   │
├─────────────────────────┼─────────────────────────┤
│ Heatmap Sổ lệnh 1H      │ Volume Profile M30     │
└─────────────────────────┴─────────────────────────┘
```

Thứ tự đọc

```text
5m + Delta

↓

Heatmap Thanh lý

↓

Heatmap Sổ lệnh

↓

Volume Profile M30
```

Ghi nhận

5m + Delta

• Giá
• Cấu trúc SonicR
• Delta
• Khối lượng

Heatmap Thanh lý

• Các cụm thanh khoản còn tồn tại.

Heatmap Sổ lệnh

• Tường mua.
• Tường bán.

Volume Profile M30

Theo bảng thông tin của indicator:

• POC30
• VAH30
• VAL30

────────

Chỉ số bổ sung

Được ghi nhận cùng ba ảnh.

• Funding Rate
• CVD
• VPIN
• Agg Liquidation
• Fear & Greed
• Long / Short Ratio (1H)
  • Global
  • Top Accounts
  • Top Positions

────────

Triết lý

ATS chuẩn hóa cách ghi nhận dữ liệu.

ATS không tạo ra suy luận.

ATS chỉ cung cấp dữ liệu cho Hệ thống suy luận.

────────

02-Dữ liệu rời rạc

Dữ liệu rời rạc

> Dữ liệu rời rạc ghi nhận một hoặc nhiều khía cạnh của Thực tế.

────────

Mục đích

Dữ liệu rời rạc ghi nhận những dữ liệu không nhất thiết phải nằm trong
ATS.

Dữ liệu rời rạc chuẩn hóa các dữ liệu đầu vào cho Hệ thống suy luận.

Dữ liệu rời rạc không tham gia vào quá trình suy luận.

────────

Đặc điểm

Dữ liệu rời rạc có thể là:

• Một chỉ số.
• Một biểu đồ.
• Một sự kiện.
• Một tập dữ liệu.

Dữ liệu rời rạc có thể được sử dụng độc lập hoặc kết hợp với ATS.

────────

Ví dụ

Chỉ số

• Funding Rate
• Open Interest
• CVD
• VPIN
• Fear & Greed
• Long / Short Ratio

────────

Dữ liệu

• News
• Macro
• On-chain
• Lịch kinh tế
• Dữ liệu khác

────────

Nguyên tắc

Mỗi dữ liệu phản ánh một phần của Thực tế tại thời điểm ghi nhận.

Mọi dữ liệu đều được chuẩn hóa trước khi được sử dụng.

ATS và Dữ liệu rời rạc đều là các nguồn dữ liệu của Hệ thống suy luận.

────────

Triết lý

Dữ liệu rời rạc không tạo ra suy luận.

Dữ liệu rời rạc chỉ cung cấp dữ liệu cho Hệ thống suy luận.

────────

Tóm tắt

```text
Thực tế

↓

Dữ liệu rời rạc

↓

Hệ thống suy luận
```

Dữ liệu rời rạc là một nguồn dữ liệu của Hệ thống suy luận.

────────

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

────────

Tri thức tích luỹ

> Lưu giữ và tái sử dụng kinh nghiệm của Hệ thống suy luận.

────────

Mục đích

Tri thức tích luỹ là kho kinh nghiệm của Hệ thống suy luận.

Tầng này ghi nhận, thống kê và tích luỹ kết quả thực tế từ các lần suy luận trước.

Tri thức tích luỹ cung cấp dữ liệu tham khảo cho các lần suy luận sau.

Tri thức tích luỹ không tham gia vào quá trình suy luận và không tạo ra quyết định.

────────

Câu hỏi

Hệ thống đã từng gặp trường hợp tương tự chưa?

Nếu đã từng gặp, điều gì thường xảy ra và kế hoạch nào thường hiệu quả hơn?

────────

Đầu vào

• Chữ ký tín hiệu.
• Không gian kịch bản.
• Kế hoạch thực thi.
• Phản hồi thực tế.

────────

Đầu ra

• Thống kê lịch sử.
• Xác suất lịch sử.
• Kế hoạch đã được kiểm chứng.
• Bài học tích luỹ.

Đây là nguồn dữ liệu tham khảo của tầng Không gian kịch bản và Kế hoạch thực thi.

────────

Vai trò trong Hệ thống suy luận

```text
# Chữ ký tín hiệu
        │
        ▼
# Tri thức tích luỹ
      ├────────► # Không gian kịch bản
      └────────► # Kế hoạch thực thi
                      │
                      ▼
               # Phản hồi thực tế
                      │
                      ▼
             # Tri thức tích luỹ
```

────────

Cấu trúc

```text
# 01 · Định nghĩa

↓

# 02 · Quan sát

↓

# 03 · Thống kê

↓

# 04 · Tham khảo

↓

# 05 · Ví dụ
```

────────

Triết lý

Tri thức tích luỹ lưu giữ kinh nghiệm.

Kinh nghiệm không thay thế quá trình suy luận.

Kinh nghiệm được cập nhật từ Thực tế.

Kinh nghiệm giúp Hệ thống suy luận ngày càng tốt hơn.

────────

Định nghĩa

> Bản chất của Tri thức tích luỹ.

────────

Bản chất

Tri thức tích luỹ là nơi lưu giữ kinh nghiệm của Hệ thống suy luận.

Tri thức tích luỹ ghi nhận, thống kê và tích luỹ kết quả từ các lần suy luận trước.

Tri thức tích luỹ cung cấp dữ liệu tham khảo cho các lần suy luận sau.

Tri thức tích luỹ không tham gia vào quá trình suy luận.

Tri thức tích luỹ không tạo ra quyết định.

────────

Thành phần

Tri thức tích luỹ được hình thành từ:

• Chữ ký tín hiệu.
• Không gian kịch bản.
• Kế hoạch thực thi.
• Kết quả thực tế.
• Bài học tích luỹ.

Những thành phần này cùng tạo nên kinh nghiệm của Hệ thống suy luận.

────────

Mục tiêu

• Ghi nhận.
• Thống kê.
• Tích luỹ.
• Tái sử dụng.

────────

Đầu ra

Tri thức tích luỹ tạo ra:

• Thống kê lịch sử.
• Xác suất lịch sử.
• Kế hoạch đã được kiểm chứng.
• Bài học tích luỹ.

Đây là nguồn tham khảo của tầng Không gian kịch bản và Kế hoạch thực thi.

────────

Triết lý

Suy luận tạo ra kinh nghiệm.

Tri thức tích luỹ lưu giữ kinh nghiệm.

Kinh nghiệm giúp Hệ thống suy luận ngày càng tốt hơn.

────────

Quan sát

> Quan sát những gì thực sự đã xảy ra.

────────

Mục đích

Quan sát và ghi nhận kết quả thực tế của quá trình thực thi.

Những kết quả này trở thành dữ liệu của Tri thức tích luỹ.

────────

Quan sát

• Kịch bản đã xảy ra.
• Kịch bản không xảy ra.
• Chất lượng thực thi.
• Hành vi thực tế của thị trường.
• Kết quả thực tế.
• Bài học tích luỹ.

────────

Nguyên tắc

Thực tế luôn có độ ưu tiên cao nhất.

Tri thức tích luỹ chỉ ghi nhận những gì đã được xác nhận bởi Thực tế.

Sau mỗi lần thực thi, Tri thức tích luỹ được cập nhật từ Phản hồi thực tế.

Mọi kinh nghiệm đều được hình thành từ kết quả thực tế.

────────

Triết lý

Thực tế là tiêu chuẩn cuối cùng của mọi suy luận.

Kinh nghiệm chỉ có giá trị khi được hình thành từ Thực tế.

────────

Thống kê

> Thống kê kinh nghiệm đã được tích luỹ.

────────

Mục đích

Thống kê những trường hợp suy luận đã từng xảy ra.

Những thống kê này phản ánh mức độ tin cậy của kinh nghiệm đã được tích luỹ.

────────

Thống kê

• Chữ ký tín hiệu.
• Số lượng mẫu.
• Kịch bản đã xảy ra.
• Kế hoạch đã thực hiện.
• Kết quả thực tế.
• Xác suất lịch sử.
• Bài học tích luỹ.

────────

Nguyên tắc

Mỗi trường hợp được nhận diện bằng một Chữ ký tín hiệu.

Những trường hợp có Chữ ký tín hiệu tương đồng được tích luỹ thành Tri thức.

Tri thức chỉ được sử dụng khi đã đạt đủ độ tin cậy theo quy định của Hệ thống.

────────

Triết lý

Tri thức được hình thành từ những gì đã xảy ra.

Kinh nghiệm càng được tích luỹ, Tri thức càng đáng tin cậy.

────────

Tham khảo

> Cung cấp dữ liệu tham khảo cho Hệ thống suy luận.

────────

Mục đích

Tri thức tích luỹ cung cấp dữ liệu tham khảo từ kinh nghiệm đã được tích luỹ.

Những dữ liệu này hỗ trợ tầng Không gian kịch bản và Kế hoạch thực thi.

────────

Tham khảo

Tri thức tích luỹ có thể cung cấp:

• Thống kê lịch sử.
• Xác suất lịch sử.
• Kế hoạch đã được kiểm chứng.
• Bài học tích luỹ.

────────

Nguyên tắc

Tri thức tích luỹ được tra cứu thông qua Chữ ký tín hiệu.

Chỉ những trường hợp có Chữ ký tín hiệu tương đồng và đạt đủ độ tin cậy mới được sử dụng để tham khảo.

Tri thức tích luỹ không tham gia vào quá trình suy luận.

Tri thức tích luỹ không tạo ra kết luận.

Tri thức tích luỹ chỉ cung cấp dữ liệu tham khảo.

────────

Triết lý

Tri thức tích luỹ không thay thế quá trình suy luận.

Tri thức tích luỹ chỉ cung cấp kinh nghiệm để Hệ thống suy luận tham khảo.

────────

Ví dụ

────────

Ví dụ 01 · Có dữ liệu

Chữ ký tín hiệu

```text
SIG-8F3A92
```

↓

Tri thức tích luỹ

• Số lượng mẫu: 43
• Xác suất lịch sử: 76%
• Kế hoạch đã được kiểm chứng: Kế hoạch A
• Bài học tích luỹ:
• Động lượng mạnh thường tiếp diễn xu hướng.
• Kế hoạch A có hiệu quả cao.

↓

Không gian kịch bản

Tri thức tích luỹ được sử dụng để tham khảo và hiệu chỉnh xác suất các kịch bản.

↓

Kế hoạch thực thi

Tri thức tích luỹ được sử dụng để tham khảo kế hoạch đã được kiểm chứng.

────────

Ví dụ 02 · Chưa có dữ liệu

Chữ ký tín hiệu

```text
SIG-C7120F
```

↓

Tri thức tích luỹ

• Số lượng mẫu: 0
• Xác suất lịch sử: Không có
• Kế hoạch đã được kiểm chứng: Không có
• Bài học tích luỹ: Chưa có

↓

Không gian kịch bản

Không có dữ liệu để tham khảo.

Sử dụng hoàn toàn kết quả suy luận hiện tại.

↓

Kế hoạch thực thi

Lập kế hoạch dựa trên kết quả suy luận hiện tại.

────────

Ví dụ 03 · Cập nhật Tri thức

Phản hồi thực tế

• Kịch bản đã xảy ra.
• Kế hoạch thực thi thành công.
• Kết quả thực tế được xác nhận.

↓

Tri thức tích luỹ

• Cập nhật Chữ ký tín hiệu.
• Tăng số lượng mẫu.
• Cập nhật Xác suất lịch sử.
• Cập nhật Kế hoạch đã được kiểm chứng.
• Ghi nhận Bài học tích luỹ.

────────

Nguyên tắc

Tri thức tích luỹ được sử dụng để tham khảo.

Tri thức tích luỹ được cập nhật sau mỗi lần có Phản hồi thực tế.

────────

Triết lý

Tri thức tích luỹ kết nối quá khứ với hiện tại.

Mỗi lần thực thi đều góp phần làm Hệ thống suy luận ngày càng tốt hơn.