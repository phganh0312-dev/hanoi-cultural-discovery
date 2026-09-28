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
