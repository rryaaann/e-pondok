# e-Pondok - Sistem Informasi Pesantren Modern

## Deskripsi
e-Pondok adalah aplikasi web untuk pengelolaan administrasi dan manajemen kegiatan di pondok pesantren. Sistem ini memudahkan santri, guru, dan operator pondok dalam mengakses data, mengelola kegiatan belajar mengajar, monitoring santri, serta pengelolaan nilai (e-Rapot).

## Fitur Utama

### Halaman Publik
- **Dashboard Utama**: Profil pondok, biodata, kegiatan, brosur, dan link pendaftaran
- **Pendaftaran Santri**: Form pendaftaran lengkap dengan upload berkas
- **Responsive Design**: Tampilan optimal untuk desktop dan mobile

### Akses Operator
- **Manajemen Santri**: Input data santri, pengelompokan kamar dan kelas
- **Manajemen Guru**: Input data guru dan pembuatan akun login
- **Manajemen Kelas**: Pembuatan kelas berdasarkan jenjang (SMP/SMK)
- **Manajemen Mata Pelajaran**: Pengaturan mata pelajaran per jenjang
- **Jadwal Pelajaran**: Pembuatan jadwal pelajaran per kelas
- **Jadwal Kegiatan**: Pengaturan jadwal kegiatan pondok
- **Sistem Pendaftaran**: Review dan approval pendaftaran santri
- **Monitoring**: Monitoring kehadiran dan pelanggaran santri
- **e-Rapot**: Sistem pengelolaan nilai santri

### Akses Guru
- **Absensi**: Input absensi santri per pertemuan
- **Input Nilai**: Input nilai tugas, UTS, dan UAS
- **e-Rapot**: Pengisian rapot santri
- **Kegiatan**: Input kegiatan dan tugas
- **Jadwal Mengajar**: Lihat jadwal mengajar

## Teknologi
- **Backend**: PHP 7.4+ (Native)
- **Database**: MySQL 5.7+
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Server**: XAMPP/Apache
- **Framework CSS**: Custom (Responsive)

## Instalasi

### Prerequisites
- XAMPP (Apache + MySQL + PHP)
- PHP 7.4 atau lebih tinggi
- MySQL 5.7 atau lebih tinggi

### Langkah Instalasi

1. **Clone Repository**
   ```bash
   git clone https://github.com/username/e-pondok.git
   cd e-pondok
   ```

2. **Setup Database**
   - Buka XAMPP Control Panel
   - Start Apache dan MySQL
   - Buka phpMyAdmin (http://localhost/phpmyadmin)
   - Buat database baru dengan nama `e_pondok`
   - Import file `database/e_pondok.sql` (jika ada)

3. **Konfigurasi Database**
   - Edit file `config/database.php`
   - Sesuaikan host, username, password, dan nama database

4. **Setup Folder**
   - Pastikan folder `uploads/` memiliki permission write
   - Folder ini untuk menyimpan file upload pendaftaran

5. **Akses Aplikasi**
   - Buka browser
   - Akses `http://localhost/e-pondok`

## Struktur Database

### Tabel Utama
- **users**: Data pengguna (operator/guru)
- **guru**: Data guru
- **santri**: Data santri
- **kelas**: Data kelas
- **mata_pelajaran**: Data mata pelajaran
- **jadwal_pelajaran**: Jadwal pelajaran
- **jadwal_kegiatan**: Jadwal kegiatan pondok
- **absensi**: Data absensi santri
- **nilai**: Data nilai santri
- **pendaftaran**: Data pendaftaran santri baru
- **kamar**: Data kamar pondok

## Akun Default

### Operator
- Username: `operator`
- Password: `operator123`

### Guru
- Buat melalui panel operator

## Struktur Folder
```
e-pondok/
├── admin/                 # Panel operator
│   ├── dashboard.php
│   ├── santri.php
│   ├── guru.php
│   ├── kelas.php
│   ├── mapel.php
│   ├── jadwal.php
│   ├── kamar.php
│   ├── pendaftaran.php
│   ├── rapot.php
│   └── monitoring.php
├── guru/                  # Panel guru
│   ├── dashboard.php
│   ├── jadwal.php
│   ├── absensi.php
│   ├── nilai.php
│   ├── rapot.php
│   ├── kegiatan.php
│   └── profil.php
├── assets/                # Asset aplikasi
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── script.js
│   └── images/
├── config/                # Konfigurasi
│   └── database.php
├── uploads/               # File upload
├── index.php              # Halaman utama
├── login.php              # Halaman login
├── pendaftaran.php        # Halaman pendaftaran
├── logout.php             # Logout
└── README.md
```

## Fitur Responsive
- **Mobile First**: Design dimulai dari tampilan mobile
- **Breakpoints**: 
  - Mobile: < 768px
  - Tablet: 768px - 1024px
  - Desktop: > 1024px
- **Navigation**: Hamburger menu untuk mobile
- **Forms**: Responsive form layout
- **Tables**: Scrollable tables untuk mobile

## Keamanan
- **Session Management**: Login berbasis session
- **Password Hashing**: Menggunakan password_hash()
- **SQL Injection Protection**: Menggunakan prepared statements
- **File Upload Security**: Validasi tipe dan ukuran file
- **XSS Protection**: Escape output HTML

## Pengembangan

### Menambah Fitur Baru
1. Buat file PHP di folder yang sesuai
2. Tambahkan menu di sidebar
3. Update database jika diperlukan
4. Test di berbagai device

### Customization
- **Theme**: Edit `assets/css/style.css`
- **Logo**: Ganti `assets/images/logo.png`
- **Colors**: Update CSS variables di file CSS

## Troubleshooting

### Error Koneksi Database
- Pastikan MySQL berjalan
- Cek konfigurasi di `config/database.php`
- Pastikan database `e_pondok` sudah dibuat

### Error Upload File
- Cek permission folder `uploads/`
- Pastikan ukuran file tidak melebihi limit PHP
- Cek tipe file yang diizinkan

### Error Session
- Pastikan session_start() dipanggil di awal file
- Cek konfigurasi PHP session

## Kontribusi
1. Fork repository
2. Buat branch fitur baru
3. Commit perubahan
4. Push ke branch
5. Buat Pull Request

## Lisensi
MIT License - lihat file LICENSE untuk detail

## Support
Untuk bantuan dan pertanyaan:
- Email: support@epondok.id
- Website: www.epondok.id
- Documentation: docs.epondok.id

## Changelog

### v1.0.0 (2025-01-XX)
- Initial release
- Fitur dasar operator dan guru
- Sistem pendaftaran santri
- e-Rapot system
- Responsive design 
