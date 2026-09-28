# Hanoi Cultural Discovery

Hệ thống khám phá không gian văn hóa cá nhân tại Hà Nội, ứng dụng AI để tìm kiếm và gợi ý địa điểm phù hợp với sở thích người dùng.

## Giới thiệu

Đề tài xây dựng một hệ thống hỗ trợ người dùng khám phá các không gian văn hóa tại Hà Nội như bảo tàng, di tích lịch sử, thư viện, hiệu sách, không gian nghệ thuật, rạp chiếu phim nghệ thuật và các không gian văn hóa đặc trưng.

Hệ thống cho phép người dùng tìm kiếm địa điểm thông qua từ khóa, bộ lọc hoặc mô tả nhu cầu bằng ngôn ngữ tự nhiên. AI được sử dụng để phân tích yêu cầu tìm kiếm và chuyển đổi thành các tiêu chí phù hợp với dữ liệu địa điểm trong hệ thống.

## Chức năng chính

- Đăng ký, đăng nhập và quản lý tài khoản
- Quản lý thông tin và sở thích cá nhân
- Xem bản đồ các không gian văn hóa tại Hà Nội
- Tìm kiếm và lọc địa điểm theo nhiều tiêu chí
- Tìm kiếm địa điểm bằng ngôn ngữ tự nhiên với AI
- Xem thông tin chi tiết về địa điểm
- Gợi ý địa điểm dựa trên sở thích người dùng
- Quản trị và quản lý dữ liệu địa điểm

## Công nghệ sử dụng

### Frontend
- React.js
- Tailwind CSS
- Leaflet

### Backend
- Python
- FastAPI
- RESTful API
- JWT Authentication

### Database
- MySQL

### AI
- OpenAI API
- Natural Language Processing
- Text Embedding / Semantic Similarity (dự kiến, nếu đảm bảo tiến độ)

### Công cụ
- Figma
- Git / GitHub
- VS Code
- Postman

## Kiến trúc hệ thống

```text
┌─────────────────┐
│    Frontend     │
│ React + Leaflet │
└────────┬────────┘
         │ REST API
         ▼
┌─────────────────┐
│     Backend     │
│ Python/FastAPI  │
└──────┬─────┬────┘
       │     │
       │     ▼
       │  ┌──────────────┐
       │  │  OpenAI API  │
       │  └──────────────┘
       │
       ▼
┌─────────────────┐
│      MySQL      │
│ Location & User │
│      Data       │
└─────────────────┘
## UML

Hệ thống được phân tích và thiết kế bằng UML nhằm mô tả các tác nhân, chức năng, luồng xử lý và cấu trúc của hệ thống.

### Use Case Diagram

Mô tả các tác nhân và chức năng chính của hệ thống.

**Actors:**
- Người dùng
- Quản trị viên
- AI API

**Các chức năng chính:**
- Đăng ký / Đăng nhập
- Quản lý hồ sơ cá nhân
- Quản lý sở thích
- Xem bản đồ văn hóa
- Tìm kiếm địa điểm
- Lọc địa điểm
- Xem chi tiết địa điểm
- Tìm kiếm bằng ngôn ngữ tự nhiên
- Xem gợi ý cá nhân hóa
- Quản lý địa điểm
- Quản lý danh mục

### Activity Diagram

Mô tả luồng xử lý của các chức năng chính:
- Tìm kiếm địa điểm
- Tìm kiếm bằng ngôn ngữ tự nhiên
- Gợi ý địa điểm cá nhân hóa
- Quản lý dữ liệu địa điểm

### Sequence Diagram

Mô tả trình tự tương tác giữa người dùng, Frontend, Backend, AI API và cơ sở dữ liệu.

Luồng tìm kiếm bằng ngôn ngữ tự nhiên:

```text
Người dùng
    ↓
Frontend (React)
    ↓
Backend (FastAPI)
    ↓
AI API
    ↓
Backend (FastAPI)
    ↓
MySQL
    ↓
Frontend
    ↓
Kết quả tìm kiếm
