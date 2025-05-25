<div align="center">

# TUGAS SISTEM OPERASI

## **SISTEM BILANGAN**

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

# 1. Fork  
Fork dalam Bahasa sederhana adalah pengcopyan fungsi awal ke fungsi barunya. Secara sederhana dapat digambarkan sebagai proses child-parent dengan penurunan hasil copy secara total sama persis dengan mother(fungsi awalnya). Hal ini dapat digambarkan secara umum dengan ilustrasi sebagai berikut

Perlu dicatat, proses id child function akan memiliki pid yang bisa jadi beda ataupun sama dengan mothernya tergantung fork jenis apa yang dipakai dengan penjelasan sebagai berikut:  
	A. fork01.c  
		Ini adalah command yang membuat salinan Tunggal fungsi child yang sama persis dengan mothernya hanya saja PID nya berbeda dengan pengilustrasian sebagai berikut
	

	B. fork02.c  
		Jika command sebelumnya hanya menghasilkan Salinan Tunggal dari mothernya, maka fork02.c pada kasus ini akan menghasilkan 2 salinan child dengan tapi pid child yang tidak sama dengan mothernya.

	C. fork03.c  
		Lalu pada fork 03.c adalah command perintah salin mother dengan child yang akan dihasilkan adalah 2 di tahap pertama. Mengapa fork03.c hanya menghasilkan 2 child di fase pertama? Karena diperluka jeda (wait) untuk penyalinannya agar tidak ada data/fungsi yang corrupt didalam pembuatan 4 child pada anak pertama (yang awalnya 2 itu)

	D. fork04.c  
		Sedangkan pada fork04.c bisa jadi versi fork01.c hanya saja didalam pembuatan childnya bertipe loop/pengulangan dan juga jika fork01.c hanya menghasilkan copy Tunggal dari mother, maka fork04.c sebenarnya bisa lebih dari 1 child dengan pengilustrasian sebagai berikut

	E. fork05.c  
		Lalu pada fork05.c adalah penyalinan dari mother ke child hanya saja jika pada fork01 hingga 04 hanya berpatok pada mothernya, maka pada fork05.c dapat memungkinkan user menghasilkan child hasil kombinasi dari program lain atau yang bisa disebut sebagai exec()

	F. fork06.c  
		Dan fork06 itu sendiri adalah kombinasi dari exec pada fork5, loop dari fork04, wait dari fork03. Karena kefleksibalitas command ini, fork06.c adalah sintaks dengan kompleksitas tertinggi diantara fork yang lain.  

## Notes tambahan:  
• If fork() returns a negative value, the creation of a child process was unsuccessful.  
• fork() returns a zero to the newly created child process.  
• fork() returns a positive value, the process ID of the child process, to the parent. The returned process ID is of type pid_t defined in sys/types.h. Normally, the process ID is an integer. Moreover, a process can use function getpid() to retrieve the process ID assigned to this process.

## Sumber Materi  
Materi dapat dibaca pada link [https://www.csl.mtu.edu/cs4411.ck/www/NOTES/process/fork/create.html](https://www.csl.mtu.edu/cs4411.ck/www/NOTES/process/fork/create.html)

