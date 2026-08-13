# OKX RSI 3m Crossing Scanner v1.0.0

Dự án mới, độc lập với dự án OKX RSI Scanner cũ.

## Chức năng

- Quét 50 USDT perpetual có khối lượng giao dịch lớn nhất trên OKX.
- RSI Wilder 14 trên khung 3 phút.
- Chỉ hiển thị coin khi RSI vừa vượt ngưỡng:
  - Quá mua: RSI nến trước <= 70 và RSI nến tín hiệu > 70.
  - Quá bán: RSI nến trước >= 30 và RSI nến tín hiệu < 30.
- Không hiển thị các coin đã nằm ngoài ngưỡng từ trước.
- Quét ngay khi nến 3 phút vừa đóng.
- Có quét bổ sung mỗi 1 phút khi trang đang mở.
- Đòn bẩy:
  - Lấy 10 nến 3 phút hoàn tất gần nhất, gồm 9 nến trước + nến tín hiệu.
  - Body % = |Close - Open| / Open × 100.
  - Lấy body % lớn nhất.
  - Leverage = ceil(10 / body % lớn nhất).
  - Bỏ qua râu nến.
- Các cột:
  1. Coin
  2. Đòn bẩy
  3. RSI
  4. Δ RSI
  5. Tín hiệu

## Cài trên GitHub Pages

1. Tạo một repository GitHub mới.
2. Upload `index.html`.
3. Vào Settings → Pages.
4. Chọn Deploy from a branch.
5. Chọn branch `main` và thư mục `/ (root)`.
6. Lưu lại và chờ GitHub Pages triển khai.

Dự án này không yêu cầu xóa hoặc sửa repository của dự án cũ.
