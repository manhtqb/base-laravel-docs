> Chức năng upload file sử dụng presigned url

## **Chức năng upload file sử dụng presigned url**

- **Sample Call:**

  ```javascript
  fetch(presignedUrl, {
      method: "PUT",
      headers: {
        "Content-Type": "multipart/form-data"
      },
      body: e.target.file[0]
    })
  ```

- **Notes:**


<p class="tip">Sử dụng trực tiếp trong component vuejs hoặc js thuần.
</p>
