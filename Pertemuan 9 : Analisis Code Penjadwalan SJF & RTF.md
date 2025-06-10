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


## 📖 Penugasan

1. Melakukan cloning pada repository [Scheduling-Algorithms](https://github.com/ferryastika/Scheduling-Algorithms) sebagai referensi untuk penugasan ini
2. Melakukan analisis terhadap 3 code program algoritma scheduling:
   - **SJF without arrival time (non-preemptive)**  
   - **SJF with arrival time (non-preemptive)**  
   - **SRTF (preemptive)**
3. Membuat laporan dalam format `.md` dengan studi kasus sesuai PPT yang nantinya akan dikumpulkan melalui link GitHub di Ethol

---

## 🔍 Analisis Code Program Algoritma Scheduling

### 🧩 Tiga Program yang Dianalisis

---

## 1️⃣ SJF Without Arrival Time (Non-Preemptive)

### 📝 Source Code

```cpp
#include<stdio.h>
struct proc
{
    int no,bt,ct,tat,wt;
};
struct proc read(int i)
{
    struct proc p;
    printf("\nProcess No: %d\n",i);
    p.no=i;
    printf("Enter Burst Time: ");
    scanf("%d",&p.bt);
    return p;
}
int main()
{
    struct proc p[10],tmp;
    float avgtat=0,avgwt=0;
    int n,ct=0;
    printf("<--SJF Scheduling Algorithm Without Arrival Time (Non-Preemptive)-->\n");
    printf("Enter Number of Processes: ");
    scanf("%d",&n);
    for(int i=0;i<n;i++)
        p[i]=read(i+1);
    for(int i=0;i<n-1;i++)
        for(int j=0;j<n-i-1;j++)    
            if(p[j].bt>p[j+1].bt)
            {
                tmp=p[j];
                p[j]=p[j+1];
                p[j+1]=tmp;
            }
    printf("\nProcessNo\tBT\tCT\tTAT\tWT\tRT\n");
    for(int i=0;i<n;i++)
    {
        ct+=p[i].bt;
        p[i].ct=p[i].tat=ct;
        avgtat+=p[i].tat;
        p[i].wt=p[i].tat-p[i].bt;
        avgwt+=p[i].wt;
        printf("P%d\t\t%d\t%d\t%d\t%d\t%d\n",p[i].no,p[i].bt,p[i].ct,p[i].tat,p[i].wt,p[i].wt);
    }
    avgtat/=n,avgwt/=n;
    printf("\nAverage TurnAroundTime=%f\nAverage WaitingTime=%f",avgtat,avgwt);
}
```

### 🔍 Analisis Program

**Konsep:** Algoritma ini mengasumsikan semua proses tiba secara bersamaan di waktu yang sama. Proses dengan burst time terkecil akan dieksekusi terlebih dahulu dan bersifat non-preemptive (tidak dapat dihentikan hingga selesai).

### 🏗️ Struktur Program

#### 1. **Struct `proc`**
```cpp
struct proc {
    int no, bt, ct, tat, wt;
};
```
- `no` → Nomor proses
- `bt` → Burst time (waktu eksekusi)  
- `ct` → Completion time (waktu selesai)
- `tat` → Turnaround time (waktu total)
- `wt` → Waiting time (waktu tunggu)

#### 2. **Fungsi `read(int i)`**
Mengambil input burst time untuk setiap proses dan menetapkan nomor prosesnya.

#### 3. **Algoritma Sorting**
```cpp
for(int i=0; i<n-1; i++)
    for(int j=0; j<n-i-1; j++)
        if(p[j].bt > p[j+1].bt)
            swap(p[j], p[j+1]);
```
Mengurutkan proses berdasarkan burst time terkecil menggunakan bubble sort.

#### 4. **Perhitungan Metrik**
```cpp
ct += p[i].bt;           // Total waktu hingga proses selesai
p[i].ct = ct;            // Completion time
p[i].tat = ct;           // TAT = CT (arrival time = 0)
p[i].wt = p[i].tat - p[i].bt;  // WT = TAT - BT
```

### 📊 Contoh Eksekusi

#### Input:
```
Jumlah Proses: 4
P1: BT = 6
P2: BT = 8  
P3: BT = 7
P4: BT = 3
```

#### Setelah Sorting:
P4(3) → P1(6) → P3(7) → P2(8)

#### Gantt Chart:
```
| P4 | P1 | P3 | P2 |
0----3----9----16---24


```

#### Output:
```
ProcessNo    BT    CT    TAT    WT    RT
P4           3     3     3      0     0
P1           6     9     9      3     3
P3           7    16    16      9     9
P2           8    24    24     16    16

Average TurnAroundTime = 13.000000
Average WaitingTime = 7.000000
```

### ⚖️ Evaluasi

#### ✅ **Kelebihan:**
- Mengurangi average waiting time dibanding FCFS
- Sederhana dalam implementasi
- Optimal untuk batch processing dengan proses pendek

#### ❌ **Kekurangan:**
- Tidak mempertimbangkan arrival time
- Dapat menyebabkan starvation untuk proses dengan burst time besar
- Tidak realistis karena asumsi semua proses tiba bersamaan

---

## 2️⃣ SJF With Arrival Time (Non-Preemptive)

### 📝 Source Code

```cpp
#include<stdio.h>
struct proc
{
    int no,at,bt,it,ct,tat,wt;
};
struct proc read(int i)
{
    struct proc p;
    printf("\nProcess No: %d\n",i);
    p.no=i;
    printf("Enter Arrival Time: ");
    scanf("%d",&p.at);
    printf("Enter Burst Time: ");
    scanf("%d",&p.bt);
    return p;
}
int main()
{
    int  n,j,min=0;
    float avgtat=0,avgwt=0;
    struct proc p[10],temp;
    printf("<--SJF Scheduling Algorithm (Non-Preemptive)-->\n");
    printf("Enter Number of Processes: ");
    scanf("%d",&n);
    for(int i=0;i<n;i++)
        p[i]=read(i+1);
    for(int i=0;i<n-1;i++)
        for(j=0;j<n-i-1;j++)    
            if(p[j].at>p[j+1].at)
            {
            temp=p[j];
            p[j]=p[j+1];
            p[j+1]=temp;
            }
    for(j=1;j<n&&p[j].at==p[0].at;j++)
        if(p[j].bt<p[min].bt)
            min=j;
    temp=p[0];
    p[0]=p[min];
    p[min]=temp;
    p[0].it=p[0].at;
    p[0].ct=p[0].it+p[0].bt;
    for(int i=1;i<n;i++)
    {
        for(j=i+1,min=i;j<n&&p[j].at<=p[i-1].ct;j++)
            if(p[j].bt<p[min].bt)
                min=j;
        temp=p[i];
        p[i]=p[min];
        p[min]=temp;
        if(p[i].at<=p[i-1].ct)
            p[i].it=p[i-1].ct;
        else
            p[i].it=p[i].at;
        p[i].ct=p[i].it+p[i].bt;
    }
    printf("\nProcess\t\tAT\tBT\tCT\tTAT\tWT\tRT\n");
    for(int i=0;i<n;i++)
    {
        p[i].tat=p[i].ct-p[i].at;
        avgtat+=p[i].tat;
        p[i].wt=p[i].tat-p[i].bt;
        avgwt+=p[i].wt;
        printf("P%d\t\t%d\t%d\t%d\t%d\t%d\t%d\n",p[i].no,p[i].at,p[i].bt,p[i].ct,p[i].tat,p[i].wt,p[i].wt);
    }
    avgtat/=n,avgwt/=n;
    printf("\nAverage TurnAroundTime=%f\nAverage WaitingTime=%f",avgtat,avgwt);
}
```

### 🔍 Analisis Program

**Konsep:** Algoritma ini mempertimbangkan arrival time dari setiap proses. Pada setiap waktu completion, sistem memilih proses dengan burst time terkecil dari proses-proses yang sudah tiba.

### 🏗️ Struktur Program

#### 1. **Struct `proc`**
```cpp
struct proc {
    int no, at, bt, it, ct, tat, wt;
};
```
- `at` → Arrival time (waktu kedatangan)
- `it` → Initial time (waktu mulai eksekusi)

#### 2. **Algoritma Utama**

**Langkah 1:** Sort berdasarkan arrival time
```cpp
for(int i=0; i<n-1; i++)
    for(j=0; j<n-i-1; j++)
        if(p[j].at > p[j+1].at)
            swap(p[j], p[j+1]);
```

**Langkah 2:** Pilih proses pertama (jika ada yang sama arrival time, pilih burst time terkecil)

**Langkah 3:** Untuk setiap completion time, pilih proses dengan burst time terkecil yang sudah tiba

### 📊 Contoh Eksekusi

#### Input:
```
Jumlah Proses: 4
P1: AT = 0, BT = 8
P2: AT = 1, BT = 4
P3: AT = 2, BT = 9  
P4: AT = 3, BT = 5
```

#### Urutan Eksekusi:
1. **t=0:** P1 mulai (satu-satunya yang tiba)
2. **t=8:** P1 selesai, pilih dari {P2, P3, P4} → P2 (BT=4)
3. **t=12:** P2 selesai, pilih dari {P3, P4} → P4 (BT=5)
4. **t=17:** P4 selesai, eksekusi P3

#### Gantt Chart:
```
| P1 | P2 | P4 | P3 |
0---8-----12---17---26
```

#### Output:
```
Process    AT    BT    CT    TAT    WT    RT
P1         0     8     8     8      0     0
P2         1     4    12    11      7     7
P4         3     5    17    14      9     9
P3         2     9    26    24     15    15

Average TurnAroundTime = 14.250000
Average WaitingTime = 7.750000
```

### ⚖️ Evaluasi

#### ✅ **Kelebihan:**
- Lebih realistis dengan mempertimbangkan arrival time
- Mengurangi average waiting time untuk proses pendek
- Cocok untuk sistem dengan proses yang datang bertahap

#### ❌ **Kekurangan:**
- Masih dapat menyebabkan starvation
- Complexity lebih tinggi dalam implementasi
- CPU dapat idle jika tidak ada proses yang tiba

---

## 3️⃣ SRTF (Shortest Remaining Time First) - Preemptive

### 📝 Source Code

```cpp
#include<stdio.h>
#define MAX 9999
struct proc
{
    int no,at,bt,rt,ct,tat,wt;
};
struct proc read(int i)
{
    struct proc p;
    printf("\nProcess No: %d\n",i);
    p.no=i;
    printf("Enter Arrival Time: ");
    scanf("%d",&p.at);
    printf("Enter Burst Time: ");
    scanf("%d",&p.bt);
    p.rt=p.bt;
    return p;
}
int main()
{
    struct proc p[10],temp;
    float avgtat=0,avgwt=0;
    int n,s,remain=0,time;
    printf("<--SRTF Scheduling Algorithm (Preemptive)-->\n");
    printf("Enter Number of Processes: ");
    scanf("%d",&n);
    for(int i=0;i<n;i++)
        p[i]=read(i+1);
    for(int i=0;i<n-1;i++)
        for(int j=0;j<n-i-1;j++)    
            if(p[j].at>p[j+1].at)
            {
            temp=p[j];
            p[j]=p[j+1];
            p[j+1]=temp;
            }
    printf("\nProcess\t\tAT\tBT\tCT\tTAT\tWT\n");
    p[9].rt=MAX;
    for(time=0;remain!=n;time++)
    {
        s=9;
        for(int i=0;i<n;i++)
            if(p[i].at<=time&&p[i].rt<p[s].rt&&p[i].rt>0)
                s=i;
        p[s].rt--;
        if(p[s].rt==0)
        {
            remain++;
            p[s].ct=time+1;
            p[s].tat=p[s].ct-p[s].at;
            avgtat+=p[s].tat;
            p[s].wt=p[s].tat-p[s].bt;
            avgwt+=p[s].wt;
            printf("P%d\t\t%d\t%d\t%d\t%d\t%d\n",p[s].no,p[s].at,p[s].bt,p[s].ct,p[s].tat,p[s].wt);
        }
    }
    avgtat/=n,avgwt/=n;
    printf("\nAverage TurnAroundTime=%f\nAverage WaitingTime=%f",avgtat,avgwt);
}
```

### 🔍 Analisis Program

**Konsep:** Algoritma preemptive yang pada setiap unit waktu memilih proses dengan remaining time terkecil. Jika proses baru dengan remaining time lebih kecil tiba, proses yang sedang berjalan akan di-preempt.

### 🏗️ Struktur Program

#### 1. **Struct `proc`**
```cpp
struct proc {
    int no, at, bt, rt, ct, tat, wt;
};
```
- `rt` → Remaining time (sisa waktu eksekusi)

#### 2. **Algoritma Simulasi Time-Based**
```cpp
p[9].rt = MAX;  // Sentinel value
for(time=0; remain!=n; time++) {
    s = 9;  // Default ke sentinel
    
    // Cari proses dengan remaining time terkecil yang sudah tiba
    for(int i=0; i<n; i++)
        if(p[i].at <= time && p[i].rt < p[s].rt && p[i].rt > 0)
            s = i;
    
    p[s].rt--;  // Eksekusi 1 unit waktu
    
    // Jika proses selesai
    if(p[s].rt == 0) {
        remain++;
        p[s].ct = time + 1;
        // Hitung TAT dan WT
    }
}
```

### 📊 Contoh Eksekusi

#### Input:
```
Jumlah Proses: 4
P1: AT = 0, BT = 8
P2: AT = 1, BT = 4
P3: AT = 2, BT = 9
P4: AT = 3, BT = 5
```

#### Simulasi Timeline:
- **t=0:** P1 mulai (RT=8)
- **t=1:** P2 tiba (RT=4 < 7), P1 di-preempt, P2 mulai
- **t=5:** P2 selesai, P1 lanjut (RT=7)
- **t=3:** P4 tiba (RT=5 < 7), P1 di-preempt lagi, P4 mulai
- **t=10:** P4 selesai, P1 lanjut (RT=7)
- **t=17:** P1 selesai
- **t=17-26:** P3 eksekusi

#### Gantt Chart:
```
|P1|P2|P2|P2|P2|P4|P4|P4|P4|P4|P1|P1|P1|P1|P1|P1|P1|P3|P3|P3|P3|P3|P3|P3|P3|P3|
0--1--2--3--4--5--6--7--8--9--10-11-12-13-14-15-16-17-18-19-20-21-22-23-24-25-26
```

#### Output:
```
Process    AT    BT    CT    TAT    WT
P2         1     4     5     4      0
P4         3     5    10     7      2
P1         0     8    17    17      9
P3         2     9    26    24     15

Average TurnAroundTime = 13.000000
Average WaitingTime = 6.500000
```

### ⚖️ Evaluasi

#### ✅ **Kelebihan:**
- Paling responsif terhadap proses pendek yang baru tiba
- Menghasilkan average waiting time yang optimal
- Cocok untuk sistem interaktif dan real-time

#### ❌ **Kekurangan:**
- Implementasi paling kompleks
- Overhead context switching tinggi
- Masih dapat menyebabkan starvation untuk proses besar
- Membutuhkan interrupt timer

---

## 📊 Perbandingan Ketiga Algoritma

| Aspek | SJF (No AT) | SJF (With AT) | SRTF |
|-------|-------------|---------------|------|
| **Preemptive** | ❌ | ❌ | ✅ |
| **Arrival Time** | ❌ | ✅ | ✅ |
| **Complexity** | Rendah | Sedang | Tinggi |
| **Avg WT** | Baik | Baik | Optimal |
| **Starvation** | ✅ | ✅ | ✅ |
| **Context Switch** | Minimal | Minimal | Tinggi |
| **Use Case** | Batch | Mixed | Interactive |

---

## 🎯 Kesimpulan

1. **SJF Without Arrival Time** cocok untuk sistem batch sederhana dengan asumsi semua proses tersedia di awal
2. **SJF With Arrival Time** lebih realistis untuk sistem yang menerima proses secara bertahap
3. **SRTF** memberikan responsivitas terbaik dan optimal untuk average waiting time, namun dengan kompleksitas implementasi yang tinggi

Pemilihan algoritma tergantung pada karakteristik sistem, jenis beban kerja, dan prioritas antara kesederhanaan implementasi versus performa optimal.

---

*📝 Laporan ini disusun sebagai bagian dari tugas Sistem Operasi untuk memahami konsep dan implementasi algoritma scheduling CPU.*
