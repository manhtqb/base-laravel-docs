> Các bước cài đặt

## Cài đặt git
Cài đặt git: https://git-scm.com/

## Cài đặt composer
Cài đặt composer: https://getcomposer.org/

## Cài đặt webserver
Một số cách cài webserver trên local phổ biến

- `Xampp`: https://www.apachefriends.org/index.html
- `Docker`: https://www.docker.com/
- `Laragon` (dễ, khuyến khích sử dụng): https://laragon.org/

<p class="tip">Cài đặt phiên bản PHP từ 7.4 trở lên</p>

## Clone dự án

``` bash
$ git clone https://github.com/manhtqb/base-laravel.git
```

## Tạo file môi trường .env

``` bash
$ cp .env.example .env
```

<p class="tip">Điền đầy đủ các thông tin config môi trường vào file .env</p>

## Cài đặt thư viện PHP
``` bash
$ composer install
```

## Cài đặt thư viện Javascript
``` bash
$ npm install
```

## Generate application key
``` bash
$ php artisan key:generate
```

## Chạy migrate tạo database

<p class="tip">Sử dụng trình quản lý database để tạo 1 database có tên giống trong config .env</p>

``` bash
$ php artisan migrate
```

## Chạy install passport

<p class="tip">Generate key passport sử dụng cho việc authentication</p>

``` bash
$ php artisan passport:install
```

## Chạy seeder dữ liệu

``` bash
$ php artisan db:seed
```

## Chạy webpack

``` bash
$ npm run dev
```

## Chạy ứng dụng

**Chạy theo domain config trong webserver (khuyến khích)**

Nếu sử dụng `laragon` thì sẽ được tự động config vitural host

**Chạy với webserver built-in của laravel**

``` bash
$ php artisan serve
```

