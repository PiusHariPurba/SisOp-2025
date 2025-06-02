# Algoritma Penjadwalan CPU (CPU Scheduling Algorithms)

| Nama Algoritma & Emoji | Konsep Dasar | Cara Kerja | Sifat | Karakteristik Utama | Kelebihan | Kekurangan |
|------------------------|--------------|------------|-------|-------------------|-----------|------------|
| **FCFS** 🚶‍♂️➡️🚶‍♀️<br>*(First-Come, First-Served)* | Proses yang pertama datang, akan dilayani pertama. | Menggunakan antrian FIFO (First-In, First-Out). Proses dieksekusi hingga selesai atau melakukan I/O. | **Non-Preemptive** | Sederhana, mudah diimplementasikan. | • Sangat sederhana dan intuitif<br>• Adil dalam artian "siapa datang lebih awal, dilayani lebih awal" | • Waktu tunggu rata-rata bisa sangat tinggi<br>• Convoy effect: proses pendek menunggu proses panjang<br>• Tidak cocok untuk sistem time-sharing |
| **SJF** 📏➡️🥇<br>*(Shortest Job First)* | Proses dengan estimasi burst time (waktu eksekusi) terpendek dieksekusi dulu. | Scheduler memilih proses dengan burst time terkecil. | **Non-Preemptive** atau **Preemptive** (SRTF) | Optimal dalam meminimalkan waktu tunggu rata-rata. | • Menghasilkan waktu tunggu dan turnaround time rata-rata minimal | • Sulit memprediksi burst time secara akurat<br>• Risiko starvation untuk proses panjang jika selalu ada proses pendek baru |
| **Priority Scheduling** ⭐👑<br>*(Penjadwalan Prioritas)* | Proses dengan prioritas tertinggi dieksekusi terlebih dahulu. | Setiap proses memiliki prioritas; scheduler memilih proses berprioritas tertinggi. Prioritas bisa statis atau dinamis. | **Non-Preemptive** atau **Preemptive** | Memungkinkan eksekusi proses penting lebih dulu. | • Proses-proses kritis atau penting dapat diselesaikan lebih cepat | • Risiko starvation untuk proses berprioritas rendah<br>• Solusi starvation: aging (meningkatkan prioritas proses yang menunggu lama) |
| **Round Robin (RR)** 🔄⏱️ | Setiap proses mendapat jatah waktu CPU (time quantum) yang sama secara bergantian. | Proses dieksekusi selama satu time quantum. Jika belum selesai, pindah ke akhir antrian FCFS. | **Preemptive** | Dirancang untuk sistem time-sharing, responsif. | • Adil, setiap proses mendapat giliran<br>• Responsif untuk pengguna interaktif | • Kinerja bergantung pada ukuran time quantum (terlalu kecil = banyak overhead; terlalu besar = mirip FCFS)<br>• Waktu tunggu rata-rata bisa lebih buruk dari SJF |
| **Multilevel Queue** 🚦🚦🚦<br>*(Antrian Bertingkat)* | Ready queue dibagi jadi beberapa antrian terpisah, masing-masing dengan algoritma & prioritas sendiri. | Proses dimasukkan permanen ke satu antrian berdasarkan tipenya (misal, interaktif vs batch). Penjadwalan antar antrian bisa fixed priority atau time slice. | **Bisa keduanya** | Fleksibel, perlakuan beda untuk jenis proses beda. | • Dapat disesuaikan untuk kebutuhan spesifik sistem | • Kurang fleksibel karena proses tidak bisa pindah antrian<br>• Potensi starvation pada antrian prioritas rendah |
| **Multilevel Feedback Queue** 🚦🔄🚦⬆️⬇️<br>*(Antrian Bertingkat dengan Umpan Balik)* | Seperti Multilevel Queue, tapi proses bisa berpindah antar antrian. | Proses bisa naik/turun antrian berdasarkan perilakunya (misal, penggunaan CPU, waktu tunggu). Antrian atas biasanya untuk I/O-bound (quantum kecil), bawah untuk CPU-bound (quantum besar). | **Preemptive** | Sangat fleksibel dan adaptif, dapat mencegah starvation dan meningkatkan responsivitas. | • Paling adaptif dan dapat dikonfigurasi<br>• Mencegah starvation jika dirancang baik (aging)<br>• Responsif dan throughput baik | • Paling kompleks untuk dirancang dan diimplementasikan<br>• Butuh konfigurasi banyak parameter (jumlah antrian, algoritma per antrian, aturan pindah) |

---

## Catatan Tambahan

### Definisi Istilah:
- **Preemptive**: Sistem operasi dapat menginterupsi proses yang sedang berjalan
- **Non-Preemptive**: Proses berjalan hingga selesai atau melakukan I/O secara sukarela
- **Burst Time**: Waktu yang dibutuhkan proses untuk menggunakan CPU
- **Time Quantum**: Jatah waktu CPU yang diberikan kepada setiap proses dalam Round Robin
- **Starvation**: Kondisi dimana proses tidak pernah mendapat kesempatan dieksekusi
- **Aging**: Teknik meningkatkan prioritas proses yang menunggu lama

