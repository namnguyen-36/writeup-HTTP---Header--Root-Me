Hello mọi người, sau đây mình sẽ hướng dẫn các bạn giải challenge **HTTP Header** thuộc mảng Web Exploitation trong Root Me nhé.
<img width="1377" height="407" alt="Screenshot 2026-05-27 145030" src="https://github.com/user-attachments/assets/9d87901e-42fb-4e07-ada7-6b443578e1b0" />

URL của chall: http://challenge01.root-me.org/web-serveur/ch5/
Mở URL của chall bằng trình duyệt ta sẽ nhận được một giao diện web như sau
<img width="1856" height="681" alt="Screenshot 2026-05-27 145050" src="https://github.com/user-attachments/assets/7585b9c4-dd12-4577-a22d-24746885fb4b" />

Theo như nội dung hiển thị trên web `Content is not the only part of an HTTP response!` chúng ta sẽ mở Dev tool của trình duyệt và truy cập vào phần mạng của web. Ấn F5 để load lại trang. 

Trong phần gợi ý của đề bài `Get an administrator access to the webpage.` chúng ta có thể hiểu rằng cần có quyền `admin` để truy cập được vào web

Đồng thời trong Responde Header ta thấy dòng `Header-RootMe-Admin: none` đang ở trạng thái là `none`. Để có quyền admin ta thử thêm trường `Header-RootMe-Admin:` vào http requets và đổi trạng thái từ `none` thành `admin`
<img width="1491" height="378" alt="Screenshot 2026-05-27 145851" src="https://github.com/user-attachments/assets/f6ddb36b-78e3-481b-8724-3fa541759fb3" />

Sau khi sửa và send request mới ta nhận được password trong nội dung trả về
 ### password: HeadersMayBeUseful
