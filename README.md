# 📚 SISTEM PRESENSI SEKOLAH
## Quick Reference Guide

---

## 🎯 OVERVIEW

Sistem Presensi Sekolah berbasis web (Laravel) dan mobile (Flutter) untuk mengelola kehadiran siswa dan guru.

### Key Features:
- ✅ **Presensi Siswa**: Diinput oleh GURU (bukan siswa yang absen sendiri)
- ✅ **Presensi Guru**: Guru absen sendiri dengan Face Recognition di mobile app
- ✅ **Foto Kelas Wajib**: Bukti mengajar untuk setiap input presensi siswa
- ✅ **Radius GPS**: Validasi lokasi guru saat absen (configurable di web)
- ✅ **Artikel & Berita**: Konten untuk landing page sekolah
- ✅ **Pengumuman Sekolah**: Sistem pengumuman internal dengan prioritas
- ✅ **7 User Roles** dengan RBAC lengkap
- ✅ **Web + Mobile Platform**

---

## 👥 USER ROLES

| No | Role | Platform | Description |
|----|------|----------|-------------|
| 1 | **Super Admin** | Web | Full system access |
| 2 | **Kepala Sekolah** | Web | Monitoring & approval |
| 3 | **Admin / Staff TU** | Web | CRUD data master |
| 4 | **Wali Kelas** | Web + Mobile | Manage class attendance |
| 5 | **Guru Mata Pelajaran** | Web + Mobile | Input presensi per subject |
| 6 | **Guru Piket** | Web + Mobile | Input keterlambatan, verifikasi izin |
| 7 | **Orang Tua** | Web | View child attendance, submit izin |

---

## 📑 MENU STRUCTURE

### 1. SUPER ADMIN (Web)

```
📊 Dashboard
👥 Manajemen User
   ├─ Daftar User
   ├─ Role & Permission
   └─ Activity Log
📚 Data Master
   ├─ Data Siswa
   ├─ Data Guru
   ├─ Data Kelas
   ├─ Jadwal Pelajaran
   └─ Tahun Ajaran
✅ Presensi
   ├─ Presensi Siswa
   │  └─ View Foto Kelas (Bukti Mengajar)
   ├─ Input Keterlambatan
   ├─ Monitoring Guru
   │  └─ GPS Location History
   └─ Face Recognition Data
📝 Perizinan
   ├─ List Semua Izin
   └─ Approval Izin
📊 Laporan
   ├─ Laporan Kehadiran Siswa (dengan foto)
   ├─ Laporan Kehadiran Guru
   │  └─ GPS Compliance Report
   └─ Custom Reports
📢 Notifikasi & Komunikasi
   ├─ Daftar Notifikasi
   ├─ Buat Pengumuman
   ├─ Broadcast WhatsApp
   └─ Riwayat Pengiriman
📰 Konten Website ⭐
   ├─ Artikel & Berita
   │  ├─ Daftar Artikel
   │  ├─ Tambah Artikel
   │  ├─ Edit/Hapus Artikel
   │  ├─ Kategori Artikel
   │  │  ├─ Berita Sekolah
   │  │  ├─ Prestasi
   │  │  ├─ Kegiatan
   │  │  └─ Pengumuman Umum
   │  ├─ Status (Draft/Published)
   │  └─ Featured Article
   └─ Pengumuman Sekolah
      ├─ Daftar Pengumuman
      ├─ Buat Pengumuman
      ├─ Edit/Hapus Pengumuman
      ├─ Prioritas (Urgent/Normal/Info)
      ├─ Target Audience
      │  ├─ Semua
      │  ├─ Guru
      │  ├─ Orang Tua
      │  └─ Per Kelas
      ├─ Masa Berlaku
      └─ Pin to Top
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
   ├─ Profil Sekolah
   └─ Kalender Akademik
👤 My Profile
🚪 Logout
```

### 2. KEPALA SEKOLAH (Web)

