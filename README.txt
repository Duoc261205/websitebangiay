
# ShoeStore (PHP + MySQL)

## Cách chạy (USBWebserver, XAMPP, WAMP đều được)
1) Mở phpMyAdmin và import file `schema.sql` để tạo CSDL + dữ liệu mẫu.
2) Chép cả thư mục `shoe_store` vào thư mục webroot của bạn:
   - USBWebserver: `USBWebserver root/`
   - XAMPP: `xampp/htdocs/`
3) Truy cập: `http://localhost/shoe_store/`

## Tài khoản quản trị
- Mặc định chưa có admin. Hãy tạo tài khoản ở trang Đăng ký, rồi vào phpMyAdmin chạy:
  ```sql
  UPDATE users SET role='admin' WHERE email='EMAIL_VUA_DANG_KY';
  ```
  Sau đó đăng nhập và vào `/shoe_store/admin/` để quản lý sản phẩm.

## Tính năng
- Xem sản phẩm, tìm kiếm
- Chi tiết sản phẩm
- Giỏ hàng (session)
- Đăng ký / Đăng nhập / Đăng xuất
- Thanh toán -> lưu đơn hàng, danh sách items
- Trang quản trị: thêm/sửa/xóa sản phẩm (+ upload ảnh)

> Demo này chú trọng đơn giản, bảo mật cơ bản (prepared statements). Khi triển khai thực tế, dùng HTTPS, CSRF token, kiểm tra file upload chặt chẽ hơn.
