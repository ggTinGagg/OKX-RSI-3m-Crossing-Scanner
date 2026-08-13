# OKX RSI 3m Crossing Scanner v1.0.6

Bản sửa lỗi cho dự án OKX RSI 3m Crossing Scanner.

- Top 50 USDT perpetual theo `volCcy24h` của OKX.
- RSI Wilder 14 trên nến 3 phút đã đóng.
- Chỉ hiển thị coin vừa crossing RSI 70/30.
- Quét lại mỗi 1 phút khi trang đang mở.
- Tính đòn bẩy = ceil(10 / thân nến (%) lớn nhất) trong 10 nến 3 phút hoàn tất, gồm cả nến tín hiệu.
- Thân nến (%) = |Close - Open| / Open × 100; không tính râu.
- Bản này sửa lỗi hiển thị `0/50` khi thực tế đã quét đủ 50 coin nhưng không có tín hiệu.
- Bản này cũng sửa bộ đếm nến từ 15 phút thành 3 phút và bỏ phụ thuộc vào các file asset không có trong gói.


## v1.0.6
- Giữ nguyên logic và dữ liệu quét của v1.0.1.
- Chỉ chỉnh tên 5 cột thành: COIN, Đòn bẩy, RSI, Delta RSI, Trạng thái.


## v1.0.6
- Khôi phục thông báo trình duyệt bằng Service Worker.
- Không còn chờ vô hạn ở `serviceWorker.ready` khi chưa đăng ký Service Worker.
- Lịch sử cảnh báo được lưu trước khi gửi notification nên vẫn hoạt động kể cả khi trình duyệt chặn notification.
- Giữ nguyên logic quét RSI 3m crossing và 5 cột: COIN, Đòn bẩy, RSI, Delta RSI, Trạng thái.


## v1.0.6
- Giữ nguyên toàn bộ logic của v1.0.4.
- Chỉ sửa cách chọn Top 50: với USDT perpetual, lấy `volCcy24h` (khối lượng 24h theo đồng cơ sở) nhân với `last` để quy đổi thành giá trị giao dịch 24h xấp xỉ bằng USDT, sau đó sắp xếp giảm dần và lấy 50 coin đầu.
- Không thay đổi logic RSI crossing 3m, đòn bẩy, thông báo, lịch sử cảnh báo hay giao diện.


### v1.0.6
- Quét chính 5 giây sau khi nến 3 phút đóng.
- Vẫn giữ quét bổ sung mỗi 60 giây khi trang đang mở.
- Chỉ hiển thị/thông báo tín hiệu có đòn bẩy ≤ 30×; tín hiệu > 30× bị bỏ qua.
