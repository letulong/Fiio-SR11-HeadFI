# 🎧 FiiO SR11 HeadFi Edition

Firmware audiophile tùy biến cho **FiiO SR11 Hi-Res Network Streamer** — bản **Beta** dành cho cộng đồng thử nghiệm.

> ⚠️ Kho này **chỉ phân phối firmware đã đóng gói** (không kèm mã nguồn). Vui lòng tải file trong mục **Releases**.

---

## ✨ Tính năng nổi bật (Beta V678)

- **HQPlayer NAA engine** bản địa: bit-perfect PCM 44.1k–768kHz · DSD64–DSD512 (Native & DoP), tự hồi phục, ưu tiên thời gian thực (SCHED_FIFO, ghim lõi CPU chuyên audio)
- **Web UI audiophile** 4 ngôn ngữ (EN/VI/ZH/RU) — điều khiển chế độ, ngõ xuất, theo dõi tín hiệu trung thực
- **Thư viện nhạc USB**: cắm ổ cứng là tự động quét & dựng thư viện (hàng chục nghìn bài), duyệt theo Album / Nghệ sĩ / Bài hát, tab Hi-Res riêng cho DSD
- **Rescue Hotspot**: mất mạng >20 giây → máy tự phát Wi-Fi `FiiO-SR11-Setup` (10.0.0.10) **kèm DHCP đầy đủ** — lấy điện thoại vào là cấu hình lại mạng được ngay
- **LCD mặt trước thông minh**: hiện NAA/LMS/SETUP khi rảnh; nhường màn hình gốc khi đang phát nhạc
- **Khóa bảo mật cứng**: bản cài mới không mở telnet/FTP; xác thực web tùy chọn (mặc định tắt cho LAN nhà — bật bằng `"web_auth": true` nếu muốn có PIN hiển thị trên LCD)

## 📦 Cài đặt (chỉ 1 file)

1. Tải **`FiiO_SR11_ZenStream_V678_Custom_OTA.zip`** trong mục [Releases](../../releases)
2. Chép file zip vào **gốc USB** (FAT32 hoặc exFAT)
3. Cắm USB vào SR11 → máy hiện hỏi cập nhật → đồng ý → **~2 phút** tự nạp & khởi động lại
   - Nếu máy không nhận gói: đổi tên file thành `SR11_update_v678.zip` rồi cắm lại
4. Mở trình duyệt: `http://sr11.local` hoặc IP hiển thị trên LCD

**Đang chạy ZenStream V640?** Cấu hình & thư viện trong máy được giữ nguyên.

**Quay về firmware gốc:** flash lại zip gốc FiiO (`SR11_update_v6xx.zip`) cùng cách — bất cứ lúc nào.

## 🔐 Kiểm tra file trước khi cài (khuyến nghị)

Xem MD5 / SHA-256 trong ghi chú Release và so khớp:
- macOS: `md5 ten-file.zip`
- Windows: `certutil -hashfile ten-file.zip MD5`

## ⚠️ Lưu ý Beta

- Dành cho SR11 đang ở firmware gốc **V630/V640** hoặc ZenStream V640
- Chế độ **Squeezelite/LMS** chưa kèm binary trong bản này — chọn sẽ nhận thông báo rõ ràng (không ảnh hưởng chế độ khác)
- Nạp firmware là rủi ro của người dùng: nguồn điện ổn định, **không rút USB giữa chừng**
- Báo lỗi / trao đổi: mục **Discussions** hoặc Issues của kho này

---
*FiiO SR11 HeadFi Edition · Beta Community Release · phân phối chỉ qua Releases*
