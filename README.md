# Bảng Phong Thần -- Cung Trời Hóa Lạc

Website tĩnh chạy trực tiếp trên trình duyệt, giao diện tiếng Việt, tối
ưu cho điện thoại và máy tính.

## Nội dung

-   Trang đăng nhập và đăng ký tài khoản.
-   Sảnh Bảng Phong Thần với bảng xếp hạng.
-   Menu chủ đề tiên hiệp, vòng nhân vật chuyển động và hai hộ vệ cầm
    kiếm.
-   Khu vực tính năng trò chơi và trang Quản Trị Viên.
-   Dữ liệu được lưu bằng `localStorage` trên trình duyệt hiện tại.

## Cấu trúc GitHub

``` text
.
├── index.html
├── README.md
└── .github/
    └── workflows/
        └── deploy.yml
```

## Chạy thử trên máy

1.  Tải hoặc clone repository.
2.  Mở `index.html` bằng trình duyệt hiện đại.
3.  Đăng ký tài khoản mới hoặc đăng nhập bằng tài khoản đã tạo trên
    chính trình duyệt đó.

Không cần cài Node.js, không cần build và không cần Firebase cho phiên
bản này.

## Triển khai GitHub Pages

1.  Tạo repository trên GitHub.
2.  Đưa `index.html`, `README.md` và thư mục `.github/workflows/` lên
    nhánh `main`.
3.  Vào **Settings → Pages**.
4.  Trong **Build and deployment**, chọn **Source: GitHub Actions**.
5.  Push commit mới lên `main`, hoặc vào **Actions** và chạy workflow
    **Deploy to GitHub Pages**.
6.  Sau khi workflow hoàn tất, mở URL GitHub Pages hiển thị trong
    **Settings → Pages**.

Workflow nằm tại `.github/workflows/deploy.yml`. Nó triển khai website
tĩnh từ thư mục gốc repository.

## Lưu ý quan trọng về tài khoản và dữ liệu

Phiên bản hiện tại là website tĩnh, không có máy chủ xác thực hoặc cơ sở
dữ liệu dùng chung:

-   Tài khoản đăng ký và dữ liệu trò chơi chỉ lưu trong `localStorage`
    của trình duyệt và thiết bị đang dùng.
-   Dữ liệu không tự đồng bộ giữa người chơi, thiết bị hoặc trình duyệt
    khác.
-   Xóa dữ liệu trình duyệt có thể làm mất tài khoản và tiến trình đã
    lưu trên thiết bị đó.
-   Thông tin đăng nhập Quản Trị Viên và khóa chỉnh sửa đang được kiểm
    tra trong JavaScript phía trình duyệt. Người xem mã nguồn có thể đọc
    được chúng; đây **không phải** cơ chế bảo mật phù hợp cho website
    công khai.
-   Không dùng phiên bản này để lưu thông tin nhạy cảm, tài sản có giá
    trị hoặc vận hành quản trị thật. Muốn bảo mật thực tế cần backend
    xác thực, phân quyền và cơ sở dữ liệu phía máy chủ.

## Cập nhật website

Chỉnh sửa `index.html`, sau đó commit và push lên nhánh `main`. GitHub
Actions sẽ tự triển khai lại.

## Giấy phép

Chưa chỉ định giấy phép. Nếu muốn cho phép người khác sử dụng hoặc chỉnh
sửa mã nguồn, hãy bổ sung tệp `LICENSE` với giấy phép phù hợp.
