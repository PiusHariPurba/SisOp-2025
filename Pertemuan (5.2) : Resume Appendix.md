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

```markdown
# Evolusi Komputer

Salah satu alasan untuk mempelajari arsitektur dan sistem operasi awal adalah bahwa fitur yang tadinya hanya dijalankan pada sistem besar pada akhirnya dapat diterapkan pada sistem yang sangat kecil. Memang benar, pengujian sistem operasi untuk mainframe dan mikrokomputer menunjukkan bahwa banyak fitur yang tadinya hanya tersedia pada mainframe telah diadopsi untuk mikrokomputer. Oleh karena itu, konsep sistem operasi yang sama sesuai untuk berbagai kelas komputer: mainframe, komputer mini, mikrokomputer, dan perangkat genggam. Untuk memahami sistem operasi modern, Anda perlu mengenali tema migrasi fitur dan sejarah panjang banyak fitur sistem operasi. Berikut sketsa perkembangan komputer dari tahun ke tahun.

## Awal mulanya

Komputer-komputer sebelum era Atlas (1940-an dan 1950-an) hanyalah mesin raksasa yang menggunakan tabung vakum, menghasilkan panas tinggi, dan memiliki keandalan rendah. Input dan output data bergantung pada media fisik seperti kartu pons atau pita kertas, tanpa adanya monitor atau keyboard interaktif. Pemrograman dilakukan langsung dalam bahasa mesin atau bahasa rakitan yang rumit, spesifik untuk tiap komputer, dan setiap program dijalankan satu per satu (secara batch) karena belum ada sistem operasi canggih yang mengatur sumber daya.

Karena keterbatasan kecepatan proses, kapasitas memori yang sangat kecil, dan biaya operasional tinggi, komputer awal ini hanya digunakan untuk tugas-tugas kalkulasi intensif seperti perhitungan ilmiah, militer, atau sensus. Pengoperasiannya tidak interaktif; pengguna menyerahkan pekerjaan dan menunggu hasilnya tanpa bisa berinteraksi langsung selama proses komputasi berlangsung. Era ini menandai fondasi awal komputasi, namun sangat berbeda jauh dari efisiensi dan kemudahan penggunaan yang mulai diperkenalkan oleh sistem-sistem selanjutnya.

## Atlas

Bisa dikatakan bahwa Atlas Computer dari University of Manchester pada tahun 1960-an (khususnya 1962) memainkan peran revolusioner yang sangat signifikan dalam pengembangan dan pengelolaan memori komputer, meskipun bukan satu-satunya "revolusi" dalam sejarah memori.

Inovasi terbesar dari proyek Atlas yang terkait dengan memori adalah penemuan Memori Virtual (Virtual Memory), yang pada saat itu disebut "one-level storage" atau penyimpanan satu tingkat. Sebelum Atlas: Programer harus secara manual mengatur transfer data antara memori utama yang kecil dan cepat (misalnya, core memory) dengan penyimpanan sekunder yang lebih besar dan lambat (misalnya, magnetic drum atau disk). Ini adalah tugas yang sangat rumit dan rawan kesalahan, serta membutuhkan rekompilasi program setiap kali ukuran memori utama berubah.

Inovasi Atlas dengan Memori Virtual: Atlas mengotomatiskan proses transfer data ini. Ia memberikan ilusi kepada setiap pengguna bahwa mereka memiliki akses ke memori yang sangat besar dan cepat, padahal kenyataannya data secara otomatis dipindahkan antara memori utama yang lebih kecil dan magnetic drum yang lebih besar (dan lebih lambat) sesuai kebutuhan. Ini dilakukan melalui teknik paging, di mana memori dibagi menjadi halaman-halaman kecil yang dapat dipindahkan antara memori fisik dan penyimpanan sekunder.

### Mengapa ini Revolusioner?

- **Menyederhanakan Pemrograman**: Programer tidak perlu lagi khawatir tentang manajemen memori secara manual. Mereka bisa menulis program seolah-olah ada memori yang tak terbatas.
- **Memungkinkan Multiprogramming yang Efisien**: Memori virtual adalah kunci untuk memungkinkan banyak program berjalan secara bersamaan di satu komputer (konkurensi), bahkan jika total memori yang dibutuhkan program-program tersebut melebihi kapasitas memori fisik yang tersedia.
- **Fondasi Sistem Operasi Modern**: Konsep memori virtual yang dipelopori oleh Atlas ini menjadi fitur standar yang sangat penting di hampir semua sistem operasi modern (Windows, Linux, macOS) dan perangkat komputasi, dari server hingga smartphone.

Meskipun teknologi memori fisik (seperti transisi dari magnetic core ke semikonduktor DRAM) juga mengalami revolusi pada periode yang sama dan setelahnya, inovasi memori virtual yang dibawa oleh Atlas adalah revolusi dalam cara memori dikelola dan digunakan, yang secara fundamental mengubah arsitektur sistem operasi dan pemrograman.

## XDS-940

XDS-940 dikembangkan oleh Berkeley Computer Corporation (BCC), sebuah spin-off dari Project Genie di University of California, Berkeley, dan dirilis sekitar tahun 1966. Sistem operasi ini secara spesifik dirancang untuk komputer SDS 940 (kemudian menjadi XDS 940 setelah Xerox mengakuisisi Scientific Data Systems). Butler Lampson adalah salah satu tokoh kunci dalam pengembangannya, yang melanjutkan pekerjaannya dari sistem Berkeley Timesharing System pada SDS 930.

Keunggulan utama XDS-940 adalah kemampuannya sebagai sistem time-sharing yang relatif canggih untuk masanya, memungkinkan banyak pengguna untuk berinteraksi dengan komputer secara bersamaan melalui terminal. Dibandingkan pendahulunya seperti CTSS (Compatible Time-Sharing System), XDS-940 menawarkan fitur-fitur yang lebih terintegrasi dan dirancang dari awal untuk time-sharing pada perangkat keras yang lebih modern saat itu. Sistem ini juga mendukung bahasa pemrograman seperti FORTRAN, LISP, dan SNOBOL.

Meskipun inovatif, XDS-940 memiliki keterbatasan dalam hal skalabilitas dan kompleksitas pengelolaan sumber daya dibandingkan dengan sistem time-sharing generasi berikutnya seperti Multics. Ketergantungan pada perangkat keras spesifik juga menjadi batasan. Pengaruhnya terlihat pada pengembangan sistem operasi selanjutnya, terutama dalam konsep time-sharing dan interaksi pengguna, namun ia akhirnya digantikan oleh sistem yang lebih portabel dan mampu menangani sumber daya yang lebih besar dan beragam.

## THE (Technische Hogeschool Eindhoven)

Sistem Operasi THE (dinamai berdasarkan almamater penciptanya, Technische Hogeschool Eindhoven, sekarang Eindhoven University of Technology) dikembangkan oleh sebuah tim yang dipimpin oleh Edsger W. Dijkstra pada pertengahan 1960-an, sekitar tahun 1965-1966. Sistem ini dirancang untuk komputer Electrologica X8 dan menjadi sangat terkenal karena struktur berlapisnya (layered structure) yang hierarkis, sebuah konsep desain perangkat lunak yang revolusioner pada masanya.

Keunggulan utama THE adalah desainnya yang sangat modular dan terstruktur. Dijkstra menggunakan konsep lapisan abstraksi, di mana setiap lapisan hanya bergantung pada lapisan di bawahnya, memudahkan verifikasi kebenaran sistem dan pengujian. Ini merupakan peningkatan signifikan dari sistem monolitik yang umum saat itu, di mana bug di satu bagian dapat dengan mudah merusak bagian lain. THE juga memperkenalkan penggunaan semafor untuk sinkronisasi proses, sebuah kontribusi penting dalam komputasi konkuren.

Namun, THE lebih merupakan proyek penelitian daripada produk komersial yang luas. Performanya mungkin tidak seoptimal sistem yang dirancang khusus untuk kecepatan, karena adanya overhead dari struktur berlapis dan fokus pada kebenaran formal. Sistem operasi selanjutnya, meskipun tidak selalu mengadopsi struktur berlapis yang ketat seperti THE, banyak dipengaruhi oleh ide-ide Dijkstra mengenai desain terstruktur, modularitas, dan manajemen proses konkuren, yang menjadi dasar bagi pengembangan sistem operasi modern.

## RC 4000 Multiprogramming System (RC 4000)

Sistem operasi RC 4000 Multiprogramming System dikembangkan oleh Per Brinch Hansen dan timnya di Regnecentralen, Denmark, pada akhir tahun 1960-an, dengan publikasi penting sekitar tahun 1969. Sistem ini dirancang untuk komputer RC 4000 dan terkenal karena konsep inti (kernel atau nucleus) kecil yang menyediakan mekanisme komunikasi antar-proses (Inter-Process Communication - IPC) dasar.

Keunggulan utama RC 4000 adalah filosofi desainnya yang menekankan pada kernel minimalis. Kernel hanya menyediakan layanan paling esensial seperti penjadwalan proses, IPC, dan manajemen memori dasar. Layanan sistem operasi yang lebih kompleks (seperti sistem berkas) diimplementasikan sebagai proses-proses pengguna yang berjalan di atas kernel dan berkomunikasi melalui mekanisme IPC. Pendekatan ini menghasilkan sistem yang fleksibel, modular, dan lebih mudah untuk dimodifikasi serta di-debug dibandingkan sistem monolitik besar. Ini adalah perbedaan signifikan dari sistem seperti OS/360 yang memiliki kernel besar dan kompleks.

Meskipun sangat berpengaruh secara konseptual, RC 4000 sendiri tidak meraih penggunaan komersial yang luas seperti beberapa sistem kontemporernya. Tantangannya mungkin termasuk performa IPC yang bisa menjadi bottleneck dan kompleksitas dalam merancang layanan sistem operasi sebagai proses terpisah secara efisien. Namun, ide microkernel dan komunikasi berbasis pesan dari RC 4000 sangat memengaruhi desain sistem operasi selanjutnya, termasuk sistem seperti Amoeba dan kemudian menjadi dasar bagi arsitektur microkernel modern yang terlihat pada QNX atau Minix, yang pada gilirannya memengaruhi Linux.

## CTSS (Compatible Time-Sharing System)

CTSS (Compatible Time-Sharing System) dikembangkan di MIT Computation Center di bawah pimpinan Fernando J. Corbató. Proyek ini dimulai pada tahun 1961 dan menjadi operasional pada tahun yang sama di komputer IBM 709, kemudian ditingkatkan untuk IBM 7090/7094. CTSS adalah salah satu sistem operasi time-sharing pertama dan sangat berpengaruh.

Keunggulan utama CTSS adalah demonstrasi kelayakan konsep time-sharing, yang memungkinkan banyak pengguna mengakses satu komputer secara simultan seolah-olah masing-masing memiliki kontrol eksklusif. Ini merupakan lompatan besar dari sistem batch processing sebelumnya yang mengharuskan pengguna menunggu giliran. CTSS memperkenalkan banyak konsep dasar time-sharing seperti penjadwalan round-robin, manajemen memori untuk banyak pengguna, dan sistem berkas yang mendukung pengguna individu. Sistem ini juga menjadi platform untuk pengembangan awal email dan pengolah kata.

Namun, sebagai sistem perintis, CTSS memiliki beberapa kekurangan. Sistem ini relatif sederhana dalam manajemen sumber daya dan proteksi dibandingkan sistem time-sharing yang lebih canggih sesudahnya. Skalabilitasnya terbatas, dan antarmukanya masih berbasis teks dan perintah baris yang mungkin kurang intuitif. Pengalaman dan pelajaran dari CTSS, baik kelebihan maupun kekurangannya, secara langsung mengarah pada pengembangan sistem yang jauh lebih ambisius dan kompleks, yaitu Multics.

## MULTICS (Multiplexed Information and Computing Service)

MULTICS adalah proyek sistem operasi time-sharing yang sangat berpengaruh, dimulai pada tahun 1964 sebagai upaya kolaboratif antara MIT (dipimpin oleh Fernando J. Corbató), General Electric (kemudian Honeywell), dan Bell Labs. Meskipun Bell Labs menarik diri pada tahun 1969, proyek ini terus berlanjut dan sistem pertama dioperasikan pada tahun 1969.

Keunggulan utama Multics adalah ambisinya untuk menjadi utilitas komputasi, menyediakan layanan komputasi yang andal dan aman untuk banyak pengguna secara bersamaan. Sistem ini memperkenalkan banyak inovasi yang kini menjadi standar, seperti memori tersegmentasi dan paging dinamis, sistem berkas hierarkis, proteksi keamanan berlapis, dan penulisan sebagian besar sistem dalam bahasa tingkat tinggi (PL/I). Dibandingkan CTSS, Multics jauh lebih canggih dalam hal keamanan, manajemen sumber daya, dan konsep rekayasa perangkat lunak.

Namun, ambisi besar Multics juga menjadi salah satu kelemahannya. Proyek ini sangat kompleks, memakan waktu lama untuk dikembangkan, dan awalnya memiliki performa yang kurang memuaskan serta membutuhkan sumber daya perangkat keras yang besar dan mahal. Meskipun tidak pernah mencapai penyebaran komersial yang luas seperti yang diharapkan, ide-ide fundamental dari Multics memiliki dampak besar. Ken Thompson dan Dennis Ritchie, yang bekerja pada Multics di Bell Labs, kemudian mengembangkan Unix, yang mewarisi banyak konsep Multics tetapi dengan implementasi yang lebih sederhana dan pragmatis.

## IBM System/360 Operating Systems (misalnya OS/360)

Sistem operasi untuk keluarga komputer IBM System/360 diperkenalkan mulai pertengahan 1960-an, dengan OS/360 menjadi yang paling signifikan, dirilis secara bertahap mulai tahun 1966. IBM sendiri adalah pengembang utama sistem operasi ini, yang dirancang untuk menyediakan satu sistem operasi yang kompatibel di seluruh lini produk System/360 yang beragam.

Keunggulan utama OS/360 dan sistem operasi terkait adalah konsep keluarga sistem operasi yang dapat diskalakan untuk berbagai model komputer dengan kemampuan berbeda, dari kecil hingga besar. Ini adalah perubahan besar dari pendekatan sebelumnya di mana setiap model komputer seringkali memiliki sistem operasi uniknya sendiri. OS/360 memperkenalkan konsep seperti Job Control Language (JCL) yang canggih, berbagai metode akses data, dan dukungan untuk multiprogramming (menjalankan beberapa tugas secara bersamaan), yang meningkatkan utilisasi CPU secara signifikan dibandingkan sistem batch sederhana sebelumnya.

Namun, kompleksitas OS/360 menjadi tantangan besar. Sistem ini sangat besar, terdiri dari jutaan baris kode assembly, dan terkenal sulit untuk diinstal, dikelola, dan di-debug. Ukurannya yang besar juga berarti membutuhkan sumber daya memori dan penyimpanan yang signifikan. Meskipun demikian, dominasi IBM di pasar mainframe memastikan penyebaran luas OS/360 dan turunannya (seperti MVS, z/OS), yang terus berevolusi dan masih digunakan hingga saat ini dalam lingkungan mainframe, menunjukkan warisan panjang dari arsitektur dan konsep awalnya.

## TOPS-20 (Timesharing OPerating System-20)

TOPS-20 dikembangkan oleh Digital Equipment Corporation (DEC) untuk keluarga komputer mainframe PDP-10 (kemudian DECSYSTEM-20) pada pertengahan hingga akhir 1970-an, dengan rilis awal sekitar tahun 1976. Sistem ini merupakan evolusi dari TOPS-10, dengan pengaruh signifikan dari sistem Tenex yang dikembangkan oleh Bolt, Beranek and Newman (BBN).

Keunggulan utama TOPS-20 adalah antarmuka pengguna yang dianggap sangat ramah dan kuat untuk masanya, serta fitur time-sharing yang canggih. Sistem ini dikenal karena kemudahan penggunaannya, perintah baris yang intuitif dengan fitur seperti penyelesaian nama berkas otomatis dan bantuan daring (online help). TOPS-20 juga menawarkan manajemen memori virtual yang canggih (berdasarkan teknologi paging dari Tenex), sistem berkas yang baik, dan lingkungan pengembangan yang kaya, menjadikannya populer di universitas dan lembaga penelitian. Dibandingkan pendahulunya seperti TOPS-10, ia menawarkan pengalaman pengguna yang lebih modern dan fitur yang lebih lengkap.

Meskipun sangat disukai oleh penggunanya, TOPS-20 berjalan pada arsitektur PDP-10/DECSYSTEM-20 yang pada akhirnya produksinya dihentikan oleh DEC pada awal 1980-an demi fokus pada arsitektur VAX dengan sistem operasi VMS. Keterikatan pada platform perangkat keras spesifik ini menjadi batasan utamanya. Namun, banyak konsep antarmuka pengguna dan fitur time-sharing dari TOPS-20 memengaruhi desain sistem operasi selanjutnya, dan komunitas penggunanya yang loyal sering mengenangnya sebagai salah satu sistem operasi terbaik pada masanya.

## CP/M & MS-DOS

CP/M (Control Program for Microcomputers) dikembangkan oleh Gary Kildall dari Digital Research, Inc. (DRI) dan pertama kali dirilis pada tahun 1974. MS-DOS (Microsoft Disk Operating System) awalnya dikembangkan oleh Seattle Computer Products sebagai QDOS (Quick and Dirty Operating System) oleh Tim Paterson pada tahun 1980, yang kemudian dibeli dan dimodifikasi oleh Microsoft untuk IBM PC dan dirilis pada tahun 1981.

Keunggulan utama CP/M adalah menjadi sistem operasi standar pertama untuk mikrokomputer berbasis prosesor Intel 8080 dan Zilog Z80, menciptakan pasar perangkat lunak pihak ketiga yang masif. MS-DOS, yang sangat dipengaruhi oleh CP/M dalam hal konsep dan antarmuka baris perintah, memiliki keunggulan karena dipilih oleh IBM untuk personal computer (PC) mereka. Hal ini memberikan MS-DOS keunggulan pasar yang luar biasa, menjadikannya standar de facto untuk PC selama bertahun-tahun. Keduanya relatif sederhana, membutuhkan sumber daya minimal, dan menyediakan fungsi dasar untuk manajemen berkas dan eksekusi program, yang merupakan peningkatan besar dibandingkan tidak adanya sistem operasi standar sebelumnya untuk mikrokomputer.

Kekurangan CP/M termasuk arsitektur 8-bit yang terbatas dalam manajemen memori (maksimal 64KB RAM). MS-DOS, meskipun 16-bit, awalnya juga memiliki batasan memori 640KB, tidak mendukung multitasking atau memori terproteksi secara inheren, dan memiliki antarmuka baris perintah yang kurang ramah pengguna bagi pemula. Sistem operasi grafis selanjutnya seperti Windows dan Mac OS menawarkan antarmuka yang jauh lebih intuitif dan kemampuan multitasking yang sebenarnya, yang akhirnya menggantikan dominasi MS-DOS di pasar desktop.

## Sistem Operasi Macintosh (Classic Mac OS & macOS) & Windows

Sistem Operasi Macintosh (awalnya hanya disebut System Software, kemudian Mac OS, dan sekarang macOS) pertama kali diperkenalkan oleh Apple Inc. pada tahun 1984 bersama dengan komputer Macintosh pertama. Windows dikembangkan oleh Microsoft, dengan versi pertama (Windows 1.0) dirilis pada tahun 1985 sebagai lingkungan operasi grafis yang berjalan di atas MS-DOS. Keduanya terinspirasi oleh antarmuka pengguna grafis (GUI) yang dikembangkan di Xerox PARC.

Keunggulan utama Macintosh OS adalah integrasi erat antara perangkat keras dan perangkat lunak, serta antarmuka pengguna grafis (GUI) yang revolusioner pada masanya, memperkenalkan konsep seperti desktop, jendela, ikon, menu, dan penggunaan mouse secara luas. Ini membuatnya jauh lebih mudah digunakan dibandingkan sistem berbasis baris perintah. Windows, meskipun awalnya kurang canggih dibandingkan Mac OS, memiliki keunggulan karena berjalan di berbagai perangkat keras PC dari banyak vendor, memberikannya pangsa pasar yang lebih besar. Keduanya membawa komputasi ke audiens yang lebih luas.

Kelemahan awal Mac OS termasuk biaya perangkat keras Apple yang relatif mahal dan kurangnya multitasking preemptive pada versi-versi awal. Windows versi awal (sebelum Windows 95 dan NT) sangat bergantung pada MS-DOS, kurang stabil, dan memiliki kemampuan multitasking yang terbatas. Sistem operasi selanjutnya dari kedua lini produk ini (macOS dan Windows modern) telah mengatasi banyak keterbatasan awal, mengadopsi arsitektur yang lebih kuat (berbasis Unix untuk macOS, kernel NT untuk Windows), multitasking preemptive, manajemen memori yang canggih, dan fitur keamanan yang jauh lebih baik, sambil terus bersaing dalam hal inovasi antarmuka dan fungsionalitas.

## Mach

Mach adalah sebuah kernel sistem operasi yang dikembangkan di Carnegie Mellon University (CMU) mulai tahun 1985 oleh sebuah tim yang dipimpin oleh Richard Rashid dan Avie Tevanian.Tujuannya adalah untuk menciptakan kernel yang sangat fleksibel dan dapat diperluas, mendukung penelitian dalam komputasi paralel dan terdistribusi, serta menyediakan kompatibilitas biner dengan Unix.
Keunggulan utama Mach adalah desain microkernel-nya. Berbeda dengan kernel monolitik tradisional (seperti Unix klasik), microkernel Mach hanya menyediakan fungsionalitas inti minimal seperti manajemen tugas dan utas, komunikasi antar-proses (IPC), dan manajemen memori virtual. Layanan sistem operasi tingkat tinggi lainnya (seperti sistem berkas, jaringan, dan bahkan antarmuka sistem operasi Unix) diimplementasikan sebagai server-server yang berjalan di ruang pengguna. Ini memungkinkan fleksibilitas, portabilitas, dan potensi keamanan yang lebih baik, karena komponen sistem dapat dimodifikasi atau diganti tanpa memengaruhi kernel inti.
Meskipun konsep microkernel sangat menarik, implementasi awal Mach menghadapi tantangan performa, terutama karena overhead komunikasi antar-proses antara server-server di ruang pengguna dan kernel. Namun, Mach sangat berpengaruh. Banyak sistem operasi komersial dan penelitian mengadopsi Mach atau konsepnya. Contoh paling terkenal adalah NeXTSTEP, yang kemudian menjadi dasar bagi macOS dan iOS Apple. Kernel XNU pada sistem operasi Apple modern masih mengandung komponen dari Mach.
## HYDRA & Cambridge CAP Computer

Hydra adalah sistem operasi berbasis kapabilitas (capability-based) yang dikembangkan di Carnegie Mellon University pada awal hingga pertengahan 1970-an (sekitar 1971-1975) untuk komputer C.mmp, sebuah sistem multiprosesor. Cambridge CAP Computer dan sistem operasinya juga merupakan proyek berbasis kapabilitas yang signifikan, dikembangkan di University of Cambridge Computer Laboratory, Inggris, pada periode yang sama, dengan komputer operasional pada tahun 1976.

Keunggulan utama dari kedua sistem ini adalah implementasi konsep keamanan berbasis kapabilitas. Dalam sistem ini, hak akses ke objek (seperti berkas atau segmen memori) dikontrol oleh token yang tidak dapat dipalsukan yang disebut kapabilitas, yang diberikan kepada proses. Ini memungkinkan kontrol akses yang sangat halus dan terstruktur, yang secara teoretis lebih aman daripada daftar kontrol akses (ACL) tradisional. Hydra secara khusus dirancang untuk mendukung multiprosesor dan eksperimen dalam sistem operasi terdistribusi. CAP Computer fokus pada integrasi perangkat keras dan perangkat lunak untuk mendukung kapabilitas secara efisien.

Namun, sistem berbasis kapabilitas murni seperti Hydra dan CAP terbukti kompleks untuk diimplementasikan secara efisien pada perangkat keras umum saat itu, dan model pemrograman yang dibutuhkan bisa jadi lebih rumit bagi pengembang. Performa juga bisa menjadi isu karena overhead manajemen kapabilitas. Meskipun tidak banyak sistem operasi komersial yang sepenuhnya mengadopsi model kapabilitas murni, ide-ide dari Hydra dan CAP memengaruhi penelitian dalam keamanan sistem operasi dan arsitektur komputer, dan beberapa konsepnya muncul kembali dalam sistem modern dalam bentuk yang dimodifikasi.

## Another System (Contoh: Unix)

Karena "Another System" bersifat generik, kita akan mengambil Unix sebagai contoh sistem operasi penting lainnya yang belum dibahas secara mendalam namun sangat berpengaruh. Unix dikembangkan di Bell Labs oleh Ken Thompson, Dennis Ritchie, dan lainnya, dimulai pada tahun 1969. Awalnya ditulis dalam bahasa assembly, kemudian sebagian besar ditulis ulang dalam bahasa C, sebuah inovasi besar pada masanya.

Keunggulan utama Unix adalah portabilitasnya (karena ditulis dalam C), sistem berkas hierarkis yang elegan, antarmuka baris perintah (shell) yang kuat dengan konsep piping dan pengalihan, serta filosofi desain yang menekankan pada program-program kecil yang melakukan satu hal dengan baik dan dapat digabungkan. Ini membuatnya sangat populer di lingkungan akademis dan penelitian, dan kemudian menjadi dasar bagi banyak varian komersial (seperti Solaris, HP-UX, AIX) dan sistem operasi modern seperti Linux dan macOS (yang kernelnya, XNU, memiliki komponen BSD Unix). Dibandingkan sistem monolitik besar sebelumnya, Unix menawarkan kesederhanaan dan fleksibilitas yang lebih besar.

Kekurangan awal Unix termasuk kurangnya antarmuka pengguna grafis yang standar (meskipun X Window System kemudian mengisi kekosongan ini) dan variasi antar implementasi (masalah "Unix wars"). Meskipun sangat kuat, baris perintahnya bisa menakutkan bagi pengguna awam. Namun, pengaruhnya sangat besar; banyak konsep dan alat Unix menjadi standar de facto dalam komputasi. Sistem operasi modern seperti Linux telah mengambil filosofi Unix dan membawanya ke berbagai platform, dari server hingga perangkat seluler, menunjukkan daya tahan dan adaptabilitas ide-ide inti Unix.
