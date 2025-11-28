# 📚 SISTEM PRESENSI SEKOLAH
## SDIT-Balikpapan Islamic School

---

## 🎯 OVERVIEW

Sistem Presensi Sekolah berbasis web (Laravel) dan mobile (Flutter) untuk mengelola kehadiran siswa dan guru dengan integrasi Landing Page Sekolah yang modern.

### Key Features:
- ✅ **Landing Page Sekolah**: Website profil dengan artikel, berita, dan informasi sekolah
- ✅ **Presensi Siswa**: Diinput oleh GURU (bukan siswa yang absen sendiri)
- ✅ **Presensi Guru & Staff**: Via mobile dengan Face Recognition + GPS
- ✅ **Riwayat Kelas Siswa**: Tracking naik kelas & pindah kelas otomatis ⭐
- ✅ **Foto Kelas Wajib**: Bukti mengajar untuk setiap input presensi siswa
- ✅ **Radius GPS**: Validasi lokasi saat absen (configurable di web)
- ✅ **Artikel & Berita**: Konten untuk landing page sekolah
- ✅ **Banner Pengumuman**: Pop-up gambar/banner pengumuman
- ✅ **6 User Roles** dengan RBAC lengkap
- ✅ **Web + Mobile Platform**

---

## 👥 USER ROLES

| No | Role | Platform | Absen Mobile | Description |
|----|------|----------|:------------:|-------------|
| 1 | **Super Admin** | Web | ❌ | Full system access |
| 2 | **Kepala Sekolah** | Web + Mobile | ✅ | Monitoring & approval |
| 3 | **Admin / Staff TU** | Web + Mobile | ✅ | CRUD data master |
| 4 | **Wali Kelas** | Web + Mobile | ✅ | Manage class attendance |
| 5 | **Guru** | Web + Mobile | ✅ | Input presensi siswa |
| 6 | **Orang Tua** | Web Only | ❌ | View child attendance & statistics, submit izin |

---

## 🌐 LANDING PAGE (Public)

### Struktur Halaman Landing

**Homepage:**
```
🏠 HERO SECTION
├─ Slider/Banner Utama
├─ Tagline: "Cerdas dan Berkarakter Qur'ani"
├─ CTA: "Daftar Sekarang" & WhatsApp Contact
└─ Informasi Kontak & Lokasi (Top Bar)

📊 STATISTIK SEKOLAH
├─ 72 Guru & Pengajaran
├─ 300+ Murid
└─ Total Siswa Counter

📸 GALERI FOTO KEGIATAN
└─ Carousel foto prestasi & kegiatan sekolah

👥 DAFTAR GURU & STAFF
├─ Table dengan: No, Nama, NIY, Jenis Kelamin, Jabatan
├─ Pagination
└─ Button: "Semua Registrasi"

📰 ARTIKEL TERBARU
├─ Preview 3 artikel terbaru
├─ Kategori: Aktivitas Siswa, Aktivitas Guru, Aktivitas Sekolah
├─ Thumbnail, Judul, Excerpt, Tanggal
└─ Button: "Semua Artikel"

📢 INFO & PENGUMUMAN
├─ CTA Section: "Butuh Informasi Lebih Lanjut?"
└─ Button: "Hubungi Kami"

📞 FOOTER
├─ Logo & Branding Sekolah
├─ Alamat Lengkap & Maps
├─ Kontak: Email, Telepon, WhatsApp
├─ Jam Operasional
├─ Social Media Links
└─ Copyright
```

**Halaman Tentang Kami:**
```
📖 PROFIL SEKOLAH
├─ Sejarah Berdiri (sejak 2014)
├─ Total Pengalaman
├─ Jumlah Guru & Murid

🎯 VISI & MISI
├─ Visi Kami (5 point)
└─ Misi Kami (6 point)

🏫 FASILITAS SEKOLAH
├─ Grid Layout dengan foto
├─ Ruang Multimedia
├─ Lab Komputer
├─ Ruang Perpustakaan
├─ Halaman & Taman Sekolah
├─ Unit Kesehatan Sekolah
├─ Ruang BK
├─ Ruang Counseling
└─ Toilet

🗺️ LOKASI & KONTAK
├─ Google Maps Embed
├─ Alamat Lengkap
├─ Email & Telepon
└─ Jam Operasional
```

**Halaman SDM (Guru & Staff):**
```
👥 DAFTAR GURU & STAFF

Header: "Guru & Staff - SDIT-Balikpapan Islamic School"

Table Structure:
┌────────────────────────────────────────────────────────┐
│ No | Nama | NIY | Jenis Kelamin | Jabatan            │
├────────────────────────────────────────────────────────┤
│ 1  | Ratnawati, S.Pd. | 00432013 | Perempuan         │
│    | Kepala Sekolah                                    │
├────────────────────────────────────────────────────────┤
│ 2  | Armina Oktavia, S.Pd. | 00532015 | Perempuan    │
│    | Wakasek Kesiswaan                                 │
├────────────────────────────────────────────────────────┤
│ 3  | Nurlitri Nurani, S.I.Kom. | 00342011 | Perempuan│
│    | Wakasek Kurikulum                                 │
└────────────────────────────────────────────────────────┘

Features:
- Pagination (10 entries per page)
- Total entries counter
- Search functionality
- Filter by Jabatan
- Responsive table
```

**Halaman Artikel:**
```
📰 ARTIKEL & BERITA

Categories:
- Aktivitas Siswa
- Aktivitas Guru  
- Aktivitas Sekolah

Article Card Layout:
┌──────────────────────────────────────┐
│ [Featured Image]                     │
├──────────────────────────────────────┤
│ 🏷️ Aktivitas Siswa                  │
│                                      │
│ SDIT-BIS Merayakan Hari Kemerdekaan │
│ RI ke-80                             │
│                                      │
│ Lorem ipsum dolor sit amet excerpt  │
│ preview text...                      │
│                                      │
│ 👤 by Rendi Aszhari Ramadhani       │
│ 📅 20 November 2024                  │
└──────────────────────────────────────┘

Features:
- Grid/Card Layout (3 columns)
- Category badge
- Featured image
- Title & excerpt
- Author & date
- Read more link
- Pagination
```

---

## 📑 MENU STRUCTURE

### 1. SUPER ADMIN (Web Only)

```
📊 Dashboard
👥 Manajemen User
   ├─ Daftar User
   ├─ Role & Permission
   └─ Activity Log
📚 Data Master
   ├─ Data Siswa
   ├─ Data Guru & Staff
   ├─ Data Kelas
   ├─ Kelola Kelas Siswa ⭐
   │  ├─ Naik Kelas Massal
   │  ├─ Pindah Kelas Individual
   │  ├─ View Riwayat Kelas
   │  └─ Mutasi Siswa
   ├─ Jadwal Pelajaran
   └─ Tahun Ajaran
✅ Presensi
   ├─ Presensi Siswa
   │  └─ View Foto Kelas (Bukti Mengajar)
   ├─ Presensi Guru
   │  └─ GPS Location History
   ├─ Presensi Orang Tua
   ├─ Input Keterlambatan
   └─ Face Recognition Data
📝 Perizinan
   ├─ List Semua Izin
   └─ Approval Izin
📊 Laporan
   ├─ Laporan Kehadiran Siswa (dengan foto)
   ├─ Laporan Kehadiran Guru (dengan GPS)
   ├─ Laporan Kehadiran Orang Tua
   └─ Custom Reports
📢 Notifikasi & Komunikasi
   ├─ Daftar Notifikasi
   ├─ Upload Banner Pengumuman ⭐
   │  ├─ Upload Gambar/Banner
   │  ├─ Set Tanggal Tayang
   │  ├─ Target Audience (All/Guru/Ortu/Per Kelas)
   │  └─ Enable/Disable Pop-up
   ├─ Broadcast WhatsApp
   └─ Riwayat Pengiriman
📰 Konten Website ⭐
   ├─ Landing Page Settings
   │  ├─ Hero Section
   │  ├─ Statistik Sekolah
   │  └─ Contact Information
   ├─ Artikel & Berita
   │  ├─ Daftar Artikel
   │  ├─ Tambah/Edit/Hapus Artikel
   │  ├─ Kategori Artikel
   │  │  ├─ Aktivitas Siswa
   │  │  ├─ Aktivitas Guru
   │  │  └─ Aktivitas Sekolah
   │  ├─ Status (Draft/Published)
   │  └─ Featured Article
   ├─ Profil Sekolah
   │  ├─ Visi & Misi
   │  ├─ Sejarah
   │  ├─ Fasilitas (dengan foto)
   │  └─ Galeri Kegiatan
   └─ Data Guru untuk Landing Page
      ├─ Tampilan Public
      └─ Sync dengan Data Master Guru
⚙️ Pengaturan
   ├─ System Settings
   ├─ Radius Absensi GPS ⭐
   │  ├─ Lokasi Sekolah (Lat, Long)
   │  ├─ Radius Maksimal (meter)
   │  └─ Enable/Disable Validation
   ├─ Foto Kelas Settings ⭐
   │  ├─ Wajib ON/OFF
   │  ├─ Max Size & Format
   │  └─ Watermark Settings
   ├─ Website Settings ⭐
   │  ├─ Landing Page Config
   │  ├─ SEO Settings
   │  └─ Social Media Links
   └─ Kalender Akademik
👤 My Profile
🚪 Logout
```

### 2. KEPALA SEKOLAH (Web + Mobile)

