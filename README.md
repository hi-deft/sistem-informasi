[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/EJc24P4I)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=19594842&assignment_repo_type=AssignmentRepo)
# Sistem Informasi Nilai
## Pengantar
Ini adalah tugas akhir untuk mata kuliah **TIF1330 Pemrograman Web**. Tugas dikerjakan secara kelompok dengan **maksimal 5 orang dan minimal 3 orang**.

Tugas ini bertujuan untuk mengembangkan aplikasi **web dinamis** yang dapat digunakan untuk mengelola data nilai di Universitas Rajin Pangkal Pandai (URP). Aplikasi ini akan dibangun menggunakan HTML, CSS, PHP, dan MySQL.

Aplikasi yang akan anda bangun sepadan dengan fitur penilaian yang ada di Google Classroom. 


## Tujuan Pembelajaran
Setelah menyelesaikan tugas ini, mahasiswa diharapkan mampu:
1. Mengimplementasikan aplikasi web dinamis menggunakan HTML, CSS, PHP, dan MySQL
2. Membangun sistem CRUD (Create, Read, Update, Delete) yang kompleks
3. Menerapkan relasi database yang tepat untuk menyimpan data akademik
4. Mengembangkan fitur pengelolaan nilai dengan berbagai jenis dan bobot
5. Mengimplementasikan sistem otentikasi dan otorisasi untuk dosen, mahasiswa, dan admin
6. Menerapkan validasi data pada sisi client dan server

## Deskripsi Tugas
Universitas Rajin Pangkal Pandai (URP) membutuhkan Sistem Informasi Nilai berbasis web. Sistem ini akan digunakan oleh dosen untuk mencatat dan mengolah nilai mahasiswa, serta oleh mahasiswa untuk melihat nilai-nilai mereka.

### Fitur Aplikasi
#### Umum:
1. **Autentikasi Pengguna**
   - Pengguna dapat login menggunakan username dan password
   - Terdapat tiga jenis pengguna: Dosen, Mahasiswa, dan Admin
   - Setiap pengguna memiliki hak akses yang berbeda
2. **Dashboard Setiap Pengguna**
   - Menampilkan informasi ringkas tentang pengguna yang sedang login
   - Menampilkan menu navigasi sesuai dengan hak akses pengguna


#### Untuk Dosen:
1. **Pengelolaan Jenis Nilai**
   - Membuat berbagai jenis nilai (UAS, UTS, Tugas, Quiz) di setiap mata kuliah
   - Mengatur bobot untuk setiap jenis nilai (total bobot harus 100%)

2. **Pengelolaan Nilai Mahasiswa Secara Online**
   - Memasukkan berbagai nilai untuk setiap mahasiswa per mata kuliah
   - Mengubah atau menghapus nilai-nilai yang sudah dimasukkan/disimpan


#### Untuk Mahasiswa:
1. **Lihat Nilai**
   - Memilih daftar mata kuliah yang diambil
   - Melihat detail nilai dan nilai akhir untuk setiap mata kuliah yang dipilih


#### Untuk Admin:
1. **Pengelolaan Pengguna**
   - Menambahkan, mengubah, dan menghapus pengguna (dosen dan mahasiswa)
  
2. **Pengelolaan Mata Kuliah**
   - Menambahkan, mengubah, dan menghapus mata kuliah

3. **Pengelolaan Semester**
   - Menambahkan, mengubah, dan menghapus semester
   - Mengatur mata kuliah yang ditawarkan pada setiap semester

4. **Pengelolaan Kelas**
   - Menambahkan, mengubah, dan menghapus kelas
   - Mengatur mahasiswa yang terdaftar dalam setiap kelas
   - Mengatur dosen pengampu untuk setiap kelas. Satu kelas bisa memiliki lebih dari satu dosen

## Struktur Database
Berikut adalah tabel-tabel di dalam database yang bisa anda gunakan. Field-field yang ada di dalam tabel bisa anda sesuaikan dengan kebutuhan aplikasi yang akan anda buat. Anda juga bisa menambah/mengurangi tabel sesuai dengan kebutuhan aplikasi.:
1. `users` - menyimpan data pengguna (dosen dan mahasiswa)
2. `mata_kuliah` - menyimpan informasi mata kuliah
3. `semester` - menyimpan informasi semester
4. `kelas` - menyimpan informasi kelas
5. `mahasiswa` - menyimpan data mahasiswa
6. `dosen` - menyimpan data dosen
7. `kelas_mahasiswa` - menyimpan relasi antara mahasiswa dan kelas
8. `kelas_dosen` - menyimpan relasi antara dosen dan kelas. Satu kelas bisa memiliki lebih dari satu dosen
9. `jenis_nilai` - menyimpan jenis-jenis nilai (misalnya: UAS, UTS, tugas, quiz)
10. `kelas_jenis_nilai_bobot` - menghubungkan kelas dengan jenis penilaian beserta bobot spesifiknya
11. `nilai` - menyimpan nilai mahasiswa untuk kelas dan jenis penilaian tertentu
12. `scores` - menyimpan nilai mahasiswa untuk setiap penilaian
13. `nilai_akhir` - menyimpan nilai akhir mahasiswa untuk setiap kelas
 



## Kriteria Penilaian
| Komponen | Bobot |
|----------|-------|
| Implementasi fitur | 50% |
| Desain antarmuka | 10% |
| Validasi data | 10% |
| Dokumentasi dan File Presentasi | 10% |
| Presentasi di Kelas | 20% |
| Total | 100% |

## Bonus
1. Jika aplikasi dihosting di server publik
2. Jika anda menambahkan *Dockerfile* dan *docker-compose.yml* untuk mempermudah menjalankan dan deployment aplikasi
## Deadline dan Pengumpulan
- Deadline tugas adalah tanggal 3 Juni 2025 jam 23:59 WIB.
- Pengumpulan tugas dilakukan melalui GitHub Classroom.

## Kelengkapan Pengumpulan
- Selain kode sumber aplikasi, pastikan anda juga menyertakan hal-hal berikut di dalam repository:
  - File presentasi (dalam format PDF/PPT)
  - Dokumentasi penggunaan aplikasi berupa file DOKUMENTASI.md. Dokumen berisi screenshot hasil implementasi dan fitur-fitur yang telah dikerjakan.
  - File SQL untuk membuat database, tabel-tabel yang diperlukan, dan sample data yang digunakan untuk pengujian.

## Petunjuk Kerja Kelompok Menggunakan Workflow GitHub

### 🧵 Gunakan Branch
```bash
git checkout -b nama-fitur
```

### 💾 Commit Secara Berkala
```bash
git commit -m "Deskripsi perubahan"
```

### 🔄 Buat Pull Request
- Setelah menyelesaikan pekerjaan, buat PR ke branch `main`
- Diskusikan dan review bersama sebelum merge

### 💬 Gunakan Issues dan PR untuk Kolaborasi
- Komunikasi tim tercermin dari aktivitas ini

### ✅ Etika Kolaborasi
- Jangan **overwrite** kerja teman tanpa diskusi.
- **Saling review** dan bantu menyelesaikan masalah.
- Jika ada **konflik dalam merge**, diskusikan secara terbuka.
- Setiap anggota harus **berkontribusi secara adil**.



Selamat mengerjakan!
