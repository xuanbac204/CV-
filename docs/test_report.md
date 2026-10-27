# Báo cáo kiểm thử — CV Portfolio

## 1. Thông tin kiểm thử

- **Dự án:** CV Portfolio - Lương Xuân Bắc
- **Ngày kiểm thử:** 27/10/2026
- **Phạm vi:** Mở trang bằng trình duyệt tích hợp qua `file://`, kiểm tra nội dung DOM, tài nguyên ảnh, điều hướng nội bộ và rà soát mã HTML/CSS.
- **Lưu ý:** Đây là kiểm thử thủ công và kiểm tra tĩnh có giới hạn; không thay thế kiểm thử tự động, kiểm thử bảo mật chuyên sâu hay kiểm thử trên môi trường hosting thực tế.

## 2. Tổng quan kết quả

| Tiêu chí | Kết quả | Tóm tắt |
|---|---|---|
| Tính đúng đắn | Đạt một phần | Trang, các mục chính, thẻ dự án và ảnh hiển thị; một số liên kết vẫn là `#`. |
| UI/UX | Đạt một phần | Giao diện desktop hiển thị; chưa xác nhận được bố cục mobile bằng viewport kiểm thử đáng tin cậy. |
| Khả năng vận hành - xử lí lỗi | Chưa đánh giá đầy đủ | Mở trang tĩnh thành công; không có luồng dữ liệu động hoặc xử lý lỗi để kiểm thử. |
| Bảo mật | Rủi ro bề mặt thấp trong phạm vi đã kiểm tra | Không thấy JavaScript, biểu mẫu hay đầu vào người dùng; chưa thực hiện kiểm thử xâm nhập hoặc kiểm tra hosting. |
| Chất lượng mã nguồn | Đạt một phần | HTML/CSS được tách riêng và có cấu trúc; còn một số chi tiết markup và liên kết cần hoàn thiện. |
| Khả năng triển khai | Đạt một phần | Có thể mở trực tiếp như website tĩnh; chưa xác minh máy chủ local hoặc triển khai production. |

## 3. Kết quả theo tiêu chí

### 3.1. Tính đúng đắn

- **Kiểm tra:** Mở `index.html`; xác nhận tiêu đề trang, các section `about`, `skills`, `projects`, `contact`, số lượng thẻ dự án, CSS và trạng thái tải ảnh; thử điều hướng tới mục Dự án.
- **Kết quả:** Trang mở được; tìm thấy đủ bốn section và bốn thẻ dự án; CSS được nạp; không có ảnh bị lỗi tải trong lần kiểm tra; điều hướng nội bộ tới `#projects` hoạt động.
- **Đánh giá:** **Đạt một phần.** Bốn liên kết “Xem chi tiết” và hai liên kết GitHub/LinkedIn hiện trỏ tới `#`, nên chưa dẫn tới đích mong muốn.
- **Minh chứng giao diện:** [Ảnh chụp toàn trang desktop](./screenshots/desktop.png), [ảnh chụp khu vực Liên hệ](./screenshots/contact.png).

### 3.2. UI/UX

- **Kiểm tra:** Quan sát bố cục, nội dung, điều hướng, thẻ dự án và khu vực liên hệ trên ảnh chụp desktop; kiểm tra CSS có breakpoint tablet `768px` và desktop `1280px`.
- **Kết quả:** Các khu vực nội dung và điều hướng hiện diện; giao diện desktop được hiển thị trong ảnh chụp. CSS khai báo các breakpoint responsive.
- **Giới hạn:** Chưa xác nhận được giao diện ở kích thước mobile. Dù đã thử đặt viewport nhỏ, trình duyệt báo `innerWidth` là `1227px`; kết quả đó không đủ tin cậy để kết luận bố cục mobile đạt hay không đạt.
- **Đánh giá:** **Đạt một phần; cần kiểm thử lại trên thiết bị hoặc viewport mobile thực.**
- **Minh chứng:** [Ảnh chụp toàn trang desktop](./screenshots/desktop.png).

### 3.3. Khả năng vận hành - xử lí lỗi