**Web:**
```
📊 Dashboard
📚 Data Master (View Only)
✅ Monitoring Presensi
   ├─ Monitoring Siswa (dengan foto kelas)
   ├─ Monitoring Guru (GPS location)
   ├─ Monitoring Orang Tua
   └─ Face Recognition Status
📝 Perizinan
📊 Laporan
📢 Notifikasi & Komunikasi
   ├─ Daftar Notifikasi
   ├─ View Banner Pengumuman
   ├─ Buat Pengumuman (Text)
   └─ Broadcast WhatsApp
📰 Konten Website
   ├─ Artikel & Berita (Approve/View)
   └─ Profil Sekolah (View)
⚙️ Pengaturan (View Only)
   ├─ Radius Absensi GPS
   └─ Website Settings
👤 My Profile
🚪 Logout
```

**Mobile:**
```
🏠 Home (Dashboard dengan GPS indicator)
👤 Absen Kepala Sekolah
   ├─ GPS Location Check ⭐
   └─ Face Recognition
📊 Monitoring Real-time
📢 Notifikasi & Banner Pop-up
👤 Profile & Settings
```

### 3. ADMIN / STAFF TU (Web + Mobile)

**Web:**
```
📊 Dashboard
👥 Manajemen User
📚 Data Master (Full CRUD)
✅ Presensi
   ├─ Presensi Siswa
   │  ├─ Input Presensi
   │  ├─ Upload Foto Kelas (Wajib) ⭐
   │  └─ Monitoring Real-time
   ├─ Presensi Guru (dengan GPS)
   ├─ Presensi Orang Tua
   └─ Input Keterlambatan
📝 Perizinan
📊 Laporan
📢 Notifikasi & Komunikasi
   ├─ Upload Banner Pengumuman ⭐
   └─ Broadcast WhatsApp
📰 Konten Website ⭐
   ├─ Landing Page Management
   ├─ Artikel & Berita (Full CRUD)
   ├─ Profil Sekolah & Fasilitas
   └─ Manage Galeri Foto
⚙️ Pengaturan
   ├─ Radius Absensi GPS ⭐
   ├─ Foto Kelas Settings ⭐
   ├─ Website Settings ⭐
   └─ Kalender Akademik
👤 My Profile
🚪 Logout
```

**Mobile:**
```
🏠 Home (Dashboard)
👤 Absen Admin/TU
   ├─ GPS Location Check ⭐
   └─ Face Recognition
📊 Monitoring
📢 Notifikasi & Banner Pop-up
👤 Profile
```

### 4. WALI KELAS (Web + Mobile)

**Web:**
```
📊 Dashboard
📚 Kelas Saya
✅ Presensi
   ├─ Input Presensi Kelas
   ├─ Upload Foto Kelas (Wajib) ⭐
   └─ Monitoring Kehadiran
📝 Perizinan
📊 Laporan
📢 Komunikasi
   ├─ View Banner Pengumuman
   └─ Kirim Pesan Kelas
📰 Artikel (View Only)
👤 My Profile
```

**Mobile:**
```
🏠 Home (Dashboard dengan GPS indicator)
📝 Presensi Siswa
   ├─ Input Presensi (Quick Mode)
   └─ 📷 Foto Kelas (Wajib) ⭐
👤 Absen Wali Kelas
   ├─ GPS Location Check ⭐
   └─ Face Recognition
📊 Monitoring & Laporan
📢 Banner Pop-up
👤 Profile & Settings
```

### 5. GURU (Web + Mobile)

**Web:**
```
📊 Dashboard
📚 Kelas yang Diajar
✅ Presensi
   ├─ Input Presensi per Mapel
   ├─ Upload Foto Kelas (Wajib) ⭐
   └─ History
📊 Laporan
📢 Notifikasi & Banner Pop-up
📰 Artikel (View Only)
👤 My Profile
```

**Mobile:**
```
🏠 Home
📝 Presensi Siswa + 📷 Foto Kelas ⭐
👤 Absen Guru
   ├─ GPS Location Check ⭐
   └─ Face Recognition
📊 Laporan
📢 Banner Pop-up
👤 Profile
```

### 6. ORANG TUA (Web Only)

```
📊 Dashboard
   ├─ Status Kehadiran Anak Hari Ini
   ├─ Kelas Saat Ini & Riwayat ⭐
   ├─ Kalender Kehadiran Bulan Ini
   ├─ Statistik Kehadiran (Grafik)
   │  ├─ Hadir: 85%
   │  ├─ Sakit: 5%
   │  ├─ Izin: 8%
   │  └─ Alpa: 2%
   └─ Pengumuman untuk Orang Tua
👶 Profil Anak
   ├─ Data Pribadi Anak
   ├─ Kelas Saat Ini & Wali Kelas ⭐
   ├─ Riwayat Kelas (Timeline) ⭐
   │  ├─ 2024/2025: Kelas 1A (Selesai)
   │  └─ 2025/2026: Kelas 2A (Aktif)
   ├─ Nomor Induk Siswa
   └─ Foto Anak
✅ Kehadiran Anak
   ├─ Kalender View (Bulanan)
   ├─ Detail Harian
   │  ├─ Jam masuk/pulang
   │  ├─ Status per mapel
   │  └─ Catatan guru
   ├─ Grafik Statistik
   │  ├─ Per bulan
   │  ├─ Per semester
   │  └─ Perbandingan dengan kelas
   └─ Export ke PDF/Excel
📝 Perizinan
   ├─ Submit Izin Baru untuk Anak
   │  ├─ Jenis: Sakit/Izin/Lainnya
   │  ├─ Tanggal & Durasi
   │  ├─ Alasan
   │  ├─ Upload Surat (Optional)
   │  └─ Submit ke Wali Kelas
   ├─ Tracking Status Izin
   │  ├─ ⏳ Pending
   │  ├─ ✅ Approved
   │  └─ ❌ Rejected
   └─ History Izin
📊 Laporan
   ├─ Laporan Kehadiran Bulanan
   ├─ Laporan Semester
   ├─ Prestasi Akademik (jika ada)
   └─ Download/Print Report
📢 Pengumuman & Komunikasi
   ├─ Banner Pengumuman untuk Orang Tua ⭐
   │  ├─ Pengumuman Umum
   │  ├─ Pengumuman Kelas Anak
   │  └─ Pengumuman Urgent
   ├─ Pesan dari Wali Kelas
   └─ Broadcast Sekolah
📰 Artikel & Berita (View Only)
   ├─ Berita Sekolah
   ├─ Prestasi Siswa
   └─ Kegiatan Sekolah
⚙️ Pengaturan
   ├─ Profil Orang Tua
   ├─ Ubah Password
   ├─ Notifikasi Email/WhatsApp
   └─ Preferensi Laporan
👤 My Profile
🚪 Logout
```

### 7. LANDING PAGE (Public - No Login) ⭐

```
Navigation Menu:
├─ 🏠 Home
├─ 📖 Tentang Kami
├─ 👥 SDM (Guru & Staff)
├─ 📰 Artikel
└─ 🔐 Registrasi / Login

🏠 HOME PAGE
├─ Hero Banner
│  ├─ Tagline: "Cerdas dan Berkarakter Qur'ani"
│  ├─ CTA: Daftar Sekarang
│  └─ WhatsApp Contact
├─ Welcome Section
│  ├─ "Selamat Datang di Website SDIT-Balikpapan"
│  ├─ Deskripsi Sekolah (since 2014)
│  └─ CTA: Profil Selengkapnya
├─ Statistik
│  ├─ 72 Guru & Pengajaran
│  ├─ 300+ Murid
│  └─ Total Siswa Counter
├─ Galeri Foto Kegiatan
├─ Daftar Guru & Staff (Preview 5 baris)
│  └─ Button: "Semua Registrasi"
├─ CTA Section: "Bergabunglah Bersama Kami!"
│  └─ Button: "Daftar Sekarang"
├─ Artikel Terbaru (3 artikel)
│  └─ Button: "Semua Artikel"
└─ Info Lanjut Section
   └─ Button: "Hubungi Kami"

📖 TENTANG KAMI
├─ Breadcrumb: Home > Tentang Kami
├─ Header: "Tentang Kami"
├─ Profil Section
│  ├─ Deskripsi Lengkap
│  ├─ 72 Guru
│  ├─ 300+ Murid
│  └─ Galeri Foto (3-4 foto)
├─ Visi Kami (5 point dengan ikon)
├─ Misi Kami (6 point dengan ikon)
├─ Fasilitas Sekolah
│  ├─ Grid Layout 3 kolom
│  ├─ Foto + Label setiap fasilitas
│  ├─ Ruang Multimedia + Lab Komputer
│  ├─ Perpustakaan + Halaman & Taman
│  ├─ Unit Kesehatan + Ruang BK
│  ├─ Ruang Counseling + Toilet
│  └─ Dan lainnya
└─ Kontak & Lokasi
   ├─ "Tetap Terhubung Bersama Kami"
   ├─ Google Maps Embed
   ├─ Alamat Lengkap
   ├─ Email & Telepon
   └─ Jam Operasional

👥 SDM (GURU & STAFF)
├─ Breadcrumb: Home > SDM
├─ Header: "Guru & Staf"
├─ Subheader: "Daftar Guru & Staf SDIT-Balikpapan Islamic School"
├─ Table dengan Yellow Header
│  ├─ Kolom: No, Nama, NIY, Jenis Kelamin, Jabatan
│  ├─ Data dari database guru
│  └─ Highlight role/jabatan
├─ Pagination
│  ├─ Showing 1 to 10 of 146 entries
│  └─ Previous / 1, 2, 3, ... / Next
└─ Search & Filter (optional)

📰 ARTIKEL
├─ Breadcrumb: Home > Artikel
├─ Header: "Artikel Terbaru Dari SDIT-BIS"
├─ Subheader: "Nantio serti SDIT-Balikpapan Islamic School"
├─ Filter Kategori
│  ├─ Aktivitas Siswa
│  ├─ Aktivitas Guru
│  └─ Aktivitas Sekolah
├─ Article Cards (Grid 3 kolom)
│  ├─ Featured Image
│  ├─ Category Badge
│  ├─ Title
│  ├─ Excerpt
│  ├─ Author & Date
│  └─ Read More Link
└─ Pagination / Load More

📞 FOOTER (All Pages)
├─ Logo & Branding
│  ├─ Logo Sekolah
│  ├─ Nama: SDIT-BALIKPAPAN ISLAMIC SCHOOL
│  └─ Tagline: "Membentuk generasi Qur'ani yang Cerdas,
│     Berjiwa Riset, Berwawasan Inklusif dan Peduli Lingkungan"
├─ Contact Info
│  ├─ 📍 Alamat: Jl. Alamanda Selatan Blok L5/1b, RT 08
│  │   Kelurahan Damai Baru, Kec. Balikpapan Selatan,
│  │   Kota Balikpapan, 76114
│  ├─ 📧 Email: admin@balikpapanislamicschool.sch.id
│  ├─ 📞 Phone: (0542)7206717 / 7206718
│  └─ 🕒 Jam Operasional
│     ├─ Senin-Jumat: 07:00-16:00 WITA
│     └─ Sabtu: 08:00-15:00 WITA
├─ Social Media
│  ├─ Instagram
│  ├─ YouTube
│  └─ Facebook
└─ Copyright
   └─ Copyright © 2024. All Rights Reserved
```

