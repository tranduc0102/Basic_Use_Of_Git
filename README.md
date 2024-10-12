# Hướng Dẫn Sử Dụng Git

## 1. Git là gì? 
Git là hệ thống quản lý phiên bản (VCS - Version Control System) giúp kiểm soát các thay đổi, phiên bản của dự án, bao gồm ai thực hiện thay đổi, khi nào và tại sao. Git cũng cho phép khôi phục lại các phiên bản trước của dự án.

### Nguyên tắc làm việc của Git:
- Kho lưu trữ trung tâm (repository).
- Lấy dữ liệu về, thực hiện công việc, và cập nhật lên kho trung tâm.
- Công cụ để giải quyết các xung đột (conflict).

### Lợi ích của Git:
- Đảm bảo không làm hỏng phiên bản hiện tại.
- Giúp cộng tác với nhiều người.
- Phát triển phiên bản mới mà không ảnh hưởng đến phiên bản cũ.
- Khôi phục lại phiên bản trước bất kỳ lúc nào.

Git ≠ GitHub: GitHub chỉ là kho lưu trữ trực tuyến hỗ trợ các công nghệ của Git.

### Cài đặt Git:
Truy cập [Git-SCM.com](https://git-scm.com) để tải về và cài đặt.

## 2. Các câu lệnh cơ bản của Git

### Các câu lệnh terminal cơ bản:
- `cd <thư_mục>`: Thay đổi thư mục làm việc.
- `cd ..`: Quay lại thư mục cha.
- `mkdir <thư_mục>`: Tạo thư mục mới.
- `touch <tên_file>`: Tạo một tệp tin mới.
- `rm <tên_file>`: Xóa file hoặc folder rỗng.
- `rm -rf <tên_file>`: Xóa tất cả các file trong thư mục.

### Các câu lệnh Git cơ bản:
- `git --help`: Hiện trợ giúp.
- `git --version`: Hiển thị phiên bản Git hiện tại.
- `git status`: Hiển thị trạng thái của kho lưu trữ.
- `git log`: Hiển thị lịch sử các commit.
- `git init [tên_repo]`: Tạo một kho lưu trữ Git mới.
- `git clone [repo] [tên_clone]`: Tạo một bản sao của repo.
- `git add <tệp>`: Thêm tệp vào index.
- `git add .`: Thêm tất cả các tệp.
- `git commit -m "<tin nhắn>"`: Tạo commit.
- `git push`: Đẩy commit lên remote repository.
- `git pull`: Lấy dữ liệu từ remote repository về local.

## 3. Xử lý lỗi conflict trong Git
Lỗi **conflict** xảy ra khi hai hoặc nhiều thay đổi mâu thuẫn với nhau, và Git không thể tự động hợp nhất (merge). Thường xảy ra khi bạn cố gắng merge hoặc pull các thay đổi từ remote vào nhánh hiện tại.

### Cách khắc phục:
Bạn cần mở file bị xung đột, xem xét sự khác biệt, và chọn giữ lại hoặc xóa phần nào theo nhu cầu. Sau đó commit lại kết quả đã sửa.

## 4. Làm việc với nhánh (Branch)
- `git branch <tên_nhánh>`: Tạo nhánh mới.
- `git checkout <tên_nhánh>`: Chuyển sang nhánh khác.
- `git branch -l`: Xem danh sách các nhánh.
- `git push -u origin <tên_nhánh>`: Tạo nhánh mới trên remote repository.
- `git merge <tên_nhánh>`: Kết hợp nhánh hiện tại với nhánh khác.

## 5. Kết nối với GitHub
1. Tạo repository trên GitHub.
2. Thêm remote:
   ```bash
   B1: Tạo một repository mới trên GitHub
   B2: Mở dự án cần push lên GitHub ở trong Git Bash
   B3: git remote add origin <link_repo_trên_github>
   B4: Cấu hình git
   B5: Chuyển sang nhánh chính git branch -M main
   B6: đẩy commit lên GitHub: git push -u origin main
   
