# 🎧 FiiO SR11 HeadFi Edition

**Custom audiophile firmware for the FiiO SR11 Hi-Res Network Streamer** — Beta community release.
Kho này **chỉ phân phối firmware đóng gói** (không kèm mã nguồn). Tải file trong mục **[Releases](../../releases)**.

🌐 **Languages:** [🇻🇳 Tiếng Việt](#-tiếng-việt) · [🇬🇧 English](#-english) · [🇨🇳 中文](#-中文) · [🇷🇺 Русский](#-русский)

---

## 🇻🇳 Tiếng Việt

Firmware tùy biến cho **FiiO SR11** (Ingenic X2000, MIPS32r2) — nâng cấp trực tiếp từ firmware gốc V630/V640 **qua USB, chỉ với 1 file zip**, không cần công cụ hay máy tính sau khi tải file.

### ✨ Tính năng mới so với firmware gốc

| Nhóm | Firmware gốc FiiO | HeadFi Edition (Beta V678) |
|---|---|---|
| **HQPlayer NAA** | ❌ Không có | ✅ Engine bản địa `naa-sr11d`: PCM 44.1k–768kHz · DSD64–DSD512 (Native & DoP), bit-perfect, tự hồi phục khi treo, ưu tiên thời gian thực (SCHED_FIFO + ghim lõi CPU chuyên audio) |
| **Web quản lý** | Giao diện cơ bản | ✅ Web UI audiophone 4 ngôn ngữ (EN/VI/ZH/RU), 7 theme — đổi chế độ, ngõ xuất, Wi-Fi, xem telemetry trung thực (không số bịa) |
| **Thư viện USB** | Duyệt file đơn thuần | ✅ Cắm ổ là **tự quét & dựng thư viện** (hàng chục nghìn bài): duyệt Album / Nghệ sĩ / Bài hát / Hi-Res, tìm kiếm, phát cả album/nghệ sĩ |
| **Mất mạng** | Máy "mù", phải cắm LAN | ✅ **Rescue Hotspot**: mất mạng >20 giây → tự phát Wi-Fi `FiiO-SR11-Setup` (10.0.0.10) **có DHCP đầy đủ** — điện thoại vào là cấu hình lại được ngay |
| **LCD mặt trước** | Chỉ hiện thị trạng thái gốc | ✅ Thông minh hơn: hiện `NAA`/`LMS`/`SETUP` khi rảnh; mã PIN ghép nối (khi bật xác thực); nhường màn hình gốc khi đang phát nhạc |
| **Khác** | Mở telnet/FTP root | ✅ Bản cài mới **khóa telnet/FTP** (chỉ mở khi cần debug); xác thực web tùy chọn kèm PIN trên LCD (mặc định tắt cho LAN nhà) |

### 📦 Cài đặt (1 file, ~2 phút)

1. Tải **`FiiO_SR11_ZenStream_V678_Custom_OTA.zip`** trong [Releases](../../releases)
2. Chép vào **gốc USB** (FAT32/exFAT) → cắm vào SR11 → máy hỏi cập nhật → đồng ý
   - Máy không nhận gói? Đổi tên file thành `SR11_update_v678.zip` rồi cắm lại
3. Sau khởi động: mở `http://sr11.local` hoặc IP hiển thị trên LCD

**Đang chạy ZenStream V640?** Nâng cấp tại chỗ — giữ nguyên cấu hình + thư viện.
**Quay về bản gốc:** flash zip gốc FiiO (`SR11_update_v6xx.zip`) cùng cách, bất cứ lúc nào.

### 🔐 Kiểm tra file trước khi cài (khuyến nghị)

MD5/SHA-256 ghi trong ghi chú Release — so khớp:
- macOS: `md5 ten-file.zip` · Windows: `certutil -hashfile ten-file.zip MD5`

### ⚠️ Giới hạn Beta

- Chế độ **Squeezelite/LMS**: chưa kèm binary — máy báo lỗi rõ ràng khi chọn (bản kế tiếp bổ sung)
- Đã kiểm chứng trên SR11 firmware gốc V630/V640 & ZenStream V640; các nền khác chưa test
- Nguồn điện ổn định khi flash, **không rút USB giữa chừng**. Nạp firmware là rủi ro của người dùng.

---

## 🇬🇧 English

Custom firmware for the **FiiO SR11** — upgrades directly from stock V630/V640 **via USB with a single zip file**. No tools needed after downloading.

### ✨ What's new vs. stock firmware

| Area | Stock FiiO | HeadFi Edition (Beta V678) |
|---|---|---|
| **HQPlayer NAA** | ❌ | ✅ Native `naa-sr11d` engine: PCM 44.1–768 kHz · DSD64–DSD512 (Native & DoP), bit-perfect, self-recovering pipeline, realtime scheduling pinned to a dedicated audio core |
| **Web manager** | Basic UI | ✅ Audiophile web UI, 4 languages (EN/VI/ZH/RU), 7 themes — modes, outputs, Wi-Fi, honest telemetry |
| **USB library** | Plain file browse | ✅ Auto-scan on plug: browse by Album / Artist / Track / Hi-Res, search, play album/artist |
| **Network loss** | Device unreachable | ✅ Rescue hotspot after 20 s: `FiiO-SR11-Setup` (10.0.0.10) **with full DHCP** — configure Wi-Fi right from your phone |
| **Front LCD** | Stock only | ✅ Smarter: `NAA`/`LMS`/`SETUP` badges, pairing PIN, yields to stock UI during playback |
| **Security** | telnet/FTP root open | ✅ Fresh installs keep telnet/FTP closed; optional web auth with LCD PIN (off by default) |

### 📦 Install (1 file, ~2 min)

1. Download **`FiiO_SR11_ZenStream_V678_Custom_OTA.zip`** from [Releases](../../releases)
2. Copy to the **root of a USB stick** (FAT32/exFAT) → plug into SR11 → confirm update
   - Not detected? Rename to `SR11_update_v678.zip` and replug
3. After reboot open `http://sr11.local` (or the IP shown on the LCD)

**On ZenStream V640?** In-place upgrade — settings and USB library are kept.
**Rollback:** flash the stock FiiO zip the same way, any time.

### ⚠️ Beta notes

- Squeezelite/LMS mode: binary not bundled yet — selecting it shows a clear error (coming next release)
- Verified on stock V630/V640 & ZenStream V640; other bases untested
- Stable power during flash, never unplug mid-flash. Flash at your own risk.

---

## 🇨🇳 中文

**FiiO SR11** 专用定制固件 — 从官方 V630/V640 固件 **通过 U 盘单个 zip 文件**直接升级,下载后无需任何工具。

### ✨ 相比官方固件的新功能

| 项目 | 官方固件 | HeadFi 版 (Beta V678) |
|---|---|---|
| **HQPlayer NAA** | ❌ | ✅ 原生 `naa-sr11d` 引擎:PCM 44.1–768kHz · DSD64–DSD512(原生 & DoP),位完美,掉线自动恢复,实时调度并独占音频核心 |
| **网页管理** | 基础界面 | ✅ 发烧友网页界面,4 种语言(英/越/中/俄),7 套主题 — 模式切换、输出、Wi-Fi、真实遥测 |
| **U 盘音乐库** | 普通文件浏览 | ✅ 插盘自动扫描建库:按专辑/艺术家/曲目/Hi-Res 浏览,搜索,整专辑播放 |
| **断网恢复** | 设备失联 | ✅ 断网 20 秒后自动开启救援热点 `FiiO-SR11-Setup`(10.0.0.10)**带完整 DHCP** — 手机即可重新配置 |
| **前面板 LCD** | 仅官方显示 | ✅ 更智能:待机显示 `NAA`/`LMS`/`SETUP`、配对 PIN;播放时让位给官方界面 |
| **安全性** | telnet/FTP root 常开 | ✅ 新安装默认关闭 telnet/FTP;可选网页认证(LCD 显示 PIN,默认关闭) |

### 📦 安装(1 个文件,约 2 分钟)

1. 在 [Releases](../../releases) 下载 **`FiiO_SR11_ZenStream_V678_Custom_OTA.zip`**
2. 复制到 **U 盘根目录**(FAT32/exFAT)→ 插入 SR11 → 确认升级
   - 未识别?把文件改名为 `SR11_update_v678.zip` 重新插入
3. 重启后浏览器打开 `http://sr11.local`(或 LCD 上显示的 IP)

**已是 ZenStream V640?** 原地升级 — 设置和音乐库保留。
**回滚:** 随时可按同样方式刷回官方固件 zip。

### ⚠️ Beta 说明

- Squeezelite/LMS 模式:暂未附带二进制 — 选择时会明确报错(下版补充)
- 已在官方 V630/V640 与 ZenStream V640 上验证;其他底包未测
- 刷机期间保持供电稳定,切勿中途拔出 U 盘。刷机风险自负。

---

## 🇷🇺 Русский

Кастомная прошивка для **FiiO SR11** — обновление со стоковой V630/V640 **через USB одним zip-файлом**, без дополнительных инструментов.

### ✨ Новое по сравнению со стоковой прошивкой

| Раздел | Сток FiiO | HeadFi Edition (Beta V678) |
|---|---|---|
| **HQPlayer NAA** | ❌ | ✅ Нативный движок `naa-sr11d`: PCM 44,1–768 кГц · DSD64–DSD512 (Native и DoP), bit-perfect, самовосстановление, realtime-планировщик с выделенным аудио-ядром |
| **Веб-панель** | Базовая | ✅ Аудиофильский веб-интерфейс, 4 языка (EN/VI/ZH/RU), 7 тем — режимы, выходы, Wi-Fi, честная телеметрия |
| **USB-библиотека** | Обзор файлов | ✅ Автоскан при подключении: Album / Artist / Track / Hi-Res, поиск, воспроизведение альбома/артиста |
| **Потеря сети** | Устройство недоступно | ✅ Спасательная точка через 20 с: `FiiO-SR11-Setup` (10.0.0.10) **с полным DHCP** — настройте Wi-Fi прямо с телефона |
| **LCD-дисплей** | Только сток | ✅ Умнее: значки `NAA`/`LMS`/`SETUP`, PIN-сопряжение; при воспроизведении уступает стоковому UI |
| **Безопасность** | telnet/FTP root открыты | ✅ При новой установке telnet/FTP закрыты; опциональная веб-аутентификация с PIN на LCD (по умолчанию выключена) |

### 📦 Установка (1 файл, ~2 мин)

1. Скачайте **`FiiO_SR11_ZenStream_V678_Custom_OTA.zip`** в [Releases](../../releases)
2. Скопируйте в **корень USB-накопителя** (FAT32/exFAT) → вставьте в SR11 → подтвердите обновление
   - Не определяется? Переименуйте в `SR11_update_v678.zip` и вставьте снова
3. После перезагрузки откройте `http://sr11.local` (или IP на дисплее)

**Уже ZenStream V640?** Обновление на месте — настройки и библиотека сохраняются.
**Откат:** в любой момент прошейте стоковый zip FiiO тем же способом.

### ⚠️ Замечания Beta

- Режим Squeezelite/LMS: бинарник пока не включён — при выборе будет ясная ошибка (в следующем выпуске)
- Проверено на стоке V630/V640 и ZenStream V640; другие базы не тестировались
- Стабильное питание при прошивке, не вынимайте USB во время процесса. Прошивка на свой риск.

---

*FiiO SR11 HeadFi Edition · Beta Community Release · распространение только через Releases*