---

## 🔐 ACCESS MATRIX

| Feature | Super Admin | Kepsek | Admin/TU | Wali Kelas | Guru | Orang Tua | Public |
|---------|:-----------:|:------:|:--------:|:----------:|:----:|:---------:|:------:|
| **Dashboard** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |
| **Landing Page** |
| - View Landing | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| - Edit Landing | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ |
| - Manage Artikel | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |
| - View Artikel | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| **Data Master** |
| - Siswa (CRUD) | ✅ | 👁️ | ✅ | 👁️* | ❌ | 👁️* | ❌ |
| - Guru (CRUD) | ✅ | 👁️ | ✅ | ❌ | ❌ | ❌ | 👁️** |
| - Kelas (CRUD) | ✅ | 👁️ | ✅ | 👁️* | 👁️* | ❌ | ❌ |
| **Presensi Siswa** |
| - Input Presensi | ✅ | ❌ | ✅ | ✅* | ✅* | ❌ | ❌ |
| - **Upload Foto Kelas** ⭐ | ✅ | ❌ | ✅ | ✅* | ✅* | ❌ | ❌ |
| - View Foto Kelas | ✅ | ✅ | ✅ | ✅* | ✅* | ❌ | ❌ |
| **Presensi Guru** |
| - Absen via Mobile | ❌ | ✅ | ✅ | ✅ | ✅ | ❌ | ❌ |
| - Face Recognition | ❌ | 📱 | 📱 | 📱 | 📱 | ❌ | ❌ |
| - **GPS Validation** ⭐ | ❌ | 📱 | 📱 | 📱 | 📱 | ❌ | ❌ |
| - View GPS History | ✅ | ✅ | ✅ | 👁️* | 👁️* | ❌ | ❌ |
| **Presensi Orang Tua** |
| - View Kehadiran | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| - Statistik Anak | ✅ | ✅ | ✅ | ✅* | ✅* | ✅ | ❌ |
| **Perizinan** |
| - Submit Izin | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ |
| - Approve/Reject | ✅ | ✅ | ✅ | ✅* | ❌ | ❌ | ❌ |
| **Banner Pengumuman** ⭐ |
| - Upload Banner | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ |
| - View Pop-up | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅* |
| - Set Target | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ |
| **Laporan** |
| - Laporan Siswa | ✅ | ✅ | ✅ | ✅* | ✅* | ✅* | ❌ |
| - Laporan Guru | ✅ | ✅ | ✅ | ❌ | 👁️* | ❌ | ❌ |
| - Laporan Orang Tua | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ |

**Legend:**
- ✅ Full Access | 👁️ View Only | ❌ No Access | 📱 Mobile Only | * Limited scope
- ⭐ = Fitur baru/updated
- ** Public dapat view data guru di landing page (nama, jabatan)

---

## ⚙️ WEB CONFIGURATION

### 1. RADIUS ABSENSI GPS ⭐

**Lokasi:** Admin → Pengaturan → Radius Absensi GPS

**Konfigurasi:**
```
📍 LOKASI SEKOLAH (SDIT-Balikpapan)
- Latitude:  [-1.2659]
- Longitude: [116.8289]
- Alamat: Jl. Alamanda Selatan Blok L5/1b, RT 08
          Kel. Damai Baru, Kec. Balikpapan Selatan
- [📍 Set dari Google Maps]
- [📍 Gunakan GPS Saat Ini]

🗺️ PREVIEW PETA
- Tampilkan marker sekolah
- Tampilkan circle radius
- Interactive zoom & pan
- Street view option

📏 RADIUS MAKSIMAL
- Default: 100 meter
- Range: 50m - 500m
- Slider adjustment
- Presets: [50m] [100m] [200m] [500m]

⚙️ VALIDASI
☑ Aktifkan Validasi Radius
☑ Izinkan Absen Manual jika Luar Radius (+ approval)
☑ Kirim Notifikasi ke Admin
☑ Log GPS History
☑ Berlaku untuk: Guru, Wali Kelas, Admin/TU, Kepsek

📊 STATISTIK HARI INI
- Total percobaan: 68
  ├─ Guru: 42
  ├─ Wali Kelas: 20
  ├─ Admin/TU: 5
  └─ Kepala Sekolah: 1
- Di dalam radius: 65 (95.6%)
- Di luar radius: 3 (4.4%)
- Rata-rata jarak: 47m
- Compliance rate:
  ├─ Guru: 95.2%
  ├─ Wali Kelas: 95.0%
  ├─ Admin/TU: 100%
  └─ Kepala Sekolah: 100%

🧪 TESTING
- Input test coordinates
- Show INSIDE/OUTSIDE result
- Show distance calculation
- Test untuk setiap role
```

---

### 2. FOTO KELAS (BUKTI MENGAJAR) ⭐

**Lokasi:** Admin → Pengaturan → Foto Kelas Settings

**Konfigurasi:**
```
⚙️ KONFIGURASI DASAR
☑ Wajibkan Upload Foto Kelas
☑ Validasi Foto Otomatis
   - Minimal resolusi: 800x600
   - Deteksi blur
   - Deteksi face (minimal 3)

📏 UKURAN FILE
- Maksimal: [5] MB
- Slider: 1MB ────●──── 10MB

📁 FORMAT
☑ JPG/JPEG
☑ PNG
☑ HEIC (iOS)

🖼️ KUALITAS KOMPRESI
⚪ Rendah (50%) - ~500KB
⚪ Sedang (75%) - ~1.5MB
⚫ Tinggi (90%) - ~2.5MB
⚪ Original (100%) - ~4MB

📝 WATERMARK OTOMATIS
☑ Tambahkan Watermark
   ☑ Logo SDIT-Balikpapan
   ☑ Nama Sekolah
   ☑ Tanggal & Waktu
   ☑ Nama Guru & NIP
   ☑ Kelas & Mata Pelajaran
   ☑ GPS Koordinat

Posisi: ⚫ Bottom Right
Opacity: 70%

💾 PENYIMPANAN
⚫ Server Lokal (storage/attendance_photos/)
⚪ Cloud Storage (AWS S3)
⚪ Google Cloud Storage

🗑️ AUTO-DELETE
☑ Hapus foto lama
   Setelah: [90] hari
☑ Backup dulu sebelum delete

📊 STORAGE STATISTICS
- Total foto: 2,456 files
- Total size: 5.2 GB
- Average: 2.1 MB per foto
- Usage: 52% (5.2GB / 10GB)
- Trend: +45 foto/hari
```

---

### 3. BANNER PENGUMUMAN (POP-UP) ⭐

**Lokasi:** Admin → Notifikasi & Komunikasi → Banner Pengumuman

