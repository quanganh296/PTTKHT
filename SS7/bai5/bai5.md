# Phân chia hệ thống Blog cá nhân theo kiến trúc 3 tầng

## 1️⃣ Mô tả nghiệp vụ

Hệ thống blog cá nhân bao gồm các chức năng chính:

- **Viết bài**: Người dùng có thể tạo, chỉnh sửa và đăng bài viết lên blog.  
- **Đọc bài**: Người dùng có thể xem các bài viết đã đăng.  
- **Quản lý bình luận**: Thêm, chỉnh sửa, xóa bình luận cho mỗi bài viết.  
- **Quản lý người dùng**: Đăng ký, đăng nhập và phân quyền người dùng.  

---

## 2️⃣ Phân rã hệ thống theo kiến trúc 3 tầng

| Tầng | Module chính | Vai trò |
|------|---------------|--------|
| **Presentation Tier** | - Giao diện người dùng (Web/Mobile) | Hiển thị danh sách bài viết, form viết bài, form đăng nhập, hiển thị bình luận. Gửi yêu cầu đến Business Logic. |
| **Business Logic Tier** | - PostService (quản lý bài viết)<br>- CommentService (quản lý bình luận)<br>- UserService (quản lý người dùng) | Xử lý nghiệp vụ: thêm/sửa/xóa bài viết, quản lý bình luận, xác thực và phân quyền người dùng. Gọi Data Access để thao tác dữ liệu. |
| **Data Access Tier** | - PostRepository<br>- CommentRepository<br>- UserRepository | Lưu trữ và truy xuất dữ liệu từ cơ sở dữ liệu: bảng bài viết, bình luận, người dùng. Cung cấp các phương thức CRUD. |

---