---
title: 'Hello mọi người, sau đây mình '

---

Hello mọi người, sau đây mình sẽ hướng dẫn các bạn giải challenge **HTTP Header** thuộc mảng Web Exploitation trong Root Me nhé.
![Screenshot 2026-05-27 145030](https://hackmd.io/_uploads/Hy8FDiqxMg.png)
URL của chall: http://challenge01.root-me.org/web-serveur/ch5/
Mở URL của chall bằng trình duyệt ta sẽ nhận được một giao diện web như sau
![Screenshot 2026-05-27 145050](https://hackmd.io/_uploads/H1oNOiqxMe.png)
Theo như nội dung hiển thị trên web `Content is not the only part of an HTTP response!` chúng ta sẽ mở Dev tool của trình duyệt và truy cập vào phần mạng của web. Ấn F5 để load lại trang. 

Trong phần gợi ý của đề bài `Get an administrator access to the webpage.` chúng ta có thể hiểu rằng cần có quyền `admin` để truy cập được vào web

Đồng thời trong Responde Header ta thấy dòng `Header-RootMe-Admin: none` đang ở trạng thái là `none`. Để có quyền admin ta thử thêm trường `Header-RootMe-Admin:` vào ht