```
📊 Dashboard
📚 Data Master (View Only)
✅ Monitoring Presensi
   ├─ Monitoring Siswa (dengan foto kelas)
   ├─ Monitoring Guru (GPS location)
   └─ Face Recognition Status
📝 Perizinan
📊 Laporan
📢 Notifikasi & Komunikasi
   ├─ Daftar Notifikasi
   ├─ Buat Pengumuman
   └─ Broadcast WhatsApp
📰 Konten Website ⭐
   ├─ Artikel & Berita (Approve/View)
   └─ Pengumuman Sekolah
      ├─ View Semua
      ├─ Buat Pengumuman
      └─ Approve Pengumuman
⚙️ Pengaturan (View Only)
   ├─ Radius Absensi GPS
   └─ Website Settings
👤 My Profile
🚪 Logout
```

### 3. ADMIN / STAFF TU (Web)

```
📊 Dashboard
👥 Manajemen User
📚 Data Master (Full CRUD)
✅ Presensi
   ├─ Presensi Siswa
   │  ├─ Input Presensi
   │  ├─ Upload Foto Kelas (Wajib) ⭐
   │  ├─ View Foto Kelas
   │  └─ Monitoring Real-time
   ├─ Input Keterlambatan
   └─ Monitoring Guru (dengan GPS)
📝 Perizinan
📊 Laporan
📢 Notifikasi & Komunikasi
📰 Konten Website ⭐
   ├─ Artikel & Berita
   │  ├─ Daftar Artikel
   │  ├─ Tambah/Edit/Hapus Artikel
   │  ├─ Manage Kategori
   │  └─ Publish/Unpublish
   └─ Pengumuman Sekolah
      ├─ Daftar Pengumuman
      ├─ Buat Pengumuman
      ├─ Edit/Hapus Pengumuman
      └─ Set Target & Prioritas
⚙️ Pengaturan
   ├─ Radius Absensi GPS ⭐
   ├─ Foto Kelas Settings ⭐
   ├─ Website Settings ⭐
   ├─ Profil Sekolah
   └─ Kalender Akademik
👤 My Profile
🚪 Logout
```

### 4. WALI KELAS (Web + Mobile)

**Web:**
```
📊 Dashboard
📚 Kelas Saya
✅ Presensi
   ├─ Input Presensi Kelas
   ├─ Upload Foto Kelas (Wajib) ⭐
   ├─ View Foto Kelas
   └─ Monitoring Kehadiran
📝 Perizinan
📊 Laporan
📢 Komunikasi
   ├─ Kirim Pengumuman Kelas ⭐
   └─ Broadcast WhatsApp
📰 Artikel & Pengumuman (View) ⭐
👤 My Profile
```

**Mobile:**
```
🏠 Home (Dashboard dengan GPS indicator)
📝 Presensi Siswa
   ├─ Input Presensi (Quick Mode)
   └─ 📷 Foto Kelas (Wajib) ⭐
👤 Absen Guru
   ├─ GPS Location Check ⭐
   └─ Face Recognition
📊 Monitoring & Laporan
👤 Profile & Settings
```

### 5. GURU MATA PELAJARAN (Web + Mobile)

**Web:**
```
📊 Dashboard
📚 Kelas yang Diajar
✅ Presensi
   ├─ Input Presensi per Mapel
   ├─ Upload Foto Kelas (Wajib) ⭐
   └─ History
📊 Laporan
📰 Artikel & Pengumuman (View) ⭐
👤 My Profile
```

**Mobile:**
```
🏠 Home
📝 Presensi Siswa + 📷 Foto Kelas ⭐
👤 Absen Guru (Face + GPS) ⭐
📊 Laporan
👤 Profile
```

### 6. GURU PIKET (Web + Mobile)

**Web:**
```
📊 Dashboard
⏰ Input Keterlambatan Siswa
✅ Monitoring Presensi
📝 Perizinan
📊 Laporan
📰 Pengumuman (View) ⭐
```

**Mobile:**
```
🏠 Home (Dashboard Piket)
⏰ Input Keterlambatan
📝 Perizinan (Quick Approve)
👤 Absen Guru (Face + GPS) ⭐
```

### 7. ORANG TUA (Web Only)

```
📊 Dashboard
   ├─ Status Kehadiran Anak Hari Ini
   ├─ Kalender Kehadiran Bulan Ini
   └─ Statistik
👶 Profil Anak
✅ Kehadiran (Kalender & Grafik)
📝 Perizinan
   ├─ Submit Izin Baru
   └─ Tracking Izin
📊 Laporan
📢 Pengumuman Sekolah ⭐
   ├─ Pengumuman Umum
   ├─ Pengumuman Kelas Anak
   └─ Pengumuman Urgent
📰 Artikel & Berita (View) ⭐
```

