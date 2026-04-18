# 🔔 Local Notification App

Aplikasi Flutter sederhana yang mendemonstrasikan penggunaan **local notification** pada Android dan iOS menggunakan package `flutter_local_notifications`.

---

## 📱 Fitur

- Menampilkan notifikasi lokal saat tombol FAB ditekan
- Notifikasi berisi waktu (jam:menit:detik) saat tombol ditekan
- Mendukung platform **Android** (min SDK 21) dan **iOS**
- Meminta izin notifikasi secara otomatis saat aplikasi pertama kali dijalankan

---

## 🛠️ Teknologi & Dependencies

| Package | Versi | Keterangan |
|---|---|---|
| `flutter_local_notifications` | ^17.2.3 | Plugin utama untuk local notification |
| `timezone` | ^0.9.4 | Dukungan timezone untuk scheduled notification |
| `cupertino_icons` | ^1.0.8 | Icon iOS style |

---

## 🚀 Cara Menjalankan

### Prasyarat
- Flutter SDK (≥ 3.11.0)
- Android Studio / Emulator Android (min API 21)
- Atau perangkat fisik Android/iOS

### Langkah-langkah

1. **Clone repository ini**
   ```bash
   git clone https://github.com/fajaaarrr/Tugas6.2-local-notification.git
   cd Tugas6.2-local-notification
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Jalankan aplikasi**
   ```bash
   flutter run
   ```

---

## 📂 Struktur Proyek

```
local_notification_app/
├── lib/
│   └── main.dart           # Entry point & semua logika aplikasi
├── android/
│   └── app/
│       └── build.gradle.kts  # Konfigurasi Android (core library desugaring)
├── ios/
│   └── Runner/
│       └── Info.plist      # Konfigurasi izin notifikasi iOS
└── pubspec.yaml            # Konfigurasi dependencies
```

---

## ⚙️ Konfigurasi Android

File `android/app/build.gradle.kts` dikonfigurasi dengan:
- `minSdk = 21` (diperlukan oleh `flutter_local_notifications`)
- `isCoreLibraryDesugaringEnabled = true` (diperlukan untuk Java 8+ API)
- Dependency `desugar_jdk_libs:2.1.4`

---

## 📸 Cara Kerja

1. Saat aplikasi dibuka, izin notifikasi diminta secara otomatis
2. Tekan tombol **+** (FAB) di pojok kanan bawah
3. Notifikasi akan muncul di status bar dengan waktu saat tombol ditekan
4. Waktu terakhir tombol ditekan juga ditampilkan di layar utama

---

## 👤 Informasi

- **Mata Kuliah**: Aplikasi Perangkat Bergerak
- **Tugas**: 6.2 - Local Notification
- **Platform**: Android & iOS
