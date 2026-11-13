# Tri-Entertainment

Bảng điều khiển 3D dạng isometric. Nó vẽ quy trình làm video ngắn (TikTok, Facebook Reels) bằng AI thành một **phòng ban ảo**: mỗi bước là một phòng kính, hạt sáng chạy theo luồng việc từ trái sang phải, và mọi bản dựng đều đi qua bàn **Trưởng phòng · Duyệt** trước khi đăng.

**Xem trực tiếp:** https://TEN-CUA-BAN.github.io/TEN-REPO/  ← thay bằng link GitHub Pages của bạn


## Có gì trong trang
- 11 phòng: Tiếp nhận → Biên kịch → Tìm & tải tư liệu → Chụp/Ảnh · Thu âm · Nhạc → Dựng phim → Kiểm duyệt (QC) → Trưởng phòng · Duyệt → Xuất bản TikTok / Facebook
- Phòng đang chạy thì sáng lên: tường phát sáng, màn hình chạy chữ, vòng xoay dưới bàn, thanh phần trăm tiến độ
- Mỗi khi một phòng xong việc, một đợt hạt sáng chạy sang phòng kế tiếp. Lúc duyệt đạt thì có xung vàng.
- Dòng sự kiện chạy ngang phía trên, bảng "Báo cáo" tự tổng hợp, thanh trạng thái phía dưới đếm số việc chờ
- Kéo để xoay, Shift + kéo để dời, cuộn để phóng to, bấm vào phòng để xem chi tiết

## Chế độ demo
Trên GitHub Pages không có dữ liệu thật, nên trang tự chạy **chế độ demo**: một quy trình mô phỏng lặp lại liên tục, có thông báo, phần trăm và thời gian giống lúc chạy thật, thỉnh thoảng có một bản bị trả lại để dựng lại. Bấm **⏸ Tạm dừng** ở góc phải dưới để dừng hoặc chạy tiếp.

Khi chạy trên máy có file `events.jsonl` nằm cạnh `index.html` (mỗi dòng là một sự kiện JSON, ví dụ `{"t":1700000000000,"room":"dung","status":"progress","msg":"Cắt cảnh 12/31","pct":39}`), trang sẽ đọc file đó mỗi giây và hiện trạng thái thật thay cho demo.

## Bật GitHub Pages
1. Vào repo trên github.com, chọn **Settings → Pages**.
2. Ở mục **Build and deployment**, phần **Source**, chọn **Deploy from a branch**.
3. Ở **Branch**, chọn `main` và thư mục `/ (root)`, rồi bấm **Save**.
4. Chờ 1–2 phút rồi mở `https://TEN-CUA-BAN.github.io/TEN-REPO/`. Dán link này vào dòng "Xem trực tiếp" ở trên.

## Kỹ thuật
Chỉ có một file HTML: canvas 2D tự vẽ hình isometric, không dùng thư viện và không cần build.
