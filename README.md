# ⛏ MC Launcher Lite

> Launcher Minecraft nhẹ, đẹp, tối ưu cho máy yếu — hỗ trợ Vanilla · Forge · Fabric · Quilt · Offline Mode

![Version](https://img.shields.io/badge/version-1.0.0-brightgreen)
![Java](https://img.shields.io/badge/Java-17%2B-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)
![License](https://img.shields.io/badge/license-MIT-green)

---

## 📋 Mục lục

- [Yêu cầu hệ thống](#-yêu-cầu-hệ-thống)
- [Cài đặt & chạy](#-cài-đặt--chạy)
- [Tính năng](#-tính-năng)
- [Preset tối ưu](#-preset-tối-ưu)
- [Cấu trúc thư mục](#-cấu-trúc-thư-mục)
- [Hướng dẫn cài Minecraft](#-hướng-dẫn-cài-minecraft)
- [Mods khuyên dùng](#-mods-khuyên-dùng)
- [Build từ source](#-build-từ-source)
- [FAQ](#-faq)

---

## 💻 Yêu cầu hệ thống

| Thành phần | Tối thiểu | Khuyên dùng |
|------------|-----------|-------------|
| **Java**   | 17+       | 21 (LTS)    |
| **RAM**    | 1 GB      | 2 GB+       |
| **CPU**    | 2 nhân    | 4 nhân+     |
| **Ổ cứng** | 500 MB    | 2 GB+       |
| **OS**     | Windows 7+ / Linux / macOS | Windows 10+ |

> ⚠️ **Java 17+ bắt buộc.** Tải tại [adoptium.net](https://adoptium.net) (chọn JRE 21 LTS).

---

## 🚀 Cài đặt & chạy

### Windows

```bat
:: 1. Giải nén MCLauncherLite-v1.0.0-Windows.zip
:: 2. Double-click file:
MCLauncherLite.bat

:: Hoặc chạy thủ công:
java -jar MCLauncherLite.jar
```

### Linux / macOS

```bash
# Giải nén
unzip MCLauncherLite-v1.0.0-Linux.zip

# Cấp quyền và chạy
chmod +x MCLauncherLite.sh
./MCLauncherLite.sh

# Hoặc trực tiếp:
java -jar MCLauncherLite.jar
```

---

## ✨ Tính năng

### 🏠 Trang chủ
- Chọn phiên bản Minecraft từ danh sách Mojang API (tự động tải)
- Chọn Mod Loader: **Vanilla**, **Forge**, **Fabric**, **Quilt**
- 4 preset tối ưu một chạm
- Nút **Khởi động** và **Cài đặt phiên bản**
- Thanh tiến trình tải về real-time

### ⚙️ Cài đặt
- **RAM slider**: 512 MB → 8 GB
- **JVM Arguments**: tùy chỉnh thủ công hoặc dùng preset
- **Đường dẫn Java**: tự phát hiện hoặc chọn thủ công
- **Render distance**: 4 → 16 chunks
- **Chế độ đồ họa**: Fast / Fancy
- Bật/tắt: Đám mây, Hiệu ứng hạt, VSync
- Kích thước cửa sổ game

### 📦 Quản lý phiên bản
- Xem các version đã cài đặt
- Chọn version nhanh để launch

### 🧩 Mods
- Danh sách 11 mod tối ưu hiệu năng
- Hướng dẫn tải và cài đặt

### 📋 Nhật ký
- Xem output game theo thời gian thực
- Phát hiện lỗi dễ dàng

### 🔐 Offline Mode
- Chơi không cần tài khoản Mojang/Microsoft
- UUID ổn định theo tên người chơi (UUID v3)

---

## 🥔 Preset tối ưu

| Preset | RAM | Render | FPS Est. | Dành cho |
|--------|-----|--------|----------|----------|
| 🥔 **Khoai Tây** | 512 MB | 4 chunks | ~25 FPS | RAM ≤ 2GB, CPU cũ |
| 💻 **Máy Yếu**   | 1 GB   | 6 chunks | ~60 FPS | RAM 2-4GB |
| 🖥 **Trung Bình** | 2 GB   | 10 chunks| ~90 FPS | RAM 4-8GB |
| 🚀 **Máy Mạnh**  | 4 GB   | 16 chunks| ~120 FPS| RAM 8GB+  |

### JVM Args mặc định (Máy Yếu):
```
-XX:+UnlockExperimentalVMOptions
-XX:+UseG1GC
-XX:G1NewSizePercent=20
-XX:G1ReservePercent=20
-XX:MaxGCPauseMillis=50
-XX:G1HeapRegionSize=8m
-Dfml.ignorePatchDiscrepancies=true
```

---

## 📁 Cấu trúc thư mục

Launcher lưu dữ liệu tại:

| OS | Đường dẫn |
|----|-----------|
| Windows | `%APPDATA%\.mclauncher\` |
| Linux   | `~/.mclauncher/` |
| macOS   | `~/Library/Application Support/.mclauncher/` |

```
.mclauncher/
├── config.json          ← Cấu hình launcher
├── versions/
│   ├── 1.8.9/
│   │   ├── 1.8.9.jar
│   │   └── 1.8.9.json
│   └── 1.20.4/
├── libraries/           ← Thư viện Minecraft
├── assets/              ← Âm thanh, ngôn ngữ, texture
│   ├── indexes/
│   └── objects/
└── mods/                ← Đặt mod .jar vào đây
```

---

## 📥 Hướng dẫn cài Minecraft

1. Mở launcher → **Trang chủ**
2. Chọn phiên bản (khuyên dùng **1.8.9** cho máy yếu)
3. Nhấn **⬇ Cài đặt phiên bản**
4. Chờ tải xong (tự động tải JAR + libraries + assets)
5. Nhấn **▶ KHỞI ĐỘNG**

> 💡 Lần đầu cài có thể mất 5–15 phút tùy tốc độ mạng.

---

## 🧩 Mods khuyên dùng

Tải mod tại [modrinth.com](https://modrinth.com) hoặc [curseforge.com](https://curseforge.com), đặt file `.jar` vào thư mục `mods/`.

| Mod | Loader | Tác dụng |
|-----|--------|----------|
| **OptiFine** | Forge | Tăng FPS, hỗ trợ Shader, Zoom |
| **Sodium** | Fabric | Render engine nhanh hơn vanilla 2-4x |
| **Lithium** | Fabric | Tối ưu game logic, mob AI |
| **Starlight** | Fabric | Viết lại lighting engine |
| **LazyDFU** | Fabric/Forge | Giảm thời gian load game |
| **FerriteCore** | Fabric/Forge | Giảm 20-30% RAM |
| **Entity Culling** | Fabric/Forge | Ẩn entity bị che khuất |
| **Dynamic FPS** | Fabric | Tiết kiệm CPU khi alt-tab |
| **Krypton** | Fabric | Tối ưu mạng multiplayer |
| **C2ME** | Fabric | Chunk loading đa luồng |
| **ImmediatelyFast** | Fabric | Tối ưu render UI/Entity batch |

---

## 🔧 Build từ source

### Yêu cầu
- JDK 17+
- Maven 3.8+ (hoặc dùng Maven Wrapper)

```bash
# Clone
git clone https://github.com/yourusername/mc-launcher-lite
cd mc-launcher-lite

# Build fat JAR
mvn clean package -DskipTests

# Chạy
java -jar target/MCLauncherLite.jar
```

### Cấu trúc source

```
src/main/java/dev/mclauncher/
├── Main.java                    ← Entry point
├── core/
│   ├── LauncherConfig.java      ← Cấu hình & persistence
│   ├── MinecraftLauncher.java   ← Build & run Minecraft process
│   └── PerformancePreset.java   ← Preset tối ưu
├── install/
│   ├── VersionManager.java      ← Mojang API, danh sách version
│   └── GameInstaller.java       ← Tải JAR, libraries, assets
└── ui/
    ├── MainFrame.java           ← Cửa sổ chính (Swing)
    └── Theme.java               ← Dark theme constants
```

---

## ❓ FAQ

**Q: Lỗi "Could not find or load main class"?**
> Chạy từ thư mục chứa file JAR, hoặc dùng đường dẫn đầy đủ:
> `java -jar C:\path\to\MCLauncherLite.jar`

**Q: Màn hình đen khi khởi động Minecraft?**
> Thử bật driver update cho GPU. Với máy rất yếu thêm JVM arg:
> `-Dorg.lwjgl.opengl.Display.allowSoftwareOpenGL=true`

**Q: Không kết nối được Mojang API (danh sách version trống)?**
> Launcher sẽ dùng danh sách offline fallback (các version phổ biến). Vẫn cài và chơi bình thường được.

**Q: Forge/Fabric chưa tự cài?**
> Hiện tại cần cài Forge/Fabric thủ công rồi launcher sẽ detect. Tính năng auto-install Forge/Fabric đang được phát triển.

**Q: Lưu tại đâu trên Windows?**
> `C:\Users\<tên>\AppData\Roaming\.mclauncher\`
> Hoặc mở File Explorer gõ `%APPDATA%\.mclauncher`

---

## ⚠️ Lưu ý pháp lý

Đây là phần mềm mã nguồn mở, không phải sản phẩm chính hãng của **Mojang Studios** hay **Microsoft**.
Minecraft là thương hiệu thuộc sở hữu của Mojang Studios / Microsoft.
Để chơi online trên server chính hãng, cần tài khoản Microsoft hợp lệ.

---

## 📄 License

MIT License — Tự do sử dụng, chỉnh sửa và phân phối.

---

*Made with ☕ Java + 💙 Swing*
