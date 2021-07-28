> Chức năng logout

## **Chức năng logout**

#### Gọi RestAPI với các thông tin dưới dây

- **URL**

  api/auth/logout

- **Headers:**

  `Accept` `application/json`
  
  `Authorization` `${token}`
- **Method:**
  
  `GET`

- **Data Params**

  **Required:**

  **Optional:**

- **Success Response:**

  <_Trường hợp response thành công_>

  - **Code:** 200 <br />
    **Content:**
    `{
    "message": "Successfully logged out"
    }`

- **Error Response:**

- **Sample Call:**

  ```javascript
  $.ajax({
    type: "GET",
    url: "/api/auth/logout",
    headers: {
      Authorization: `Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJhdWQiOiIxIiwianRpIjoiNjcxMzkyODRmOGVjMDQwYjk4MGVjNGMyZjY2NWY0NWE1NmFiNjU2OWYwYTZiY2YxMWY1OTEwNDEzZjRjMDc1MzE1YTA5ZWZkZWRjY2M2MTgiLCJpYXQiOjE2Mjc0ODM0OTQuOTUzMzEsIm5iZiI6MTYyNzQ4MzQ5NC45NTMzMTQsImV4cCI6MTY1OTAxOTQ5NC45NDM4NjksInN1YiI6IjIxIiwic2NvcGVzIjpbXX0.O2Y95SJDJJ2VcsdxovvFJufvrubsSZopmlNHGULgC7vED8ME4vnAsf3vo_a25IoL07lkjDUEXYIJRGY6eUaou1TkDdCjpGbI4JjpFCH6SGE2QNAF2w0mNn130KKe-E8pyeMSjT5tRx95oyS_BC1CxfL6-ztdkwp1mldmGozPE64XSMiBQ139XYSj2pWpltEtjfxRQ0v8FxbmZmIt9XmkNQJzLt7Wv87zJTzVFoM-lTjkpaOpko-2g1piDK6QH-6EaGz62SGAqkLMoRWN2o8dUiDbFOJVgJoivUE9WOAADNjN29IuiDi54QktJrGi2EJGDljgdoL1Y3SUHtzOsv9oCWOpXmofrZKqpShd7kPTpRu4_gSjCyitSns7sCYqFI-jwl3sEfbV5sMyvgBsncj_WyGrq03TanZ-gmPwG5LIWMxRALos9415jedoQlc4liPxg7epIrHMhSiRhgeaHrqNJStDWE7Kj8wUuxxc0GGHNQyf_WvOdrgpLU_jOajHr-YByqEmw2g2_0FNUYjOpyLHkna2IuwUKobP6JkBbB6LBy8qDzT41qVPlGz_hIVTnSmTpsPpP1r95JPDA75e6Pq05BdPW_aFZXB5dwmj-CYK3AyC5PB1p7HtpukY_Du2lhiy5Xq_U-edjRTwtL-pJ4yIj2-fYYMBK4GDrAJVfCvH5no `
    },
    success: () => {},
    dataType: "json",
  });
  ```

- **Notes:**