- **Kiểm tra:** Mở trang trực tiếp từ file local và kiểm tra tài nguyên hiển thị.
- **Kết quả:** Trang mở được, stylesheet được tải và các ảnh trong trang tải thành công ở lần kiểm tra.
- **Giới hạn:** Website hiện là trang tĩnh, không có JavaScript, biểu mẫu, API hay xử lý dữ liệu để kiểm tra các tình huống lỗi nghiệp vụ, lỗi mạng hoặc phục hồi sau lỗi. Chưa chạy website qua máy chủ HTTP.
- **Đánh giá:** **Chưa đánh giá đầy đủ.** Kết quả chỉ xác nhận khả năng mở trang local và tải tài nguyên trong phiên kiểm thử này.
- **Minh chứng:** [Ảnh chụp toàn trang desktop](./screenshots/desktop.png).

### 3.4. Bảo mật

- **Kiểm tra:** Rà soát mã trang để tìm script, biểu mẫu và bề mặt nhập liệu phía người dùng.
- **Kết quả:** Không thấy thẻ `<script>`, `<form>` hoặc luồng nhập liệu trong `index.html`; phạm vi chức năng hiện tại là website tĩnh.
- **Giới hạn:** Đây không phải kiểm thử bảo mật chuyên sâu. Chưa đánh giá cấu hình HTTPS, HTTP security headers, máy chủ, hosting, thư viện phụ thuộc hoặc các rủi ro từ môi trường triển khai.
- **Đánh giá:** **Chưa phát hiện bề mặt tấn công động trong phạm vi rà soát; không thể xem đây là chứng nhận an toàn.**
- **Minh chứng:** Ảnh [giao diện desktop](./screenshots/desktop.png) chỉ minh họa trang đang chạy; kết luận này dựa trên rà soát mã nguồn, không thể chứng minh chỉ bằng ảnh giao diện.

### 3.5. Chất lượng mã nguồn

- **Kiểm tra:** Rà soát cấu trúc HTML và CSS liên quan đến bố cục, điều hướng và responsive.
- **Kết quả:** Nội dung được chia thành các section có định danh; stylesheet đặt riêng tại `assets/css/styles.css`; có quy tắc Flexbox/Grid và breakpoint.
- **Điểm cần cải thiện:** Liên kết GitHub đang chứa thẻ `<github class="com">` thay vì văn bản/liên kết chuẩn; thuộc tính `class` của một liên kết dự án chứa chuỗi URL; các liên kết mạng xã hội và dự án còn là placeholder. Chưa có kết quả lint hoặc kiểm thử tự động trong phạm vi lần này.
- **Đánh giá:** **Đạt một phần; nên chuẩn hóa markup và hoàn thiện URL trước khi phát hành.**
- **Minh chứng giao diện:** [Ảnh chụp khu vực Liên hệ](./screenshots/contact.png). Các vấn đề markup cần đối chiếu trực tiếp với mã nguồn.

### 3.6. Khả năng triển khai

- **Kiểm tra:** Mở trực tiếp website từ `index.html` và đối chiếu hướng dẫn chạy website tĩnh trong README.
- **Kết quả:** Có thể mở trang trực tiếp từ file local; dự án không yêu cầu framework hoặc bước build theo mô tả hiện có.
- **Giới hạn:** Chưa chạy bằng máy chủ HTTP và chưa triển khai lên hosting; chưa xác minh đường dẫn tài nguyên, cấu hình HTTPS hoặc hành vi trên production.
- **Đánh giá:** **Đạt một phần.** Có thể xem như website tĩnh chạy local; khả năng triển khai production chưa được xác nhận.
- **Minh chứng:** [Ảnh chụp toàn trang desktop](./screenshots/desktop.png).

## 4. Danh sách ảnh minh chứng

- [desktop.png](./screenshots/desktop.png) — ảnh chụp toàn trang ở chế độ desktop.
- [contact.png](./screenshots/contact.png) — ảnh chụp khu vực liên hệ ở chế độ desktop.

## 5. Đề xuất trước khi phát hành

1. Thay các liên kết `#` của dự án, GitHub và LinkedIn bằng URL đích hợp lệ.
2. Chuẩn hóa markup liên hệ GitHub và bỏ chuỗi URL khỏi thuộc tính `class`.
3. Kiểm tra lại responsive trên viewport mobile thực và tablet.
4. Chạy website qua máy chủ HTTP, sau đó kiểm thử lại các đường dẫn trước khi triển khai.
5. Nếu triển khai công khai, kiểm tra HTTPS và cấu hình bảo mật ở hosting.