**Fitur Baru:**
```
📢 MANAGEMENT BANNER PENGUMUMAN

Upload Banner:
┌─────────────────────────────────────────────┐
│ [+ Upload Banner Baru]  [Banner Aktif: 3]   │
├─────────────────────────────────────────────┤
│                                             │
│ Form Upload:                                │
│                                             │
│ Judul Banner: *                             │
│ [_____________________________________]     │
│                                             │
│ Upload Gambar/Banner: * (Recommended: 800x600) │
│ [📁 Browse File]                            │
│ Format: JPG, PNG (Max 2MB)                  │
│ [Preview Banner]                            │
│                                             │
│ Target Audience: *                          │
│ ☐ Semua User (termasuk public)             │
│ ☐ Guru & Staff (Kepsek, Admin, Wali, Guru) │
│ ☐ Orang Tua                                 │
│ ☐ Per Kelas: [Dropdown Kelas]              │
│ ☐ Public Only (Landing Page)               │
│                                             │
│ Periode Tayang:                             │
│ Mulai: [20 Nov 2024 08:00] 📅              │
│ Selesai: [25 Nov 2024 23:59] 📅            │
│                                             │
│ Pop-up Settings:                            │
│ ☑ Tampilkan sebagai Pop-up                  │
│ ☐ Auto-close setelah [10] detik            │
│ ☑ Show Close Button (X)                    │
│ ☑ Don't show again today (cookie)          │
│ Priority: ⚫ High ⚪ Medium ⚪ Low          │
│                                             │
│ Link Action (Optional):                     │
│ ☐ Add Button ke Banner                     │
│    Button Text: [Info Selengkapnya]        │
│    URL: [https://...]                       │
│    Open in: ⚫ New Tab ⚪ Same Page        │
│                                             │
│ Status:                                     │
│ ⚫ Aktif ⚪ Jadwal ⚪ Nonaktif              │
│                                             │
│ [💾 Upload & Publish] [👁️ Preview] [❌]   │
└─────────────────────────────────────────────┘

List Banner Aktif:
┌─────────────────────────────────────────────┐
│ 📢 Banner Pengumuman Aktif                 │
├─────────────────────────────────────────────┤
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ [🖼️ Preview]                            │ │
│ │ Libur Nasional 17 Agustus               │ │
│ │ Target: Semua | Priority: High          │ │
│ │ Periode: 15-18 Aug 2024                 │ │
│ │ Views: 2,345 | Clicks: 234              │ │
│ │ Status: 🟢 Active                       │ │
│ │ [Edit] [Nonaktifkan] [Delete] [Stats]  │ │
│ └─────────────────────────────────────────┘ │
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ [🖼️ Preview]                            │ │
│ │ Pengumpulan Rapor Semester              │ │
│ │ Target: Orang Tua | Priority: Medium    │ │
│ │ Periode: 20-25 Nov 2024                 │ │
│ │ Views: 456 | Clicks: 78                 │ │
│ │ Status: 🟢 Active                       │ │
│ │ [Edit] [Nonaktifkan] [Delete] [Stats]  │ │
│ └─────────────────────────────────────────┘ │
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ [🖼️ Preview]                            │ │
│ │ Pendaftaran Siswa Baru 2024/2025        │ │
│ │ Target: Public | Priority: High         │ │
│ │ Periode: 01 Dec 2024 - 31 Jan 2025     │ │
│ │ Views: 890 | Clicks: 123                │ │
│ │ Status: 🟠 Scheduled                    │ │
│ │ [Edit] [Aktifkan] [Delete] [Stats]     │ │
│ └─────────────────────────────────────────┘ │
└─────────────────────────────────────────────┘

Analytics:
┌─────────────────────────────────────────────┐
│ 📊 Banner Statistics                       │
├─────────────────────────────────────────────┤
│ Total Banner: 15                            │
│ Active: 3 | Scheduled: 2 | Inactive: 10    │
│                                             │
│ Performance (7 hari terakhir):              │
│ Total Impressions: 12,345                   │
│ Total Clicks: 1,234                         │
│ CTR: 10%                                    │
│                                             │
│ Top Banner:                                 │
│ 1. Libur Nasional - 2,345 views (19%)     │
│ 2. Pendaftaran Baru - 890 views (7%)      │
│ 3. Rapor Semester - 456 views (4%)        │
│                                             │
│ By Target:                                  │
│ • Semua: 45%                                │
│ • Guru & Staff: 30%                         │
│ • Orang Tua: 20%                            │
│ • Public: 5%                                │
└─────────────────────────────────────────────┘
```

**Cara Kerja Pop-up:**
```
1. User Login / Visit Landing Page
2. Check ada banner aktif untuk role user?
3. Check periode tayang valid?
4. Check cookie "don't show again"?
5. If semua OK → Show Pop-up

Pop-up Design:
┌────────────────────────────────────┐
│                              [✕]   │
│  [🖼️ Banner Image Full Width]     │
│                                    │
│  [Button: Info Selengkapnya →]    │
│  (Optional, jika ada URL)          │
│                                    │
│  ☐ Jangan tampilkan lagi hari ini │
└────────────────────────────────────┘

Features:
- Overlay background (semi-transparent)
- Centered modal
- Responsive (mobile & desktop)
- ESC key to close
- Click outside to close
- Auto-close timer (optional)
- Cookie management
```

---

### 4. ARTIKEL & BERITA (LANDING PAGE) ⭐

**Lokasi:** Admin → Konten Website → Artikel & Berita

**Updated untuk Landing Page:**
```
📰 MANAGEMENT ARTIKEL

Daftar Artikel:
┌─────────────────────────────────────────────┐
│ [+ Tambah Artikel Baru]  [Kategori] [Filter]│
├─────────────────────────────────────────────┤
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ [Featured] SDIT-BIS Merayakan Hari     │ │
│ │ Kemerdekaan RI ke-80                    │ │
│ │ Kategori: Aktivitas Siswa               │ │
│ │ Status: Published                       │ │
│ │ Penulis: Rendi Aszhari | 20 Nov 2024    │ │
│ │ Views: 1,234 | Landing Page: ✅         │ │
│ │ [Edit] [Delete] [Unpublish] [Pin]       │ │
│ └─────────────────────────────────────────┘ │
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ SDIT-BIS Mengadakan Upgrading          │ │
│ │ Guru dan Ngaji Kitab                    │ │
│ │ Kategori: Aktivitas Guru | Draft        │ │
│ │ Penulis: Admin TU | 19 Nov              │ │
│ │ Landing Page: ❌                         │ │
│ │ [Edit] [Publish] [Delete]               │ │
│ └─────────────────────────────────────────┘ │
└─────────────────────────────────────────────┘

Form Tambah/Edit Artikel:
┌─────────────────────────────────────────────┐
│ ✏️ Artikel Baru                            │
├─────────────────────────────────────────────┤
│                                             │
│ Judul: *                                    │
│ [_____________________________________]     │
│                                             │
│ Slug (URL):                                 │
│ [auto-generated-from-title___________]      │
│                                             │
│ Kategori: *                                 │
│ [Dropdown ▼]                                │
│ • Aktivitas Siswa                           │
│ • Aktivitas Guru                            │
│ • Aktivitas Sekolah                         │
│                                             │
│ Excerpt (Ringkasan untuk Landing): *        │
│ [_____________________________________]     │
│ [_____________________________________]     │
│ Max 200 karakter                            │
│                                             │
│ Featured Image: * (Tampil di Landing)       │
│ [📁 Upload Image] (Max 2MB, 800x600)       │
│ Recommended: 800x600 atau 1200x630          │
│ [Preview: image.jpg]                        │
│                                             │
│ Konten: *                                   │
│ [Rich Text Editor with:]                    │
│ • Bold, Italic, Underline                   │
│ • Heading 1-6                               │
│ • List, Quote                               │
│ • Insert Image                              │
│ • Insert Link                               │
│ • Code Block                                │
│                                             │
│ Author Display:                             │
│ [Dropdown: Pilih Penulis]                   │
│ • by Rendi Aszhari Ramadhani                │
│ • by Admin                                  │
│ • Custom: [_________________]               │
│                                             │
│ Tags: (Pisah dengan koma)                   │
│ [siswa, prestasi, kemerdekaan_________]    │
│                                             │
│ Landing Page Settings:                      │
│ ☑ Tampilkan di Landing Page                 │
│ ☐ Set as Featured (Hero Slider)            │
│ ☐ Pin to Top                                │
│ Display Order: [1-100] (untuk sorting)      │
│                                             │
│ SEO Settings:                               │
│ ┌─────────────────────────────────────┐     │
│ │ Meta Title:                         │     │
│ │ [_________________________________] │     │
│ │                                     │     │
│ │ Meta Description:                   │     │
│ │ [_________________________________] │     │
│ │ [_________________________________] │     │
│ │                                     │     │
│ │ Meta Keywords:                      │     │
│ │ [_________________________________] │     │
│ └─────────────────────────────────────┘     │
│                                             │
│ Status:                                     │
│ ⚪ Draft (Save as draft)                    │
│ ⚪ Published (Publish immediately)          │
│ ⚪ Scheduled (Set publish date/time)        │
│                                             │
│ Publish Date: [25 Nov 2024 08:00] 📅       │
│                                             │
│ [💾 Simpan] [👁️ Preview Landing] [❌]     │
└─────────────────────────────────────────────┘

Kategori Management:
┌─────────────────────────────────────────────┐
│ 📁 Kategori Artikel                        │
├─────────────────────────────────────────────┤
│                                             │
│ [+ Tambah Kategori]                         │
│                                             │
│ • Aktivitas Siswa (45 artikel) [Edit] [Del]│
│ • Aktivitas Guru (23 artikel) [Edit] [Del] │
│ • Aktivitas Sekolah (34 artikel) [Edit]    │
│                                             │
└─────────────────────────────────────────────┘

Landing Page Preview:
┌─────────────────────────────────────────────┐
│ 📰 Preview di Landing Page                 │
├─────────────────────────────────────────────┤
│                                             │
│ Article Card:                               │
│ ┌───────────────────────────────────────┐   │
│ │ [Featured Image 800x600]              │   │
│ ├───────────────────────────────────────┤   │
│ │ 🏷️ Aktivitas Siswa                    │   │
│ │                                       │   │
│ │ SDIT-BIS Merayakan Hari Kemerdekaan  │   │
│ │ RI ke-80                              │   │
│ │                                       │   │
│ │ Excerpt text preview max 200 chars... │   │
│ │                                       │   │
│ │ 👤 by Rendi Aszhari Ramadhani         │   │
│ │ 📅 20 November 2024                   │   │
│ │                                       │   │
│ │ [Baca Selengkapnya →]                 │   │
│ └───────────────────────────────────────┘   │
│                                             │
│ Layout: Grid 3 kolom                        │
│ Sorting: Latest first / Pin to top          │
│ Pagination: 9 artikel per halaman           │
└─────────────────────────────────────────────┘
```

---

### 5. PROFIL SEKOLAH & FASILITAS ⭐

**Lokasi:** Admin → Konten Website → Profil Sekolah

