> Chức năng upload ảnh

## **Chức năng upload ảnh**

<_Chức năng đăng ký người dùng._>

Trước khi bắt đầu cần config s3.

Dưới đây là 1 ví dụ về config `s3` trong `.env`

```
AWS_ACCESS_KEY_ID=SFWYRTYRHGFHFGHFGH
AWS_SECRET_ACCESS_KEY=AIOSUDOAISIDUASIODUOAISD
AWS_DEFAULT_REGION=ap-northeast-1
AWS_BUCKET=example-bucket
AWS_URL=https://example-bucket.s3.ap-northeast-1.amazonaws.com
MIX_AWS_URL=https://example-bucket.s3.ap-northeast-1.amazonaws.com
```

#### Gọi RestAPI với các thông tin dưới dây

- **URL**

  api/common/upload-image

- **Headers:**

  `Accept` `application/json`

- **Method:**

  `POST`

- **Data Params**

  **Required:**

      `image=[file]`

  **Optional:**

- **Success Response:**

  <_Trường hợp response thành công_>

  - **Code:** 200 <br />
    **Content:**
    `{
    "data": "images/1627483908.png"
    }`

- **Error Response:**

- **Sample Call:**

  ```javascript
  let formData = new FormData()
  formData.append('image', e.target.file[0])
  $.ajax({
    type: "POST",
    url: "/api/common/upload-image",
    data: formData,
    success: () => {},
    dataType: "json",
  });
  ```

- **Notes:**

<p class="tip">
URL image API trả về là đường dẫn tương đối của file đã upload. Muốn hiển thị cần thêm prefix là AWS_URL đã config trong `.env`
Ví dụ: https://example-bucket.s3.ap-northeast-1.amazonaws.com/images/1627483908.png

Sửa đường dẫn lưu ảnh tại file `Modules/Common/Config/config.php`

Sửa logic tại `Modules/Common/Http/Controllers/ImageController.php`
</p>