### 8. LANDING PAGE (Public - No Login) ⭐

```
🏠 Home
📰 Artikel & Berita
   ├─ Berita Terbaru
   ├─ Prestasi Sekolah
   ├─ Kegiatan
   └─ Galeri Foto
📢 Pengumuman Umum
   ├─ Pengumuman Penting
   └─ Info Pendaftaran
📚 Profil Sekolah
   ├─ Visi & Misi
   ├─ Sejarah
   ├─ Fasilitas
   └─ Struktur Organisasi
👥 Tenaga Pendidik
📞 Kontak
🔐 Login (Redirect ke Dashboard)
```

---

## 🔐 ACCESS MATRIX

| Feature | Admin | Kepsek | TU | Wali | Guru | Piket | Ortu | Public |
|---------|:-----:|:------:|:--:|:----:|:----:|:-----:|:----:|:------:|
| **Dashboard** | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ❌ |
| **Data Master** |
| - Siswa (CRUD) | ✅ | 👁️ | ✅ | 👁️ | ❌ | ❌ | 👁️* | ❌ |
| - Guru (CRUD) | ✅ | 👁️ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| - Kelas (CRUD) | ✅ | 👁️ | ✅ | 👁️* | 👁️* | ❌ | ❌ | ❌ |
| **Presensi Siswa** |
| - Input Presensi | ✅ | ❌ | ✅ | ✅* | ✅* | ✅ | ❌ | ❌ |
| - **Upload Foto Kelas** ⭐ | ✅ | ❌ | ✅ | ✅* | ✅* | ✅ | ❌ | ❌ |
| - **View Foto Kelas** ⭐ | ✅ | ✅ | ✅ | ✅* | ✅* | ✅ | ❌ | ❌ |
| - Edit Presensi | ✅ | ❌ | ✅ | ✅* | ✅* | ✅ | ❌ | ❌ |
| **Presensi Guru** |
| - Face Registration | N/A | 📱 | 📱 | 📱 | 📱 | 📱 | ❌ | ❌ |
| - Face Recognition | N/A | 📱 | 📱 | 📱 | 📱 | 📱 | ❌ | ❌ |
| - **GPS Validation** ⭐ | N/A | 📱 | 📱 | 📱 | 📱 | 📱 | ❌ | ❌ |
| - View GPS History | ✅ | ✅ | ✅ | ❌ | 👁️* | ❌ | ❌ | ❌ |
| **Perizinan** |
| - Submit Izin | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ |
| - Approve/Reject | ✅ | ✅ | ✅ | ✅* | ❌ | ✅ | ❌ | ❌ |
| **Laporan** |
| - Laporan Siswa | ✅ | ✅ | ✅ | ✅* | ✅* | ✅* | ✅* | ❌ |
| - Laporan Guru | ✅ | ✅ | ✅ | ❌ | 👁️* | ❌ | ❌ | ❌ |
| **Artikel & Berita** ⭐ |
| - View Artikel | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ |
| - Create Artikel | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| - Edit/Delete Artikel | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| - Approve Artikel | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| - Manage Kategori | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| **Pengumuman** ⭐ |
| - View Pengumuman | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅ | ✅* |
| - Create Pengumuman | ✅ | ✅ | ✅ | ✅* | ❌ | ❌ | ❌ | ❌ |
| - Edit/Delete Pengumuman | ✅ | ✅ | ✅ | ✅* | ❌ | ❌ | ❌ | ❌ |
| - Set Prioritas | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| - Target Audience | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| **Pengaturan** |
| - System Settings | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| - **Radius GPS** ⭐ | ✅ | 👁️ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| - **Foto Kelas** ⭐ | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |
| - **Website Settings** ⭐ | ✅ | 👁️ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ |

**Legend:**
- ✅ Full Access | 👁️ View Only | ❌ No Access | 📱 Mobile Only | * Limited scope
- ⭐ = Fitur baru

**Notes:**
- *Siswa (Ortu): Only view own child
- *Wali: Can create announcement for own class only
- *Public: Can view public announcements only (urgent/general)
- *Artikel: All authenticated users can view, only admin/kepsek/TU can manage

