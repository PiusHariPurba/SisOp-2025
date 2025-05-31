<div align="center">

# RESUME PC OS development over time

## **PENGENALAN SISTEM OPERASI**

![Pens Logo](https://belajargiat.id/wp-content/uploads/2020/10/logo-PENS.png)

**Dosen Pengampu:**

Dr. Ferry Astika Saputra, S.T., M.Sc.

**Disusun Oleh:**

Pius Purba (3124521015)

## **PROGRAM STUDI D3 TEKNIK INFORMATIKA PSDKU LAMONGAN**  
DEPARTEMEN TEKNIK INFORMATIKA DAN KOMPUTER  
POLITEKNIK ELEKTRONIKA NEGERI SURABAYA  
2025

</div>

---

# 1.34 Transisi User ke Kernel Mode

Secara sederhana sebenarnya ini adalah pemberian batas waktu bagi suatu permintaan / tugas dari user mode ke kernel mode untuk dieksekusi. Semua permintaan / tugas ini adalah semua inputan yang ada di PC user meliputi game, browsingan, bahkan untuk hanya sekedar ketikan/klikan mouse adalah requestan dari user mode. Berikut alur peralihan dan sekaligus pengeksekusiannya:

1. Timer diatur untuk menghentikan komputer setelah beberapa periode waktu. Timer di sini untuk mencegah terjadinya loop tak terbatas / proses yang memonopoli sumber daya yang bisa merusak sistem. (Blue screen adalah contohnya agar sistem tidak korup jika semakin jauh terjadi)
2. Simpan penghitung yang dikurangi oleh jam fisik
3. Sistem operasi mengatur penghitung (instruksi istimewa)
4. Ketika counter zero menghasilkan interupsi
5. Disiapkan sebelum proses penjadwalan untuk mendapatkan kembali kontrol atau menghentikan program yang melebihi waktu yang dialokasikan

# 1.35 Manajemen Proses

Proses adalah program yang sedang dijalankan. Proses adalah unit kerja dalam sistem. Program adalah entitas pasif, sedangkan proses adalah entitas aktif. Dalam pengeksekusian suatu perintah maka jelas akan ada prosedur yang akan dijalankan dan dalam sistem operasi, manajemen proses perintah dari user mode itulah dinamakan **PROSES** dan satuan dari **PROSES** disebut **THREAD**.

> Analoginya: Ketika seorang siswa mendapatkan pekerjaan rumah dari guru, maka PR yang dia bawa itulah yang disebut *proses* dalam sistem operasi. Sedangkan tugas apa saja yang diberikan — entah itu PR fisika, kimia, atau biologi — maka itulah yang dinamakan *thread*, yang jelas di dalamnya akan memakan waktu pengeksekusian (materi sebelumnya), sumber daya seperti CPU, memori, I/O, berkas, dan data inisialisasi.

Perlu diingat bahwa penghentian proses juga turut memerlukan pengambilan kembali sumber daya yang dapat digunakan kembali.

- **Proses single-threaded** memiliki satu penghitung program yang menentukan lokasi instruksi berikutnya untuk dieksekusi. Proses mengeksekusi instruksi secara berurutan, satu per satu, hingga selesai.
- **Proses multi-threaded** memiliki satu penghitung program per thread. Biasanya sistem memiliki banyak proses, beberapa pengguna, beberapa sistem operasi yang berjalan secara bersamaan pada satu atau lebih CPU.

> Konkurensi dilakukan dengan multiplexing CPU di antara proses / thread.

# 1.36 Aktivitas Manajemen Proses

Sistem operasi bertanggung jawab atas aktivitas berikut sehubungan dengan manajemen proses seperti:

- Membuat dan menghapus proses pengguna dan sistem
- Menangguhkan dan melanjutkan proses
- Menyediakan mekanisme untuk sinkronisasi proses
- Menyediakan mekanisme untuk komunikasi proses
- Menyediakan mekanisme penanganan kebuntuan

# 1.37 Manajemen Memori

Manajemen memori ialah proses yang menentukan apa yang ada di memori dan kapan, demi penoptimalan penggunaan CPU dan respons komputer terhadap pengguna. Untuk menjalankan setiap program, semua (atau sebagian) instruksi dan data yang dibutuhkan oleh program harus berada di dalam memori.

Kegiatan manajemen memori meliputi:

1. Pelacakan setiap bagian memori mana yang sedang digunakan dan oleh siapa
2. Memutuskan proses (atau bagian-bagiannya) dan data mana yang akan dipindahkan ke dalam dan keluar dari memori
3. Mengalokasikan dan mendealokasi ruang memori sesuai kebutuhan

# 1.38 Manajemen Sistem File

OS menyediakan tampilan penyimpanan informasi yang seragam dan logis (bersifat abstraksi) yang setiap media dikontrol oleh perangkat (misalnya, disk drive, tape drive). Properti yang bervariasi meliputi kecepatan akses, kapasitas, laju transfer data, metode akses (berurutan atau acak).

File biasanya diatur dalam direktori yang kontrol akses pada sebagian besar sistem untuk menentukan siapa yang dapat mengaksesnya.

Kegiatan OS meliputi:

1. Membuat dan menghapus file dan direktori
2. Primitif untuk memanipulasi file dan direktori
3. Memetakan file ke penyimpanan sekunder
4. Cadangkan file ke media penyimpanan yang stabil (non-volatil)
5. (Inilah yang meliputi command line dasar yang praktikumnya dilakukan di terminal Linux seperti `mkdir`, `mydir`, `echo`, `cat`, `vim`, `cd`, dll.)

# 1.39 Mass-Storage Management

Secara sederhana, **Mass-storage Management** (penyimpanan massal) adalah proses penyimpanan data yang tidak muat di memori utama atau data yang harus disimpan dalam jangka waktu *lama*. Oleh karena itu, manajemen yang tepat adalah hal yang sangat penting yang cepat lambatnya bergantung pada subsistem disk dan algoritmanya.

Aktivitas sistem operasi Mass-Storage meliputi:

1. Memasang dan melepas
2. Manajemen ruang bebas
3. Alokasi penyimpanan
4. Penjadwalan disk
5. Partisi
6. Perlindungan

Beberapa penyimpanan tidak perlu cepat:

- Penyimpanan tersier meliputi penyimpanan optik, pita magnetik
- Masih harus dikelola — oleh OS atau aplikasi

# 1.40 Caching

**Caching** adalah teknik untuk meningkatkan performa sistem komputer dengan menyimpan salinan data yang sering digunakan di tempat penyimpanan yang lebih cepat, disebut **cache**.  
Dilakukan di banyak level dalam komputer (dalam perangkat keras, sistem operasi atau perangkat lunak seperti FB, Instagram). Informasi yang digunakan disalin dari penyimpanan yang lebih lambat ke penyimpanan yang lebih cepat untuk sementara.

Penyimpanan yang lebih cepat (cache) diperiksa terlebih dahulu untuk menentukan apakah informasi ada di sana:

1. Jika ya, informasi digunakan langsung dari cache (cepat).
2. Jika tidak, data disalin ke cache dan digunakan di sana.

Cache lebih kecil dari penyimpanan yang di-cache:

1. Masalah desain penting manajemen cache.
2. Ukuran cache dan kebijakan penggantian.

