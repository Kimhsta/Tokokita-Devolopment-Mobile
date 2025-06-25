# 🛍️ Tokokita Development - Mobile & API

Tokokita adalah aplikasi mobile berbasis Flutter untuk toko online sederhana, didukung oleh backend API Laravel. Aplikasi ini memungkinkan pengguna untuk melakukan registrasi, login, melihat daftar produk, dan logout.

## 📦 Teknologi yang Digunakan

### 🔧 Backend - Laravel

- Laravel 10+
- RESTful API
- MySQL / MariaDB
- Autentikasi API (token)
- File upload (produk)

### 📱 Frontend - Flutter

- Flutter SDK 3.x
- State Management (BLoC / FutureBuilder)
- HTTP (API Communication)
- Material Design

---

## 📁 Struktur Proyek

```
Tokokita-Devolopment-Mobile/
│
├── backend-laravel/        # Source code Laravel REST API
│   ├── app/
│   ├── config/
│   ├── database/
│   ├── routes/
│   └── .env.example        # Contoh file konfigurasi environment
│
└── frontend_flutter/       # Aplikasi Flutter Mobile
    ├── lib/
    │   ├── bloc/           # State management logic
    │   ├── helpers/        # API service & URL constants
    │   ├── model/          # Struktur data (Produk, User, dsb.)
    │   └── ui/             # Tampilan halaman (login, register, dsb.)
    └── pubspec.yaml
```

---

## 🚀 Cara Menjalankan

### 1. Setup Backend (Laravel)

```bash
cd backend-laravel
cp .env.example .env
composer install
php artisan key:generate
# Edit .env dan sesuaikan DB_DATABASE, DB_USERNAME, DB_PASSWORD
php artisan migrate --seed
php artisan serve
```

Laravel akan berjalan di `http://127.0.0.1:8000`

### 2. Setup Frontend (Flutter)

```bash
cd ../frontend_flutter
flutter pub get
# Pastikan base URL API diubah di helpers/api.dart
flutter run
```

---

## 🧪 Fitur Aplikasi

- ✅ Register & Login
- ✅ Logout (hapus token dari SharedPreferences)
- ✅ Tampilkan daftar produk dari backend
- 🔒 Token API tersimpan di local device
- ⌛ Future update: Tambah produk, detail produk, dsb.

---

## ⚙️ Catatan Pengembangan

- Gunakan Android Emulator / Chrome Web / Perangkat Fisik untuk testing.
- Pastikan Laravel backend aktif sebelum menjalankan aplikasi Flutter.
- Cek koneksi API di file: `helpers/api.dart`.

---

## ✍️ Kontributor

- **Kimhsta** — [GitHub](https://github.com/Kimhsta)

---

## 📄 Lisensi

Proyek ini menggunakan lisensi [MIT](LICENSE).
