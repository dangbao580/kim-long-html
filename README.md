# Kim Long Trading

Trang xem sản phẩm tĩnh và trang quản trị CRUD cho `products.json`.

## Chạy thử

Mở bằng máy chủ HTTP, không mở trực tiếp bằng `file://` vì trang công khai cần `fetch('products.json')`.

```powershell
npx serve .
```

Sau đó mở `index.html`. Trang quản trị nằm ở `admin.html`.

## Đưa lên GitHub Pages

1. Tạo repository GitHub và đẩy các file trong thư mục này lên nhánh `main`.
2. Vào **Settings > Pages**, chọn **Deploy from a branch**, chọn `main` và thư mục `/ (root)`.
3. Mở URL GitHub Pages sau khi GitHub triển khai xong.

## Dùng trang quản trị

1. Tạo fine-grained Personal Access Token trên GitHub.
2. Chỉ chọn đúng repository này, cấp quyền **Contents: Read and write**, rồi tạo token.
3. Trong `admin.html`, nhập `owner/repo`, nhánh `main`, và PAT để tải dữ liệu.
4. PAT chỉ được giữ trong bộ nhớ của tab hiện tại, không được ghi vào repo. Hãy xoá/revoke token sau khi dùng xong hoặc khi nghi ngờ bị lộ.

Trang quản trị ghi đè `products.json` qua GitHub Contents API. Ảnh có thể là URL công khai hoặc đường dẫn tới file ảnh đã có trong repo, ví dụ `images/snack.jpg`.
