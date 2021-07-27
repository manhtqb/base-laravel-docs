> database

Chứa các thư mục làm việc với cấu trúc và dữ liệu mẫu của database 

1. **factories**

Chứa các class factory là các bộ khung về cấu trúc dữ liệu mẫu cho 1 model cụ thể

2. **migrations**

Chứa các class định nghĩa cấu trúc các table trong database

3. **seeders**

Chứa các class định nghĩa việc tạo dữ liệu mẫu.
Trong class seeder sẽ gọi đến `factory`