**Management:**
```
📖 MANAGEMENT PROFIL SEKOLAH

Tabs:
├─ Informasi Umum
├─ Visi & Misi
├─ Fasilitas
└─ Galeri Kegiatan

┌─────────────────────────────────────────────┐
│ Tab: INFORMASI UMUM                        │
├─────────────────────────────────────────────┤
│                                             │
│ Nama Sekolah: *                             │
│ [SDIT-Balikpapan Islamic School______]     │
│                                             │
│ Tagline/Slogan:                             │
│ [Cerdas dan Berkarakter Qur'ani______]     │
│                                             │
│ Tahun Berdiri:                              │
│ [2014]                                      │
│                                             │
│ Deskripsi Singkat (Landing Page):           │
│ [Rich Text Editor]                          │
│ [SDIT-Balikpapan telah berdiri sejak...]   │
│                                             │
│ Deskripsi Lengkap (Halaman About):          │
│ [Rich Text Editor]                          │
│ [SDIT-Balikpapan Islamic School...]        │
│                                             │
│ Statistik Display:                          │
│ ☑ Tampilkan di Landing                      │
│ Jumlah Guru: [72] (Auto-sync dari DB)      │
│ Label Guru: [Guru & Pengajaran______]      │
│ Jumlah Murid: [300+] (Manual input)        │
│ Label Murid: [Murid__________________]      │
│                                             │
│ Logo Sekolah:                               │
│ [📁 Upload Logo] (PNG, Max 1MB)            │
│ [Preview Logo]                              │
│                                             │
│ [💾 Simpan] [🔄 Reset] [👁️ Preview]       │
└─────────────────────────────────────────────┘

┌─────────────────────────────────────────────┐
│ Tab: VISI & MISI                           │
├─────────────────────────────────────────────┤
│                                             │
│ VISI KAMI:                                  │
│ [+ Tambah Point Visi]                       │
│                                             │
│ 1. [Icon ▼] Menyebarkan pendidikan...      │
│    [Edit] [Delete] [↑] [↓]                 │
│                                             │
│ 2. [Icon ▼] Menyebarkan pendidikan...      │
│    [Edit] [Delete] [↑] [↓]                 │
│                                             │
│ 3. [Icon ▼] Meningkatkan budaya...         │
│    [Edit] [Delete] [↑] [↓]                 │
│                                             │
│ ... (Total 5 point)                         │
│                                             │
│ MISI KAMI:                                  │
│ [+ Tambah Point Misi]                       │
│                                             │
│ 1. [Icon ▼] Mengembangkan jiwa...          │
│    [Edit] [Delete] [↑] [↓]                 │
│                                             │
│ 2. [Icon ▼] Mengembangkan budaya...        │
│    [Edit] [Delete] [↑] [↓]                 │
│                                             │
│ ... (Total 6 point)                         │
│                                             │
│ Icon Options:                               │
│ • 📚 Book • 🎓 Graduate • ⭐ Star          │
│ • 🎯 Target • 💡 Light • ✅ Check         │
│ • Custom Icon Upload                        │
│                                             │
│ [💾 Simpan Semua] [👁️ Preview Landing]    │
└─────────────────────────────────────────────┘

┌─────────────────────────────────────────────┐
│ Tab: FASILITAS                             │
├─────────────────────────────────────────────┤
│                                             │
│ [+ Tambah Fasilitas Baru]                   │
│                                             │
│ Grid Layout (Edit Mode):                    │
│                                             │
│ ┌──────────┐ ┌──────────┐ ┌──────────┐     │
│ │ [Foto 1] │ │ [Foto 2] │ │ [Foto 3] │     │
│ │ Ruang    │ │ Lab      │ │ Perpus   │     │
│ │ Multi    │ │ Komputer │ │          │     │
│ │ media    │ │          │ │          │     │
│ │[Edit][X] │ │[Edit][X] │ │[Edit][X] │     │
│ └──────────┘ └──────────┘ └──────────┘     │
│                                             │
│ ┌──────────┐ ┌──────────┐ ┌──────────┐     │
│ │ [Foto 4] │ │ [Foto 5] │ │ [Foto 6] │     │
│ │ Halaman &│ │ Unit     │ │ Ruang BK │     │
│ │ Taman    │ │ Kesehatan│ │          │     │
│ │          │ │          │ │          │     │
│ │[Edit][X] │ │[Edit][X] │ │[Edit][X] │     │
│ └──────────┘ └──────────┘ └──────────┘     │
│                                             │
│ Form Tambah/Edit Fasilitas:                 │
│                                             │
│ Nama Fasilitas: *                           │
│ [_____________________________________]     │
│                                             │
│ Deskripsi (Optional):                       │
│ [_____________________________________]     │
│                                             │
│ Foto Fasilitas: * (Recommended: 600x400)    │
│ [📁 Upload Foto] (Max 2MB)                 │
│ [Preview]                                   │
│                                             │
│ Layout Grid:                                │
│ ⚫ Full Width (1 kolom)                     │
│ ⚪ Half Width (2 kolom)                     │
│ ⚪ Third Width (3 kolom) - Default          │
│                                             │
│ Display Order: [___]                        │
│                                             │
│ [💾 Simpan] [❌ Batal]                     │
│                                             │
│ Current Facilities: 8                       │
│ ├─ Ruang Multimedia                         │
│ ├─ Lab Komputer                             │
│ ├─ Ruang Perpustakaan                       │
│ ├─ Halaman & Taman Sekolah                  │
│ ├─ Unit Kesehatan Sekolah                   │
│ ├─ Ruang BK                                 │
│ ├─ Ruang Counseling                         │
│ └─ Toilet                                   │
│                                             │
│ [💾 Simpan Semua] [👁️ Preview Landing]    │
└─────────────────────────────────────────────┘

┌─────────────────────────────────────────────┐
│ Tab: GALERI KEGIATAN                       │
├─────────────────────────────────────────────┤
│                                             │
│ [+ Upload Foto Kegiatan] [+ Upload Batch]   │
│                                             │
│ Galeri Preview (Grid Masonry):              │
│                                             │
│ ┌──────┐ ┌────────┐ ┌──────┐               │
│ │ [1]  │ │ [2]    │ │ [5]  │               │
│ │      │ │        │ │      │               │
│ └──────┘ │        │ └──────┘               │
│ ┌──────┐ │        │ ┌──────┐               │
│ │ [3]  │ │        │ │ [6]  │               │
│ │      │ │        │ │      │               │
│ └──────┘ └────────┘ └──────┘               │
│ ┌──────┐ ┌──────┐ ┌────────┐               │
│ │ [4]  │ │ [7]  │ │ [8]    │               │
│ │      │ │      │ │        │               │
│ └──────┘ └──────┘ │        │               │
│                   │        │               │
│                   └────────┘               │
│                                             │
│ Each Photo:                                 │
│ - Thumbnail preview                         │
│ - Title/Caption (editable)                  │
│ - Date uploaded                             │
│ - [Edit] [Delete] [Set Featured]            │
│                                             │
│ Upload Form:                                │
│ ┌─────────────────────────────────────┐     │
│ │ Upload Foto Kegiatan                │     │
│ ├─────────────────────────────────────┤     │
│ │                                     │     │
│ │ Judul/Caption:                      │     │
│ │ [_____________________________]     │     │
│ │                                     │     │
│ │ Tanggal Kegiatan:                   │     │
│ │ [20 Nov 2024] 📅                   │     │
│ │                                     │     │
│ │ Upload Foto:                        │     │
│ │ [📁 Choose Files] (Multiple)       │     │
│ │ Max 5MB per foto                    │     │
│ │                                     │     │
│ │ Kategori Kegiatan:                  │     │
│ │ [Dropdown ▼]                        │     │
│ │ • Prestasi Siswa                    │     │
│ │ • Kegiatan Kelas                    │     │
│ │ • Event Sekolah                     │     │
│ │ • Ekstrakurikuler                   │     │
│ │                                     │     │
│ │ ☐ Tampilkan di Hero Landing Page    │     │
│ │                                     │     │
│ │ [💾 Upload] [❌ Batal]             │     │
│ └─────────────────────────────────────┘     │
│                                             │
│ Total Galeri: 45 foto                       │
│ Storage Used: 156MB / 500MB                 │
│                                             │
│ [💾 Simpan Order] [👁️ Preview Landing]    │
└─────────────────────────────────────────────┘
```

**Display di Landing Page:**
```
HOMEPAGE:
- Hero: Slider galeri featured (3-5 foto)
- Galeri Section: Grid 6 foto terbaru
- CTA: "Lihat Semua Galeri"

TENTANG KAMI:
- Visi & Misi (dengan ikon)
- Fasilitas (grid 3 kolom dengan foto)
- Galeri Kegiatan (4 foto preview)
```

---

### 6. DATA GURU DI LANDING PAGE ⭐

**Auto-sync dari Data Master:**
```
📊 SYNC DATA GURU KE LANDING PAGE

Konfigurasi:
┌─────────────────────────────────────────────┐
│ Data Guru untuk Landing Page               │
├─────────────────────────────────────────────┤
│                                             │
│ ☑ Sinkronisasi Otomatis dengan Data Master │
│                                             │
│ Kolom yang Ditampilkan:                     │
│ ☑ No (auto)                                 │
│ ☑ Nama                                      │
│ ☑ NIY                                       │
│ ☑ Jenis Kelamin                             │
│ ☑ Jabatan                                   │
│ ☐ Foto (Optional)                           │
│                                             │
│ Filter & Privacy:                           │
│ ☐ Tampilkan semua guru                      │
│ ⚫ Hanya guru dengan flag "Public=Yes"      │
│ ☐ Exclude role tertentu                     │
│                                             │
│ Tampilan Tabel:                             │
│ Baris per halaman: [10 ▼]                  │
│ ☑ Pagination                                │
│ ☑ Search functionality                      │
│ ☐ Sort by kolom                             │
│                                             │
│ Custom Header:                              │
│ Page Title: [Guru & Staf_______________]    │
│ Subtitle: [Daftar Guru & Staf SDIT...]     │
│                                             │
│ Preview di Landing:                         │
│ [👁️ Preview SDM Page]                      │
│                                             │
│ Current Data:                               │
│ Total Guru di Database: 72                  │
│ Tampil di Landing: 72 (100%)                │
│ Hidden: 0 (0%)                              │
│                                             │
│ Last Sync: 20 Nov 2024, 14:30 WITA          │
│ [🔄 Sync Now]                               │
│                                             │
│ [💾 Simpan Settings]                        │
└─────────────────────────────────────────────┘

Landing Page Display:
┌─────────────────────────────────────────────┐
│ Header: Guru & Staf                        │
│ Subtitle: Daftar Guru & Staf SDIT-BIS      │
├─────────────────────────────────────────────┤
│                                             │
│ ┌─ Table (Yellow Header) ─────────────────┐ │
│ │ No | Nama | NIY | JK | Jabatan         │ │
│ ├─────────────────────────────────────────┤ │
│ │ 1  | Ratnawati, S.Pd. | 00432013 |     │ │
│ │    | Perempuan | Kepala Sekolah        │ │
│ ├─────────────────────────────────────────┤ │
│ │ 2  | Armina Oktavia, S.Pd. | 00532015  │ │
│ │    | Perempuan | Wakasek Kesiswaan     │ │
│ ├─────────────────────────────────────────┤ │
│ │ 3  | Nurlitri Nurani, S.I.Kom. | ...   │ │
│ │    | Perempuan | Wakasek Kurikulum     │ │
│ └─────────────────────────────────────────┘ │
│                                             │
│ Showing 1 to 10 of 72 entries               │
│ [Previous] [1] [2] [3] ... [Next]           │
└─────────────────────────────────────────────┘
```

