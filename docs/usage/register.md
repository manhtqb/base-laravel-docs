> Chức năng register/email confirm

## **Chức năng register/email confirm**

<_Chức năng đăng ký người dùng._>
Trước khi bắt đầu cần config email để gửi mail active cho user.
Có thể sử dụng `mailtrap` để test, dưới đây là 1 ví dụ về config `mailtrap` trong `.env`

```
MAIL_MAILER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=1231414124
MAIL_PASSWORD=124124124124
MAIL_ENCRYPTION=tls
```

#### Gọi RestAPI với các thông tin dưới dây

- **URL**

  /api/auth/signup

- **Headers:**

  `Accept` `application/json`

- **Method:**

  `POST`

- **Data Params**

  **Required:**

      `name=[string]`
      `email=[string]`
      `password=[string]`
      `password_confirmation=[string]`

  **Optional:**

- **Success Response:**

  <_Trường hợp response thành công_>

  - **Code:** 200 <br />
    **Content:**
    `{ "message": "Successfully created user!", "user": { "name": "new User", "email": "newemail@gmail.com", "updated_at": "2021-07-28T14:00:37.000000Z", "created_at": "2021-07-28T14:00:37.000000Z", "id": 21 } } `

- **Error Response:**

  <_Lỗi validate form._>

  - **Code:** 422 UNPROCESSABLE ENTITY <br />
    **Content:** `{ "message": "The given data was invalid.", "errors": { "name": [ "The name field is required." ], "email": [ "The email must be a valid email address." ], "password": [ "The password field is required." ] } }`

- **Sample Call:**

  ```javascript
  $.ajax({
    type: "POST",
    url: "/api/auth/signup",
    data: {
      name: "new User",
      email: "newemail@gmail.com",
      password: "12345678",
      password_confirmation: "12345678",
    },
    success: () => {},
    dataType: "json",
  });
  ```

- **Notes:**

  <_Sửa logic|message validate|rule validate tại._> `Modules/JwtAuthentication/Http/Controllers/AuthController.php` function `signup`

<p class="tip">Sau khi đăng ký thành công, hệ thống sẽ gửi 1 email xác thực tới email đã đăng ký chứa activation_code sẽ sử dụng trong chức năng active user
</p>
