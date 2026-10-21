# E-commerce UI Improvement - High-Ticket EV Store

## 1. Giới thiệu
Dự án nghiên cứu và cải tiến giao diện thương mại điện tử giá trị cao (High-Ticket E-commerce) cho ngành công nghiệp ô tô điện thông minh, tập trung giải quyết bài toán hiển thị thông số pin, lựa chọn màu sơn và tối ưu quy trình đặt cọc giữ xe trực tuyến tại Việt Nam.

## 2. Website tham khảo
- Tên website: VinFast Auto Vietnam
- URL: https://vinfastauto.com/vn_vi (Hệ thống cổng thông tin & đặt cọc ô tô điện trực tuyến chính thức của VinFast tại Việt Nam)
- Khu vực đã khảo sát: Trang chủ, Danh mục xe điện, Chi tiết cấu hình xe (Configurator), Bản đồ trạm sạc & Dịch vụ, Giỏ cọc và thanh toán trực tuyến.

## 3. Chức năng
- Danh sách sản phẩm xe điện hiện đại theo phong cách Cyber Dark Theme.
- Tích hợp cụm thông số kỹ thuật cốt lõi của xe điện: Tầm hoạt động (km/lần sạc), công suất động cơ, thời gian sạc nhanh.
- Bảng màu sơn nhanh (Color palette swatches) giúp khách hàng dễ hình dung ngoại thất.
- Minh bạch phương án giá: Giá mua đứt kèm pin song song với chi phí thuê pin hoặc trả góp hàng tháng.
- Nút kêu gọi hành động đặt cọc số tiền nhỏ (15–50 triệu) rõ ràng, tăng tỷ lệ hoàn tất giao dịch.

## 4. Công nghệ
- HTML5 (Cấu trúc ngữ nghĩa chuẩn SEO: header, main, section, article, footer)
- CSS3 (CSS Grid, Flexbox, Dark Mode theme, Media Queries Responsive)

## 5. Cách chạy
- Mở trực tiếp file `index.html` bằng trình duyệt Google Chrome hoặc Edge.
- Xem trực tiếp thông qua đường dẫn GitHub Pages công khai.

## 6. Cải tiến đã thực hiện
- **Vấn đề ban đầu trên website tham khảo:** Trên thiết bị di động của trang danh mục xe `vinfastauto.com/vn_vi`, mỗi dòng xe chiếm diện tích cuộn quá lớn nhưng lại thiếu các thông số kỹ thuật cốt lõi (Quãng đường di chuyển/lần sạc, thời gian sạc, công suất). Người dùng muốn so sánh giữa các dòng xe bắt buộc phải bấm vào từng trang chi tiết con rồi back quay lại, gây mất thời gian và khó đối chiếu.
- **Thay đổi đã thực hiện:**
  + Đưa trực tiếp bộ 3 thông số vàng (Quãng đường, Mã lực, Thời gian sạc) lên ngay thẻ sản phẩm bên ngoài.
  + Thêm bộ chọn chấm màu ngoại thất trực quan.
  + Phân biệt rõ số tiền cọc (15tr - 30tr - 50tr) để người mua không bị nhầm lẫn với tổng giá trị tiền tỷ của chiếc xe.
  + Tự điều chỉnh Responsive 1 cột trên màn hình điện thoại dưới 640px để tránh vỡ khối thông số pin.

## 7. Hỗ trợ từ AI
- AI hỗ trợ: Gợi ý khung phân tích 5 khu vực TMĐT xe hơi; đề xuất cấu trúc bảng thông số kỹ thuật trong thẻ sản phẩm bằng CSS Grid.
- Bản thân kiểm tra & điều chỉnh: Trực tiếp vào `https://vinfastauto.com/vn_vi` để đối chiếu số liệu thật của các dòng VF 3, VF 6, VF 7, VF 9; loại bỏ ảo giác của AI (như việc AI tự tạo dòng xe "VF 2"); tự viết lại CSS Responsive trên mobile để thông số không bị chèn chữ; loại bỏ các script thừa để mã nguồn thuần túy nhẹ nhất.
