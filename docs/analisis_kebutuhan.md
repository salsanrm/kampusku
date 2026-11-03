# Dokumen Analisis Kebutuhan Awal Proyek Semester
**Nama Aplikasi:** KampusKu
**Institusi:** Universitas Teknologi Bandung

---

## 1. Pernyataan Masalah (Problem Statement)
Mahasiswa UTB menerima jadwal kuliah, tugas, dan pengumuman dari berbagai saluran terpisah seperti portal akademik, grup chat WhatsApp, dan platform e-learning. Hal ini membuat informasi penting mudah terlewat, seperti perubahan ruang kelas mendadak atau keterlambatan pengumpulan tugas. Solusi yang ada saat ini belum terintegrasi dalam satu platform mobile yang praktis, terorganisir, dan dapat memberikan notifikasi pengingat secara otomatis.

---

## 2. Persona Pengguna

### Persona 1: Rina (Mahasiswi Aktif)
* **Profil:** Mahasiswi Teknik Informatika Semester 3, 19 Tahun, tinggal di kos.
* **Perangkat:** Smartphone Android kelas menengah, kuota internet terbatas.
* **Tujuan:** Mengetahui jadwal kuliah harian dengan cepat dan mencatat tugas agar tidak melampaui tenggat.
* **Masalah:** Informasi jadwal sering mendadak berubah di grup WhatsApp dan mudah tertimbun pesan lain.
* **Kebiasaan:** Membuka HP di sela jam kuliah, menyukai antarmuka sederhana dan cepat.
* **Kutipan:** *"Saya sering baru tahu kelas pindah ruang setelah sampai di depan kelas lama."*

---

## 3. Daftar Fitur & User Story (Metode MoSCoW)

| No | User Story | Fitur | Prioritas | Pertemuan Terkait |
|---|---|---|---|---|
| 1 | Sebagai mahasiswa, saya ingin melihat jadwal kuliah harian agar tidak salah ruang kelas. | Ringkasan Jadwal Harian | Must | 4, 6 |
| 2 | Sebagai mahasiswa, saya ingin mencatat daftar tugas beserta batas waktunya agar tidak terlambat mengumpul. | Pengelola Tugas (CRUD) | Must | 6, 12 |
| 3 | Sebagai mahasiswa, saya ingin membaca pengumuman kampus terbaru agar selalu update informasi. | Feed Pengumuman API | Must | 11 |
| 4 | Sebagai mahasiswa, saya ingin mendapatkan notifikasi pengingat sebelum tenggat tugas habis. | Local Notification | Should | 12 |
| 5 | Sebagai mahasiswa, saya ingin login menggunakan akun kampus agar data tersimpan di cloud. | Autentikasi Firebase | Should | 13 |
| 6 | Sebagai mahasiswa, saya ingin mengaktifkan mode gelap agar nyaman dibaca pada malam hari. | Dark Theme Support | Could | 5 |
| 7 | Sebagai mahasiswa, saya ingin menandai tugas yang sudah selesai dikerjakan. | Checkbox / Status Tugas | Could | 6 |
| 8 | Sebagai mahasiswa, saya ingin melakukan percakapan langsung dengan dosen pengampu. | Direct Chat Dosen | Won't (Semester ini) | - |

---

## 4. Kebutuhan Non-Fungsional
1. **Performa:** Waktu buka awal aplikasi (*startup time*) tidak boleh melebihi 3 detik pada perangkat menengah ke bawah.
2. **Ketersediaan Offline:** Informasi jadwal kuliah yang sudah diunduh harus tetap dapat diakses meskipun perangkat tidak terhubung ke internet.
3. **Aksesibilitas & UI:** Teks dan elemen antarmuka tetap responsive serta terbaca dengan jelas saat ukuran font sistem ditingkatkan.