[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Dj7qWeHQ)
# 📌 D-Cinema – Hệ thống bán vé xem phim trực tuyến dành cho chuỗi các rạp

## 📖 Introduction
[cite_start]D-Cinema là nền tảng web đóng vai trò là cổng thương mại điện tử tập trung cho toàn bộ chuỗi rạp chiếu phim[cite: 10]. [cite_start]Hệ thống cho phép khán giả trên nhiều khu vực dễ dàng lựa chọn chi nhánh rạp, cập nhật lịch chiếu và thực hiện quy trình mua vé, chọn ghế, đặt đồ ăn nhẹ hoàn toàn qua mạng[cite: 11]. [cite_start]Dự án dồn toàn lực vào trải nghiệm B2C trực tuyến với thiết kế giao diện Dark Theme hiện đại kết hợp điểm nhấn Neon Green, đồng thời tích hợp module quản trị dữ liệu cốt lõi mạnh mẽ[cite: 12, 13, 21].

## 🔬 Core Technical & Research Focus
Trong dự án này, nhóm đặt trọng tâm nghiên cứu và giải quyết các bài toán kỹ thuật thực tế sau:
* [cite_start]**Kiến trúc & Cơ sở dữ liệu:** Thiết kế cơ sở dữ liệu liên kết đa tầng (Chuỗi rạp - Chi nhánh - Phim - Phòng - Suất chiếu - Ghế) trên SQL Server[cite: 7, 17]. [cite_start]Hệ thống API RESTful được xử lý bất đồng bộ thông qua Node.js và framework Express.js[cite: 8, 15].
* [cite_start]**Bài toán đồng thời (Concurrency Control):** Đảm bảo tính toàn vẹn dữ liệu, khóa ghế tạm thời (real-time) khi có nhiều khách hàng cùng truy cập và chọn một vị trí ghế tại cùng một thời điểm[cite: 7, 25, 50].
* [cite_start]**Xác thực & Bảo mật:** Sử dụng Middlewares kết hợp với JWT (JSON Web Token) để rẽ nhánh quyền truy cập an toàn cho từng nhóm đối tượng[cite: 26].

## 👥 System Roles & Features
[cite_start]Hệ thống phân chia quyền hạn rõ ràng dựa trên 3 nhóm tác nhân (Actors) cốt lõi[cite: 29]:

1. [cite_start]**Guest (Khách vãng lai):** Tra cứu thông tin danh sách phim, chi nhánh rạp, lịch chiếu, các chính sách ưu đãi và đăng ký tài khoản mới[cite: 30, 31, 35, 36, 38].
2. [cite_start]**Customer (Khách hàng thành viên):** Lựa chọn chi nhánh, đặt vé, chọn ghế trực tiếp trên sơ đồ phòng chiếu thời gian thực, mua combo bắp nước, áp dụng voucher, thanh toán trực tuyến và nhận vé điện tử bằng QR Code[cite: 42, 48, 49, 51, 53, 56].
3. [cite_start]**Admin (Quản trị viên hệ thống):** Quản lý toàn diện thông tin rạp, cấu hình phòng chiếu (Ghế thường, VIP, Couple), thiết lập lịch chiếu (tự động cảnh báo trùng giờ), quản lý doanh thu và kiểm duyệt đánh giá từ người dùng[cite: 60, 62, 63, 66, 73, 74].

💡 **Tính năng tích hợp AI đột phá:**
* [cite_start]**Recommendation AI:** Gợi ý phim cá nhân hóa dựa trên lịch sử và sở thích bằng Collaborative Filtering[cite: 77, 78, 79].
* [cite_start]**AI Chatbot:** Hỗ trợ giải đáp, tra cứu lịch chiếu và hướng dẫn đặt vé 24/7 thông qua NLP[cite: 84, 85, 86].
* [cite_start]**Demand Prediction AI:** Phân tích dữ liệu lịch sử để dự đoán nhu cầu lượng khách, từ đó tối ưu hóa số lượng suất chiếu[cite: 91, 92].

## 🚀 Installation & Setup Instructions
Để triển khai và chạy thử nghiệm hệ thống tại môi trường cục bộ (Local), vui lòng làm theo các bước sau:

### 1. Yêu cầu hệ thống (Prerequisites)
* [cite_start]**Môi trường chạy:** [Node.js](https://nodejs.org/) [cite: 15] (Khuyến nghị phiên bản LTS).
* [cite_start]**Trình soạn thảo mã nguồn:** [Visual Studio Code (VS Code)](https://code.visualstudio.com/)[cite: 16].
* [cite_start]**Trình quản lý cơ sở dữ liệu:** SQL Server (Quản lý trực tiếp qua Azure Data Studio)[cite: 17, 18].

### 2. Các bước cài đặt
1. **Clone mã nguồn từ GitHub Repository:**
   ```bash
   git clone [https://github.com/FUSU26SWR302/project-course-team-4.git](https://github.com/FUSU26SWR302/project-course-team-4.git)
   cd project-course-team-4
