# Cấu trúc thư mục
> app

Chứa các thư mục chính của dự án

1. **Console**

Nơi định nghĩa các file php chạy dưới dạng command line

Các file command sẽ nằm trong thư mục con `Commands` (trong phiên bản mới laravel đã bỏ thư mục này trong khởi tạo)

File `kernel.php` là nơi định nghĩa việc chạy schedule (các lệnh chạy theo lịch lên sẵn)

2. **Exceptions**

Nơi handle mọi exception của hệ thống. Có thể custom việc xử lý exception như gửi mail, bắn notification...

3.  **Http**

Thư mục làm việc chính với các requests

- `Controller`: chứa các file controller (**C** trong **MVC**)
- `Middleware`: chứa các file middleware như là phần trung gian giữa request và controller
- `Requests`: chứa các  file request để validation

