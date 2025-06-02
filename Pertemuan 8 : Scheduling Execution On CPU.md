<div align="center">

# RESUME PC OS development over time

## **SCHEDULING EXECUTION ON CPU **

![Image](https://github.com/user-attachments/assets/3ad88b6e-7159-44a2-a004-c909b974a88c)


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

## 🅐. Gantt Chart Penjadwalan (Soal Baru)

### *1. FCFS (First-Come, First-Served)*

*Burst Time:*

| Proses | Burst Time |
| ------ | ---------- |
| P1     | 6 ms       |
| P2     | 2 ms       |
| P3     | 4 ms       |
| P4     | 5 ms       |
| P5     | 3 ms       |

*Urutan eksekusi (sesuai urutan datang):*


| P1(6) | P2(2) | P3(4) | P4(5) | P5(3) |
0       6       8       12      17      20


---

### *2. SJF (Shortest Job First)*

*Urutan berdasarkan burst time terkecil ke terbesar:*


| P2(2) | P5(3) | P3(4) | P4(5) | P1(6) |
0       2       5       9       14      20


---

### *3. RR (Round Robin), Q = 2ms*

*Eksekusi dengan quantum 2 ms:*


| P1(2) | P2(2) | P3(2) | P4(2) | P5(2) | P1(2) | P3(2) | P4(2) | P5(1) | P1(2) | P4(1) |
0       2       4       6       8       10      12      14      16      17      19      21


---

## 🅑. Perhitungan Waktu Tunggu (WT)

### *1. FCFS*

*Completion Time:*

* P1 = 6, P2 = 8, P3 = 12, P4 = 17, P5 = 20

*Waiting Time:*

* P1: 6 - 6 = 0
* P2: 8 - 2 = 6
* P3: 12 - 4 = 8
* P4: 17 - 5 = 12
* P5: 20 - 3 = 17

*Rata-rata WT FCFS:*
(0 + 6 + 8 + 12 + 17) / 5 = 43 / 5 = 8.6 ms

---

### *2. SJF*

*Completion Time:*

* P2 = 2, P5 = 5, P3 = 9, P4 = 14, P1 = 20

*Waiting Time:*

* P2: 2 - 2 = 0
* P5: 5 - 3 = 2
* P3: 9 - 4 = 5
* P4: 14 - 5 = 9
* P1: 20 - 6 = 14

*Rata-rata WT SJF:*
(0 + 2 + 5 + 9 + 14) / 5 = 30 / 5 = 6 ms

---

### *3. RR (Q = 2ms)*

*Completion Time:*

* P1: 21
* P2: 4
* P3: 14
* P4: 21
* P5: 17

*Waiting Time:*

* P1: 21 - 6 = 15
* P2: 4 - 2 = 2
* P3: 14 - 4 = 10
* P4: 21 - 5 = 16
* P5: 17 - 3 = 14

*Rata-rata WT RR:*
(15 + 2 + 10 + 16 + 14) / 5 = 57 / 5 = 11.4 ms

---

## ⚫ Average Time

| Algoritma | Rata-rata Waiting Time |
| --------- | ---------------------- |
| FCFS      | 8.6 ms                 |
| SJF       | 6 ms (TERENDAH)        |
| RR (Q=2)  | 11.4 ms (TERTINGGI)    |

---