### Pemilihan Algoritma:
- **FCFS**: Cocok untuk sistem batch sederhana
- **SJF**: Optimal untuk meminimalkan waktu tunggu rata-rata
- **Priority**: Untuk sistem dengan proses berkritikalitas berbeda
- **Round Robin**: Ideal untuk sistem time-sharing dan interaktif
- **Multilevel Queue**: Untuk sistem dengan jenis proses yang jelas berbeda
- **Multilevel Feedback Queue**: Untuk sistem kompleks yang membutuhkan adaptabilitas tinggi

### LATIHAN
![Image](https://github.com/user-attachments/assets/3ca0d8e8-13da-4bf1-a700-ae8ebb28bd40)

📝 Data Proses
Berikut adalah data proses yang akan digunakan untuk analisis:
Proses IDPrioritasWaktu Tiba (AT)Burst Time (BT) P1 🔵30 ms11 msP2 🟢23 ms8 msP3 🟡35 ms10 msP4 🔴17 ms5 msP5 🟣212 ms10 ms

📌 Catatan: Quantum Waktu untuk Round Robin (QT) = 3 ms


🚶‍♂️➡️🚶‍♀️ Algoritma FCFS (First-Come, First-Served)
🎯 Karakteristik

Prinsip: Siapa datang pertama, dilayani pertama
Urutan Eksekusi: P1 → P2 → P3 → P4 → P5

📊 Gantt Chart FCFS
┌─────────┬────────┬─────────┬────────┬─────────┐
│ P1 (11) │ P2 (8) │ P3 (10) │ P4 (5) │ P5 (10) │
└─────────┴────────┴─────────┴────────┴─────────┘
0        11       19        29       34        44
📈 Perhitungan Waktu
ProsesATBTCTTAT (CT-AT)WT (TAT-BT)P1 🔵01111110P2 🟢3819168P3 🟡510292414P4 🔴75342722P5 🟣1210443222Rata-rata ⭐---22.0 ms13.2 ms

📏➡️🥇 Algoritma SJF (Shortest Job First) Non-Preemptive
🎯 Karakteristik

Prinsip: Proses dengan burst time terpendek dieksekusi lebih dulu
Urutan Eksekusi: P1 → P4 → P2 → P3 → P5

📊 Gantt Chart SJF
┌─────────┬────────┬────────┬─────────┬─────────┐
│ P1 (11) │ P4 (5) │ P2 (8) │ P3 (10) │ P5 (10) │
└─────────┴────────┴────────┴─────────┴─────────┘
0        11       16       24        34        44
📈 Perhitungan Waktu
ProsesATBTCTTAT (CT-AT)WT (TAT-BT)P1 🔵01111110P4 🔴751694P2 🟢38242113P3 🟡510342919P5 🟣1210443222Rata-rata ⭐---20.4 ms11.6 ms

🔄⏱️ Algoritma Round Robin (RR) dengan QT = 3 ms
🎯 Karakteristik

Prinsip: Setiap proses mendapat jatah waktu yang sama secara bergiliran
Urutan Eksekusi: P1, P2, P3, P4, P5, P1, P2, P3, P4✅, P5, P1, P2✅, P3, P5, P1✅, P3✅, P5✅

📊 Gantt Chart RR (QT=3)
┌────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┬────┐
│P1(3)│P2(3)│P3(3)│P4(3)│P5(3)│P1(3)│P2(3)│P3(3)│P4(2)│P5(3)│P1(3)│P2(2)│P3(3)│P5(3)│P1(2)│P3(1)│P5(1)│
└────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┴────┘
0    3    6    9   12   15   18   21   24   26   29   32   34   37   40   42   43   44

💡 Keterangan: Angka dalam kurung menunjukkan durasi eksekusi pada setiap slot waktu

⏰ Waktu Selesai (CT)

P1 🔵: 42 ms
P2 🟢: 34 ms
P3 🟡: 43 ms
P4 🔴: 26 ms
P5 🟣: 44 ms

📈 Perhitungan Waktu
ProsesATBTCTTAT (CT-AT)WT (TAT-BT)P1 🔵011424231P2 🟢38343123P3 🟡510433828P4 🔴75261914P5 🟣1210443222Rata-rata ⭐---32.4 ms23.6 ms

🏆 Perbandingan & Rekomendasi Algoritma
📊 Ringkasan Performa
AlgoritmaRata-rata TATRata-rata WTRankingSJF Non-Preemptive 🥇20.4 ms11.6 ms1️⃣FCFS 🥈22.0 ms13.2 ms2️⃣Round Robin (QT=3) 🥉32.4 ms23.6 ms3️⃣
🎯 Kesimpulan

✨ Rekomendasi: Algoritma SJF (Shortest Job First) Non-Preemptive memberikan performa terbaik dengan rata-rata waktu tunggu tersingkat sebesar 11.6 ms untuk kumpulan proses ini.

💡 Analisis Mendalam

🏃‍♂️ SJF: Optimal untuk meminimalkan waktu tunggu rata-rata
🚶‍♂️ FCFS: Sederhana namun dapat menyebabkan convoy effect
🔄 Round Robin: Adil dan responsif, cocok untuk sistem time-sharing meski waktu tunggu lebih tinggi
