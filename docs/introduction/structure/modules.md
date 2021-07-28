> Modules

Thư mục rất quan trọng, sẽ chứa source code của từng module được chia theo business.

Mỗi module sẽ là 1 ứng dụng Laravel thu nhỏ.

#### thư mục config
Các giá trị ở đây sẽ được gọi ra theo cú pháp `config(${module_name}.config_key)`

Ví dụ: `config('common.'file_path_post_editor_image)`

#### thư mục Database

Chứa các file database của riêng module.

Khi chạy migrate ở root folder thì mặc định sẽ chạy tất cả trong các module.

Muốn chạy riêng 1 module: xem thêm ở mục `Các command line sử dụng`

#### thư mục Entities

Đây chính là thư mục chứa model

#### thư mục Routes

Các route được khai báo trong module sẽ được merge với các route của root folder.

Chạy `php artisan route:list` để kiểm tra danh sách route