---

## ⚙️ WEB CONFIGURATION

### 1. RADIUS ABSENSI GPS ⭐

**Lokasi:** Admin → Pengaturan → Radius Absensi GPS

**Konfigurasi:**
```
📍 LOKASI SEKOLAH
- Latitude:  [-6.200000]
- Longitude: [106.816666]
- [📍 Set dari Google Maps]
- [📍 Gunakan GPS Saat Ini]

🗺️ PREVIEW PETA
- Tampilkan marker sekolah
- Tampilkan circle radius
- Interactive zoom & pan

📏 RADIUS MAKSIMAL
- Default: 100 meter
- Range: 50m - 500m
- Slider adjustment
- Presets: [50m] [100m] [200m] [500m]

⚙️ VALIDASI
☑ Aktifkan Validasi Radius
☐ Izinkan Absen Manual jika Luar Radius
☑ Kirim Notifikasi ke Admin
☑ Log GPS History

📊 STATISTIK HARI INI
- Total percobaan: 42
- Di dalam radius: 40 (95%)
- Di luar radius: 2 (5%)
- Rata-rata jarak: 45m

🧪 TESTING
- Input test coordinates
- Show INSIDE/OUTSIDE result
- Show distance calculation
```

**Cara Kerja:**
1. Admin set lokasi sekolah (Lat, Long)
2. Admin set radius (misal 100m)
3. Saat guru absen di mobile, sistem:
   - Capture GPS guru
   - Calculate distance (Haversine Formula)
   - If distance ≤ radius: ✅ Allow
   - If distance > radius: ❌ Block
4. All attempts logged untuk compliance

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
- Total foto: 1,234 files
- Total size: 2.5 GB
- Average: 2.1 MB per foto
- Usage: 78% (7.5GB / 10GB)
```

**Cara Kerja:**
1. Guru input presensi siswa (web/mobile)
2. Setelah mark semua siswa → Wajib upload foto
3. Guru ambil foto kelas via camera/galeri
4. Sistem validasi foto (size, quality, faces)
5. Auto-apply watermark
6. Upload ke storage
7. If tidak upload → Error: "Foto wajib"
8. Admin bisa view foto di monitoring

---

### 3. ARTIKEL & BERITA (LANDING PAGE) ⭐

**Lokasi:** Admin → Konten Website → Artikel & Berita

**Konfigurasi:**
```
📰 MANAGEMENT ARTIKEL

Daftar Artikel:
┌─────────────────────────────────────────────┐
│ [+ Tambah Artikel Baru]  [Kategori] [Filter]│
├─────────────────────────────────────────────┤
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ [Featured] Prestasi Siswa di Olimpiade │ │
│ │ Kategori: Prestasi | Status: Published  │ │
│ │ Penulis: Admin | Tanggal: 20 Nov 2024   │ │
│ │ Views: 1,234 | Comments: 5              │ │
│ │ [Edit] [Delete] [Unpublish] [Pin]       │ │
│ └─────────────────────────────────────────┘ │
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ Kegiatan Ekstrakurikuler Semester Ini  │ │
│ │ Kategori: Kegiatan | Status: Draft      │ │
│ │ Penulis: Admin TU | Tanggal: 19 Nov     │ │
│ │ [Edit] [Publish] [Delete]               │ │
│ └─────────────────────────────────────────┘ │
│                                             │
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
│ • Berita Sekolah                            │
│ • Prestasi                                  │
│ • Kegiatan                                  │
│ • Pengumuman Umum                           │
│                                             │
│ Excerpt (Ringkasan): *                      │
│ [_____________________________________]     │
│ [_____________________________________]     │
│                                             │
│ Featured Image: *                           │
│ [📁 Upload Image] (Max 2MB, 1200x630)      │
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
│ Tags: (Pisah dengan koma)                   │
│ [siswa, prestasi, olimpiade__________]     │
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
│ Publish Settings:                           │
│ ☐ Set as Featured Article                   │
│ ☐ Allow Comments                            │
│ ☐ Pin to Top                                │
│                                             │
│ Status:                                     │
│ ⚪ Draft (Save as draft)                    │
│ ⚪ Published (Publish immediately)          │
│ ⚪ Scheduled (Set publish date/time)        │
│                                             │
│ Publish Date: [25 Nov 2024 08:00] 📅       │
│                                             │
│ [💾 Simpan] [👁️ Preview] [❌ Batal]       │
│                                             │
└─────────────────────────────────────────────┘

