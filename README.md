# Hệ Thống Quản Lý Nội Thất - Dự Án Web

## 1. Yêu cầu hệ thống

### 1.1. Các công cụ sử dụng

| Tool           | Name                              |
| -------------- | --------------------------------- |
| Environment    | ASPNETCORE\_ENVIRONMENT, NodeJS   |
| IDE            | Visual Studio Code, Visual Studio |
| Database       | SQL Server                        |
| Source Control | GitHub, Docker Hub                |

### 1.2. Yêu cầu môi trường

Để chạy được project trên môi trường local, cần chuẩn bị máy tính với các công cụ sau:

* Cài đặt `npm`
* Cài đặt `ReactJS`, `NodeJS`, `TypeScript`
* Cài đặt `SQL Server` và `SQL Server Management Studio`
* Có `Windows Terminal` hoặc `Command Prompt`
* Có `Visual Studio Code` và `Visual Studio 2022`

---

## 2. Các bước tiến hành

### 2.1. Chạy với môi trường localhost

#### Backend

1. Clone project backend từ GitHub
   ✨ *(Link GitHub backend ở đây)*
2. Dùng Visual Studio mở project backend
3. Mở PowerShell và chạy lệnh:

   ```bash
   dotnet run
   ```

#### Frontend (User, Admin)

1. Clone project frontend user từ GitHub
   ✨ *(Link GitHub frontend user ở đây)*
2. Clone project frontend admin từ GitHub
   ✨ *(Link GitHub frontend admin ở đây)*
3. Mở từng folder frontend bằng Visual Studio Code
4. Trong từng folder, chạy lệnh sau để cài đặt và khởi chạy:

   ```bash
   npm install
   npm run
   ```

---

### 2.2. Chạy với môi trường networking (Production)

1. Mua VPS hoặc thuê dịch vụ (Ví dụ: [vpssieutoc.vn](https://vpssieutoc.vn/clientarea.php)), cài đặt hệ điều hành Ubuntu 19.
2. Tải toàn bộ source code (backend, frontend user, frontend admin) vào cùng một thư mục trên VPS, bao gồm cả các file Docker Compose.
3. Chạy lệnh sau để build và chạy container:

   ```bash
   docker-compose -f docker-compose-frontend.yml up -d --build
   docker-compose -f docker-compose-backend.yml up -d --build
   ```
4. Thuê tên miền tại [tenten.vn](https://tenten.vn/vi) hoặc dịch vụ khác.
5. Map tên miền và port trong cấu hình Docker.
   ✨ **Tên miền sử dụng**: [noithatvn.click](http://noithatvn.click)

---

## 3. Cấu trúc thư mục

```plaintext
project-root/
│
├── backend/               # Source code backend (ASP.NET Core)
│
├── frontend-user/         # Source code frontend giao diện người dùng (ReactJS)
│
├── frontend-admin/        # Source code frontend giao diện admin (ReactJS)
│
├── ...
├── ...
└── README.md
```

---

## 4. Thông tin liên hệ

* **Nhóm phát triển**: \Nhóm Nguyễn Tấn Phát(21110911) - Trần Tuấn Anh(21110369) KLTN Khóa K21 CNPM SPKT
* **Email**: 21110911@student.hcmute.edu.vn || 21110369@student.hcmute.edu.vn
* **Ngày cập nhật**: 12-06-2025

## License

[MIT](https://choosealicense.com/licenses/mit/)
