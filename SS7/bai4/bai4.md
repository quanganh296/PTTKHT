# Thiết kế Class – Tầng Business & Data

## 1️⃣ Mô tả

Hệ thống bán hàng online có các lớp chính:

- **OrderService (Business Layer)**  
  Chứa các nghiệp vụ liên quan đến đơn hàng:
  - `createOrder(orderData)`: Tạo mới đơn hàng, kiểm tra tồn kho, áp dụng khuyến mãi.  
  - `updateOrderStatus(orderId, status)`: Cập nhật trạng thái đơn hàng (chờ xử lý, đã giao, hủy…).  
  - `calculateTotal(orderId)`: Tính tổng tiền đơn hàng, bao gồm thuế và giảm giá.  

- **OrderRepository (Data Layer)**  
  Chứa các phương thức truy xuất dữ liệu:
  - `add(order)`: Thêm đơn hàng vào cơ sở dữ liệu.  
  - `update(order)`: Cập nhật thông tin đơn hàng.  
  - `delete(orderId)`: Xóa đơn hàng theo ID.  
  - `getById(orderId)`: Lấy thông tin đơn hàng theo ID.  
  - `getAll()`: Lấy danh sách tất cả đơn hàng.  

---

## OrderService (Business Layer)
- Chỉ xử lý logic nghiệp vụ, không thao tác trực tiếp với cơ sở dữ liệu.  
- Gọi các phương thức của `OrderRepository` để lưu/truy xuất dữ liệu.  
- Các method chính:
  - `createOrder(orderData)`: Tạo đơn hàng mới, kiểm tra tồn kho, áp dụng khuyến mãi.  
  - `updateOrderStatus(orderId, status)`: Cập nhật trạng thái đơn hàng.  
  - `calculateTotal(orderId)`: Tính tổng tiền đơn hàng, bao gồm thuế và giảm giá.

## OrderRepository (Data Layer)
- Thao tác trực tiếp với cơ sở dữ liệu (CRUD).  
- Không chứa logic nghiệp vụ để đảm bảo **Separation of Concerns**.  
- Các method chính:
  - `add(order)`: Thêm đơn hàng vào cơ sở dữ liệu.  
  - `update(order)`: Cập nhật thông tin đơn hàng.  
  - `delete(orderId)`: Xóa đơn hàng theo ID.  
  - `getById(orderId)`: Lấy thông tin đơn hàng theo ID.  
  - `getAll()`: Lấy danh sách tất cả đơn hàng.

## Mối quan hệ
- `OrderService` phụ thuộc vào `OrderRepository`.  
- Việc tách biệt giúp dễ dàng bảo trì, mở rộng và kiểm thử.  