Kategori Management:
┌─────────────────────────────────────────────┐
│ 📁 Kategori Artikel                        │
├─────────────────────────────────────────────┤
│                                             │
│ [+ Tambah Kategori]                         │
│                                             │
│ • Berita Sekolah (45 artikel) [Edit] [Del] │
│ • Prestasi (23 artikel) [Edit] [Del]       │
│ • Kegiatan (34 artikel) [Edit] [Del]       │
│ • Pengumuman Umum (12 artikel) [Edit] [Del]│
│                                             │
└─────────────────────────────────────────────┘
```

**Landing Page Display:**
```
Homepage:
- Hero Section (Carousel 3-5 featured articles)
- Latest News (6 artikel terbaru)
- Prestasi Terbaru
- Kegiatan & Event

Artikel Page:
- Full article dengan featured image
- Breadcrumb navigation
- Related articles
- Share buttons (Facebook, Twitter, WhatsApp)
- Comment section (optional)
```

---

### 4. PENGUMUMAN SEKOLAH ⭐

**Lokasi:** Admin → Konten Website → Pengumuman Sekolah

**Konfigurasi:**
```
📢 MANAGEMENT PENGUMUMAN

Daftar Pengumuman:
┌─────────────────────────────────────────────┐
│ [+ Buat Pengumuman]  [Filter Prioritas]     │
├─────────────────────────────────────────────┤
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ 🔴 URGENT | Libur Nasional 17 Agustus  │ │
│ │ Target: Semua | Pin: Yes                │ │
│ │ Berlaku: 15-18 Aug 2024                 │ │
│ │ Dibuat: Admin | Views: 2,345            │ │
│ │ [Edit] [Delete] [Unpin]                 │ │
│ └─────────────────────────────────────────┘ │
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ 🟡 NORMAL | Pengumpulan Rapor Semester │ │
│ │ Target: Orang Tua | Pin: No             │ │
│ │ Berlaku: 20-25 Nov 2024                 │ │
│ │ Dibuat: Admin TU | Views: 456           │ │
│ │ [Edit] [Delete] [Pin]                   │ │
│ └─────────────────────────────────────────┘ │
│                                             │
│ ┌─────────────────────────────────────────┐ │
│ │ 🔵 INFO | Jadwal UTS Semester Ganjil   │ │
│ │ Target: Kelas X, XI, XII | Pin: No      │ │
│ │ Berlaku: 01-15 Dec 2024                 │ │
│ │ Dibuat: Kepala Sekolah | Views: 890     │ │
│ │ [Edit] [Delete]                         │ │
│ └─────────────────────────────────────────┘ │
│                                             │
└─────────────────────────────────────────────┘

Form Buat/Edit Pengumuman:
┌─────────────────────────────────────────────┐
│ 📢 Pengumuman Baru                         │
├─────────────────────────────────────────────┤
│                                             │
│ Judul Pengumuman: *                         │
│ [_____________________________________]     │
│                                             │
│ Prioritas: *                                │
│ ⚪ 🔴 Urgent (Merah - Sangat Penting)       │
│ ⚫ 🟡 Normal (Kuning - Penting)             │
│ ⚪ 🔵 Info (Biru - Informasi)               │
│                                             │
│ Isi Pengumuman: *                           │
│ [Rich Text Editor]                          │
│ [_____________________________________]     │
│ [_____________________________________]     │
│ [_____________________________________]     │
│                                             │
│ Lampiran (Optional):                        │
│ [📁 Upload File] (PDF, DOC, max 5MB)       │
│ [Preview: file.pdf]                         │
│                                             │
│ Target Audience: *                          │
│ ☐ Semua (Guru, Orang Tua, Siswa)           │
│ ☐ Guru Saja                                 │
│ ☐ Orang Tua Saja                            │
│ ☐ Per Kelas:                                │
│   ☐ Kelas X                                 │
│   ☐ Kelas XI                                │
│   ☐ Kelas XII                               │
│   ☐ Pilih Kelas Spesifik: [Dropdown ▼]     │
│                                             │
│ Masa Berlaku:                               │
│ Dari: [20 Nov 2024] 📅                     │
│ Sampai: [25 Nov 2024] 📅                   │
│                                             │
│ Tampilan:                                   │
│ ☐ Pin to Top (Tampil paling atas)          │
│ ☐ Show on Dashboard                         │
│ ☐ Show on Landing Page (Public)            │
│ ☐ Send Email Notification                   │
│ ☐ Send WhatsApp Notification                │
│                                             │
│ [💾 Simpan & Publish] [👁️ Preview] [❌]   │
│                                             │
└─────────────────────────────────────────────┘

