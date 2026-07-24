---
title: Build
id: trading-build
version: 1.4.0
status: Stable
author: HTLH
language: vi
---

# Build

> Quy định cách biên dịch Trading Domain thành các Bundle dùng cho AI.

---

# Mục đích

Build chuẩn hóa việc đóng gói Trading Domain.

Build không thay đổi nội dung Domain.

Build chỉ tạo các Bundle phục vụ AI.

---

# Thư mục

Trading/

↓

Build/

---

# Build Targets

## Build Core

Sinh:

Trading-Core.md

Bao gồm:

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

VERSION

↓

CHANGELOG

↓

GLOSSARY

↓

READY

---

## Build Data

Sinh:

Trading-Data.md

Bao gồm:

README - Nguồn dữ liệu

↓

ATS

↓

Dữ liệu rời rạc

---

## Build Reasoning

Sinh:

Trading-Reasoning.md

Bao gồm:

README - Hệ thống suy luận

↓

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

---

## Build Knowledge

Sinh:

Trading-Knowledge.md

Bao gồm:

README - Tri thức nền

↓

Tri thức nền

---

## Build Memory

Sinh:

Trading-Memory.md

Bao gồm:

README - Tri thức tích luỹ

↓

01-Định nghĩa

↓

02-Quan sát

↓

03-Thống kê

↓

04-Tham khảo

↓

05-Ví dụ

---

## Build Bundle

Sinh:

Trading-Domain-Full.md

Bao gồm:

Trading-Core

↓

Trading-Data

↓

Trading-Reasoning

↓

Trading-Knowledge

↓

Trading-Memory

↓

Trading-Domain-Full.md

↓

AI Bundle

---

## Build Release

Sinh:

Trading-Domain-vX.X.X.zip

├── Trading-Core.md

├── Trading-Data.md

├── Trading-Reasoning.md

├── Trading-Knowledge.md

├── Trading-Memory.md

└── Trading-Domain-Full.md

---

# Build Flow

Core

↓

Data

↓

Reasoning

↓

Knowledge

↓

Memory

↓

Bundle

↓

Release

↓

Deploy

---

# Quy tắc

Build không:

- thay đổi Domain
- thay đổi Logic
- thay đổi Module

Build chỉ tạo Bundle.

---

# Triết lý

Một Domain.

↓

Nhiều Bundle.

↓

Một điểm khởi động.

↓

Một cách vận hành.