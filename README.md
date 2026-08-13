# OKX RSI 3m Crossing Scanner v1.0.3

Bản sửa lỗi cho dự án OKX RSI 3m Crossing Scanner.

- Top 50 USDT perpetual theo `volCcy24h` của OKX.
- RSI Wilder 14 trên nến 3 phút đã đóng.
- Chỉ hiển thị coin vừa crossing RSI 70/30.
- Quét lại mỗi 1 phút khi trang đang mở.
- Tính đòn bẩy = ceil(10 / thân nến (%) lớn nhất) trong 10 nến 3 phút hoàn tất, gồm cả nến tín hiệu.
- Thân nến (%) = |Close - Open| / Open × 100; không tính râu.
- Bản này sửa lỗi hiển thị `0/50` khi thực tế đã quét đủ 50 coin nhưng không có tín hiệu.
- Bản này cũng sửa bộ đếm nến từ 15 phút thành 3 phút và bỏ phụ thuộc vào các file asset không có trong gói.


## v1.0.3
- Giữ nguyên logic và dữ liệu quét của v1.0.1.
- Chỉ chỉnh tên 5 cột thành: COIN, Đòn bẩy, RSI, Delta RSI, Trạng thái.