Statistics:
┌─────────────────────────────────────────────┐
│ 📊 Statistik Pengumuman                    │
├─────────────────────────────────────────────┤
│                                             │
│ Total Pengumuman: 45                        │
│ Active: 12                                  │
│ Expired: 33                                 │
│                                             │
│ By Priority:                                │
│ • Urgent: 5 (11%)                           │
│ • Normal: 25 (56%)                          │
│ • Info: 15 (33%)                            │
│                                             │
│ Total Views: 12,345                         │
│ Avg Views per Announcement: 274             │
│                                             │
│ Most Viewed:                                │
│ 1. Libur Nasional - 2,345 views            │
│ 2. Jadwal UTS - 890 views                  │
│ 3. Pengumpulan Rapor - 456 views           │
│                                             │
└─────────────────────────────────────────────┘
```

**Display di Dashboard:**
```
Untuk Guru/Wali Kelas:
┌─────────────────────────────────────────────┐
│ 📢 PENGUMUMAN                              │
├─────────────────────────────────────────────┤
│                                             │
│ 🔴 [URGENT] Libur Nasional 17 Agustus     │
│    Berlaku: 15-18 Aug 2024                  │
│    [Lihat Detail]                           │
│                                             │
│ 🟡 Pengumpulan Rapor Semester              │
│    Berlaku: 20-25 Nov 2024                  │
│    [Lihat Detail]                           │
│                                             │
│ [Lihat Semua Pengumuman (12)]              │
└─────────────────────────────────────────────┘

Untuk Orang Tua:
┌─────────────────────────────────────────────┐
│ 📢 PENGUMUMAN UNTUK ORANG TUA              │
├─────────────────────────────────────────────┤
│                                             │
│ 🔴 [URGENT] Libur Nasional                │
│ 🟡 Pengumpulan Rapor - Kelas X IPA 1       │
│ 🔵 Jadwal Parent Meeting                   │
│                                             │
│ [Lihat Semua]                               │
└─────────────────────────────────────────────┘

Landing Page (Public):
┌─────────────────────────────────────────────┐
│ 📢 PENGUMUMAN PENTING                      │
├─────────────────────────────────────────────┤
│                                             │
│ 🔴 Libur Nasional 17 Agustus 2024         │
│ 🟡 Pendaftaran Siswa Baru 2024/2025        │
│                                             │
│ [Lihat Semua Pengumuman]                   │
└─────────────────────────────────────────────┘
```

---

## 📱 MOBILE APP

### Platform
- Android 8.0+
- iOS 12.0+

### Target User
✅ Guru (Wali Kelas, Guru Mapel, Guru Piket)

### Important Notes
- ✅ **Foto Kelas Wajib**: Tidak bisa skip
- ✅ **GPS Required**: Untuk absen guru
- ✅ **Internet Required**: Semua fitur

---

### FITUR MOBILE

#### 1. Dashboard
```
Components:
- Greeting & Date
- GPS Status: 📍 "Di Area Sekolah" / ⚠️ "Di Luar Area"
- 📢 Pengumuman Urgent (Banner merah jika ada)
- Face Recognition Status
- Jadwal Mengajar Hari Ini
  ├─ Status presensi: ✅/❌
  └─ Status foto kelas: 📷 ✅/❌
- Quick Stats
- Kehadiran Saya (Guru)
```

#### 2. Presensi Siswa + Foto Kelas ⭐

**Step 1: Input Presensi (Quick Mode)**
```
Target: 2-3 menit untuk 30 siswa

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

**Total Time:** ~4 menit (termasuk foto)

