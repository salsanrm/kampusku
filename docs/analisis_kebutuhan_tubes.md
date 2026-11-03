# Dokumen Analisis Kebutuhan Proyek: Event Hub Kampus
**Institusi:** Universitas Teknologi Bandung (UTB)  
**Mata Kuliah:** Pemrograman Mobile II (IF-024)

---

## 1. Pernyataan Masalah (Problem Statement)
Mahasiswa dan pihak penyelenggara (organisasi kampus/himpunan) sering mengalami kesulitan dalam menyebarkan dan memantau informasi kegiatan atau reuni alumni karena informasi tersebar di banyak grup chat WhatsApp dan poster fisik yang mudah terlewat. Akibatnya, tingkat partisipasi mahasiswa rendah dan peserta sering ketinggalan batas akhir pendaftaran. Belum ada satu aplikasi mobile khusus di kampus yang mengintegrasikan informasi acara, sistem registrasi, dan pengingat jadwal kegiatan secara terpusat.

---

## 2. Persona Pengguna

### Persona 1: Nisa (Mahasiswa / Panitia Kegiatan)
* **Profil:** Mahasiswi aktif pengurus organisasi/HIMATIF, usia 20 tahun.
* **Perangkat:** Smartphone Android kelas menengah, koneksi internet seluler standar.
* **Tujuan:** Ingin menyebarkan informasi acara/reuni dengan mudah dan memastikan peserta mendapatkan notifikasi jadwal yang akurat.
* **Masalah:** Brosur digital sering tenggelam di grup chat dan rekap jumlah pendaftar masih dilakukan secara manual via Google Forms yang terpisah-pisah.
* **Kutipan:** *"Seringkali peserta mendadak tanya info acara padahal sudah dishare berulang kali di grup karena tertutup pesan lain."*

---

## 3. Ruang Lingkup dan Batasan Proyek (Scope and Limitations)

### A. Ruang Lingkup Proyek (Project Scope)
Proyek aplikasi **Event Hub Kampus** ini mencakup fungsionalitas inti yang dirancang untuk pengguna mahasiswa dan pengelola acara tingkat universitas/himpunan, yang meliputi:
1. **Modul Autentikasi & Profil:** Sistem masuk sederhana bagi mahasiswa menggunakan akun kampus.
2. **Modul Informasi Beranda:** Menampilkan daftar dan detail event akademik, seminar, maupun reuni alumni.
3. **Modul Pendaftaran & Interaksi:** Fitur pendaftaran event (*CRUD data pendaftaran*) dan penyimpanan tiket digital sederhana secara lokal atau berbasis *cloud*.
4. **Modul Pengingat:** Sistem notifikasi lokal untuk mengingatkan jadwal event yang akan segera dimulai.

### B. Batasan Proyek (Project Limitations)
Agar proyek dapat diselesaikan tepat waktu dalam skala semester ini, terdapat beberapa batasan sistem yang diterapkan:
1. **Cakupan Pengguna:** Sistem autentikasi pada versi semester ini difokuskan untuk peran mahasiswa (sebagai peserta), sementara manajemen pengelolaan event secara penuh oleh panitia dibatasi pada fungsionalitas dasar.
2. **Metode Pembayaran:** Aplikasi tidak menyediakan fitur transaksi keuangan atau pembelian tiket berbayar (semua event diasumsikan gratis atau menggunakan validasi eksternal).
3. **Platform Target:** Pengembangan diutamakan untuk platform **Android** dan diuji melalui emulator serta browser web, belum mencakup rilis resmi ke Apple App Store (iOS).

---

## 4. Daftar Fitur & User Story (Metode MoSCoW)

| No | User Story | Fitur | Prioritas | Pertemuan Terkait |
|---|---|---|---|---|
| 1 | Sebagai mahasiswa, saya ingin melihat daftar event atau reuni kampus yang akan datang agar bisa ikut serta. | Berita & Daftar Event | **Must Have** | 4, 6 |
| 2 | Sebagai mahasiswa, saya ingin mendaftar ke sebuah event langsung dari aplikasi dan mendapatkan tiket digital. | Pendaftaran & Tiket Event (CRUD) | **Must Have** | 6, 12 |
| 3 | Sebagai penyelenggara, saya ingin mempublikasikan pengumuman atau perubahan jadwal acara terbaru. | Manajemen & Publish Event | **Should Have** | 11 |
| 4 | Sebagai mahasiswa, saya ingin mendapatkan notifikasi pengingat beberapa jam sebelum acara dimulai. | Push / Local Notification | **Should Have** | 12 |
| 5 | Sebagai mahasiswa, saya ingin menyaring event berdasarkan kategori (Akademik, Seminar, atau Reuni). | Filter Kategori Event | **Could Have** | 5 |
| 6 | Sebagai mahasiswa, saya ingin menyimpan event ke daftar favorit agar mudah diakses kembali. | Bookmark / Favorit | **Could Have** | 6 |
| 7 | Sebagai mahasiswa, saya ingin membagikan link rincian event ke media sosial atau aplikasi perpesanan. | Share Button | **Could Have** | 8 |
| 8 | Sebagai mahasiswa, saya ingin melakukan chat langsung dengan narasumber atau panitia acara. | Live Q&A / Chat | **Won't Have** (Semester ini) | - |

---

## 5. Fitur di Kemudian Hari (Future Enhancements)
Sebagai tahap pengembangan lanjutan di masa depan (*post-semester* atau ketika produk ingin diskalakan menjadi aplikasi komersial/resmi kampus), fitur berikut dapat ditambahkan:
1. **Integrasi QR Code Scanner untuk Kehadiran (Check-in):** Panitia dapat memindai tiket digital peserta secara langsung menggunakan kamera ponsel saat memasuki ruangan acara atau reuni.
2. **Sistem Sertifikat Otomatis:** Peserta yang telah menghadiri event akan otomatis mendapatkan e-sertifikat berformat PDF yang bisa diunduh langsung dari aplikasi.
3. **Push Notification Berbasis Cloud (Firebase Cloud Messaging):** Mengirimkan broadcast notifikasi real-time langsung ke perangkat seluruh mahasiswa saat ada event mendadak.
4. **Fitur Diskusi / Q&A Interaktif per Event:** Ruang obrolan atau sesi tanya jawab khusus antara peserta dan narasumber/panitia di dalam halaman detail event.
5. **Rekomendasi Pintar Berbasis Minat (*AI Recommendation*):** Sistem yang mempelajari kebiasaan dan riwayat event yang pernah diikuti mahasiswa untuk memberikan rekomendasi acara yang relevan.

---

## 6. Kebutuhan Non-Fungsional
1. **Performa:** Waktu muat awal aplikasi (*startup time*) dan navigasi antar halaman harus kurang dari 3 detik.
2. **Ketersediaan Offline:** Data ringkasan event yang sudah pernah dimuat harus tetap dapat diakses saat koneksi internet terputus.
3. **Aksesibilitas:** Teks dan tata letak antarmuka tetap responsif serta nyaman dibaca pada berbagai ukuran layar perangkat Android kelas menengah.