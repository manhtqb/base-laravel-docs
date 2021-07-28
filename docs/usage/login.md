> Chức năng login

## **Chức năng login**

#### Gọi RestAPI với các thông tin dưới dây

- **URL**

  api/auth/login

- **Headers:**

  `Accept` `application/json`

- **Method:**

  `POST`

- **Data Params**

  **Required:**

      `email=[string]`
      `password=[string]`

  **Optional:**

- **Success Response:**

  <_Trường hợp response thành công_>

  - **Code:** 200 <br />
    **Content:**
    `{
    "access_token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJhdWQiOiIxIiwianRpIjoiNTgxMWNhNGFmNzFmN2NkYzQ4YzNiODAzODlhZmFmZWUxY2NkZmE4OTMwMjAxNmJiY2JlOTI0YzI5MTlkMzA3ODg0MTM0OWY2ZWE5ZjgyMWMiLCJpYXQiOjE2Mjc0ODMwNjYuNjY0MDYzLCJuYmYiOjE2Mjc0ODMwNjYuNjY0MDY3LCJleHAiOjE2NTkwMTkwNjYuNjU1Nzk1LCJzdWIiOiIyMSIsInNjb3BlcyI6W119.YxXMA1GZ7RsZRjxL9cOvNo5TABohSxOG8bfVILlP_ovGRsiCmdEGvMP8nCEKrwD9e7iKgQoXc06mKBTkm0Wd_jGk-QoF_5jvjSZoVQW5cmexlByz1-eqpuDivXCEjFqeL_3O8rCiiu2hhBqXMFv0BOsnyWRGFjwYW3I0UII5bFNczsRYSUBK2j4yWK8EtoHUD9vXWZhGm5VMgZkS6Yt_BBaVDAjI_yW-c3forGNlSQs7nxQZ40vXP3smhNulsBLc3gc2cuL1Pvbtla1O0id5dQfMRme0oJdPunYYVFXKqEJoZdIm3l6Oad7QzqrmtPbpHuMsRZGQ5t52b09waDn3LJCHZzsXyub06NXgCByD1oG8e2fTFQ-OVfSc_hQ9dpaseqAThszhQ87P8VDjxlq00417d7Htvs86x9cop1WhwW3R-WyQdNHRGcEGVuN4JqI8T9yeJFR9rlvYMFLUep9XM33IBHjIvMxZmPVl9jbDIBiMUlk5Hybi55k3i_oA8ozI61rfhxpla1YjXX94qeDeExUobKE9Q_-87qieZbN_YOn74nyIfibbTAp8ZT5ofrQ1C8m2nxsJkbcrAR1UynguOS5SmVFhiYcD2rULqVjmCskLt1P_dzB9woY2NoIWmFt_K8Z5Gzn5HMk8bUzWz0-GEiTip-N2HgSE1oGv1AGdSU4",
    "token_type": "Bearer",
    "expires_at": "2022-07-28 14:37:46"
    }`

- **Error Response:**

  <_Lỗi validate form._>

  - **Code:** 422 UNPROCESSABLE ENTITY <br />
    **Content:** 
    `{
    "message": "The given data was invalid.",
    "errors": {
    "email": [
    "The email field is required."
    ]
    }
    }`

  - **Code:** 401 <br />
    **Content:**
    `{
    "message": "Password not match"
    }`
- **Sample Call:**

  ```javascript
  $.ajax({
    type: "POST",
    url: "/api/auth/login",
    data: {
      "email": "newemail@gmail.com",
      "password": "123454678"
    },
    success: () => {},
    dataType: "json",
  });
  ```

- **Notes:**
Giá trị `token` trả về sẽ cần được lưu lại ở client, và gửi kèm headers của api khác theo cú pháp:
  - `Authorization` `Bearer ${token}`
