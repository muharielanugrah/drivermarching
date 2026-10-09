# DriverMarching: cara membuat APK

## Cara 1 (gratis, tanpa install apa pun): GitHub
1. Buat akun di github.com, lalu buat repository baru bernama `drivermarching`.
2. Upload SEMUA isi folder ini (termasuk folder `.github` dan `www`) ke repository itu.
3. Buka tab **Actions**, pilih **Build APK**, tekan **Run workflow**.
4. Tunggu sekitar 5-8 menit sampai ada tanda centang hijau.
5. Klik hasil build tersebut, unduh **DriverMarching-apk** (berbentuk zip), ekstrak, dapatlah `app-debug.apk`.
6. Kirim ke WhatsApp/HP kamu, buka, izinkan "pasang dari sumber tidak dikenal", lalu pasang.

## Cara 2: di laptop (perlu Node.js 20+, Java 21, Android Studio)
```
npm install
npx cap add android
npx cap sync android
cd android
./gradlew assembleDebug
```
Hasil: `android/app/build/outputs/apk/debug/app-debug.apk`

## Catatan
- Isi aplikasi ada di `www/index.html`.
- Catatan uang tersimpan di dalam aplikasi itu sendiri dan tidak ikut pindah dari versi browser.
- Font (Chakra Petch) butuh internet. Tanpa internet, huruf memakai font bawaan HP, fungsi tetap jalan.
