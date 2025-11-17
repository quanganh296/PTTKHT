# Hệ thống quản lý bán hàng đa nền tảng

---

## 1. Các thành phần chính của hệ thống

| Thành phần           | Mô tả ngắn gọn |
|----------------------|----------------|
| **Frontend**         | Giao diện người dùng trên **Web** (trình duyệt) và **Mobile** (ứng dụng iOS/Android). Chịu trách nhiệm hiển thị sản phẩm, giỏ hàng, thanh toán và thông tin cá nhân. |
| **Backend / API**    | Xử lý **logic nghiệp vụ**, bao gồm: tìm kiếm sản phẩm, quản lý giỏ hàng, xử lý đơn hàng, xác thực người dùng, tích hợp với các dịch vụ bên ngoài. Exposed qua API để Frontend gọi. |
| **Database**         | Lưu trữ dữ liệu hệ thống: thông tin sản phẩm, người dùng, đơn hàng, giỏ hàng, lịch sử thanh toán, v.v. |
| **External Services**| Các dịch vụ bên ngoài: <br>• Thanh toán (VNPay, PayPal, Stripe…) <br>• Giao vận (GHTK, GrabExpress…) <br>• Email / Notification (SendGrid, Firebase Cloud Messaging…) |

---

## 3. Giải thích sơ đồ kiến trúc tổng thể

1. **Frontend (Web + Mobile)**:  
   - Tương tác trực tiếp với người dùng.  
   - Gửi yêu cầu qua **API** tới Backend.  

2. **Backend / API**:  
   - Chịu trách nhiệm **xử lý nghiệp vụ**, xác thực, và kết nối dữ liệu giữa Frontend, Database, và External Services.  

3. **Database**:  
   - Lưu trữ tất cả dữ liệu hệ thống một cách tập trung.  
   - Backend đọc/ghi dữ liệu theo nghiệp vụ.  

4. **External Services**:  
   - Hỗ trợ thanh toán, giao vận, thông báo, gửi email, v.v.  
   - Backend gọi các API của dịch vụ này để thực hiện nghiệp vụ tương ứng.
