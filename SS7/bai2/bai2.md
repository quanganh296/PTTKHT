# Kiến trúc 3-tier trong Hệ thống Quản lý Kho

## 1️⃣ Các tầng trong kiến trúc 3-tier

| Tầng | Vai trò và chức năng |
|------|--------------------|
| **Presentation Tier (Giao diện)** | Tầng tương tác với người dùng: Web hoặc Mobile. Hiển thị danh sách sản phẩm, thông tin nhà cung cấp, form nhập xuất kho, báo cáo tồn kho. Gửi yêu cầu tới Business Logic Tier. |
| **Business Logic Tier (Logic nghiệp vụ)** | Xử lý các nghiệp vụ: quản lý sản phẩm, quản lý nhà cung cấp, theo dõi nhập/xuất kho, tính toán tồn kho, kiểm tra tồn kho trước khi xuất hàng. |
| **Data Access Tier (CSDL / Data Layer)** | Lưu trữ dữ liệu: bảng sản phẩm, bảng nhà cung cấp, bảng nhập/xuất kho. Cung cấp API CRUD cho tầng Business Logic. |

## 2️⃣ Giải thích logic phân tầng

### Presentation Tier
- Tương tác trực tiếp với người dùng.
- Hiển thị dữ liệu và nhận thao tác như thêm/sửa/xóa sản phẩm, tạo đơn nhập/xuất kho.
- Gọi các phương thức từ **Business Logic Tier** để thực hiện nghiệp vụ.

### Business Logic Tier
- Xử lý các nghiệp vụ:
  - **Quản lý sản phẩm:** thêm, sửa, xóa, tìm kiếm.
  - **Quản lý nhà cung cấp:** lưu trữ thông tin, theo dõi đơn hàng từ nhà cung cấp.
  - **Nhập – Xuất kho:** kiểm tra tồn kho, ghi nhận số lượng nhập/xuất, tính toán tồn kho hiện tại.
- Giao tiếp với **Data Access Tier** để đọc/ghi dữ liệu.

### Data Access Tier
- Lưu trữ tất cả dữ liệu: sản phẩm, nhà cung cấp, đơn nhập/xuất kho.
- Cung cấp các phương thức **CRUD** (Create, Read, Update, Delete) cho tầng **Business Logic Tier**.
