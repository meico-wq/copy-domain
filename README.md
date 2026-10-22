# Copy Domain Android

Aplikasi untuk mengambil domain dari URL, termasuk beberapa URL redirect Google.

## Fitur
- Tempel URL manual atau dari clipboard.
- Bagikan link dari browser melalui menu **Bagikan / Share** lalu pilih Copy Domain.
- Salin domain saja tanpa protokol, path, atau query.

## Build APK otomatis lewat GitHub Actions (bisa dari HP)
1. Download dan ekstrak ZIP project ini.
2. Buat repository baru di GitHub.
3. Upload seluruh isi folder project ke repository (termasuk folder `.github/workflows`).
4. Buka tab **Actions** di repository. Jika diminta, aktifkan Actions.
5. Jalankan workflow **Build Copy Domain APK** lewat **Run workflow**, atau push ke branch `main`/`master`.
6. Setelah selesai, buka run workflow yang sukses, scroll ke **Artifacts**, lalu download `copy-domain-debug-apk`.
7. Ekstrak artifact dan instal `app-debug.apk` di Android. Jika diminta, izinkan instalasi dari sumber tersebut.

Workflow menggunakan Java 17 dan Gradle 8.9 di runner GitHub, lalu mengunggah APK debug sebagai artifact.

## Build lokal
Buka folder ini di Android Studio, tunggu Gradle sync, lalu pilih **Build > Build APK(s)**.

Minimal Android 6.0 (API 23). Android tidak mengizinkan aplikasi biasa menambahkan opsi klik-kanan ke aplikasi lain seperti ekstensi desktop. Gunakan menu Bagikan/Share atau tempel URL ke aplikasi.
