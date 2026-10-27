# CV Portfolio - Lương Xuân Bắc

## 1. Tên dự án
CV Portfolio - Lương Xuân Bắc

## 2. Mô tả dự án
Đây là một trang CV/portfolio cá nhân được xây dựng bằng HTML và CSS, nhằm giới thiệu thông tin cá nhân, kỹ năng, dự án tiêu biểu và phương thức liên hệ. Dự án tập trung vào thiết kế đơn giản, hiện đại, thân thiện với người dùng và tương thích với các thiết bị khác nhau.

## 3. Chức năng chính
- Hiển thị thông tin cá nhân và vai trò nghề nghiệp
- Mục giới thiệu về bản thân
- Hiển thị các kỹ năng và công nghệ sử dụng
- Trình bày các dự án tiêu biểu theo dạng thẻ card
- Hiển thị thông tin liên hệ
- Giao diện responsive trên màn hình desktop, tablet và mobile
- Có điều hướng nội bộ giữa các section bằng anchor links

## 4. Công nghệ sử dụng
- HTML5
- CSS3
- Flexbox và Grid Layout
- Responsive Web Design
- Tài nguyên hình ảnh tĩnh trong thư mục assets

## 5. Yêu cầu môi trường
Dự án là một website tĩnh, do đó không yêu cầu môi trường phức tạp.

### Yêu cầu tối thiểu
- Trình duyệt hiện đại: Chrome, Edge, Firefox, Safari
- Không cần cài đặt Node.js, npm hay framework
- Một hệ điều hành: Windows, macOS hoặc Linux

## 6. Cài đặt
Không cần cài đặt thư viện hoặc dependency phức tạp.

### Cách 1: Mở trực tiếp file HTML
1. Tải hoặc clone project về máy
2. Mở thư mục dự án
3. Double-click vào file `index.html`
4. Trang sẽ mở trong trình duyệt mặc định

### Cách 2: Chạy bằng máy chủ tĩnh local
Từ thư mục dự án, thực hiện lệnh sau:

```bash
python -m http.server 8000
```

Sau đó truy cập:

```text
http://localhost:8000
```

## 7. Cấu hình
Dự án không yêu cầu file cấu hình phức tạp. Nếu bạn muốn chỉnh sửa thông tin cá nhân, hãy cập nhật trong file `index.html`.

### Các phần chính cần chỉnh sửa
- Tên, tiêu đề và mô tả giới thiệu
- Kỹ năng
- Dự án tiêu biểu
- Thông tin liên hệ
- Ảnh đại diện và hình minh họa dự án

### Cấu trúc thư mục
```text
CV--main/
├── index.html
├── README.md
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── img/
```

## 8. Hướng dẫn chạy thử

### Windows
1. Mở Command Prompt hoặc PowerShell
2. Di chuyển đến thư mục dự án:

```bash
cd "đường_dẫn_đến_thư_mục_CV--main"
```

3. Chạy máy chủ tĩnh:

```bash
python -m http.server 8000
```

4. Mở trình duyệt và truy cập:

```text
http://localhost:8000
```

### macOS
1. Mở Terminal
2. Di chuyển đến thư mục dự án:

```bash
cd /đường/dẫn/đến/CV--main
```

3. Chạy lệnh:

```bash
python3 -m http.server 8000
```

4. Truy cập trong trình duyệt:

```text
http://localhost:8000
```

### Linux
1. Mở Terminal
2. Di chuyển vào thư mục dự án:

```bash
cd /đường/dẫn/đến/CV--main
```

3. Chạy lệnh:

```bash
python3 -m http.server 8000
```

4. Mở đường dẫn sau trong trình duyệt:

```text
http://localhost:8000
```

## 9. Gỡ lỗi nhanh
- Nếu trang không hiển thị đúng, hãy đảm bảo bạn đang ở đúng thư mục dự án
- Nếu ảnh không xuất hiện, kiểm tra lại đường dẫn trong `index.html`
- Nếu file CSS không áp dụng, hãy chắc chắn `styles.css` nằm trong `assets/css/` và đường dẫn được ghi đúng
- Nếu máy không có `python`, hãy cài đặt Python hoặc mở trực tiếp file `index.html`

## 10. Thông tin liên hệ
- Tên: Lương Xuân Bắc
- Email: meoconsatthu66b@example.com
- GitHub: github.com/xuanbac204
- LinkedIn: linkedin.com/in/66bnguyensysach

## 11. Ghi chú
Dự án này là một website tĩnh, dễ tùy biến và phù hợp để dùng như mẫu CV cá nhân hoặc portfolio bán hàng trong học tập, thực hành và xây dựng hồ sơ cá nhân.

## 12. License
Dự án này được cung cấp cho mục đích học tập và cá nhân. Bạn có thể tùy chỉnh, sửa đổi và phát triển theo nhu cầu của mình.
