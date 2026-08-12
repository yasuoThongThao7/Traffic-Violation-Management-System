# Traffic Violation Management System

Một hệ thống quản lý vi phạm giao thông viết bằng C# (.NET / ASP.NET Core). Ứng dụng cho phép ghi nhận, theo dõi và xử lý vi phạm giao thông, lưu trữ bằng chứng (hình ảnh / video) và sinh báo cáo thống kê.

---

## Mục lục

- [Tính năng](#tính-năng)  
- [Công nghệ sử dụng](#công-nghệ-sử-dụng)  
- [Yêu cầu trước](#yêu-cầu-trước)  
- [Cài đặt](#cài-đặt)  
- [Cấu hình](#cấu-hình)  
- [Cơ sở dữ liệu & Migration](#cơ-sở-dữ-liệu--migration)  
- [Chạy ứng dụng](#chạy-ứng-dụng)  
- [Kiểm thử](#kiểm-thử)  
- [Đóng góp](#đóng-góp)  
- [Giấy phép](#giấy-phép)  
- [Liên hệ](#liên-hệ)

---

## Tính năng

- Ghi nhận hồ sơ vi phạm (thời gian, địa điểm, loại vi phạm).  
- Quản lý thông tin phương tiện và người vi phạm.  
- Tải lên và lưu trữ bằng chứng (hình ảnh, video).  
- Tạo quyết định xử phạt và theo dõi trạng thái (mới / đang xử lý / đã xử lý).  
- Tìm kiếm, lọc, phân trang danh sách vi phạm.  
- Báo cáo thống kê: theo khu vực, theo loại vi phạm, theo khoảng thời gian.  
- Phân quyền cơ bản: Admin, Officer, Viewer.  
- API RESTful cho các thao tác chính (nếu dự án là Web API).

## Công nghệ sử dụng

- Ngôn ngữ: C#  
- Framework: ASP.NET Core / .NET 6+  
- ORM: Entity Framework Core (nếu có)  
- Cơ sở dữ liệu: SQL Server / PostgreSQL / SQLite (tùy cấu hình)  
- Thư viện phổ biến: AutoMapper, Serilog, FluentValidation, JWT authentication (nếu áp dụng)

## Yêu cầu trước

- .NET SDK 6.0 hoặc 7.0  
- Một DB tương thích (SQL Server, PostgreSQL hoặc SQLite)  
- (Tùy chọn) Docker & Docker Compose nếu repo hỗ trợ container

## Cài đặt

1. Clone repository:
   git clone https://github.com/yasuoThongThao7/Traffic-Violation-Management-System.git
   cd Traffic-Violation-Management-System

2. Restore và build:
   dotnet restore
   dotnet build --configuration Release

(Nếu repo có nhiều project, chuyển vào thư mục project Web trước khi chạy.)

## Cấu hình

- Mở file `appsettings.json` hoặc `appsettings.Development.json` để cấu hình connection string, JWT và các thông số lưu file.

Ví dụ (SQL Server):
```json
"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=TrafficViolationDB;Trusted_Connection=True;"
}
