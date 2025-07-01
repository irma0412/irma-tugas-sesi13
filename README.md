# Tugas Sesi 13

Repo ini berisi project pengujian mobile menggunakan **API Demos** sebagai aplikasi uji. Pengujian dilakukan dengan bantuan **Appium** dan **WebdriverIO (WDIO)** untuk mengotomasi langkah-langkah testing.  

## Struktur File dalam Repo  

1. **File Konfigurasi**  
   - `package.json`: Berisi metadata project serta daftar dependensi yang dibutuhkan untuk menjalankan pengujian.  
   - `package-lock.json`: Digunakan untuk memastikan instalasi dependensi tetap konsisten di berbagai lingkungan.  

2. **Konfigurasi WebdriverIO**  
   - File konfigurasi WDIO memuat pengaturan untuk menjalankan pengujian pada perangkat mobile yang terhubung langsung dengan komputer (real device).  
   - Beberapa parameter penting yang harus disesuaikan:  
     - **Device Name:** Nama perangkat yang akan diuji.  
     - **Platform Version:** Versi sistem operasi perangkat.  
     - **App Package:** Package aplikasi yang akan diuji.  
     - **App Activity:** Aktivitas awal aplikasi saat dibuka.  

3. **Folder `test`**  
   - Folder ini berisi script pengujian, seperti file `appdemo.test.js`, yang mengotomasi langkah-langkah membuka aplikasi **API Demos**.  

## Langkah Persiapan  
Sebelum menjalankan pengujian, pastikan:  
1. **Appium Server** sudah diaktifkan.  
2. Perangkat mobile terhubung dengan komputer menggunakan kabel USB.  
3. Informasi perangkat dan aplikasi (seperti `deviceName`, `platformVersion`, `appPackage`, dan `appActivity`) sudah disesuaikan pada file konfigurasi WDIO.  

## Cara Memeriksa Detail Perangkat dan Aplikasi  
1. **Device Name:**  
   - Jalankan perintah berikut di CMD/Terminal untuk mendapatkan nama perangkat:  
     ```bash
     adb devices
     ```  
   - Nama perangkat akan muncul pada daftar yang dihasilkan.  

2. **App Package dan App Activity:**  
   - Jalankan perintah berikut di CMD/Terminal untuk mendapatkan informasi aplikasi:  
     ```bash
     adb shell dumpsys window | find "mCurrentFocus"
     ```  
   - Output akan menunjukkan `appPackage/appActivity`.  

## Langkah Pengujian  
Pengujian dilakukan pada perangkat mobile (real device) yang terhubung langsung ke komputer menggunakan USB.  
Tahap pengujian yang dilakukan saat ini:  
1. Membuka aplikasi **API Demos** pada perangkat mobile.  
2. Validasi bahwa aplikasi berhasil terbuka tanpa error.  

Hasil pengujian ditunjukkan melalui screenshot pada CMD, yang menandakan pengujian berjalan dengan sukses. Dokumentasi hasil pengujian mengikuti panduan pada slide 22.  

## Teknologi yang Digunakan  
- **Appium:** Framework open-source untuk pengujian otomatis aplikasi mobile.  
- **WebdriverIO (WDIO):** Alat untuk menjalankan pengujian berbasis WebDriver pada perangkat mobile.  

Tahap pengujian selanjutnya akan mencakup eksplorasi lebih lanjut dari fitur aplikasi.  
