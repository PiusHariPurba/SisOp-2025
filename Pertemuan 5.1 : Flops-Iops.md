<div align="center">

# TUGAS SISTEM OPERASI

## **HOW TO SEE PERFORMANCE OUR PC WITH FLOPS & IOPS**

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

---
# 🚀 1.Bench Util

🔧 secara sederhana sebenarnya fungsi bench util sendiri itu adalah untuk mengetes dan menguji performakomputer meliputi:
- 🖥️ **cpu** 
- 💾 **memori** 
- 💿 **penyimpanan** 
- 🌐 **jaringan** 
- ⚡ **fungsi spesifik** yang dapat dijalankan oleh suatu komputer dalam satuan **FLOPS** & **IOPS**.

---

# 🔨 2. Build Binaries

```bash
$ make
```

⚙️ fungsi command line ini adalah untuk menghapus file objek (`.o`) dan binary eksekusi untuk memastikan kompilasi ulang tanpa konflik dari build sebelumnya.

# 📦 3. Install Binaries

```bash
$ sudo make install
```

✅ Perintah ini akan menyalin binary yang telah dikompilasi ke direktori sistem agar dapat diakses secara global.

# 🗑️ 4. uninstall Binaries

```bash
$ sudo make uninstall
```

❌ Perintah ini akan menghapus binary yang telah diinstal dari sistem.

# 🎯 5. Usage

```bash
$ ./bench -i
```

📊 Menjalankan benchmark untuk **IOPS** (Input/Output Operations Per Second).

```bash
$ ./bench -f
```

🧮 Menjalankan benchmark untuk **FLOPS** (Floating Point Operations Per Second).

```bash
$ ./bench -h
```

❓ Menampilkan bantuan terkait penggunaan program.

# 🤔 LANTAS

💭 apa bedanya **flops32**, **iops32** & **flops64**, **iops64**? apa perbedaan dari **32** dan **64** pada perintah tersebut?

## 🔢 Integer Operations (IOPS)

```bash
$ iops32 $(nproc)
```

🏃‍♂️ **Benchmark32-bit Integer Operations** menggunakan semua core CPU.

```bash
$ iops64 $(nproc)
```

🏃‍♀️ **Benchmark64-bit Integer Operations** menggunakan semua core CPU.

## 🧮 Floating Point Operations (FLOPS)

```bash
$ flops32 $(nproc)
```

🚀 **Benchmark32-bit Floating Operations** menggunakan semua core CPU.

```bash
$ flops64 $(nproc)
```

💪 **Benchmark64-bit Floating Operations** menggunakan semua core CPU.

## 📝 Kesimpulan

### 🆚 IOPS vs FLOPS
- 🔢 **IOPS** menggunakan operasi integer (lebih cepat, digunakan dalam perhitungan umum)
- 🧮 **FLOPS** mengukur operasi floating-point (digunakan dalam aplikasi numerik dan ilmiah)

### ⚖️ 32bit vs 64bit
- 🎯 **64-bit** lebih akurat dan cocok untuk CPU modern tetapi proses agak berat
- 🪶 **32bit** lebih ringan dan cocok untuk CPU jadul

---

# 📊 B. Laporan Performa laptop saya

<div align="center">
  
![Image](https://github.com/user-attachments/assets/82e07ce5-7ea1-46bc-b931-83c9ad7fd3ba)

🟰

![Image](https://github.com/user-attachments/assets/6e134770-68bc-4276-96ba-eda2be4c8892)
</div>
