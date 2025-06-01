<div align="center">

# TUGAS SISTEM OPERASI

## **APPENDIX A ~ PERKEMBANGAN OS DARI TAHUN KE TAHUN**

![Image](https://github.com/user-attachments/assets/3ad88b6e-7159-44a2-a004-c909b974a88c)

**Dosen Pengampu:**  
Dr. Ferry Astika Saputra, S.T., M.Sc.  
(197708232001121002)

**Disusun Oleh:**  
Pius Purba (3124521015)

## **PROGRAM STUDI D3 TEKNIK INFORMATIKA PSDKU LAMONGAN**  
DEPARTEMEN TEKNIK INFORMATIKA DAN KOMPUTER  
POLITEKNIK ELEKTRONIKA NEGERI SURABAYA  
2025

</div>

~~~

# Evolusi Komputer

## 1. Evolusi Komputer
Salah satu alasan untuk mempelajari arsitektur dan sistem operasi awal adalah bahwa fitur yang tadinya hanya dijalankan pada sistem besar pada akhirnya dapat diterapkan pada sistem yang sangat kecil. Memang benar, pengujian sistem operasi untuk mainframe dan mikrokomputer menunjukkan bahwa banyak fitur yang tadinya hanya tersedia pada main-frame telah diadopsi untuk mikrokomputer. Oleh karena itu, konsep sistem operasi yang sama sesuai untuk berbagai kelas komputer: mainframe, komputer mini, mikrokomputer, dan perangkat genggam. Untuk memahami sistem operasi modern, Anda perlu mengenali tema migrasi fitur dan sejarah panjang banyak fitur sistem operasi . berikut sketsa perkembangan komputer dari tahun ke tahun

## 2. Awal mulanya
Komputer-komputer sebelum era Atlas (1940-an dan 1950-an) hanyalah mesin raksasa yang menggunakan tabung vakum, menghasilkan panas tinggi, dan memiliki keandalan rendah. Input dan output data bergantung pada media fisik seperti kartu pons atau pita kertas, tanpa adanya monitor atau keyboard interaktif. Pemrograman dilakukan langsung dalam bahasa mesin atau bahasa rakitan yang rumit, spesifik untuk tiap komputer, dan setiap program dijalankan satu per satu (secara batch) karena belum ada sistem operasi canggih yang mengatur sumber daya.

Karena keterbatasan kecepatan proses, kapasitas memori yang sangat kecil, dan biaya operasional tinggi, komputer awal ini hanya digunakan untuk tugas-tugas kalkulasi intensif seperti perhitungan ilmiah, militer, atau sensus. Pengoperasiannya tidak interaktif; pengguna menyerahkan pekerjaan dan menunggu hasilnya tanpa bisa berinteraksi langsung selama proses komputasi berlangsung. Era ini menandai fondasi awal komputasi, namun sangat berbeda jauh dari efisiensi dan kemudahan penggunaan yang mulai diperkenalkan oleh sistem-sistem selanjutnya

## 3. Atlas
Atlas Computer dari University of Manchester pada tahun 1960-an (khususnya 1962) memainkan peran revolusioner yang sangat signifikan dalam pengembangan dan pengelolaan memori komputer. Inovasi terbesar dari proyek Atlas adalah penemuan **Memori Virtual (Virtual Memory)**.

**Sebelum Atlas:** Programmer harus secara manual mengatur transfer data antara memori utama yang kecil dan cepat dengan penyimpanan sekunder yang lebih besar dan lambat.

**Inovasi Atlas dengan Memori Virtual:** Atlas mengotomatiskan proses ini dan memberikan ilusi kepada setiap pengguna bahwa mereka memiliki akses ke memori besar dan cepat, dengan teknik **paging**.

**Mengapa ini Revolusioner?**
- **Menyederhanakan Pemrograman**
- **Memungkinkan Multiprogramming yang Efisien**
- **Fondasi Sistem Operasi Modern**

## 4. XDS-940
Dikembangkan oleh Berkeley Computer Corporation (BCC) sekitar tahun 1966. Sistem ini dirancang untuk komputer SDS 940 dan merupakan sistem **time-sharing** canggih.

**Keunggulan:**
- Mendukung banyak pengguna secara bersamaan
- Mendukung bahasa FORTRAN, LISP, dan SNOBOL

**Keterbatasan:**
- Skalabilitas terbatas
- Ketergantungan pada perangkat keras spesifik

## 5. THE (Technische Hogeschool Eindhoven)
Dikembangkan oleh Edsger W. Dijkstra sekitar 1965–1966 untuk komputer Electrologica X8. Terkenal karena **struktur berlapis (layered structure)**.

**Keunggulan:**
- Modular dan terstruktur
- Menggunakan **semafor** untuk sinkronisasi proses

**Kelemahan:**
- Lebih merupakan proyek penelitian
- Overhead dari struktur berlapis

## 6. RC 4000 Multiprogramming System
Dikembangkan oleh Per Brinch Hansen di Denmark, akhir 1960-an. Dikenal karena konsep **kernel minimalis**.

**Keunggulan:**
- Kernel menyediakan IPC dan manajemen memori dasar
- Layanan OS dijalankan sebagai proses pengguna

**Kelemahan:**
- IPC bisa menjadi bottleneck
- Kompleksitas dalam desain modular

## 7. CTSS (Compatible Time-Sharing System)
Dikembangkan di MIT tahun 1961. Salah satu sistem **time-sharing** pertama.

**Keunggulan:**
- Penjadwalan round-robin
- Manajemen memori multi-user
- Dukungan sistem berkas pengguna individu

**Kekurangan:**
- Manajemen sumber daya dan proteksi sederhana
- Skalabilitas terbatas

## 8. MULTICS (Multiplexed Information and Computing Service)
Dimulai tahun 1964 oleh MIT, General Electric, dan Bell Labs.

**Keunggulan:**
- Memori tersegmentasi dan paging dinamis
- Sistem berkas hierarkis
- Penulisan dengan PL/I

**Kelemahan:**
- Kompleks dan membutuhkan hardware besar
- Performanya awalnya kurang

## 9. IBM System/360 Operating Systems (OS/360)
Diperkenalkan pertengahan 1960-an. OS/360 menjadi sistem operasi penting dari IBM.

**Keunggulan:**
- Kompatibel lintas model
- Mendukung multiprogramming

**Kekurangan:**
- Kompleksitas tinggi
- Membutuhkan sumber daya besar

## 10. TOPS-20
Dikembangkan oleh DEC sekitar 1976 untuk PDP-10/DECSYSTEM-20.

**Keunggulan:**
- Antarmuka pengguna intuitif
- Fitur **memori virtual** dan **time-sharing** canggih

**Kelemahan:**
- Tergantung pada platform khusus

## 11. CP/M & MS-DOS
**CP/M** dirilis 1974 oleh Digital Research. **MS-DOS** dikembangkan dari QDOS tahun 1980, dirilis 1981.

**Keunggulan:**
- CP/M: standar mikrokomputer awal
- MS-DOS: diadopsi IBM PC, pasar besar

**Kekurangan:**
- CP/M: 8-bit, RAM terbatas
- MS-DOS: tidak mendukung multitasking

## 12. Macintosh & Windows
**Macintosh OS** pertama kali pada 1984, **Windows** mulai 1985.

**Keunggulan:**
- GUI intuitif (ikon, jendela, mouse)
- Windows berjalan di banyak perangkat keras

**Kekurangan:**
- Mac: mahal, multitasking terbatas (awal)
- Windows: bergantung pada MS-DOS (awal)

## 13. Mach
Dikembangkan di Carnegie Mellon University mulai 1985 oleh Richard Rashid dan Avie Tevanian.

**Keunggulan:**
- **Desain microkernel**
- Layanan OS sebagai server di ruang pengguna
- Mendukung komputasi paralel dan terdistribusi

```
