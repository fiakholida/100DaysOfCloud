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
  Amazon EFS menyediakan penyimpanan file di cloud. Dengan Amazon EFS, Anda dapat membuat sistem file, memasang sistem file ke Amazon EC2 instance, kemudian membaca dan menulis data ke dan dari sistem file Anda. Anda dapat memasang sistem file Amazon EFS di VPC Anda melalui NFS versi 4.0 dan 4.1 (NFSv4).
## Amazon Simple Storage Service Glacier



## Cloud Research



## Try yourself



### Step 1 — Summary of Step



### Step 1 — Summary of Step


### Step 3 — Summary of Step



## ☁️ Cloud Outcome



## Next Steps



## Social Proof



[link](link)
