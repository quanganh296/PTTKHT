"""# 1. Nhận biết loại hệ thống thông tin phù hợp

---

Dựa trên mô tả nghiệp vụ của hệ thống quản lý giao hàng online, ta xác định các loại hệ thống thông tin phù hợp như sau:

## a. TPS – Transaction Processing System (Hệ thống xử lý giao dịch)

**Phù hợp vì:**
- Hệ thống phải tiếp nhận và cập nhật các đơn hàng liên tục.
- Theo dõi trạng thái đơn hàng theo thời gian thực.
- Lưu trữ thông tin từng giao dịch giao hàng.

**➡ TPS là lớp hệ thống cốt lõi bắt buộc.**

---

## b. MIS – Management Information System (Hệ thống thông tin quản lý)

**Phù hợp vì:**
- Cung cấp báo cáo tổng hợp về số lượng đơn, trạng thái giao hàng.
- Hỗ trợ quản lý theo dõi hiệu suất giao hàng.

**➡ MIS phục vụ quản lý cấp trung.**

---

## c. DSS – Decision Support System (Hệ thống hỗ trợ ra quyết định)

**Phù hợp vì:**
- Phân tích tuyến đường tối ưu.
- Gợi ý tài xế phù hợp, tuyến đường nhanh nhất.
- Hỗ trợ các quyết định chiến lược vận hành logistics.

**➡ DSS phù hợp với bài toán “phân tích tuyến đường và lập kế hoạch vận chuyển”.**

---

# 2. Mô hình phát triển phần mềm phù hợp

---

## a. Agile (Scrum) – Khuyến nghị

**Lý do nên chọn:**
- Yêu cầu thay đổi liên tục từ doanh nghiệp.
- Nhiều tính năng cần mở rộng (GPS, phân tích dữ liệu, tích hợp API).
- Cần phản hồi nhanh theo tình hình vận hành.

**➡ Agile phù hợp nhất.**

---

## b. Waterfall – Ít khuyến nghị

Chỉ phù hợp khi:
- Yêu cầu rõ ràng ngay từ đầu.
- Ít thay đổi.

**➡ Không phù hợp với hệ thống logistics thực tế.**

---

# 3. Kết luận

---

| Thành phần | Lựa chọn phù hợp | Giải thích |
|-----------|------------------|-------------|
| **Loại hệ thống thông tin** | TPS | Xử lý giao dịch đơn hàng |
| | MIS | Báo cáo, tổng hợp dữ liệu |
| | DSS | Phân tích tuyến đường, tối ưu hóa |
| **Mô hình phát triển** | Agile | Linh hoạt, dễ mở rộng, phù hợp thay đổi thường xuyên |

"""