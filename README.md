[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Dj7qWeHQ)
# 📌 CineChain ERP – Cinema Chain Management & Online Ticketing System

## 📖 Introduction
CineChain ERP là hệ thống quản lý chuỗi rạp chiếu phim và đặt vé trực tuyến toàn diện, được phát triển trong khuôn khổ môn học Software Requirements (SWR302). Hệ thống giải quyết bài toán vận hành thực tế của các chuỗi rạp lớn, hỗ trợ đồng bộ dữ liệu lịch chiếu, quản lý doanh thu, quản lý phòng chiếu, thức ăn kèm (combo) và tối ưu hóa quy trình đặt vé trực tuyến cho khách hàng.

## 🔬 Research Based Learning (RBL) Focus
Trong dự án này, nhóm tập trung nghiên cứu và tối ưu sâu vào yếu tố **Kiến trúc hệ thống và Kiểm soát truy cập (System Architecture & Access Control)**:
* **Nội dung focus:** Nghiên cứu và triển khai hệ thống phân quyền dựa trên vai trò (Role-Based Access Control - RBAC) sử dụng cơ chế Filters và Listeners trong kiến trúc Java Web. Hệ thống phân tách nghiêm ngặt quyền hạn giữa các tầng người dùng: **Admin** (Quản trị hệ thống), **Manager** (Quản lý từng cụm rạp), và **Customer** (Khách hàng đặt vé).
* **Mục tiêu nghiên cứu:** Đảm bảo tính toàn vẹn của dữ liệu luồng đặt vé, ngăn chặn tình trạng xung đột tài nguyên khi nhiều khách hàng cùng đặt một ghế tại cùng một thời điểm (Concurrency Control) và bảo mật các endpoint quản trị chi nhánh.

## 👥 System Roles & Features
Hệ thống được thiết kế với 3 nhóm vai trò cốt lõi:
1. **Admin:** Quản lý danh mục phim, thể loại, chuỗi rạp trên toàn quốc, tài khoản nhân viên và thống kê doanh thu tổng.
2. **Manager (Quản lý rạp):** Điều phối lịch chiếu chi tiết cho từng phòng, cập nhật trạng thái phòng chiếu, quản lý kho bãi combo đồ ăn/thức uống tại chi nhánh phụ trách.
3. **Customer:** Tìm kiếm phim theo rạp/thời gian, chọn ghế trực thời gian thực, đặt combo và thực hiện quy trình thanh toán vé trực tuyến.

## 🚀 Installation & Setup Instructions
Để triển khai và chạy thử nghiệm hệ thống tại môi trường local, vui lòng làm theo các bước sau:

### 1. Yêu cầu hệ thống (Prerequisites)
* **Môi trường chạy:** [Node.js](https://nodejs.org/) (Khuyến nghị phiên bản LTS).
* **Trình soạn thảo mã nguồn:** [Visual Studio Code (VS Code)](https://code.visualstudio.com/).
* **Trình quản lý cơ sở dữ liệu:** SQL Server (Quản lý qua Azure Data Studio) hoặc cơ sở dữ liệu nhóm đang sử dụng.

### 2. Các bước cài đặt
1. **Clone mã nguồn từ GitHub Repository:**
   ```bash
   git clone [https://github.com/FUSU26SWR302/project-course-team-4.git](https://github.com/FUSU26SWR302/project-course-team-4.git)
   cd project-course-team-4
