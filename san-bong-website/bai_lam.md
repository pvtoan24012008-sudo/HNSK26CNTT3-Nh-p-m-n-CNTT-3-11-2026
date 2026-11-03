# BÀI LÀM – HACKATHON 02

- **Mã đề:** 01
- **Họ tên:Phạm Viết Toàn **
- **Lớp:CNTT3**
- **Link repository:**
- **Hệ điều hành (Windows/macOS):Windows**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
ls -Force
mv .\ghi_chu_ban_giao.txt .\docs
mkdir backup
cp .\data\dat_san_thang_10.xlsx .\backup
rm .\temp_002.tmp
cd logs
ls
cd.. 
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
Directory:
    C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap\starter-kit\starter-kit\san-bong-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         11/3/2026   2:12 PM                backup
d-----         11/3/2026   2:01 PM                data
d-----         11/3/2026   2:07 PM                docs
d-----         11/3/2026   1:59 PM                evidence
d-----         11/3/2026   2:01 PM                logs
d-----         11/3/2026   1:49 PM                web
-a----         11/3/2026   1:49 PM             76 .env
-a----         11/3/2026   1:49 PM           2409 bai_lam.md


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap\starter-kit\starter-kit\san-b
    ong-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   1:49 PM           6074 dat_san_thang_10.xlsx


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap\starter-kit\starter-kit\san-b
    ong-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   1:49 PM           6074 dat_san_thang_10.xlsx


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap\starter-kit\starter-kit\san-b
    ong-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   1:49 PM            154 ghi_chu_ban_giao.txt


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap\starter-kit\starter-kit\san-b
    ong-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   1:49 PM            956 access.log


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap\starter-kit\starter-kit\san-b
    ong-website\web


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         11/3/2026   1:49 PM                images
-a----         11/3/2026   1:49 PM            590 app.js
-a----         11/3/2026   1:49 PM            529 index.html
-a----         11/3/2026   1:49 PM            460 style.css


    Directory: C:\Users\Dell\Downloads\starter-kit\starter-kit\starter-kit\trung-tam-tieng-anh\Luyen_Tap\starter-kit\starter-kit\san-b
    ong-website\web\images


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/3/2026   1:49 PM           3101 logo-san-bong.png
```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```shell
Get-Content .\logs\access.log | Select-String "status=500" > .\logs\loi_500.txt
Get-Content .\logs\loi_500.txt -Head 3
```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
2026-10-28 08:24:34 POST /api/thanh-toan status=500
2026-10-28 08:28:45 POST /api/thanh-toan status=500
```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
(Get-Content .\logs\access.log | Select-String "status=404"). Count
```

```text
4
```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
.\tong_hop.ps1
```

### Nội dung file logs/tong_hop.txt

```text
Dang tao bao cao...
Hoan thanh!
```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)~~strikethrough text~~
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 |  |  |  |
| 2 |  |  |  |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/dat_san_thang_10.xlsx`, không cần ghi vào đây.
