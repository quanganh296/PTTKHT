# Kiến trúc hệ thống bán lẻ tích hợp External Service

## 1️⃣ Mô tả nghiệp vụ

Hệ thống bán lẻ thực hiện các chức năng chính:

- **Quản lý tồn kho**: Theo dõi số lượng sản phẩm trong kho và tình trạng tồn kho.  
- **Thanh toán online**: Cho phép khách hàng thanh toán qua VNPay.  
- **Gửi email xác nhận**: Hệ thống tự động gửi email xác nhận sau khi thanh toán thành công, sử dụng dịch vụ SMTP.  

Hệ thống cần tích hợp các **dịch vụ ngoài** (External Service) như VNPay và SMTP để thực hiện thanh toán và gửi email.

---

## 2️⃣ Các thành phần chính và dịch vụ tích hợp

| Thành phần | Vai trò |
|------------|--------|
| **Presentation Layer** | Giao diện người dùng, cho phép khách hàng chọn sản phẩm, thêm vào giỏ hàng và thanh toán. |
| **Business Logic Layer** | Xử lý các nghiệp vụ: quản lý đơn hàng, kiểm tra tồn kho, tính toán tổng tiền, gọi các dịch vụ thanh toán và gửi email. |
| **Data Access Layer** | Truy xuất dữ liệu: sản phẩm, đơn hàng, khách hàng. Thực hiện các phương thức CRUD. |
| **VNPay Service (External)** | Thực hiện thanh toán online, trả kết quả giao dịch cho hệ thống. |
| **SMTP Service (External)** | Gửi email xác nhận tới khách hàng sau khi thanh toán thành công. |