---

## 📱 MOBILE APP

### Platform
- Android 8.0+
- iOS 12.0+

### Target User
✅ **Role yang Dapat Absen via Mobile:**
- Kepala Sekolah
- Admin / Staff TU
- Wali Kelas
- Guru

❌ **Role Web Only (Tidak Ada Mobile App):**
- Super Admin
- Orang Tua

### Important Notes
- ✅ **Banner Pop-up**: Notifikasi dengan gambar (web & mobile untuk guru/staff)
- ✅ **Foto Kelas Wajib**: Tidak bisa skip (untuk Guru & Wali Kelas)
- ✅ **GPS Required**: Untuk semua absen mobile (Kepsek, Admin/TU, Wali, Guru)
- ✅ **Face Recognition**: Untuk semua role yang absen mobile
- ✅ **Internet Required**: Semua fitur
- ℹ️ **Orang Tua**: Akses web only untuk melihat statistik & kehadiran anak

---

### FITUR MOBILE

#### 1. Dashboard

**Untuk Kepala Sekolah, Admin/TU, Wali Kelas, Guru:**
```
Components:
- Greeting & Date
- Banner Pop-up (jika ada pengumuman aktif) ⭐
- GPS Status: 📍 "Di Area Sekolah" / ⚠️ "Di Luar Area"
- Face Recognition Status
- Role-specific info:
  ├─ Kepsek: Statistik kehadiran hari ini
  ├─ Admin/TU: Quick access data entry
  ├─ Wali Kelas: Info kelas & jadwal
  └─ Guru: Jadwal mengajar hari ini
- Jadwal Mengajar (untuk Wali & Guru)
  ├─ Status presensi siswa: ✅/❌
  └─ Status foto kelas: 📷 ✅/❌
- Quick Stats
- Status Kehadiran Sendiri
```

#### 2. Presensi Siswa + Foto Kelas (Guru & Wali Kelas) ⭐

**Step 1: Input Presensi (Quick Mode)**
```
Target: 2-3 menit untuk 30 siswa

- List siswa dengan foto
- Swipe Right → ✅ Hadir
- Swipe Left → Status Options
- Bulk action: [Set All Hadir]
- Status: Hadir/Sakit/Izin/Alpa/Terlambat
```

**Step 2: Upload Foto Kelas (WAJIB)**
```
Setelah mark semua siswa:

┌─────────────────────────────────┐
│ 📷 FOTO KELAS (Bukti Mengajar) │
├─────────────────────────────────┤
│ Foto kelas wajib sebagai bukti  │
│                                 │
│ [📷 AMBIL FOTO SEKARANG]       │
│ [📁 Upload dari Galeri]         │
└─────────────────────────────────┘

After capture:
- Preview foto
- Validasi otomatis:
  ✅ Size: 2.1 MB (Valid)
  ✅ Resolution: 1920x1080
  ✅ Faces detected: 8
- [🔄 Ambil Ulang] [✅ Gunakan]

Upload:
- Progress bar
- Auto-watermark
- Success: "Presensi & foto tersimpan"

Error jika tidak upload:
❌ "Foto kelas wajib diupload"
```

#### 3. Absen (Kepsek, Admin/TU, Wali Kelas, Guru) ⭐

**Pre-check GPS:**
```
Berlaku untuk:
├─ Kepala Sekolah
├─ Admin / Staff TU
├─ Wali Kelas
└─ Guru

Flow:
1. User tap "Absen Sekarang"
2. Check GPS Location
   ├─ Get current coordinates
   ├─ Calculate distance dari sekolah
   ├─ If OUTSIDE radius (>100m):
   │  └─ BLOCK dengan error:
   │     ┌──────────────────────────┐
   │     │ ⚠️ DI LUAR AREA SEKOLAH │
   │     ├──────────────────────────┤
   │     │ Jarak: 487 meter        │
   │     │ Max: 100 meter          │
   │     │                         │
   │     │ Role: [Guru]            │
   │     │ Nama: [Ahmad Yani]      │
   │     │                         │
   │     │ [🗺️ Buka Maps]         │
   │     │ [🔄 Cek Ulang]         │
   │     │ [📞 Hubungi Admin]     │
   │     └──────────────────────────┘
   │     └─> STOP (tidak bisa lanjut)
   │
   └─ If INSIDE radius:
      └─> Continue ke Face Recognition ✓
```

**Face Recognition Camera:**
```
Interface:
- Live camera preview
- Face detection overlay (green box)
- GPS Indicator (top): 
  "📍 Di Area Sekolah ✓ (45m)"
- Role Display: [Guru / Wali Kelas / Admin / Kepsek / Orang Tua]
- Status: "😊 Wajah terdeteksi!"

Auto-capture → Extract descriptor → Send to server

Server Validation:
1. Face match ≥85%? 
2. GPS inside radius?
3. Role valid?
4. All valid → ✅ Save attendance

Success Screen (Different by Role):

For Guru/Wali/Admin/Kepsek:
┌──────────────────────────┐
│ ✅ ABSEN BERHASIL!      │
├──────────────────────────┤
│ Check-in: 07:05:30      │
│ Role: Guru              │
│ Kecocokan: 94%          │
│ 📍 Lokasi: 45m          │
│                         │
│ Selamat Mengajar! 📚    │
└──────────────────────────┘

Failed - Face (<85%):
- Show tips
- [Coba Lagi] (max 3x)
- After 3x: [Input Manual + Admin Approval]

Failed - GPS Outside:
┌──────────────────────────┐
│ ⚠️ DI LUAR AREA         │
├──────────────────────────┤
│ Face berhasil tapi GPS  │
│ di luar radius.         │
│                         │
│ Silakan hubungi admin   │
│ untuk approval manual.  │
│                         │
│ [📞 Hubungi Admin]      │
└──────────────────────────┘
```

**Manual Fallback (dengan Approval):**
```
Setelah 3x gagal face recognition:

Form Manual:
┌──────────────────────────────────┐
│ 📝 Absen Manual                 │
│ (Perlu Approval Admin)          │
├──────────────────────────────────┤
│                                 │
│ Nama: [Auto-fill dari profile] │
│ Role: [Auto-fill]               │
│                                 │
│ Waktu: [07:15] (editable)       │
│                                 │
│ Alasan:                         │
│ ⚪ Face Recognition Gagal       │
│ ⚪ Camera Error                  │
│ ⚪ Kondisi Cahaya Buruk          │
│ ⚪ Lainnya: [______________]    │
│                                 │
│ Foto Bukti: * (Required)        │
│ [📷 Ambil Foto Wajah]          │
│ [Preview]                       │
│                                 │
│ GPS Location: (auto-captured)   │
│ Lat: -1.2659, Long: 116.8289    │
│ Jarak: 45m                      │
│                                 │
│ Catatan Tambahan:               │
│ [_________________________]     │
│                                 │
│ ⚠️ Status: PENDING APPROVAL    │
│                                 │
│ [✅ Submit] [❌ Batal]          │
└──────────────────────────────────┘

After Submit:
- Notif ke admin
- Status di dashboard: "⏳ Pending"
- Track approval status
```

#### 4. Banner Pop-up (Semua Role) ⭐

```
Trigger: 
- Saat buka app / login
- Saat masuk dashboard
- Interval tertentu (jika multi banner)

Display:
┌────────────────────────────────────┐
│                              [✕]   │
│  [🖼️ Banner Image Full Width]     │
│                                    │
│  [Button: Info Selengkapnya →]    │
│  (Optional, jika ada URL)          │
│                                    │
│  ☐ Jangan tampilkan lagi hari ini │
└────────────────────────────────────┘

Features:
- Full-screen modal overlay
- Swipe down to dismiss
- Tap outside to close
- Button action (jika ada)
  ├─ Open URL in-app browser
  ├─ Navigate to specific page
  └─ Download file (jika lampiran)
- Cookie: "Don't show again today"
- Priority sorting (High first)
- Target audience filtering

Banner Types:
├─ Urgent (Red border)
├─ Normal (Yellow border)
└─ Info (Blue border)

Examples for Different Roles:

Guru/Wali Kelas:
- Pengumuman rapat guru
- Update jadwal
- Informasi training

Admin/TU/Kepsek:
- Deadline report
- System maintenance
- Policy update

Public (Landing Page):
- Pendaftaran siswa baru
- Open house event
- Prestasi sekolah

Note: Banner untuk Orang Tua ditampilkan di Web Dashboard
```

#### 5. Monitoring & Laporan

**Untuk Guru/Wali Kelas:**
```
- Real-time monitoring presensi siswa
- View foto kelas (thumbnail → full)
- History presensi
- Laporan per kelas/mapel
```