#### 3. Absen Guru (Face + GPS) ⭐

**Pre-check GPS:**
```
Sebelum face recognition:

1. Check GPS Location
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
   │     │ [🗺️ Buka Maps]         │
   │     │ [🔄 Cek Ulang]         │
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
- Status: "😊 Wajah terdeteksi!"

Auto-capture → Extract descriptor → Send to server

Server Validation:
1. Face match ≥85%? 
2. GPS inside radius?
3. Both valid → ✅ Save attendance

Success:
┌──────────────────────────┐
│ ✅ ABSEN BERHASIL!      │
├──────────────────────────┤
│ Check-in: 07:05:30      │
│ Kecocokan: 94%          │
│ 📍 Lokasi: 45m          │
└──────────────────────────┘

Failed - Face (<85%):
- Show tips
- [Coba Lagi] (max 3x)
- After 3x: [Input Manual]

Failed - GPS Outside:
┌──────────────────────────┐
│ ⚠️ DI LUAR AREA         │
├──────────────────────────┤
│ Face berhasil tapi GPS  │
│ di luar radius.         │
│ Hubungi admin.          │
└──────────────────────────┘
```

**Manual Fallback:**
```
Setelah 3x gagal face recognition:

Form:
- Waktu (editable)
- Alasan: Face gagal/Camera error/dll
- Foto Bukti (required)
- GPS location (auto)
- Status: PERLU REVIEW ADMIN

Submit → Notif ke admin
```

#### 4. Monitoring & Laporan
```
- Real-time monitoring
- View foto kelas (thumbnail → full view)
- GPS compliance stats
- Laporan dengan foto kelas
```

#### 5. Profile & Settings
```
Profile:
- Face Recognition Status
- GPS Compliance: 18/20 (90%)

Settings:
├─ Notifikasi
├─ Tampilan
├─ Keamanan
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
CMS:          Built-in (Artikel & Pengumuman)
```

### Web Frontend
```
Template:     Blade / Vue.js / React
CSS:          Tailwind CSS / Bootstrap
Charts:       Chart.js / ApexCharts
Maps:         Leaflet.js / Google Maps
Editor:       TinyMCE / CKEditor (Rich Text)
```

### Mobile App
```
Framework:    Flutter 3.16+
Language:     Dart 3.2+
State:        Provider / Riverpod
Face:         google_ml_kit (ML Kit Face Detection)
GPS:          geolocator package
Camera:       camera package
Image:        image_picker package
HTTP:         Dio
Push:         Firebase Cloud Messaging
```

### Face Recognition
```
Client (Flutter):
- ML Kit Face Detection
- Extract 128D descriptor

Server (Laravel):
- Cosine Similarity comparison
- Threshold: 85% (configurable)
- Storage: MySQL JSON
```

### GPS & Location
```
Client (Flutter):
- geolocator package
- Get coordinates (lat, long)
- Accuracy tracking

Server (Laravel):
- Haversine Formula
- Distance calculation
- Radius validation
```

### CMS Features
```
Artikel:
- WYSIWYG Editor (TinyMCE/CKEditor)
- Image upload & management
- SEO meta tags
- Publish scheduling
- Comment system (optional)

Pengumuman:
- Rich text editor
- Priority levels (Urgent/Normal/Info)
- Target audience filtering
- Expiry date
- View tracking
```

---

## 📊 PERFORMANCE TARGETS

**Mobile App:**
- App size: <60MB
- Cold start: <3s
- Face recognition: <3s
- GPS lock: <5s (outdoor)
- Photo upload: <10s (5MB on 4G)
- Input presensi + foto: <4 minutes

**Web:**
- Page load: <2s
- Dashboard refresh: <1s
- Report generation: <5s
- Landing page: <1.5s

**CMS:**
- Article page load: <1.5s
- Article creation: Smooth editing
- Image upload: <5s per image

---

## 📚 RELATED DOCUMENTATION

- **README.md** - Full documentation
- **Web_Menu_Fitur_Lengkap.md** - Detailed web features
- **Mobile_App_Screens_Lengkap.md** - Mobile UI/UX flows
- **Arsitektur_Face_Recognition.md** - Face recognition architecture
- **Fitur_Modul_Sistem_Presensi.md** - All modules & features

---
