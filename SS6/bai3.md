# Phân tích Stakeholders và Yêu cầu – Hệ thống E-learning

## 1. Danh sách Stakeholders

| Stakeholder | Vai trò / Lợi ích | Nguồn yêu cầu |
|-------------|-------------------|----------------|
| Học viên (Student) | Mua khóa học, xem bài giảng, làm bài tập, theo dõi tiến độ | Nhu cầu học tập & sử dụng |
| Giảng viên (Instructor) | Tạo khóa học, upload bài giảng, quản lý học viên tham gia | Quy trình giảng dạy |
| Quản trị hệ thống (Admin) | Quản lý người dùng, khóa học, doanh thu, bảo mật hệ thống | Vận hành & quản trị |
| Bộ phận hỗ trợ (Support) | Tiếp nhận phản hồi, hỗ trợ kỹ thuật cho học viên & giảng viên | Dịch vụ hỗ trợ |
| Bộ phận tài chính | Theo dõi doanh thu, hóa đơn, đối soát thanh toán | Quy trình tài chính |
| Đối tác thanh toán | Xử lý giao dịch thanh toán | Tích hợp cổng thanh toán |
| Cơ quan quản lý nội dung | Kiểm duyệt nội dung, bản quyền | Quy định pháp lý |

---

## 2. Yêu cầu chức năng (Functional Requirements)

### FR1 – Quản lý tài khoản
- Đăng ký, đăng nhập, đặt lại mật khẩu.
- Cập nhật thông tin cá nhân.

### FR2 – Quản lý khóa học
- Giảng viên tạo khóa học, chỉnh sửa, xóa.
- Upload video, tài liệu PDF, bài quiz.
- Admin phê duyệt khóa học.

### FR3 – Mua và thanh toán khóa học
- Học viên mua khóa học.
- Thanh toán qua VNPay, Momo, Visa/Master.
- Xuất hóa đơn điện tử.

### FR4 – Học trực tuyến
- Xem video bài giảng.
- Đánh dấu bài đã xem.
- Làm bài kiểm tra.
- Theo dõi tiến độ.

### FR5 – Quản lý lớp học
- Giảng viên xem danh sách học viên.
- Gửi thông báo cho học viên.

### FR6 – Bình luận & đánh giá
- Học viên đánh giá khóa học.
- Giảng viên phản hồi.

### FR7 – Báo cáo & thống kê
- Admin xem doanh thu theo thời gian.
- Giảng viên xem số học viên.

### FR8 – Hỗ trợ người dùng
- Học viên gửi ticket hỗ trợ.
- Bộ phận support xử lý ticket.

---

## 3. Yêu cầu phi chức năng (Non-functional Requirements)

### NFR1 – Hiệu năng
- Hỗ trợ 5000 người truy cập đồng thời.
- Trang tải trong ≤ 3 giây.

### NFR2 – Bảo mật
- Mã hóa mật khẩu.
- Sử dụng HTTPS/TLS.
- Phân quyền truy cập.

### NFR3 – Khả năng mở rộng
- Thêm khóa học, giảng viên không giới hạn.
- Hỗ trợ video lớn qua CDN.

### NFR4 – Ổn định
- Uptime 99.5%.
- Sao lưu hằng ngày.

### NFR5 – Khả dụng
- UI dễ dùng.
- Hỗ trợ Web – Mobile.

### NFR6 – Tương thích
- Chrome, Safari, Edge, Firefox.
- Windows, macOS, Android, iOS.

### NFR7 – Bảo trì
- Kiến trúc mô-đun.
- Cập nhật không mất dữ liệu.