**Untuk Admin/TU/Kepsek:**
```
- Monitoring all
- GPS compliance stats
- Face recognition analytics
- Approval pending list
- Comprehensive reports
```

**Untuk Orang Tua (Web Dashboard):**
```
- Kehadiran anak (kalender view)
- Statistik bulanan & grafik
- History izin anak
- Download laporan kehadiran
- Submit izin untuk anak
```

#### 6. Profile & Settings

**Semua Role (Mobile):**
```
Profile:
- Foto profil
- Nama lengkap
- Role/Jabatan
- Face Recognition Status
- GPS Compliance: 18/20 (90%)
- Total Absen (bulan ini)

Settings:
├─ Notifikasi
│  ├─ Banner Pop-up: ON
│  ├─ Push Notification: ON
│  └─ Email Notification: OFF
├─ Tampilan
│  ├─ Theme: Light/Dark
│  └─ Language: Indonesia/English
├─ Keamanan
│  ├─ Change Password
│  ├─ Face Recognition
│  │  ├─ Register/Update Face
│  │  └─ Face Data Status
│  └─ PIN Code
└─ GPS & Face Recognition
   ├─ GPS Tracking: ON (Required)
   ├─ Show Distance: ON
   ├─ Anti-spoofing: Normal
   └─ Camera: Front
```

---

## 🛠️ TECH STACK

### Backend
```
Framework:    Laravel 10+
Language:     PHP 8.1+
Database:     MySQL 8.0 / PostgreSQL 14+
Cache:        Redis 7+
API:          RESTful + JWT
Storage:      Local / AWS S3 / Google Cloud
CMS:          Built-in (Artikel, Banner, Profil)
Queue:        Laravel Queue (for notifications)
```

### Web Frontend
```
Template:     Blade / Vue.js / React
CSS:          Tailwind CSS / Bootstrap 5
Charts:       Chart.js / ApexCharts
Maps:         Leaflet.js / Google Maps API
Editor:       TinyMCE / CKEditor (Rich Text)
Lightbox:     Fancybox / PhotoSwipe (Galeri)
```

### Mobile App
```
Framework:    Flutter 3.16+
Language:     Dart 3.2+
State:        Provider / Riverpod
Face:         google_ml_kit (ML Kit Face Detection)
GPS:          geolocator package
Camera:       camera package
Image:        image_picker / image_cropper
HTTP:         Dio
Push:         Firebase Cloud Messaging (FCM)
Local DB:     Sqflite / Hive
```

### Face Recognition
```
Client (Flutter):
- ML Kit Face Detection
- Extract 128D descriptor
- Liveness detection (anti-spoofing)

Server (Laravel):
- Cosine Similarity comparison
- Threshold: 85% (configurable)
- Storage: MySQL JSON
- Berlaku untuk: Kepsek, Admin/TU, Wali Kelas, Guru
```

### GPS & Location
```
Client (Flutter):
- geolocator package
- Get coordinates (lat, long)
- Accuracy tracking
- Background location (optional)

Server (Laravel):
- Haversine Formula
- Distance calculation
- Radius validation
- Berlaku untuk: Kepsek, Admin/TU, Wali, Guru, Orang Tua
```

### Banner Pop-up System
```
Backend:
- Table: banners
  ├─ id, title, image_path
  ├─ target_audience (json)
  ├─ priority, start_date, end_date
  ├─ url_action, button_text
  └─ views, clicks, active
- API: /api/banners/active
- Image Processing: Intervention/Image

Frontend (Web & Mobile):
- Modal/Overlay component
- Cookie management (don't show again)
- Click tracking
- Responsive image
```

### Landing Page CMS
```
Tables:
- articles (title, slug, content, category, author, status, views)
- article_categories
- school_profile (visi, misi, facilities)
- school_gallery (photos, category, featured)
- banners (pengumuman pop-up)

Features:
- SEO-friendly URLs
- Image optimization
- Page caching
- Sitemap generation
```

---

## 📊 PERFORMANCE TARGETS

**Mobile App:**
- App size: <65MB (termasuk banner assets)
- Cold start: <3s
- Face recognition: <3s
- GPS lock: <5s (outdoor)
- Photo upload: <10s (5MB on 4G)
- Input presensi + foto: <4 minutes
- Banner pop-up load: <1s

**Web:**
- Page load: <2s
- Dashboard refresh: <1s
- Report generation: <5s
- Landing page: <1.5s
- Article page: <1.5s
- Banner upload: <3s

**CMS:**
- Article creation: Smooth editing
- Image upload: <5s per image
- Bulk upload: <30s for 10 images
- Gallery load: <2s

---

## 🔄 WORKFLOW EXAMPLES

### 1. Workflow Absen Guru/Wali Kelas di Mobile
```
1. Guru buka app (07:00)
2. Banner pop-up muncul (jika ada)
   └─ "Rapat Guru Hari Ini 15:00"
3. GPS check: ✓ Dalam radius (45m)
4. Face recognition: ✓ 92% match
5. Absen berhasil tersimpan
6. Dashboard update status: ✅ Hadir
7. Lihat jadwal mengajar hari ini
8. Input presensi siswa (kelas X IPA 1)
9. Upload foto kelas (wajib)
10. Selesai
```

### 2. Workflow Admin Upload Banner
```
1. Admin login web
2. Menu: Notifikasi → Banner Pengumuman
3. [+ Upload Banner Baru]
4. Upload gambar (800x600)
5. Set target: Orang Tua
6. Set periode: 20-25 Nov 2024
7. Aktifkan pop-up: ✓
8. Priority: High
9. [Upload & Publish]
10. Banner aktif dan muncul di web dashboard orang tua
```

### 3. Workflow Orang Tua Melihat Statistik Anak (Web) ⭐
```
1. Orang Tua login ke web dashboard
2. Banner pop-up muncul: "Pengumpulan Rapor 20-25 Nov"
3. Dashboard menampilkan:
   ├─ Status kehadiran anak hari ini: ✅ Hadir
   ├─ Kalender kehadiran bulan ini
   └─ Statistik: Hadir 85%, Sakit 5%, Izin 8%, Alpa 2%
4. Klik "Kehadiran Anak"
5. View kalender detail per hari
6. View grafik statistik (bulanan/semester)
7. Check history izin yang pernah diajukan
8. Submit izin baru jika anak sakit
9. Download laporan kehadiran (PDF/Excel)
```

### 4. Workflow Pengunjung Landing Page
```
1. Buka website sekolah
2. Homepage:
   ├─ Hero banner "Cerdas dan Berkarakter Qur'ani"
   ├─ Banner pop-up: "Pendaftaran Siswa Baru 2025" (Public)
   ├─ Scroll: Profil sekolah
   ├─ Statistik: 72 Guru, 300+ Murid
   └─ Artikel terbaru (3 preview)
3. Klik menu "Tentang Kami"
   ├─ Profil lengkap
   ├─ Visi & Misi (5+6 point)
   ├─ Fasilitas (grid foto)
   └─ Galeri kegiatan
4. Klik menu "SDM"
   └─ Table guru & staff (pagination)
5. Klik menu "Artikel"
   └─ Browse artikel by category
6. Tertarik → Klik "Registrasi"
   └─ Form pendaftaran / contact
```

### 5. Workflow Naik Kelas Massal (Admin) ⭐
```
Skenario: Akhir tahun ajaran 2024/2025, siswa Kelas 1A naik ke Kelas 2A

1. Admin login web
2. Menu: Data Master → Kelola Kelas Siswa
3. Tab: Naik Kelas Massal
4. Form Input:
   ├─ Tahun Ajaran Sumber: 2024/2025
   ├─ Kelas Sumber: Kelas 1A (30 siswa)
   ├─ Tahun Ajaran Tujuan: 2025/2026
   └─ Kelas Tujuan: Kelas 2A
5. [Preview Siswa]
   └─ Table showing all 30 students
6. [Execute Naik Kelas]
7. System Processing:
   For each student:
   ├─ Update riwayat lama: status → 'selesai', tanggal_selesai → today
   ├─ Update siswa.kelas_id → Kelas 2A
   └─ Create riwayat baru: Kelas 2A, status → 'aktif'
8. Success notification
9. Generate report: "30 siswa berhasil naik kelas"
10. Auto-notify parents via WhatsApp/Email
```

### 6. Workflow Pindah Kelas Individual (Admin) ⭐
```
Skenario: Ahmad pindah dari Kelas 2A ke Kelas 2B (mid-year)

1. Admin: Data Master → Kelola Kelas Siswa
2. Tab: Pindah Kelas Individual
3. Search siswa: "Ahmad" (NIS: 2024001)
4. Current info displayed:
   ├─ Nama: Ahmad Fauzi
   ├─ Kelas Sekarang: Kelas 2A
   ├─ Wali Kelas: Ibu Siti
   └─ Riwayat: 1A (2024) → 2A (2025, aktif)
5. Form Pindah Kelas:
   ├─ Kelas Tujuan: [Dropdown] Kelas 2B
   ├─ Tanggal Pindah: [15 Nov 2025]
   ├─ Alasan: [Permintaan orang tua]
   └─ Catatan: [Optional]
6. [Validasi] - Check if target class has capacity
7. [Proses Pindah]
8. System:
   ├─ Update riwayat lama (2A): status → 'pindah', tanggal_selesai
   ├─ Update siswa.kelas_id → Kelas 2B
   ├─ Create riwayat baru (2B): status → 'aktif'
   └─ Notify: Old wali kelas, New wali kelas, Parent
9. Success: "Ahmad berhasil dipindahkan ke Kelas 2B"
```

