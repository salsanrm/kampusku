# Jawaban Latihan Soal Praktikum Flutter (Pertemuan 3)

## 1. Fungsi Opsi `--org` pada `flutter create` & Alasan Tidak Boleh Diganti
* **Fungsi:** Opsi `--org` berfungsi untuk menetapkan **domain terbalik** (*reverse domain*) organisasi yang menjadi dasar **Application ID** (Android) atau **Bundle ID** (iOS).
* **Alasan Tidak Boleh Diganti:** Nilai ini tidak boleh diganti setelah aplikasi dirilis karena Play Store dan App Store menggunakan ID tersebut sebagai **identitas unik** aplikasi. Mengubah ID ini akan membuat aplikasi dianggap sebagai aplikasi baru, sehingga pengguna lama tidak bisa melakukan pembaruan (*update*).

---

## 2. 5 Folder/File Utama dalam Proyek Flutter dan Fungsinya
1. **`lib/`**  
   Berisi seluruh kode program utama berbasis Dart.
2. **`pubspec.yaml`**  
   File konfigurasi utama proyek untuk mengatur nama, versi, dependensi/package, assets, dan font.
3. **`android/`**  
   Berisi berkas proyek native Android (seperti Gradle, Manifest, izin aplikasi, dan ikon).
4. **`ios/`**  
   Berisi berkas proyek native iOS (seperti proyek Xcode, `Info.plist`, dan konfigurasi izin).
5. **`test/`**  
   Berisi berkas pengujian kode (unit test dan widget test).

---

## 3. Perbedaan `dependencies` dan `dev_dependencies`
* **`dependencies`**  
  Package yang ikut dikompilasi dan dibutuhkan saat aplikasi berjalan di tingkat produksi/rilis.  
  *Contoh:* `intl`, `http`, `google_fonts`.
* **`dev_dependencies`**  
  Package yang hanya digunakan selama fase pengembangan (untuk pengujian, linting, atau *code generation*) dan tidak ikut dimasukkan ke dalam build aplikasi akhir.  
  *Contoh:* `flutter_test`, `flutter_lints`.

---

## 4. Rentang Versi SemVer dengan Caret Syntax (`^`)
* **`^2.4.1`**  
  Mengizinkan pembaruan versi $\ge 2.4.1$ dan $< 3.0.0$.
* **`^0.13.0`**  
  Mengizinkan pembaruan versi $\ge 0.13.0$ dan $< 0.14.0$ (pada versi `0.x`, kenaikan digit minor dianggap membawa *breaking changes*).

---

## 5. Efek `_counter++` Tanpa `setState()` pada Aplikasi Counter
Nilai variabel `_counter` akan **tetap bertambah di memori**, tetapi tampilan antarmuka (**UI**) pada layar **tidak akan berubah atau diperbarui**. 

*Alasan:* `setState()` berfungsi untuk memberi tahu framework Flutter bahwa ada perubahan data/state, sehingga fungsi `build()` akan dijalankan ulang untuk merender tampilan baru di layar.

---

## 6. Perbandingan *Layer-first* vs *Feature-first*
* **Layer-first:**  
  Mengelompokkan berkas berdasarkan jenisnya (contoh: `models/`, `screens/`, `widgets/`). Sangat cocok untuk aplikasi skala kecil hingga menengah.
* **Feature-first:**  
  Mengelompokkan berkas berdasarkan fitur modularnya (contoh: `jadwal/`, `tugas/`, di mana setiap folder fitur memiliki model, screen, dan widget sendiri).
* **Kapan Beralih:**  
  Beralih ke *feature-first* saat aplikasi berkembang menjadi skala besar, memiliki banyak fitur terpisah, atau dikerjakan oleh tim besar dengan pembagian tugas berbasis fitur.

---

## 7. Alasan `pubspec.lock` Di-commit sedangkan `build/` Tidak
* **`pubspec.lock` (Di-commit):**  
  Mencatat versi pasti dari seluruh *dependency* yang terpasang agar seluruh anggota tim pengembangan menggunakan versi pustaka yang identik.
* **`build/` (Di-ignore / Tidak Di-commit):**  
  Berisi hasil kompilasi dan binari sementara yang dihasilkan secara otomatis saat aplikasi dijalankan. Berkas di dalamnya berukuran besar dan berbeda-beda pada tiap komputer pengembangan.

---

## 8. User Story Aplikasi Beserta Prioritas MoSCoW
1. **User Story 1:**  
   Sebagai mahasiswa, saya ingin melihat jadwal kuliah harian di halaman utama agar tidak salah ruang kelas.  
   *(Prioritas: **Must Have**)*
2. **User Story 2:**  
   Sebagai mahasiswa, saya ingin mencatat daftar tugas beserta tanggal tenggatnya agar dapat mengatur waktu pengerjaan.  
   *(Prioritas: **Must Have**)*
3. **User Story 3:**  
   Sebagai mahasiswa, saya ingin mengaktifkan mode gelap (*dark theme*) agar tidak silau saat membaca jadwal di malam hari.  
   *(Prioritas: **Could Have**)*