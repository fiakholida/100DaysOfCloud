# CLOUD COMPUTING - AWS Cloud Foundationn Chapter 7 [Pemateri: Tiara Dwi Maulita Sari]
# Chapter 7 - Storage
## Introduction
- Amazon Elastic Block Store (Amazon EBS)
- Amazon Simple Storage Service (Amazon S3)
- Amazon Elastic File System (Amazon EFS)
- Amazon Simple Storage Service Glacier
## Amazon Elastic Block Store (Amazon EBS)
  Amazon EBS memberikan volume penyimpanan tingkat blok yang persisten untuk digunakan dengan Amazon EC2 instance. Penyimpanan persisten adalah perangkat penyimpanan data yang menyimpan data setelah daya ke perangkat dimatikan. Terkadang, ini juga disebut penyimpanan non-volatile.
  Amazon EBS memungkinkan membuat volume penyimpanan individu dan melampirkannya ke Amazon EC2 instance:
  - Amazon EBS menawarkan penyimpanan tingkat blok
  - Volume direplikasi secara otomatis dalam Availabilty Zone
  - Hal ini dapat dicadangkan secara otomatis ke Amazon S3 melalui snapshot cadangan
  - Penggunaan vlume Amazon EBS mencakup:
    - Volume boot dan penyimpanan untuk instans Amazon EC2
    - Penyimpanan data dengan sistem file
    - Host basis data
    - Aplikasi korporasi
### Fitur Amazon EBS
- Snapshot
  - Snapshot waktu tertentu
  - Membuat ulang volume baru kapan saja
- Enkripsi
  - Volume Amazon EBS terenkripsi
  - tanpa biaya tambahan
- Elastisitas
  - Meningkatkan kapasitas
  - Mengubah ke tipe yang berbeda
### Amazon EBS: Volume, IOPS, dan harga
1. Volume
   - Volume Amazon EBS bertahan secara independen dari instans
   - Semua jenis volume dikenakan biaya dengan jumlah yang disediakan per bulan
2. IOPS
   - SSD Tujuan Umum
     - Dikenakan biaya sejumlah yang disediakan alam GB per bulan hiingga penyimpanan dileaskan
   - Magnetik
     - Dikenakan biaya sejumlah permintaan ke volume
   - SSD Provisioned IOPS
     - DIkenakan biaya sejumlah yang disediakan di IOPS (dikalikan dengan persentase hari yang disediakan untuk bulan tersebut)
       Harga dan penyediaan Amazon EBS rumit. Secara umum, Anda membayar untuk ukuran volume dan penggunaannya.
### Amazon EBS: Snapshot dan transfer data
3. Snapshot
   - Biaya tambahan snapshot Amazon EBS ke Amazon S3 adalah per Gb-bulan dari data yang disimpan
4. Transfer data
   - Transfer data masuk gratis
   - Transfer data keluar di seluruh Wilayah terkena biaya
     
## Amazon Simple Storage Service (Amazon S3)
  Amazon S3 adalah penyimpanan tingkat objek, yang artinya jika Anda ingin mengubah satu bagian file, Anda harus melakukan perubahan lalu mengunggah ulang seluruh file yang diubah. Amazon S3 menyimpan data sebagai objek dalam sumber daya yang dikenal sebagai bucket.
  Data yang Anda simpan di Amazon S3 tidak terkait dengan server tertentu, dan Anda tidak perlu mengelola infrastruktur sendiri. Anda dapat menempatkan objek ke Amazon S3 sebanyak yang Anda inginkan. Amazon S3 menyimpan triliunan objek dan secara teratur mencapai jutaan permintaan per detik.
  Amazon S3 menawarkan berbagai kelas penyimpanan tingkat objek yang dirancang untuk kasus penggunaan yang berbeda:
  - Amazon S3 Standard -  dirancang untuk penyimpanan objek dengan ketahanan, ketersediaan, dan kinerja tinggi untuk data yang sering diakses
  - Amazon S3 Intelligent-Tiering - Kelas penyimpanan Amazon S3 Intelligent-Tiering dirancang untuk mengoptimalkan biaya dengan memindahkan data secara otomatis ke tingkat akses yang paling efektif, tanpa dampak kinerja atau overhead operasional.
  - Amazon S3 Standard-Infrequent Access (Amazon S3 Standard-IA) – Kelas penyimpanan Amazon S3 Standard-IA digunakan untuk data yang lebih jarang diakses, tetapi memerlukan akses cepat saat diperlukan. Amazon S3 Standard-IA menawarkan ketahanan tinggi, throughput tinggi, dan latensi rendah seperti Amazon S3 Standard, dengan harga penyimpanan per GB dan biaya pengambilan per GB yang rendah.
  - Amazon S3 One Zone-Infrequent Access (Amazon S3 One Zone-IA) – Amazon S3 One Zone-IA adalah untuk data yang lebih jarang diakses, tetapi membutuhkan akses cepat bila diperlukan. Tidak seperti kelas penyimpanan Amazon S3 lainnya, yang menyimpan data dalam minimal tiga Availability Zone, Amazon S3 One Zone-IA menyimpan data dalam Availability Zone tunggal dan biayanya lebih rendah dari Amazon S3 Standard-IA.
  - Amazon S3 Glacier – Amazon S3 Glacier adalah layanan penyimpanan yang aman, tahan lama, dan rendah biaya untuk pengarsipan data. Anda dapat menyimpan sejumlah data dengan andal dengan biaya yang kompetitif atau lebih murah daripada solusi on-premise.
  - Amazon S3 Glacier Deep Archive – Amazon S3 Glacier Deep Archive adalah kelas penyimpanan biaya terendah untuk Amazon S3. Kelas ini mendukung retensi dan preservasi digital jangka panjang untuk data yang mungkin diakses satu atau dua kali dalam setahun.
  - 
