# 🍱 Use Case Chi tiết: Đặt hàng (Place Order)

## 🧾 Tên Use Case
**Đặt hàng (Place Order)**

## Actor

| **Tên Actor** | **Vai trò** |
|----------------|--------------|
| **Khách hàng** | Primary Actor – người thực hiện hành động đặt món ăn |
| **Hệ thống giao đồ ăn** | Thực thi, xử lý và lưu thông tin đơn hàng |
| **Nhà hàng / Cửa hàng** | Xác nhận và chuẩn bị món ăn |
| **Hệ thống Thanh toán** | Xử lý giao dịch thanh toán trực tuyến |



## 🔄 Luồng chính

| **Bước** | **Mô tả hành động** |
|-----------|----------------------|
| 1 | Khách hàng đăng nhập vào ứng dụng. |
| 2 | Khách hàng tìm kiếm món ăn hoặc nhà hàng mong muốn. |
| 3 | Khách hàng chọn món ăn và thêm vào giỏ hàng. |
| 4 | Khách hàng xem giỏ hàng, kiểm tra số lượng và tổng tiền. |
| 5 | Khách hàng xác nhận đặt hàng. |
| 6 | Hệ thống gửi yêu cầu đơn hàng đến **nhà hàng**. |
| 7 | **Nhà hàng** xác nhận đơn và bắt đầu chuẩn bị món. |
| 8 | Hệ thống yêu cầu khách hàng chọn phương thức thanh toán. |
| 9 | **Hệ thống thanh toán** xử lý giao dịch. |
| 10 | Hệ thống hiển thị thông báo **“Đặt hàng thành công”** và tạo mã đơn hàng. |

---

## ⚠️ Luồng lỗi

| **Tình huống lỗi** | **Hành động của hệ thống / Ứng xử** |
|--------------------|--------------------------------------|
| Món ăn đã hết hàng | Hệ thống thông báo món không còn, gợi ý món tương tự. |
| Kết nối mạng bị gián đoạn | Hệ thống lưu trạng thái tạm thời và yêu cầu người dùng thử lại. |
| Thanh toán thất bại | Hệ thống hiển thị thông báo lỗi, cho phép người dùng chọn phương thức khác. |
| Nhà hàng không phản hồi | Hệ thống hủy đơn hàng sau thời gian chờ, gửi thông báo đến khách hàng. |
