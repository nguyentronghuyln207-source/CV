# Portfolio CV - Nguyễn Trọng Huy

Website portfolio cá nhân giới thiệu Nguyễn Trọng Huy, các kỹ năng, dự án tiêu biểu và thông tin liên hệ. Giao diện được xây dựng theo hướng ưu tiên thiết bị di động, có thể xem trên máy tính, máy tính bảng và điện thoại.

## Chức năng

- Hiển thị phần giới thiệu cá nhân và ảnh đại diện.
- Trình bày danh sách kỹ năng và các dự án tiêu biểu.
- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Cung cấp liên kết email, Facebook, LinkedIn và TikTok.
- Giao diện responsive, có thể mở bằng trình duyệt web hiện đại.

## Công nghệ

- HTML5
- CSS3 (Flexbox, CSS Grid, custom properties và media queries)
- Nginx (tùy chọn, dùng để phục vụ trang trong Docker)

Dự án không sử dụng framework, thư viện JavaScript, backend, cơ sở dữ liệu hay bước biên dịch.

## Yêu cầu môi trường

### Chạy trực tiếp

- Windows, macOS hoặc Linux.
- Trình duyệt web hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Để chạy qua máy chủ web cục bộ: Python 3 hoặc Node.js đã được cài đặt. Không cần cài thêm package.

### Chạy bằng Docker

- Docker Engine trên Linux hoặc Docker Desktop trên Windows/macOS.
- Docker đang chạy và có thể tải image `nginx:alpine` trong lần chạy đầu tiên.

## Cài đặt

Tải hoặc sao chép mã nguồn về máy, sau đó mở terminal tại thư mục dự án. Cấu trúc cần giữ nguyên để các đường dẫn ảnh và CSS hoạt động:

```text
.
├── index.html
└── assets/
    ├── css/
    │   └── styles.css
    └── img/
```

Không cần chạy lệnh cài đặt dependency.

## Cấu hình và tùy chỉnh

Đây là website tĩnh và hiện không có tệp cấu hình môi trường hoặc biến `.env`.

- Chỉnh nội dung, tiêu đề, dự án và thông tin liên hệ trong `index.html`.
- Chỉnh màu sắc, bố cục và kiểu chữ trong `assets/css/styles.css`.
- Thay ảnh trong `assets/img/`; nếu đổi tên hoặc vị trí ảnh, cập nhật đường dẫn tương ứng trong `index.html`.
- Các liên kết dự án chưa có URL cụ thể đang dùng `#`; hãy thay bằng địa chỉ dự án thực tế khi cần.

## Chạy thử

### Windows

Mở PowerShell tại thư mục dự án:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có, thử:

```powershell
python -m http.server 8000
```

### macOS

Mở Terminal tại thư mục dự án:

```bash
python3 -m http.server 8000
```

### Linux

Mở terminal tại thư mục dự án:

```bash
python3 -m http.server 8000
```

Sau khi máy chủ khởi động, mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C`.

Có thể mở trực tiếp `index.html` bằng trình duyệt, nhưng dùng máy chủ cục bộ sẽ mô phỏng cách website được phục vụ tốt hơn.

## Chạy bằng Docker

Các lệnh sau chạy Nginx và phục vụ nội dung thư mục dự án dưới dạng chỉ đọc tại cổng `8080`. Không cần tạo Dockerfile.

### Windows (PowerShell)

Chạy tại thư mục dự án:

```powershell
docker run --rm --name cv-portfolio -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

### macOS và Linux

Chạy tại thư mục dự án:

```bash
docker run --rm --name cv-portfolio -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080> để xem trang. Dừng container bằng `Ctrl+C`. Nếu cổng `8080` đang được sử dụng, đổi phần `8080:80` thành một cổng trống khác, ví dụ `8081:80`, rồi mở cổng tương ứng trên trình duyệt.

## Thông tin liên hệ

- **Email:** [nguyentronghuyln207@gmail.com](mailto:nguyentronghuyln207@gmail.com)
- **Facebook:** [facebook.com/nguyentronghuy](https://www.facebook.com/nguyentronghuy)
- **LinkedIn:** [linkedin.com/in/nguyentronghuy](https://www.linkedin.com/in/nguyentronghuy)
- **TikTok:** [@nth1801207](https://www.tiktok.com/@nth1801207)