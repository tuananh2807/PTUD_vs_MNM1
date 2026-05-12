# PTUD_vs_MNM1 <br>

**Bài tập 3_Lê tuấn anh_k225480106001** <br>

**SỬ DỤNG WORDPRESS ĐỂ TẠO WEB SITE** <br>

**deadline : 23h59 ngày 12 tháng 5 năm 2026.** <br>

**Bước 1 — Tạo thư mục dự án** <br>
<img width="517" height="77" alt="image" src="https://github.com/user-attachments/assets/a7e9c53b-8a7a-4c02-bbec-b01bcef8ce9f" /> <br>

**Bước 2 — Tạo file docker-compose.yml** <br>
<img width="457" height="601" alt="image" src="https://github.com/user-attachments/assets/0406e292-005f-4c54-aba2-973803ecb26a" /> <br>
<img width="468" height="587" alt="image" src="https://github.com/user-attachments/assets/cb3fdbad-56fe-4aa0-b1eb-60440961c801" /> <br>
<img width="1536" height="827" alt="image" src="https://github.com/user-attachments/assets/a7db6865-15c1-4140-bf99-4c8421609b9e" /> <br>

**Bước 3 — Khởi động** <br>
<img width="1536" height="187" alt="image" src="https://github.com/user-attachments/assets/b8133c7a-3af1-47fd-8b27-19f2cd9165c9" /> <br>

các container đã ở trang thái up <br>
<img width="1536" height="157" alt="image" src="https://github.com/user-attachments/assets/22a2eb51-0f53-4560-9cd2-04f9a4d2b8ac" /> <br>

**Bước 4 — Cài đặt WordPress** <br>
- Mở trình duyệt → http://localhost:8084 <br>
- điền thông tin <br>
<img width="747" height="687" alt="image" src="https://github.com/user-attachments/assets/ed1d12ce-0ef3-4719-9bef-d245fe1bc254" /> <br>

- sau đó đăng nhập tại Đăng nhập tại http://localhost:8084/wp-admin <br>
<img width="980" height="307" alt="image" src="https://github.com/user-attachments/assets/f17ea622-215c-40a8-932b-fae10f458df3" /> <br>

**Bước 6 — Cài Cloudflare Tunnel (public lên internet)** <br>
6.1 Cài cloudflared <br>
<img width="917" height="277" alt="image" src="https://github.com/user-attachments/assets/ce502cae-6a1c-40ad-90e4-de307f61d912" /> <br>

6.2 Tạo tunnel <br>
<img width="736" height="333" alt="image" src="https://github.com/user-attachments/assets/21089e30-683e-4eca-bde6-372c1b921142" /> <br>

- dán token này vào ubuntu <br>
<img width="603" height="78" alt="image" src="https://github.com/user-attachments/assets/427b543f-8d5a-4a6e-82cf-08f755f7ea6f" /> <br>

- tải cloudflared về máy Ubuntu <br>
<img width="1536" height="581" alt="image" src="https://github.com/user-attachments/assets/704ff413-86e2-46e2-8e9a-fe1a2de12a21" /> <br>

- Chạy lệnh chứa Token <br>
<img width="1532" height="100" alt="image" src="https://github.com/user-attachments/assets/6bef8e38-c867-4c42-9212-68b38f93142e" /> <br>

- đã thông suốt với Cloudflare. <br>
<img width="731" height="43" alt="image" src="https://github.com/user-attachments/assets/bcc700aa-2df5-4b4f-8e0f-8cb20736d2c3" /> <br>

- Trỏ tên miền về website WordPress. <br>
<img width="672" height="707" alt="image" src="https://github.com/user-attachments/assets/e23917a1-cf6f-4e09-ae74-8d34a0c70046" /> <br>
<img width="503" height="457" alt="image" src="https://github.com/user-attachments/assets/4819dca8-8d8c-4341-a592-15077a570b5e" /> <br>

- tạo bài viết <br>
<img width="1536" height="821" alt="image" src="https://github.com/user-attachments/assets/4bf4b300-7759-41e3-aa0f-dec4486b5c51" /> <br>

<img width="1536" height="810" alt="image" src="https://github.com/user-attachments/assets/e03dfaa1-38c7-40d9-84d4-45cb785639d0" /> <br>

**NHẬN XÉT: SỬ DỤNG MÃ NGUỒN MỞ WORDPRESS TRÊN NỀN TẢNG DOCKER** <br>

1. Về công sức thiết lập (Effort) <br>
Tiết kiệm thời gian đáng kể: Thay vì phải cài đặt thủ công từng thành phần (LAMP/LEMP stack) mất hàng giờ đồng hồ, việc sử dụng Docker Compose giúp gói gọn toàn bộ MariaDB, WordPress và PhpMyAdmin chỉ trong một file cấu hình. Chỉ cần một lệnh docker compose up -d, hệ thống sẽ sẵn sàng sau vài phút.<br>
Đồng nhất môi trường: Việc triển khai bằng Docker giúp tránh hoàn toàn các lỗi xung đột phiên bản PHP hay thư viện hệ thống trên Ubuntu, điều mà cách cài đặt truyền thống thường gặp phải. <br>

2. Về độ khó sử dụng (Usability) <br>
Dễ dùng cho người mới: WordPress cung cấp giao diện quản trị (Dashboard) rất trực quan. Việc tạo bài viết, tùy chỉnh giao diện (Theme) hay cài thêm tính năng (Plugin) được thực hiện hoàn toàn bằng click chuột, không đòi hỏi kỹ năng lập trình chuyên sâu. <br>
Public web dễ dàng: Kết hợp với Cloudflare Tunnel, việc đưa website ra internet trở nên cực kỳ đơn giản và an toàn. Sinh viên không cần can thiệp vào cấu hình Modem/Router hay lo lắng về bảo mật cổng mở (port forwarding). <br>

3. Về tiêu tốn tài nguyên máy chủ (Resources) <br>
RAM: Đây là điểm cần lưu ý nhất. WordPress chạy trên nền PHP và MariaDB tiêu tốn khá nhiều RAM. Theo thực tế triển khai: <br>
MariaDB: Chiếm khoảng 200MB - 400MB RAM. <br>
WordPress (PHP-FPM): Chiếm khoảng 150MB - 300MB RAM. <br>
Khuyến nghị: Máy chủ (VPS/SSH) nên có tối thiểu 2GB RAM để hệ thống vận hành mượt mà khi có nhiều container cùng chạy. <br>
CPU và Dung lượng: CPU tiêu thụ không đáng kể khi website ở trạng thái tĩnh. Tuy nhiên, Docker Image và các bản lưu dữ liệu (Volumes) sẽ chiếm khoảng vài GB dung lượng ổ cứng sau một thời gian sử dụng. <br>

4. Đánh giá chung <br>
Sử dụng WordPress mã nguồn mở kết hợp với công nghệ Containerization (Docker) là phương pháp tối ưu nhất cho sinh viên và doanh nghiệp nhỏ để xây dựng website nhanh chóng. <br>
Ưu điểm: Nhanh, mạnh mẽ, cộng đồng hỗ trợ lớn, triển khai linh hoạt. <br>
Nhược điểm: Tốn tài nguyên RAM hơn các bộ mã nguồn viết bằng ngôn ngữ khác (như Golang hay Node.js) và cần chú ý cập nhật thường xuyên để tránh lỗ hổng bảo mật. <br>

