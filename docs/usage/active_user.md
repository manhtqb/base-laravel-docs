> Chức năng active user đã đăng ký

## **Chức năng active user đã đăng ký**

#### Gọi RestAPI với các thông tin dưới dây

- **URL**

  api/auth/signup/activate/{token}

- **Headers:**

  `Accept` `application/json`

- **Method:**

  `GET`

* **URL Params**

  **Required:**

  `token=[string]`

* **Data Params**

  None

- **Success Response:**

  <_Trường hợp response thành công_>

  - **Code:** 200 <br />
    **Content:**
    `{ "id": 21, "name": "new User", "email": "newemail@gmail.com", "active": true, "created_at": "2021-07-28T14:00:37.000000Z", "updated_at": "2021-07-28T14:21:52.000000Z", "deleted_at": null } `

- **Error Response:**

- **Sample Call:**

  ```javascript
  $.ajax({
    type: "GET",
    url: "api/auth/signup/activate/BfdspJh80GfKN0DkQQwV73ET6IulzwlsAtS7bZtvH6xFvajHFT1hnqUMZq5n",
    data: {},
    success: () => {},
    dataType: "json",
  });
  ```

- **Notes:**