## Amazon Elastic File System (Amazon EFS)
  Amazon Elastic File System (Amazon EFS)menyediakan penyimpanan file yang sederhana, dapat diskalakan, dan elastis untuk digunakan dengan layanan AWS dan sumber daya on-premise. Sistem ini mudah digunakan dan menawarkan antarmuka sederhana yang memungkinkan Anda membuat dan mengonfigurasi sistem file dengan cepat dan mudah.
  Amazon EFS dibangun untuk menskalakan sesuai permintaan secara dinamis tanpa mengganggu aplikasi—yang akan tumbuh dan menyusut secara otomatis saat Anda menambahkan dan menghapus file. Ini dirancang agar aplikasi Anda memiliki penyimpanan yang dibutuhkan, saat aplikasi membutuhkannya.
  Fitu Amazon EFS:
  - Penyimpanan file di AWS Cloud
  - Bekerja dengan baik untuk *big data* dan analitik, alur kerja pemrosesan media, manajemen konten, penayangan web, dan dirktori rumah
  - Siste file berskala petabyte dan latensi rendah
  - Penyimpanan bersama
  - kapasitas elastis
  - Mendukung Sistem File Jaringan (NFS) versi 4.0 dan 4.1 (NFSv4)
  - Kompatibel dengan semua AMI berbasis-Linus untuk Amazon EC2

  Amazon EFS adalah layanan terkelola penuh yang memudahkan penyiapan dan penskalaan penyimpanan file di AWS Cloud. Anda dapat menggunakan Amazon EFS untuk membangun sistem file untuk big data dan analitik, alur kerja pemrosesan media, pengelolaan konten, penayangan web, dan direktori rumah.
  Di Amazon EFS, sistem file adalah sumber daya utama. Setiap sistem file memiliki karakteristik seperti:
  - ID
  - Token pembuatan
  - Waktu pembuatan
  - Ukuran sistem file dalam byte
  - Jumlah target mount yang dibuat untuk sistem file
  - Status sistem file
    
    Target mount: Untuk mengakses sistem file, Anda harus membuat target pemasangan di VPC Anda. Tiap target mount memiliki properti berikut:
    - ID target mount
    - ID subnet untuk subnet tempatnya dibuat
    - ID sistem file untuk sistem file tempatnya dibuat
    - Alamat IP tempat sistem file dapat di-mount
    - Status target mount
## Amazon Simple Storage Service Glacier
  Amazon S3 Glacier adalah layanan pengarsipan data yang didesain untuk keamanan, ketahanan, dan sangat hemat biaya.
  - Amaozon S3 Glacier didesain untuk memberikan daya tahan hingga 99,999999999% pada objek
  - Mendukung enkripsi data bergerak dan data diam mellaui Secure Sockets Layer (SSL) atau Transport Layer Security (TLS)
  - Fitur Vault Lock memberlakukan kepatuhan mellaui kebijakan
  - Desain berbiaya sangat rendah ini ideal untuk pengarsipan jangka panjajng
    - Menyediakan tiga opsi akses ke arsip-dipercepat, standar, dan massal-rentang waktu pengambilan berkisar dari beberapa menit hingga beberapa jam.

  Ada tiga istilah utama Amazon S3 Glacier yang harus di pahami:
  - Arsip-Tiap objek (misalnya foto, video, file, atau dokumen yang Anda simpan di Amazon S3 Glacier. Ini adalah unit penyimpanan dasar di Amazon S3 Glacier. Tiap arsip memiliki ID uniknya sendiri dan dapat memiliki deskripsi.
  - Vault–Kontainer untuk menyimpan arsip. Saat Anda membuat vault, Anda akan menentukan nama vault dan Wilayah untuk menemukan vault.
  - Kebijakan akses vault–Menentukan siapa saja yang dapat dan tidak dapat mengakses data yang disimpan dalam vault, dan operasi apa yang dapat dilakukan dan tidak dapat dilakukan pengguna. Satu kebijakan izin akses vault dapat dibuat bagi tiap vault agar dapat mengelola izin akses untuk vault tersebut.
    tiga opsi untuk mengambil data dengan berbagai waktu dan biaya akses:
    - Pengambilan dipercepat biasanya tersedia dalam waktu 1–5 menit (biaya tertinggi).
    - Pengambilan standar biasanya selesai dalam waktu 3–5 jam (lebih lama dari opsi dipercepat, lebih cepat dari opsi massal).
    - Pengambilan massal biasanya selesai dalam 5–12 jam (biaya paling rendah)
## Knowledge Chapter 7
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/04ef3926-b0f1-4140-b84f-aee721d78b5d)

