# OpenClaw - Trợ Lý AI Trên Telegram

<p align="center">
  <img src="https://img.shields.io/badge/Telegram-Bot-blue?style=for-the-badge&logo=telegram" alt="Telegram Bot">
  <img src="https://img.shields.io/badge/Language-Python-success?style=for-the-badge&logo=python" alt="Python">
  <img src="https://img.shields.io/badge/AI-GPT-orange?style=for-the-badge" alt="AI GPT">
</p>

---

## 📌 Giới Thiệu Dự Án

**OpenClaw** là một bot Telegram thông minh được xây dựng trên nền tảng AI, giúp người dùng thực hiện các tác vụ liên quan đến email và tìm kiếm thông tin một cách nhanh chóng và hiệu quả. Với khả năng tích hợp các công nghệ AI tiên tiến, OpenClaw mang đến trải nghiệm người dùng mượt mà và hữu ích trong việc quản lý email cũng như tra cứu thông tin trên web.

Dự án được phát triển với mục tiêu tự động hóa các công việc lặp đi lặp lại liên quan đến email, giúp người dùng tiết kiệm thời gian và nâng cao năng suất làm việc.

---

## ✨ Các Tính Năng Chính

### 1. 📧 Đọc Email
- Kết nối và truy cập hộp thư email của người dùng một cách an toàn
- Hiển thị nội dung email với định dạng rõ ràng, dễ đọc
- Hỗ trợ nhiều nhà cung cấp dịch vụ email phổ biến (Gmail, Outlook, Yahoo, v.v.)
- Truy xuất thông tin người gửi, ngày nhận, tiêu đề và nội dung chính

### 2. 📝 Tóm Tắt Email
- Sử dụng công nghệ AI để phân tích và tóm tắt nội dung email
- Trích xuất các điểm chính của email một cách nhanh chóng
- Giúp người dùng nắm bắt nội dung quan trọng mà không cần đọc toàn bộ email
- Hỗ trợ tóm tắt cả email dài với nội dung phức tạp

### 3. 🔍 Tìm Kiếm Web
- Tích hợp khả năng tìm kiếm thông tin trên internet
- Trả về kết quả tìm kiếm chính xác và phù hợp với yêu cầu
- Hỗ trợ tìm kiếm bằng tiếng Việt và tiếng Anh
- Cập nhật thông tin theo thời gian thực

---

## 🚀 Hướng Dẫn Cài Đặt

### Yêu Cầu Hệ Thống

| Thành phần | Phiên bản tối thiểu |
|------------|---------------------|
| Python     | 3.8 trở lên         |
| pip        | Phiên bản mới nhất  |
| API Token  | Telegram Bot Token  |

### Các Bước Cài Đặt

#### 1. Clone dự án về máy
```bash
git clone https://github.com/your-repo/openclaw.git
cd openclaw
```

#### 2. Tạo môi trường ảo (khuyến nghị)
```bash
# Trên Windows
python -m venv venv
venv\Scripts\activate

# Trên Linux/MacOS
python3 -m venv venv
source venv/bin/activate
```

#### 3. Cài đặt các thư viện cần thiết
```bash
pip install -r requirements.txt
```

#### 4. Cấu hình biến môi trường
Tạo file `.env` trong thư mục gốc của dự án và cấu hình các biến môi trường cần thiết (xem phần **Cấu hình biến môi trường** bên dưới).

#### 5. Chạy ứng dụng
```bash
python main.py
```

---

## ⚙️ Cấu Hình Biến Môi Trường

File `.env` chứa các cấu hình quan trọng cho ứng dụng. Dưới đây là danh sách các biến môi trường cần thiết:

### Biến Bắt Buộc

| Biến môi trường | Mô tả | Ví dụ |
|-----------------|-------|-------|
| `TELEGRAM_BOT_TOKEN` | Token bot Telegram lấy từ BotFather | `1234567890:ABCdefGHIjklMNOpqrsTUVwxyz` |
| `OPENAI_API_KEY` | API Key từ OpenAI để sử dụng tính năng AI | `sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxx` |
| `EMAIL_ADDRESS` | Địa chỉ email để đọc và tóm tắt | `your_email@gmail.com` |
| `EMAIL_PASSWORD` | Mật khẩu email hoặc App Password | `xxxxxxxxxxxx` |