### 7. Workflow Orang Tua Lihat Riwayat Kelas ⭐
```
1. Buka website sekolah
2. Homepage:
   ├─ Hero banner "Cerdas dan Berkarakter Qur'ani"
   ├─ Banner pop-up: "Pendaftaran Siswa Baru 2025" (Public)
   ├─ Scroll: Profil sekolah
   ├─ Statistik: 72 Guru, 300+ Murid
   └─ Artikel terbaru (3 preview)
3. Klik menu "Tentang Kami"
   ├─ Profil lengkap
   ├─ Visi & Misi (5+6 point)
   ├─ Fasilitas (grid foto)
   └─ Galeri kegiatan
4. Klik menu "SDM"
   └─ Table guru & staff (pagination)
5. Klik menu "Artikel"
   └─ Browse artikel by category
6. Tertarik → Klik "Registrasi"
   └─ Form pendaftaran / contact
```

---

## 📚 RELATED DOCUMENTATION

### **Student Class History Management** ⭐

Sistem ini mendukung pengelolaan riwayat kelas siswa untuk menangani kasus:
- ✅ **Naik Kelas**: Siswa pindah ke tingkat berikutnya (Kelas 1A → Kelas 2A)
- ✅ **Pindah Kelas**: Siswa pindah rombel (Kelas 2A → Kelas 2B)
- ✅ **Mutasi**: Siswa pindah sekolah

**Struktur Data:**
```
Table: siswa
- kelas_id: Selalu menunjuk ke kelas AKTIF saat ini

Table: riwayat_kelas_siswa
- Menyimpan SEMUA riwayat kelas siswa
- Status: aktif (1 record), selesai, pindah, mutasi
```

**Workflow Naik Kelas:**
```
Skenario: Ahmad naik dari Kelas 1A ke Kelas 2A

1. Tahun Ajaran 2024/2025:
   siswa.kelas_id = Kelas 1A
   riwayat_kelas_siswa:
   - kelas_id: Kelas 1A
   - status: aktif
   - tanggal_mulai: 2024-07-01
   - tanggal_selesai: null

2. Naik Kelas (2025-06-30):
   Admin/TU melakukan "Naik Kelas Massal"
   
   Step 1: Update record lama
   riwayat_kelas_siswa (record lama):
   - status: aktif → selesai
   - tanggal_selesai: 2025-06-30
   
   Step 2: Update siswa.kelas_id
   siswa.kelas_id = Kelas 1A → Kelas 2A
   
   Step 3: Create record baru
   riwayat_kelas_siswa (record baru):
   - siswa_id: Ahmad
   - kelas_id: Kelas 2A
   - tahun_ajaran_id: 2025/2026
   - status: aktif
   - tanggal_mulai: 2025-07-01
   - tanggal_selesai: null

3. Tahun Ajaran 2025/2026:
   siswa.kelas_id = Kelas 2A
   
   Riwayat lengkap Ahmad:
   [2024/2025] Kelas 1A (status: selesai)
   [2025/2026] Kelas 2A (status: aktif) ← current
```

**Workflow Pindah Kelas:**
```
Skenario: Siti pindah dari Kelas 2A ke Kelas 2B (mid-year)

1. Kondisi Awal:
   siswa.kelas_id = Kelas 2A
   riwayat_kelas_siswa:
   - kelas_id: Kelas 2A
   - status: aktif

2. Proses Pindah Kelas:
   
   Update record lama:
   - status: aktif → pindah
   - tanggal_selesai: 2024-11-15
   - keterangan: "Pindah ke Kelas 2B atas permintaan orang tua"
   
   Update siswa:
   - siswa.kelas_id = Kelas 2B
   
   Create record baru:
   - kelas_id: Kelas 2B
   - status: aktif
   - tanggal_mulai: 2024-11-16
```

**Features di Web Admin:**
```
📊 Menu: Data Master → Kelola Kelas Siswa

1. NAIK KELAS MASSAL
   - Pilih tahun ajaran
   - Pilih kelas sumber (misal: Kelas 1A)
   - Pilih kelas tujuan (misal: Kelas 2A)
   - Preview siswa yang akan naik
   - [Execute Naik Kelas]
   - System auto-update:
     ├─ siswa.kelas_id
     ├─ riwayat (status: selesai)
     └─ riwayat baru (status: aktif)

2. PINDAH KELAS INDIVIDUAL
   - Search siswa
   - Pilih kelas tujuan
   - Tanggal pindah
   - Alasan pindah
   - [Simpan]
   - System auto-create riwayat

3. VIEW RIWAYAT KELAS
   - Per siswa: Lihat semua kelas yang pernah dijalani
   - Timeline view dengan status
   - Export history ke PDF
```

**Query Examples:**
```sql
-- Get current class of student
SELECT s.nama_lengkap, k.nama as kelas_sekarang
FROM siswa s
JOIN kelas k ON s.kelas_id = k.id
WHERE s.id = 1;

-- Get full class history of student
SELECT 
  s.nama_lengkap,
  k.nama as kelas,
  ta.nama as tahun_ajaran,
  rk.tanggal_mulai,
  rk.tanggal_selesai,
  rk.status
FROM riwayat_kelas_siswa rk
JOIN siswa s ON rk.siswa_id = s.id
JOIN kelas k ON rk.kelas_id = k.id
JOIN tahun_ajaran ta ON rk.tahun_ajaran_id = ta.id
WHERE s.id = 1
ORDER BY rk.tanggal_mulai DESC;

-- Get all students in specific class with their history
SELECT 
  s.nama_lengkap,
  COUNT(rk.id) as jumlah_pindah_kelas
FROM siswa s
LEFT JOIN riwayat_kelas_siswa rk ON s.id = rk.siswa_id
WHERE s.kelas_id = 5  -- Kelas 2A
GROUP BY s.id;

-- Get attendance across all classes
SELECT 
  s.nama_lengkap,
  k.nama as kelas,
  ps.tanggal,
  ps.status
FROM presensi_siswa ps
JOIN siswa s ON ps.siswa_id = s.id
JOIN kelas k ON ps.kelas_id = k.id
WHERE s.id = 1
ORDER BY ps.tanggal DESC;
```

**Reports & Analytics:**
```
Laporan yang Memanfaatkan Riwayat Kelas:

1. Laporan Kehadiran Per Tahun Ajaran
   - Aggregate attendance per year per student
   - Show class transitions
   - Compare performance across classes

2. Laporan Tracking Siswa
   - Full student journey from Kelas 1 to 6
   - Performance trends
   - Behavior trends

3. Dashboard Orang Tua
   - Current class info
   - Historical performance
   - "Anak Anda telah menyelesaikan Kelas 1A 
      dengan kehadiran 95%"
```

**Important Notes:**
- ⚠️ Only ONE record per student can have `status = 'aktif'`
- ✅ `siswa.kelas_id` always reflects CURRENT class
- ✅ All historical data preserved in `riwayat_kelas_siswa`
- ✅ Presensi data always references correct class at time of attendance
- ✅ Parent dashboard shows current class + full history

---

## 📚 RELATED DOCUMENTATION

- **README.md** - Full documentation
- **Web_Menu_Fitur_Lengkap.md** - Detailed web features
- **Mobile_App_Screens_Lengkap.md** - Mobile UI/UX flows
- **Landing_Page_Design.md** - Landing page specifications
- **Banner_System.md** - Banner pop-up documentation
- **Arsitektur_Face_Recognition.md** - Face recognition architecture
- **Fitur_Modul_Sistem_Presensi.md** - All modules & features

---

## 📝 NOTES & BEST PRACTICES

### Landing Page
- Optimasi SEO: meta tags, sitemap, robots.txt
- Responsive design: mobile-first approach
- Fast loading: lazy load images, caching
- Accessibility: alt text, ARIA labels
- Analytics: Google Analytics integration

### Banner Pop-up
- Jangan terlalu sering muncul (max 1x per day per user)
- Respect user preference ("Don't show again")
- Clear close button
- Mobile-friendly size
- Track performance (views, clicks, CTR)

### Orang Tua (Web Only)
- Web dashboard untuk monitoring kehadiran anak
- Real-time statistics & grafik kehadiran
- Submit izin untuk anak via web
- Banner pengumuman ditampilkan di web dashboard
- Download laporan kehadiran anak
- Komunikasi dengan wali kelas via web

### Content Management
- Regular content update (min 2 artikel/minggu)
- High-quality images (optimized)
- SEO-friendly content
- Social media integration
- Comment moderation (jika enabled)

### Security
- HTTPS only
- CSRF protection
- XSS prevention
- SQL injection prevention
- Rate limiting API
- Secure file upload validation
- Face data encryption
- GPS location encryption

---

### 7. Workflow Orang Tua Lihat Riwayat Kelas ⭐
```
1. Orang Tua login web dashboard
2. Banner pop-up: "Pengumuman Libur Semester"
3. Dashboard shows:
   ├─ "Ahmad - Kelas 2A" (current)
   └─ "Kehadiran Hari Ini: Hadir ✓"
4. Klik "Profil Anak"
5. Section: Riwayat Kelas (Timeline View)
   ┌─────────────────────────────────────┐
   │ 📚 RIWAYAT KELAS                   │
   ├─────────────────────────────────────┤
   │                                     │
   │ ● 2025/2026 - Kelas 2A (Aktif)     │
   │   Jul 2025 - Sekarang              │
   │   Wali Kelas: Ibu Ratna            │
   │   Kehadiran: 95% (18/19 hari)      │
   │   [Lihat Detail]                   │
   │                                     │
   │ ○ 2024/2025 - Kelas 1A (Selesai)   │
   │   Jul 2024 - Jun 2025              │
   │   Wali Kelas: Ibu Siti             │
   │   Kehadiran: 96% (193/201 hari)    │
   │   [Lihat Detail] [Download Rapor]  │
   │                                     │
   └─────────────────────────────────────┘
6. Klik "Lihat Detail" pada Kelas 1A
7. View full attendance report for that year
8. View academic performance (if integrated)
9. Download PDF report per class/year
