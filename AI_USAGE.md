# AI Usage Log

## 1. Công cụ AI
Tên công cụ: ChatGPT (OpenAI) & Antigravity Assistant (Google)

## 2. Mục đích sử dụng
- Hỗ trợ phân tích nghiệp vụ và thiết kế trải nghiệm người dùng (UX) cho website TMĐT VinFast Auto.
- Khảo sát chuyên sâu 5 khu vực chức năng: Trang chủ, Danh mục xe điện, Chi tiết cấu hình xe, Tìm kiếm & Trạm sạc, Giỏ hàng & Đặt cọc.
- Đề xuất giải pháp mã nguồn HTML5 và CSS3 cải tiến thẻ sản phẩm xe điện.

## 3. Prompt đã sử dụng
> "Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng cho website thương mại điện tử. Tôi đang khảo sát website: VinFast Auto (https://shop.vinfastauto.com). Hãy giúp tôi lập bảng phân tích các khu vực: 1. Trang chủ, 2. Danh mục sản phẩm (các dòng xe điện), 3. Chi tiết sản phẩm và cấu hình xe, 4. Tìm kiếm và mạng lưới dịch vụ, 5. Giỏ hàng và đặt cọc trực tuyến. Với mỗi khu vực hãy nêu: Mục đích chức năng, Thành phần giao diện cần có, Điểm thuận tiện, Một vấn đề có thể phát sinh, Một đề xuất cải tiến. Không khẳng định những tính năng chưa được kiểm chứng. Phân biệt rõ nhận xét dựa trên quan sát và đề xuất của AI."

## 4. Kết quả AI đề xuất
- AI lập bảng phân tích chi tiết 5 khu vực, phân tách giữa "Quan sát thực tế" và "Đề xuất cải tiến của AI".
- AI nhận diện được quy trình cọc xe 3 bước của VinFast qua cổng OnePay/chuyển khoản và rào cản tâm lý từ điều khoản cọc không hoàn lại.
- AI đề xuất thứ tự ưu tiên: Ưu tiên cao nhất cho việc minh bạch giá, khoản đặt cọc và tóm tắt cấu hình xe trước khi thanh toán.

## 5. Kiểm tra và điều chỉnh (Đối chiếu thực tế)
- **Phát hiện ảo giác AI (Hallucination) và loại bỏ:** 
  + Trong mục Danh mục xe, ChatGPT đã tự bịa ra dòng xe ô tô **"VF 2"** (`...các mẫu như VF 2, VF 3, VF 5...`). Sau khi kiểm tra trực tiếp danh mục thực tế của VinFast, tôi xác nhận VinFast hoàn toàn không có mẫu xe nào tên là VF 2 (dải xe bắt đầu từ VF 3). Tôi đã loại bỏ hoàn toàn thông tin sai lệch này khỏi bài báo cáo.
  + AI đề xuất tạo mới công cụ so sánh 3 xe; tuy nhiên kiểm tra thực tế cho thấy VinFast đã có sẵn trang so sánh (`/so-sanh-xe`), chỉ là công cụ này bị giấu sâu và chưa tối ưu giao diện cuộn ngang trên điện thoại.
- **Bổ sung nhận xét của bản thân:**
  + Vấn đề lớn nhất trên mobile của trang danh mục VinFast là ảnh xe chiếm trọn màn hình nhưng thiếu hẳn thông số quan trọng (km/lần sạc, công suất, thời gian sạc). Người dùng buộc phải bấm vào từng trang con rồi bấm quay lại, rất mất thời gian.
  + Thêm vào bài toán phân định rõ ràng giữa "Giá mua pin" và "Chi phí thuê pin hàng tháng" kèm số tiền cọc ban đầu (15 - 50 triệu) để khách hàng an tâm ra quyết định.
- **Tự điều chỉnh mã nguồn:** Khi kiểm tra file giao diện bằng Chrome DevTools trên màn hình điện thoại (375px - 414px), bố cục 2 cột ban đầu khiến 3 ô thông số `ev-specs` bị tràn lề ngang và chữ bị đè lên nhau. Tôi đã chỉnh sửa CSS media query thành `grid-template-columns: 1fr` trên màn hình dưới 640px, chuyển các thẻ xe sang dạng khối dọc hiển thị đầy đủ, thoáng mắt.

## 6. Phần tôi hiểu và có thể giải thích
- Hiểu cấu trúc thẻ ngữ nghĩa HTML5: `<article>` dùng cho từng thẻ xe độc lập, `<section>` phân chia khu vực showroom, `<header>` và `<footer>`.
- Hiểu kỹ thuật CSS Grid và Flexbox kết hợp: Grid ngoài chia cột xe, Flexbox bên trong định vị giá và nút cọc sát đáy (`margin-top: auto`).
- Nắm vững vai trò của Media Query trong việc tối ưu hóa trải nghiệm người dùng đa thiết bị (Desktop vs Mobile).
- Nắm được phương pháp luận sử dụng AI có trách nhiệm: Luôn kiểm chứng chéo với thực tế để loại bỏ ảo giác dữ liệu trước khi đưa vào sản phẩm.
