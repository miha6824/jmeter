# Báo cáo JMeter
Thời gian phản hồi (Response Time)

📌Lần chạy 1:
+ Trung bình (Average): 581ms
+ Tối thiểu (Min): 245ms
+ Tối đa (Max): 21670ms
+ Độ lệch chuẩn (Std. Dev.): 2326.01ms

📌Lần chạy 2:
+ Trung bình (Average): 657ms
+ Tối thiểu (Min): 26ms
+ Tối đa (Max): 21632ms
+ Độ lệch chuẩn (Std. Dev.): 2583.64ms

📌 Nhận xét:
+ Độ trễ trung bình tăng lên từ 581ms → 657ms ở lần chạy sau, cho thấy có sự thay đổi về tải hoặc tài nguyên hệ thống.
+ Thời gian phản hồi tối đa rất cao (trên 21 giây), có thể do một số request bị nghẽn hoặc quá tải tạm thời.
2. Thông lượng (Throughput)
+ Lần chạy 1: 31.6 requests/giây
+ Lần chạy 2: 42.8 requests/giây

📌 Nhận xét:
+ Throughput đã tăng từ 31.6 lên 42.8, cho thấy hệ thống có thể xử lý nhiều yêu cầu hơn ở lần chạy thứ hai.
+ Tuy nhiên, nếu throughput tăng mà thời gian phản hồi cũng tăng, có thể hệ thống đang bị tải cao hơn.
3. Tỷ lệ lỗi (Error Rate)
+ Lần chạy 1: 0.00% (không có lỗi)
+ Lần chạy 2: 0.29% (một số lỗi xuất hiện)

📌 Nhận xét:
+ Tỷ lệ lỗi 0.29% là rất nhỏ nhưng có thể do một số request bị timeout hoặc lỗi từ server.
+ Nếu hệ thống tiếp tục tăng tải, cần kiểm tra kỹ hơn để tránh lỗi gia tăng.
4. Tốc độ truyền dữ liệu

📌Lần chạy 1:
+ Nhận: 674.15 KB/s
+ Gửi: 7.35 KB/s

📌Lần chạy 2:
+ Nhận: 910.31 KB/s
+ Gửi: 9.93 KB/s

📌 Nhận xét:
+ Tốc độ nhận và gửi dữ liệu tăng ở lần chạy 2, có thể do tăng lượng request hoặc dung lượng dữ liệu phản hồi.
+ Nếu tiếp tục tăng, có thể ảnh hưởng đến băng thông hoặc tải máy chủ

Kết luận về hiệu suất
✅ Ưu điểm:

✔️ Throughput tăng từ 31.6 lên 42.8 request/s, cho thấy hệ thống có thể xử lý tải cao hơn.

✔️ Tỷ lệ lỗi vẫn thấp (0.29%), chưa có dấu hiệu lỗi nghiêm trọng.

⚠️ Nhược điểm & Cảnh báo:

❗ Thời gian phản hồi tối đa cao (~21 giây), có thể gây trải nghiệm kém cho người dùng.

❗ Độ lệch chuẩn lớn (~2300ms+), phản ánh sự không ổn định trong thời gian phản hồi.

❗ Nếu tải tiếp tục tăng, hệ thống có thể gặp vấn đề về hiệu suất hoặc tài nguyên.
- Với số lượng 20 người:
![Mô tả ảnh](https://github.com/miha6824/image/blob/main/Screenshot%202025-02-08%20154750.png)
![Mô tả ảnh](https://github.com/miha6824/image/blob/main/Screenshot%202025-02-08%20154808.png)
- Với số lượng 30 người:
![Mô tả ảnh](https://github.com/miha6824/image/blob/main/Screenshot%202025-02-08%20155257.png)
![Mô tả ảnh](https://github.com/miha6824/image/blob/main/Screenshot%202025-02-08%20155316.png)
# Câu hỏi thảo luận:
1. Tại sao kiểm thử phi chức năng lại quan trọng trong phần mềm?
- Kiểm thử phi chức năng giúp đảm bảo phần mềm không chỉ hoạt động đúng về mặt chức năng mà còn đáp ứng các yêu cầu về hiệu suất, bảo mật, khả năng mở rộng, tính ổn định và khả năng sử dụng.

2. Các thông số quan trọng cần theo dõi trong kiểm thử hiệu suất
- Thời gian phản hồi (Response Time): Thời gian hệ thống xử lý và phản hồi một yêu cầu.
- Thông lượng (Throughput): Số lượng yêu cầu mà hệ thống có thể xử lý trong một khoảng thời gian nhất định.
- Sử dụng tài nguyên (Resource Utilization): Mức độ sử dụng CPU, RAM, băng thông mạng, ổ đĩa.
- Số lượng người dùng đồng thời (Concurrent Users): Số lượng người dùng có thể truy cập hệ thống cùng lúc mà không ảnh hưởng đến hiệu suất.
- Tỷ lệ lỗi (Error Rate): Số lượng lỗi xảy ra trong quá trình xử lý yêu cầu.

3. Nếu hệ thống không đáp ứng yêu cầu hiệu suất, bạn sẽ đề xuất giải pháp gì?
- Tối ưu hóa mã nguồn: Kiểm tra và cải tiến thuật toán, giảm số lượng truy vấn không cần thiết.
- Tối ưu hóa cơ sở dữ liệu: Sử dụng indexing, caching, tối ưu hóa truy vấn SQL.

