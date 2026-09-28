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
## Phân tích hệ thống

### 1. Phân chia các tầng

Hệ thống được thiết kế theo mô hình phân tầng, gồm:

- **Presentation Layer:** React.js, Tailwind CSS và Leaflet. Phụ trách giao diện, bản đồ và tương tác với người dùng.
- **Business Logic Layer:** Python + FastAPI. Xử lý các nghiệp vụ, xác thực, tìm kiếm, lọc và gợi ý địa điểm.
- **Data Access Layer:** Thực hiện truy xuất và quản lý dữ liệu trong MySQL.
- **AI Service Layer:** Kết nối OpenAI API để phân tích yêu cầu tìm kiếm bằng ngôn ngữ tự nhiên và chuyển đổi thành các tiêu chí/tag phù hợp.

### 2. Các thực thể chính

- **User:** thông tin tài khoản và hồ sơ người dùng.
- **Interest:** sở thích của người dùng.
- **Location:** thông tin các địa điểm văn hóa.
- **Category:** phân loại địa điểm.
- **Tag:** các thuộc tính mô tả địa điểm.
- **Recommendation:** thông tin phục vụ việc gợi ý địa điểm.

### 3. Dữ liệu

Hệ thống quản lý các nhóm dữ liệu chính:

- Thông tin tài khoản và người dùng.
- Sở thích người dùng.
- Thông tin địa điểm văn hóa.
- Danh mục và tag.
- Vị trí địa lý của địa điểm.
- Hình ảnh và nội dung mô tả địa điểm.

Dữ liệu địa điểm được thu thập và chuẩn hóa từ các địa điểm thực tế tại Hà Nội trước khi lưu trữ trong MySQL.

### 4. Các hành động chính

- Đăng ký, đăng nhập và quản lý tài khoản.
- Quản lý thông tin và sở thích cá nhân.
- Xem bản đồ các không gian văn hóa.
- Tìm kiếm và lọc địa điểm.
- Tìm kiếm bằng ngôn ngữ tự nhiên thông qua AI.
- Xem thông tin chi tiết địa điểm.
- Nhận gợi ý địa điểm phù hợp với sở thích.
- Quản lý dữ liệu địa điểm và danh mục.

### 5. Giao diện chính

- **Đăng nhập / Đăng ký**
- **Trang khám phá:** bản đồ, tìm kiếm và bộ lọc.
- **Trang kết quả tìm kiếm:** danh sách địa điểm và bản đồ.
- **Trang chi tiết địa điểm:** hình ảnh, mô tả, thông tin và vị trí.
- **Trang gợi ý cá nhân:** các địa điểm phù hợp với sở thích.
- **Trang hồ sơ:** thông tin tài khoản và sở thích.
- **Trang quản trị:** quản lý địa điểm và danh mục.