### Biến Tùy Chọn

| Biến môi trường | Mô tả | Mặc định |
|-----------------|-------|----------|
| `EMAIL_IMAP_SERVER` | Địa chỉ server IMAP | `imap.gmail.com` |
| `EMAIL_IMAP_PORT` | Cổng IMAP | `993` |
| `SEARCH_API_KEY` | API Key cho dịch vụ tìm kiếm web | - |
| `LOG_LEVEL` | Cấp độ ghi log | `INFO` |

### Ví Dụ File `.env`

```env
# Telegram Bot Configuration
TELEGRAM_BOT_TOKEN=1234567890:ABCdefGHIjklMNOpqrsTUVwxyz

# OpenAI Configuration
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxx

# Email Configuration
EMAIL_ADDRESS=your_email@gmail.com
EMAIL_PASSWORD=xxxxxxxxxxxx
EMAIL_IMAP_SERVER=imap.gmail.com
EMAIL_IMAP_PORT=993

# Search Configuration
SEARCH_API_KEY=your_search_api_key

# Logging
LOG_LEVEL=INFO
```

> **⚠️ Lưu ý quan trọng:** 
> - Không bao giờ chia sẻ file `.env` lên repository công khai
> - Đối với Gmail, bạn cần bật "Less secure app access" hoặc sử dụng App Password
> - Bảo mật thông tin đăng nhập email bằng cách sử dụng xác thực hai yếu tố

---

## 📖 Hướng Dẫn Sử Dụng

### Khởi Đầu

1. Mở ứng dụng Telegram và tìm kiếm bot của bạn qua username đã đăng ký với BotFather
2. Nhấn nút **Start** hoặc gửi tin nhắn `/start` để bắt đầu

### Các Lệnh Có Sẵn

| Lệnh | Mô tả |
|------|-------|
| `/start` | Khởi động bot và hiển thị tin nhắn chào mừng |
| `/help` | Hiển thị hướng dẫn sử dụng chi tiết |
| `/reademail` | Đọc email mới nhất trong hộp thư |
| `/summarize` | Tóm tắt email gần đây nhất |
| `/search <từ khóa>` | Tìm kiếm thông tin trên web |
| `/status` | Kiểm tra trạng thái kết nối |

### Ví Dụ Sử Dụng

#### Đọc email mới
```
Người dùng: /reademail
Bot: 📧 Email mới nhất từ: sender@example.com
     Tiêu đề: Meeting Tomorrow
     Nội dung: Dear Team,
     We have a meeting scheduled for tomorrow at 2 PM...
```

#### Tóm tắt email
```
Người dùng: /summarize
Bot: 📝 Tóm tắt email:
     - Cuộc họp được lên lịch vào ngày mai lúc 14:00
     - Tham dự: Toàn bộ đội nhóm
     - Chủ đề: Cập nhật dự án hàng quý
```

#### Tìm kiếm web
```
Người dùng: /search人工智能发展趋势
Bot: 🔍 Kết quả tìm kiếm cho "人工智能发展趋势":
     
     1. Xu hướng AI 2024 - Vietnix
     https://vietnix.vn/xu-huong-ai-2024/
     
     2. Trí tuệ nhân tạo - Wikipedia
     https://vi.wikipedia.org/wiki/Tr%C3%AD_tu%E1%BB%87_nh%C3%A2n_t%E1%BA%A1o
```

---

## ✅ Kế Hoạch Xác Minh

### Mục Tiêu Xác Minh

Đảm bảo các tính năng chính của OpenClaw hoạt động đúng như thiết kế và đáp ứng yêu cầu người dùng.

### Các Bước Xác Minh

