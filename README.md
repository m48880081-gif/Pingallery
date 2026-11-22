# WallHub

Aplikasi Android native (Kotlin + Jetpack Compose) untuk cari dan pasang wallpaper.
Sumber: Wallhaven, Pinterest (scraper), Pexels, Unsplash.

## Cara build lewat GitHub Actions
1. Buat repo baru di GitHub, lalu upload semua isi folder ini (termasuk folder `.github`).
2. Buka tab **Actions** > **Build APK** > **Run workflow** (atau push ke branch `main`).
3. Setelah hijau, buka run-nya dan unduh **WallHub-debug-apk** di bagian Artifacts, lalu pasang APK-nya.
4. Mau rilis permanen? Buat tag, misalnya `v1.0`; APK otomatis muncul di halaman Releases.

## API key (opsional)
Wallhaven dan Pinterest jalan tanpa key. Untuk Pexels dan Unsplash, tambahkan di
**Settings > Secrets and variables > Actions** dengan nama `PEXELS_KEY` dan `UNSPLASH_KEY`.
Sumber tanpa key otomatis tidak muncul di aplikasi.

## Catatan
- Pinterest memakai endpoint web internal, jadi bisa rusak atau diblokir sewaktu-waktu dan melanggar ToS mereka.
  Kodenya terpisah di `Pinterest.kt`; hapus dari daftar di `MainViewModel.kt` kalau tidak mau dipakai.
- APK yang dihasilkan bertanda tangan debug. Cukup untuk pemakaian pribadi, bukan untuk Play Store.
- Hak cipta gambar tetap milik pembuatnya; aplikasi tidak menyimpan ulang gambar di server mana pun.
