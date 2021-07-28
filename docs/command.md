> Các command line sử dụng

Tham khảo thêm tại docs chính thức của thư viện: https://nwidart.com/laravel-modules/v6/advanced-tools/artisan-commands

###### Tạo mới 1 module
```bash
php artisan module:make Blog
```

###### Chạy migration cho 1 module cụ thể
```bash
php artisan module:migrate Blog
```

###### Chạy seeder cho 1 module cụ thể
```bash
php artisan module:seed Blog
```

###### Enable/Disable 1 module
```bash
php artisan module:enable Blog
php artisan module:disable Blog
```
###### Tạo migration
```bash
php artisan module:make-migration create_posts_table Blog
```
###### Tạo seeder
```bash
php artisan module:make-seed seed_fake_blog_posts Blog
```

###### Tạo controller
```bash
php artisan module:make-controller PostsController Blog
```
###### Tạo model
```bash
php artisan module:make-model Post Blog
```
###### Tạo provider
```bash
php artisan module:make-provider BlogServiceProvider Blog
```
###### Tạo request
```bash
php artisan module:make-request CreatePostRequest Blog
```

