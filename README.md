<div align="center">

<!-- Ganti dengan logo aplikasi -->
<img src="https://i.imgur.com/DWZZ1Lf.png" alt="Logo ASESTAR" width="120">

# ASESTAR

**Sistem Asesmen Digital**

Aplikasi desktop mode terkunci (kiosk) untuk melaksanakan asesmen/ujian berbasis Microsoft Forms secara lebih tertib dan terawasi.

![Platform](https://img.shields.io/badge/platform-Windows-0078D6?logo=windows&logoColor=white)
![Versi](https://img.shields.io/badge/versi-2.0-2c5aa0)
![Status](https://img.shields.io/badge/rilis-binary%20only-lightgrey)

</div>

---

## 📖 Tentang Aplikasi

**ASESTAR** adalah aplikasi desktop yang membantu sekolah menjalankan asesmen digital dengan lingkungan yang terkontrol. Peserta memindai kode QR dari pengawas, lalu halaman asesmen (Microsoft Forms) dibuka dalam **jendela layar penuh yang terkunci**, sehingga peserta tidak bisa berpindah ke aplikasi lain selama asesmen berlangsung.

---

## 📸 Tampilan Aplikasi

### 1. Splash Screen
Muncul saat aplikasi dibuka, dilengkapi progress bar dan pesan status saat sistem disiapkan.

<p align="center">
  <img src="https://i.imgur.com/kd4Eq6d.png" alt="Splash Screen" width="320">
</p>

### 2. Input Sumpah dan Halaman Utama
Jendela utama berukuran potret yang tetap berada di atas jendela lain. Digunakan untuk memindai kode QR dari pengawas melalui kamera.

<p align="center">
  <img src="https://i.imgur.com/wcx8ARy.png" alt="Input Sumpah" width="320">
</p>

<p align="center">
  <img src="https://i.imgur.com/bpkxvGR.png" alt="Halaman Utama" width="320">
</p>

### 4. Mode Asesmen (Layar Penuh)
Halaman Microsoft Forms tampil layar penuh tanpa bingkai jendela, selalu di atas aplikasi lain.

<p align="center">
  <img src="https://i.imgur.com/5qKUjPY.png" alt="Mode Asesmen" width="720">
</p>

### 5. Layar "Submit Berhasil"
Muncul otomatis begitu jawaban terkirim. Menampilkan jam dan tanggal untuk diperlihatkan kepada pengawas.

<p align="center">
  <img src="https://i.imgur.com/OFvvzrM.png" alt="Submit Berhasil" width="720">
</p>

---

## ✨ Fitur Utama

### 🔒 Mode Terkunci (Kiosk)
- Jendela asesmen **layar penuh, tanpa bingkai, dan selalu di atas** jendela lain.
- Jendela tidak bisa diminimalkan atau ditutup dengan cara biasa; jika diminimalkan, otomatis kembali ke layar penuh.
- **Pintasan keyboard diblokir**, antara lain:
  - `Alt + F4`, `Alt + Tab`, `Win + Tab`
  - `Win + D`, `Win + M`, `Win + L`
  - `F4`, `Esc`, `F11`, `F12`, `PrintScreen`
  - `Ctrl + C`, `Ctrl + X`, `Ctrl + A`, `Ctrl + P`, `Ctrl + S`
- Klik kanan (context menu) dan drag & drop dinonaktifkan.
- Perekaman layar (*screen capture*) dinonaktifkan pada WebView asesmen.
- **Clipboard dibersihkan** saat sesi asesmen ditutup.

### 📷 Pemindai QR Bawaan
- Memindai kode QR langsung dari kamera perangkat, tanpa aplikasi tambahan.
- Mendukung **pergantian kamera** (depan/belakang atau kamera eksternal).

### 🎛️ Kontrol Panel Mengambang
- Jam dan tanggal real-time.
- Indikator **baterai** (persentase dan status pengisian).
- Indikator **jaringan** (WiFi / LAN / offline).
- Tombol **Kembali**, **Reload**, dan **Keluar** (dengan konfirmasi).
- Dapat dilipat agar tidak menghalangi soal.

### ✅ Deteksi Submit Otomatis
- Aplikasi mendeteksi pesan keberhasilan pengiriman dari Microsoft Forms (versi bahasa Indonesia maupun Inggris).
- Setelah terdeteksi, tampil layar **"SUBMIT BERHASIL"** berisi jam & tanggal untuk ditunjukkan kepada pengawas.
- Sesi login asesmen **dihapus otomatis** (cookie, cache, dan folder sesi), sehingga peserta harus login ulang pada sesi berikutnya.

### 🛡️ Keamanan Tambahan
- **Single instance**: aplikasi hanya dapat dijalankan satu kali pada saat yang sama.
- **Sesi asesmen terpisah** dari data aplikasi, sehingga data login tidak bercampur.
- Navigasi ke situs luar dibatasi; tautan tertentu (media sosial dan sejenisnya) dibuka di browser eksternal, bukan di dalam jendela asesmen.
- Akses ke berkas sistem di luar folder aplikasi diblokir.
- Konten aplikasi disimpan dalam arsip `_data_` yang diproteksi dan diekstrak otomatis saat aplikasi dibuka.

---

## 💻 Persyaratan Sistem

| Komponen | Keterangan |
|---|---|
| Sistem operasi | Windows 10 / 11 (64-bit) |
| Kamera | Diperlukan untuk memindai kode QR |
| Koneksi internet | Diperlukan untuk membuka Microsoft Forms |
| Ruang disk | Sekitar `661 MB`|

---

## 🚀 Cara Menggunakan

### Instalasi
1. Buka halaman [**Releases**](https://github.com/lurma813/asestar-sman1tahunan/releases) di repositori ini.
2. Unduh installer terbaru (`asestar-setup.exe`).
3. Jalankan installer, lalu ikuti petunjuk di layar (**Next → Install → Finish**).
4. Buka aplikasi dari **Start Menu** atau **shortcut Desktop** "Asestar".

<p align="center">
  <img src="https://i.imgur.com/Xx21ACY.png" alt="Installer ASESTAR" width="480">
</p>

> ⚠️ Jangan memindahkan, mengubah nama, atau menghapus berkas di dalam folder instalasi. Jika berkas ini hilang atau rusak, aplikasi tidak dapat dibuka. Jika itu terjadi, instal ulang aplikasi.

### Pembaruan & Penghapusan
- **Memperbarui**: unduh installer versi terbaru dan jalankan; instal di lokasi yang sama.
- **Menghapus**: gunakan **Settings → Apps → Installed apps → ASESTAR → Uninstall** atau uninstaller di folder instalasi.
- Data sementara aplikasi tersimpan di `%LOCALAPPDATA%\AsestarData`. Folder ini dapat dihapus manual jika ingin membersihkan sisa data.

### Alur Pemakaian
1. **Buka aplikasi.** Tunggu splash screen selesai.
2. **Minta kode/QR kepada pengawas**, lalu arahkan ke kamera.
3. Setelah kode terbaca, halaman asesmen terbuka dalam **mode layar penuh**.
4. **Login** dengan akun yang diminta, lalu kerjakan asesmen.
5. Klik **Submit** di Microsoft Forms setelah selesai.
6. Layar **"SUBMIT BERHASIL"** akan muncul. **Perlihatkan layar tersebut kepada pengawas.**
7. Klik **Tutup Halaman** untuk menutup sesi asesmen.

### Keluar di Tengah Asesmen
Klik **Keluar** pada Kontrol Panel di pojok kanan bawah, lalu konfirmasi. Gunakan hanya jika benar-benar diperlukan dan atas izin pengawas.

---

## ❓ Pertanyaan Umum (FAQ)

**Aplikasi tidak mau terbuka dan muncul pesan "Gagal menginisiasi data aplikasi".**
Berkas `_data_` di folder instalasi kemungkinan hilang atau rusak. Instal ulang aplikasi dengan installer terbaru.

**Muncul pesan "Aplikasi Sudah Berjalan".**
Aplikasi hanya boleh dijalankan satu kali. Tutup jendela yang sudah terbuka, atau akhiri prosesnya lewat Task Manager.

**Kamera tidak berfungsi.**
Pastikan kamera tidak sedang dipakai aplikasi lain dan izin kamera untuk aplikasi desktop sudah aktif di pengaturan Windows. Anda juga dapat mencoba tombol ganti kamera.

**Indikator baterai tidak muncul.**
Perangkat desktop tanpa baterai tidak menampilkan informasi baterai.

**Saya sudah submit, tetapi layar "Submit Berhasil" tidak muncul.**
Tunggu beberapa detik hingga halaman konfirmasi Microsoft Forms tampil sepenuhnya. Jika tetap tidak muncul, hubungi pengawas.

**Di mana aplikasi menyimpan data?**
Di folder `AsestarData` pada `%LOCALAPPDATA%`. Data sesi asesmen dihapus otomatis setelah submit berhasil.

---

## 🗂️ Struktur Folder Setelah Instalasi

```
<folder instalasi>/
├── ASESTAR.exe      # Aplikasi utama
├── _data_           #
├── _icon_           #
└── unins000.exe     # Uninstaller
```

---

## 📝 Catatan

- Aplikasi dirancang untuk asesmen berbasis **Microsoft Forms** (`forms.office.com` / `forms.microsoft.com`).
- Pembatasan pada aplikasi ini bertujuan menjaga ketertiban asesmen, bukan pengganti pengawasan langsung.
- Windows Defender / SmartScreen dapat menampilkan peringatan saat menjalankan installer karena belum ditandatangani secara digital. Pilih **More info → Run anyway** jika Anda yakin berkas berasal dari sumber resmi.

---

## 📬 Kontak & Dukungan

Menemukan bug atau punya saran? Buka [**Issues**](https://github.com/lurma813/asestar-sman1tahunan/issues) di repositori ini.

<!-- Isi dengan kontak yang diinginkan -->
- Pengembang: `Amrul Fatah`
- Email: `amrulfattah150297@gmail.com`

---