| STT | Tính năng | Mô tả xác minh | Kết quả mong đợi |
|-----|-----------|----------------|------------------|
| 1 | Kết nối Telegram Bot | Bot phản hồi lệnh `/start` | Bot gửi tin nhắn chào mừng |
| 2 | Đọc Email | Kiểm tra kết nối IMAP và truy xuất email | Hiển thị nội dung email đầy đủ |
| 3 | Tóm Tắt Email | AI tóm tắt nội dung email | Trả về tóm tắt ngắn gọn, chính xác |
| 4 | Tìm Kiếm Web | Tìm kiếm với từ khóa thử nghiệm | Trả về kết quả phù hợp |
| 5 | Xử Lý Lỗi | Kiểm tra các trường hợp lỗi | Hiển thị thông báo lỗi thân thiện |

### Tiêu Chí Thành Công

- ✅ Bot Telegram hoạt động ổn định và phản hồi nhanh
- ✅ Tính năng đọc email hoạt động với ít nhất 1 nhà cung cấp email phổ biến
- ✅ Tóm tắt email cho kết quả chính xác trong vòng 5 giây
- ✅ Tìm kiếm web trả về kết quả liên quan đến từ khóa
- ✅ Xử lý lỗigraceful, không làm crash ứng dụng

---

## 🧪 Kiểm Tra Thủ Công

### Checklist Kiểm Tra Chi Tiết

#### 1. Kiểm Tra Kết Nối

- [ ] Bot Telegram kết nối thành công với API
- [ ] Bot phản hồi các lệnh cơ bản (`/start`, `/help`, `/status`)
- [ ] Kết nối email IMAP hoạt động ổn định

#### 2. Kiểm Tra Tính Năng Đọc Email

- [ ] Đọc danh sách email trong hộp thư
- [ ] Hiển thị thông tin người gửi, tiêu đề, ngày nhận
- [ ] Hiển thị nội dung email với định dạng đúng
- [ ] Xử lý đúng các email có file đính kèm

#### 3. Kiểm Tra Tính Năng Tóm Tắt Email

- [ ] AI phân tích nội dung email chính xác
- [ ] Tóm tắt ngắn gọn, dễ hiểu
- [ ] Xử lý được email dài (trên 1000 từ)
- [ ] Thời gian phản hồi dưới 10 giây

#### 4. Kiểm Tra Tính Năng Tìm Kiếm Web

- [ ] Tìm kiếm bằng tiếng Việt chính xác
- [ ] Tìm kiếm bằng tiếng Anh hoạt động
- [ ] Kết quả tìm kiếm có liên quan đến từ khóa
- [ ] Hiển thị đường dẫn và mô tả ngắn

#### 5. Kiểm Tra Xử Lý Lỗi

- [ ] Thông báo lỗi khi không có kết nối internet
- [ ] Thông báo lỗi khi đăng nhập email thất bại
- [ ] Thông báo lỗi khi không tìm thấy kết quả
- [ ] Bot không crash khi gặp lỗi

### Môi Trường Kiểm Thử

| Thành phần | Phiên bản | Ghi chú |
|------------|-----------|---------|
| Python | 3.8+ | Môi trường phát triển |
| Telegram | Phiên bản mới nhất | Sử dụng ứng dụng di động hoặc desktop |
| Gmail | - | Tài khoản test có sẵn |
| OpenAI API | GPT-4 | Sử dụng API key hợp lệ |

---

## 📝 Ghi Chú Bổ Sung

### Bảo Mật

- Luôn bảo mật thông tin đăng nhập email và API keys
- Sử dụng mã hóa khi truyền dữ liệu nhạy cảm
- Không lưu trữ thông tin cá nhân của người dùng

### Giới Hạn

- Giới hạn số lượng email đọc trong một lần: 10 email
- Giới hạn độ dài nội dung tóm tắt: 500 ký tự
- Giới hạn kết quả tìm kiếm: 5 kết quả

### Hỗ Trợ

Nếu gặp vấn đề hoặc cần hỗ trợ, vui lòng tạo issue trên repository hoặc liên hệ qua Telegram.

---

## 📄 Giấy Phép

Dự án này được phát hành theo giấy phép MIT. Xem file `LICENSE` để biết thêm chi tiết.

---

<p align="center">
  <sub>© 2024 OpenClaw. Được phát triển với ❤️ bằng Python và AI.</sub>
</p>
