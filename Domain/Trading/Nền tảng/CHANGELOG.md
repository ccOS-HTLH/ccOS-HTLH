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