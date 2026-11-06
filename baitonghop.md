# (Bài tập tổng hợp) Hành Trình Xử Lý 1 Lỗi Cài Đặt Thật
### **Phần 1 –** Googling đúng cách
1. 1 Tìm kiếm có chiến thuật 
Khi gõ npm -v và nhận về thông báo lỗi kinh điển trên Terminal (PowerShell/CMD):
'npm' is not recognized as an internal or external command, operable program or batch file.
Thay vì gõ cụt ngủn cả câu thông báo lỗi, ta thu hẹp phạm vi tìm kiếm bằng các toán tử nâng cao:
Sử dụng site: để lọc kết quả ưu tiên từ nguồn uy tín
Sử dụng dấu ngoặc kép "" để ép trình duyệt tìm chính xác cụm từ khóa lỗi kỹ thuật.
Sử dụng dấu trừ - để loại bỏ các bài viết cũ không liên quan (ví dụ: -windows 7).
### **phần 2** Thẩm định câu trả lời trên StackOverflow
- Dấu tích xanh: đây là câu trả lời được chủ thớt xác nhận
- điểm số : ưu tiên câu trả lời có số vote cao, vì đã được cộng đồng kiểm chứng
- tính thời gian: kiểm tra xem câu trả lời cho Windowns 10/11 hay các phiên bản quá cũ
- khu vực bình luận : đọc phần bình luận phía dưới câu trả lời để phát hiện các lỗi phát sinh hoặc lưu ý bảo mật
### **Phần 3** hỏi AI đúng cách và nhận diện rủi ro 
[CONTEXT]
Tôi vừa cài đặt Node.js phiên bản mới nhất trên máy tính xách tay Windows 11 dùng hệ điều hành sạch. Khi mở Visual Studio Code Terminal để kiểm tra, tôi gặp sự cố không gọi được lệnh npm.
[RAW ERROR]
'npm' is not recognized as an internal or external command,
operable program or batch file.
[INSTRUCTION]
1. Giải thích nguyên nhân tại sao Windows 11 báo lỗi không tìm thấy lệnh npm dù quá trình cài đặt đã hoàn tất.
2. Hướng dẫn chi tiết từng bước kiểm tra và thêm đường dẫn vào Environment Variables (PATH) trên Windows 11 bằng giao diện đồ họa.
### **Phần 4**  Viết Bug Report chuẩn để nhờ hỗ trợ
### 1. Môi trường (Environment)
- Hệ điều hành: Windows 11 Home (64-bit)
- Công cụ: VS Code Terminal (PowerShell)
- Phiên bản Node.js: v22.x LTS (Mới tải trực tiếp từ trang chủ nodejs.org)

### 2. Các bước tái tạo (Steps to Reproduce)
1. Tải và cài đặt file `.msi` của Node.js với tùy chọn mặc định (Next -> Next -> Install).
2. Mở phần mềm VS Code, bật cửa sổ Terminal mới.
3. Gõ câu lệnh kiểm tra: `node -v` (chạy thành công, hiển thị phiên bản).
4. Gõ câu lệnh kiểm tra: `npm -v` (gặp lỗi).

### 3. Kết quả mong đợi vs. Thực tế (Expected vs. Actual)
- **Mong đợi:** Terminal trả về chuỗi phiên bản của npm (ví dụ: `10.x.x`).
- **Thực tế:** Terminal báo lỗi `'npm' is not recognized as an internal or external command...`.

### 4. Nhật ký lỗi / Minh chứng (Logs & Screenshots)
PS C:\Users\Tram> npm -v
npm : The term 'npm' is not recognized as the name of a cmdlet, function, script file, or operable program.
Check the spelling of the name, or if a path was included, verify that the path is correct and try again.
At line:1 char:1
+ npm -v
+ ~~~
    + CategoryInfo          : ObjectNotFound: (Error: Báo lỗi không tìm thấy lệnh)