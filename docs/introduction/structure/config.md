> config

Chứa các file PHP config các thông số quan trọng của dự án, một số file thường dùng.

1. **app.php**

File config trung tâm, chứa rất nhiều thông tin quan trọng, và là nơi đăng ký Provider (những Provider đăng ký tại đây mới có thể khởi chạy)

2. **auth.php**

Nơi define auth providers và auth guards
- `providers`: định nghĩa provider sẽ sử dụng driver nào (mặc định là eloquent) và sẽ map với model nào (authentication với bảng nào trong DB)
- `guards`: định nghĩa guard sẽ sử dụng provider nào và phương thức authentication nào (quan trọng nhất là `session` và `passport`)

3. **database.php**

Nơi chứa config cho database.
Có nhiều `connections` khác nhau, mặc định sẽ là mysql

5. **filesystems.php**

Nơi chứa config cho filesystem.

Các `disk` mặc định:
- `local`: sẽ lưu file ở thư mục `storage`
- `public`: sẽ lưu file ở thư mục `public`, có thể tạo symlink tới thư mục `storage`
- `s3`: lưu trữ file trên s3 của aws, là phương án phổ biến.

Có thể thay đổi `disk` mặc định bằng cách config `FILESYSTEM_DRIVER` ở `.env`

Nếu muốn gọi trực tiếp tới 1 `disk` thì sử dụng facade `\Storage::disk($diskName)`

6. **session.php**

Nơi chứa config cho session

- `driver`: định nghĩa driver-nơi sẽ lưu trữ session. Phổ biến nhất là `file`, `database`, `memcached`, `redis`
- `lifetime`: thời gian hết hạn session
- `encrypt`: có mã hóa session không, mặc định là `false`