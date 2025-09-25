# Simple Authentication
### Mở cmd cài đặt 
- Mở terminal cmd, chuyển đến thư mục `simple_auth`.
- Chạy lệnh:
```bash
npm install
```
## 1. Basic Auth
### Test API với POSTMAN

1. **Khởi động server:**
   - Mở terminal cmd, chuyển đến thư mục `simple_auth`.
   - Chạy lệnh:  
     ```bash
     node basic_auth.js
 ![Khởi động server](.public/image/image2.png)    
2. **Test API với POSTMAN:**
   - Mở POSTMAN.
   - Khởi tạo một request mới với phương thức `GET` tới địa chỉ:  
     ```
     http://localhost:3000
     ```
   - Chọn mục **Authorization**.
   - Ở mục **Type**, chọn **Basic Auth**.
   - Nhập:
     - **Username:** `admin`
     - **Password:** `12345`
   - Nhấn **Send** request và kiểm tra kết quả trả về.
   ![Kiểm tra kết quả](.public/image/image1.png)
## 2. Cookie Auth
### Test API với POSTMAN

1. **Khởi động server:**
   - Mở terminal cmd, chuyển đến thư mục `simple_auth`.
   - Chạy lệnh:  
     ```bash
     node cookie_auth.js
     ```
 ![Khởi động server](.public/image/image3.png) 
2. **Test API đăng nhập với POSTMAN:**
   - Mở POSTMAN.
   - Tạo một request mới với phương thức `POST` tới địa chỉ:  
     ```
     http://localhost:3001/login
     ```
   - Chọn tab **Body** → chọn **raw** → chọn **JSON**.
   - Nhập nội dung:
     ```json
     {
       "username": "admin",
       "password": "12345"
     }
     ```
   - Nhấn **Send** để gửi request.
   - Sau khi đăng nhập thành công, kiểm tra mục **Cookies** ở góc phải POSTMAN để xem cookie đã được tạo.
    ![Kiểm tra kết quả](.public/image/image4.png)

3. **Kiểm tra cookie trong MongoDB:**
   - Mở MongoDB Compass hoặc công cụ quản lý MongoDB.
   - Truy cập database `cookieApp`, collection `cookies`.
   - Kiểm tra document chứa thông tin cookie vừa tạo.

   ![Hiển thị cookie trong MongoDB](.public/image/image5.png)
