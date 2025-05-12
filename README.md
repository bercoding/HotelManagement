# Hệ Thống Quản Lý Khách Sạn (Hotel Management System)

Hệ thống quản lý khách sạn toàn diện được xây dựng với Node.js, Express và MongoDB, cung cấp các giải pháp quản lý phòng, đặt phòng, và dịch vụ khách hàng.

## Tính Năng

- **Quản lý người dùng**: Đăng ký, đăng nhập, phân quyền (Admin, Nhân viên, Khách hàng)
- **Quản lý phòng**: Thêm, sửa, xóa, xem danh sách phòng
- **Đặt phòng**: Tìm kiếm phòng trống, đặt phòng, hủy đặt phòng
- **Thanh toán**: Tích hợp Stripe để xử lý thanh toán trực tuyến
- **Quản lý dịch vụ**: Đặt dịch vụ bổ sung cho khách hàng
- **Quản trị viên**: Bảng điều khiển admin với thống kê và quản lý hệ thống
- **API**: RESTful API cho tích hợp với các dịch vụ bên ngoài

## Công Nghệ Sử Dụng

- **Backend**: Node.js, Express.js
- **Database**: MongoDB với Mongoose
- **Frontend**: EJS, CSS, JavaScript
- **Xác thực**: JWT, express-session, bcrypt
- **Thanh toán**: Stripe API
- **Email**: Nodemailer
- **Khác**: Moment.js, Connect-flash, Method-override

## Cài Đặt

### Yêu Cầu
- Node.js (v14 trở lên)
- MongoDB
- npm hoặc yarn

### Các Bước Cài Đặt

1. Clone repository
   ```
   git clone https://your-repository-url.git
   cd hotel-management-system
   ```

2. Cài đặt các phụ thuộc
   ```
   npm install
   ```

3. Tạo file .env và thiết lập các biến môi trường
   ```
   PORT=5010
   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   SESSION_SECRET=your_session_secret
   STRIPE_SECRET_KEY=your_stripe_secret_key
   EMAIL_USER=your_email
   EMAIL_PASS=your_email_password
   ```

4. Chạy ứng dụng
   ```
   npm run dev    # Chế độ phát triển với nodemon
   npm start      # Chế độ sản phẩm
   ```

5. Truy cập ứng dụng tại `http://localhost:5010`

## Cấu Trúc Dự Án

```
|-- config/           # Cấu hình database và các biến môi trường
|-- controllers/      # Xử lý logic nghiệp vụ
|-- middleware/       # Middleware xác thực và phân quyền
|-- models/           # Mô hình dữ liệu MongoDB
|-- public/           # Tài nguyên tĩnh (CSS, JS, hình ảnh)
|-- routes/           # Định nghĩa các route
|-- services/         # Các dịch vụ nghiệp vụ
|-- utils/            # Tiện ích và hàm hỗ trợ
|-- views/            # Template EJS
|-- app.js            # Điểm khởi đầu ứng dụng
|-- package.json      # Quản lý phụ thuộc
```

## Mô Hình Dữ Liệu

- **User**: Quản lý thông tin người dùng, phân quyền
- **Room**: Thông tin về phòng, loại phòng, giá cả, tình trạng
- **Booking**: Quản lý thông tin đặt phòng
- **ServiceRequest**: Yêu cầu dịch vụ từ khách hàng

## Hướng Dẫn Sử Dụng

### Dành Cho Người Dùng
- Đăng ký tài khoản và đăng nhập
- Tìm kiếm và đặt phòng
- Yêu cầu dịch vụ bổ sung
- Xem lịch sử đặt phòng và thanh toán

### Dành Cho Admin
- Quản lý người dùng
- Thêm/sửa/xóa phòng
- Xem và xác nhận đặt phòng
- Quản lý dịch vụ
- Xem báo cáo doanh thu

## Đóng Góp

Vui lòng đọc [CONTRIBUTING.md](CONTRIBUTING.md) để biết chi tiết về quy trình gửi pull request.

## Giấy Phép

Dự án này được cấp phép theo giấy phép ISC - xem file [LICENSE](LICENSE) để biết thêm chi tiết.

## Liên Hệ

Nếu có bất kỳ câu hỏi hoặc đề xuất, vui lòng liên hệ với chúng tôi qua email: [your-email@example.com] 