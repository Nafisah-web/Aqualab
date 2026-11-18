# AquaLab — IPAS Kelas V
Aplikasi statis interaktif, berbasis Three.js 0.170.0 (disertakan lokal), diadaptasi dari modul “Air Berubah, Apa yang Terjadi?” oleh Rustia Ningsi, S.Pd., Gr., SDIT Asy Syafi'i. Tidak menyertakan daftar nama peserta didik dari dokumen sumber.

## Jalankan lokal
Jalankan `python3 -m http.server 8000` dari folder ini, lalu buka http://localhost:8000. Jangan membuka index.html langsung lewat file:// karena menggunakan ES modules.

## Deploy ke Vercel
1. Ekstrak ZIP; unggah isi folder aqualab ke repositori GitHub.
2. Di Vercel, pilih Add New → Project dan impor repositori tersebut.
3. Framework Preset: Other. Root Directory: folder yang berisi index.html (aqualab jika mengunggah folder induknya).
4. Build Command dan Install Command: kosongkan. Output Directory: `.`.
5. Klik Deploy. Tidak memerlukan API key, backend, database, atau npm.
Alternatif dengan Vercel CLI yang sudah terpasang: jalankan `vercel --prod` dari folder ini dan ikuti autentikasi akun Anda.

## Pembahasan materi baru
Menu Pembahasan materi memuat enam bab: pengenalan air, perubahan wujud, pelarutan garam, pengaratan, pembandingan gelembung, serta simpulan dan aksi. Setiap bab memuat ilustrasi Three.js 3D lokal dengan tombol putar dan zoom, uraian, contoh keseharian, pertanyaan dengan jawaban buka-tutup, dan tautan ke laboratorium/jurnal.

## Isi
- Tiga simulasi 3D: wujud air; pelarutan/penguapan larutan garam; reaksi soda kue dan cuka serta pengaratan besi.
- Seret untuk rotasi 360°, gulir atau tombol untuk zoom, reset kamera, Play/Pause, Ulangi, Berikutnya/Kembali.
- Suhu, kemajuan proses, pilihan reaksi, penjelasan ilmiah, peta konsep, 10 soal dengan umpan balik.
- Jurnal lokal, refleksi, pilihan produk, unduhan TXT. Data disimpan di browser perangkat itu; bukan sinkronisasi daring dan bukan buku nilai guru. Mode privat/bersih data dapat menghapus jurnal.
- Font Google opsional; jika tanpa internet, font sistem tetap tersedia. Semua kode dan mesin 3D disertakan lokal.

## Batas model
Simulasi adalah model konseptual, bukan pengukuran eksperimen. Ukuran partikel, durasi reaksi, dan pengaratan disederhanakan/dipercepat. Suhu menampilkan keadaan utama air pada sekitar 1 atm setelah perpindahan kalor; perubahan fase sebenarnya membutuhkan kalor laten dan dua fase dapat hadir bersamaan. Uap air tidak terlihat; bola 3D menggambarkan partikel, bukan foto uap.
Play menjalankan proses; Pause menghentikan waktu proses dan gerakan partikel. Penggeser tetap dapat digunakan saat pause. Gerak maskot ringan mengikuti proses; preferensi reduced-motion mengurangi gerak maskot. Rotasi manual tetap tersedia.
Percobaan nyata harus didampingi guru. Air panas ditangani guru. Jangan mencicipi bahan.

## Berkas
index.html, style.css, app.js, vercel.json, vendor/three.module.js.
Lisensi Three.js tersedia dalam vendor/LICENSE.
