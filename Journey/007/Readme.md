# CLOUD COMPUTING - AWS Cloud Foundationn Chapter 6 [Pemateri: Tiara Dwi Maulita Sari]
# Chapter 6 - Compute
## Introduction
- Compute services overview
- Amazon EC2
- Amazon EC2 Cost Optimization
- Container services
- Introduction to AWS Lambda
- Introduction to AWS Elastic Beanstalk

## Compute services overview
### Layanan komputasi AWS
  **Amazon EC2** menyediakan mesin virtual yang dapat di kelola sesuai pilihan.
  **Amazon EC2 Auto Scaling** mendukung ketersediaan aplikasi dengan menentukan kondisi yag secara otomatis akan meluncurkan atau mengakhiri EC2 instance.
  **Amazon EC2 Container Registry (ECR)** digunakan untuk menyimpan dan mengambil image Docker. 
  **Amazon Elastic Container Service (Amazon ECS)** adalah layanan orkestrasi kontainer yang mendukung Docker.•
  **VMware cloud on AWS** memungkinkan Anda menyediakan cloud hybrid tanpa perangkat keras kustom.
  **AWS Elastic Beanstalk** menyediakan cara sederhana untuk menjalankan dan mengelola aplikasi web.
  **AWS Lambda** adalah solusi komputasi nirserver. Anda cukup membayar waktu komputasi yang digunakan.
  **Amazon Elastic Kubernetes Service (Amazon EKS)** memungkinkan Anda menjalankan Kubernetes terkelola di AWS.
  **Amazon Lightsail** menyediakan layanan sederhana untuk membangun aplikasi atau situs web.
  **AWS Batch** menyediakan alat untuk menjalankan tugas batch pada skala apa pun.
  **AWS Fargate** menyediakan cara untuk menjalankan kontainer yang mengurangi kebutuhan Anda untuk mengelola server atau kluster.
  **AWS Outposts** menyediakan cara untuk menjalankan layanan AWS pilihan di pusat data on-premise Anda.
  **AWS Serverless Application Repository** menyediakan cara untuk menemukan, men-deploy, dan memublikasikan aplikasi nirserver.
## Amazon EC2
  **Amazon Elastic Compute Cloud (Amazon EC2)** menyediakan mesin virtual agar Anda dapat meng-host jenis aplikasi yang sama yang mungkin dijalankan pada server on-premise tradisional. Layanan ini menyediakan kapasitas komputasi yang aman dan ukurannya dapat diubah di cloud. EC2 instance dapat mendukung berbagai beban kerja. Penggunaan umum untuk EC2 instance termasuk, namun tidak terbatas pada:
  - Server aplikasi
  - Server web
  - Server basis data
  - Server game
  - Server email
  - Server media
  - Server katalog
  - Server file
  - Server komputasi
  - Server proxy
  Singkatan EC2 di Amazon EC2 adalah Elastic Compute Cloud:
- **Elastic** artinya Anda dapat dengan mudah menambah atau mengurangi jumlah server yang dijalankan untuk mendukung aplikasi secara otomatis, dan Anda juga dapat menambah atau mengurangi ukuran server yang ada.
- **Compute** mengacu pada alasan sebagian besar pengguna menjalankan server, yaitu untuk meng-host aplikasi yang berjalan atau memproses data—tindakan yang memerlukan sumber daya komputasi, termasuk daya pemrosesan (CPU) dan memori (RAM).
- **Cloud** mengacu pada fakta bahwa EC2 instance yang Anda jalankan di-host di cloud.
  Amazon EC2 menyediakan mesin virtual di cloud dan memberi Anda kontrol administratif penuh atas sistem operasi Windows atau Linux yang berjalan pada instans. Sebagian besar sistem operasi server didukung, termasuk: **Windows 2008, 2012, 2016, dan 2019, Red Hat, SuSE, Ubuntu, dan Amazon Linux.**
  Dengan Amazon EC2, dapat meluncurkan sejumlah instans dari berbagai ukuran ke dalam Availability Zone mana saja di dunia dalam hitungan menit. Instans meluncur dari Amazon Machine Images (AMI), yang sebenarnya templatmesin virtual. AMI dibahas secara lebih detail nanti dalam modul ini.
  **Amazon Machine Image (AMI)** adalah templat yang digunakan untuk membuat EC2 instance yaitu mesin virtual atau VM, yang berjalan di AWS Cloud. Berisi sistem operasi Windows atau Linux, seringkali juga memiliki beberapa perangkat lunak pra-install.
### 1. Pilihan AMI:
  - **Quick Start** - AMI Linux dan Windows yang disediakan oleh AWS
  - **AMI Saya** - Setiap AMI yang dibuat
  - **AWS Marketplace** - Templat yang telah dikonfigurasi dari pihak ketiga
  - **AMI Komunitas** - AMI yang dibagikan oleh orang lain, gunakanlah secara hati-hati
### 2. Pilih tipe instans
    Tipe instans terdiri atas berbagai kombinasi CPU, memori, penyimpanan, dan kapasitas jaringan. Tipe instans berbeda memberikan fleksibilitas dalam memilih campuran sumber daya yang tepat untuk aplikasi Anda.
### Penamaan dan ukuran jenis EC2 instance
  T adalah nama family, yang kemudian diikuti dengan angka. Di sini, angka tersebut adalah 3. Angka itu adalah nomorgenerasi dari jenis tersebut. Jadi, instans t3 adalah generasi ketiga dari family T. Secara umum, tipe instans dari generasi yang lebih tinggi bersifat lebih kuat dan memberikan nilai lebih untuk harganya.Bagian selanjutnya dari nama tersebut adalah porsi ukuran instans. Ketika membandingkan ukuran, penting untuk melihat porsi koefisien dari kategori ukuran.
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/42824a2c-7351-42b0-8a5d-d99d3dac6132)
Contohnya, t3.2xlarge memiliki dua kali vCPU dan memori dibanding t3.xlarge. Begitu juga, t3.xlarge memiliki dua kali vCPU dan memori dari t3.large.
  Tipe instans bervariasi dari berbagai segi, termasuk: jenis CPU, CPU atau jumlah inti, jenis penyimpanan, jumlah penyimpanan, jumlah memori, dan kinerja jaringan. Grafik memberikan tampilan tingkat tinggi dari kategori instans berbeda, serta family dan nomor generasi tipe instans mana yang cocok untuk setiap jenis kategori. Pertimbangkan beberapa tipe instans lebih detail:
  - Instans T3 menyediakaninstans tujuan umum berkinerja burstable yang memberikan garis dasar kinerja CPU dengan kemampuan untuk melonjak di atas garis dasar. Kasus penggunaan untuk tipe instans ini mencakup situs web dan aplikasi web, lingkungan pengembangan, server pembangun, repositori kode, layanan mikro, lingkungan pengujian dan tahapan, dan aplikasi lini bisnis.
  - Instans C5 dioptimalkan untuk beban kerja dengan komputasi intensif, dan memberikan kinerja tinggi hemat biaya dengan harga rendah per rasio komputasi. Kasus penggunaannya meliputi pemodelan ilmiah, pemrosesan batch, penayangan iklan, game multipemain yang dapat diskalakan, dan pengodean video.
  - Instans R5 dioptimalkan untuk aplikasi intensif memori. Kasus penggunaan mencakup basis data kinerja tinggi, penambangan dan analisis data, basis data dalam memori, cache dalam memori dengan skala web terdistribusi, aplikasi yang menjalankan pemrosesan real-time untuk big data tidak terstruktur, klaster Apache Hadoop atau Apache Spark, dan aplikasi perusahaan lainnya.
  Setiap tipe instans menyediakan tingkat kinerja jaringan yang didokumentasikan. Misalnya, instans a1.medium akan menyediakan hingga 10 Gbps, tetapi instans p3dn.24xlarge menyediakan hingga 100 Gbps. Pilih tipe instans yang memenuhi kebutuhan.
### 3. Pengaturan jaringan
  Pilihan wilayah harus dibuat sebelum memulai Wizard Luncurkan Instans. Verifikasi bahwa Anda berada di halaman Wilayah konsol Amazon EC2 yang benar sebelum memilih Luncurkan Instans.
  Ketika Anda meluncurkan sebuah instans dalam VPC default, AWS akan memberinya alamatIP publik secara default. Ketika Anda meluncurkan instans ke VPC nondefault, subnet memiliki atribut yang menentukan apakah instans yang diluncurkan ke subnet itu menerima alamat IP publik dari kumpulan alamat IPv4 publik. Secara default, AWS tidak akan menetapkan alamat IP publik ke instans yang diluncurkan di subnet nondefault. Anda dapat mengontrol apakah instans Anda menerima alamat IP publik baik dengan memodifikasi atribut pemberian alamat IP publik subnet Anda, atau dengan mengaktifkan atau menonaktifkan fitur pemberian alamat IP publik selama peluncuran (yang menimpa atribut pemberian alamat IP publik milik subnet).
### 4. Lampirkan IAM role (opsional)
  AWS memungkinkan Anda melampirkan peran AWS Identity and Access Management (IAM) untuk EC2 instance. Profil instans adalah kontainer untuk IAM role.Jika Anda menggunakan AWS Management Console untuk membuat peran bagi Amazon EC2, konsol tersebut secara otomatis membuat profil instans dan memberikan nama yang sama dengan peran. Ketika Anda kemudian menggunakan konsol Amazon EC2 untuk meluncurkan instans dengan IAM role, Anda dapat memilih peran untuk dikaitkan dengan instans. Di konsol tersebut, daftar yang ditampilkan sebenarnya adalah daftar nama profil instans
### 5. Skrip data pengguna (opsional)
  Data pengguna dapat mengautomasi penyelesaian instalasi dan konfigurasi pada peluncuran instans. Contohnya, skrip data pengguna dapat melakukan patch dan memperbarui sistem operasi instans, mengambil dan menginstal kunci lisensi perangkat lunak, atau menginstal perangkat lunak tambahan.
  Ketika EC2 instance dibuat, skrip data pengguna akan berjalan dengan hak istimewa root selama fase akhir proses booting. Pada instans Linux, itu dijalankan oleh layanan cloud-init. Pada instans Windows, itu dijalankan oleh utilitas EC2Config atau EC2Launch. Secara default, data pengguna hanya berjalan saat pertama kali instans dimulai. 
### 6. Tentukan penyimpanan
  Saat meluncurkan EC2 instance, Anda dapat mengonfigurasi opsi penyimpanan. Misalnya, Anda dapat mengonfigurasi ukuran volume root tempat sistem operasi tamu diinstal. Anda juga dapat melampirkan volume penyimpanan tambahan saat meluncurkan instans. Beberapa AMI juga dikonfigurasi untuk meluncurkan lebih dari satu volume penyimpanan secara default untuk menyediakan penyimpanan yang terpisah dari volume root.
### Pilihan penyimpanan Amazon EC2
- Amazon Elastic Block Store(Amazon EBS)
  - Volume penyimpanan tingkat blok yang tahan lama
  - Dapat menghentikan instans serta memulianya lagi, dan datanya akan tetap ada di sana.
- Amazon EC2 Instance Store
  - Penyimpanan Ephemeral disediakan pada disk yang melekat pada komputer host tempat EC2 instance berjalan.
  - Jika instans berhenti, data yang disimpan disini akan dihapus
- Pilihan lain untuk penyimpanan (bukan untuk volume root)
  - Pasang sistem file Amazon Elastic File System (Amazon EFS)
  - Sambungkan ke Amazon Simple Storage Service (Amazon S3)
### 7. Tambahkan tag
  Tag adalah label yang dapat diberikan ke sumber daya AWS yang terdiri dari *kunci* dan *nilai opsional*. Pemberian tag adalah cara anda dapat memasangkan metadata ke EC2 instance. Manfaat potensial dari penandaan pemfilteran, otomatisasi, alokasi biaya, dan kontrol akses.
  Kunci tag dan nilai tag bersifat peka huruf besar dan kecil. Sebagai contoh, tag yang umum digunakan untuk EC2 instance adalah kunci tag yang disebut Namadan nilai tag yang menggambarkan instansnya, seperti Server Web Saya. Tag Namaditampilkan secara default di halaman Instans konsol Amazon EC2. Namun, jika Anda membuat kunci yang disebut nama(dengan huruf nkecil), itu tidak akan muncul di kolom Namauntuk daftar instans (meskipun akan masih muncul di panel detail instans di tab Tag).
### 8. Pengaturan grup keamanan
  Grup keamanan adalah seperangkat aturan firewall yang mengontrol lalu lintas ke instans, Grup ada di luar OS tamu instans ini. Suatugrup keamananbertindak sebagai firewall virtual yang mengontrol lalu lintas untuk satu instans atau lebih. Ketika meluncurkan instans, Anda dapat menentukan satu grup keamanan atau lebih; jika tidak, grup keamanan default digunakan. 
### 9. Mengidentifikasi atau membuat pasangan kunci
  Amazon EC2 menggunakan kriptografi kunci–publik untuk mengenkripsi dan mendekripsi informasi login. Teknologi ini menggunakankunci publikuntuk mengenkripsi potongan data, lalu penerima menggunakan kunci pribadi untuk mendekripsi data. Kunci publik dan pribadi dikenal sebagai pasangan kunci. Kriptografi kunci publik memungkinkan Anda mengakses instans Anda secara aman dengan menggunakan kunci privat, bukan kata sandi.
### Metadata EC2 instance
  Metadata instans adalah data tentang instans. Anda dapat melihatnya saat Anda terhubung ke instans. Untuk mengaksesnya di browser, buka URL berikut: http://169.254.169.254/latest/meta-data/. Data juga dapat dibaca secara terprogram, seperti dari jendela terminal yang memiliki utilitas cURL. Di jendela terminal, jalankan curl http://169.254.169.254/latest/meta-data/untuk mengambilnya. Alamat IP 169.254.169.254adalah alamat tautan lokal dan hanya valid dari instans tersebut
### Amazon Cloudwatch untuk pemantauan
  Amazon EC2 menyediakan pemantauan dasar,yang mengirimkan data metrik ke CloudWatch dalam periode 5 menit. Untuk mengirim data metrik instans Anda ke CloudWatch dalam periode 1 menit, Anda dapat mengaktifkan pemantauan mendetail pada instans tersebut. Anda dapat menggunakan Amazon CloudWatch untuk menangkap dan meninjau metrik pada EC2 instance.
## Amazon EC2 Cost Optimization
  Instans Sesuai Permintaan paling fleksibel, tanpa kontrak jangka panjang dan tarif rendah. 
  Instans Spot memberikan skala besar dengan harga diskon yang signifikan.
  Instans Cadangan adalah pilihan yang baik jika Anda memiliki kebutuhan komputasi terprediksi atau terus-menerus (misalnya, instans yang ingin terus Anda jalankan sebagian besar atau sepanjang waktu selama berbulan-bulan atau bertahun-tahun).
  Host Khusus adalah pilihan yang baik ketika Anda memiliki pembatasan lisensi untuk perangkat lunak yang ingin dijalankan di Amazon EC2, atau ketika Anda memiliki kepatuhan atau persyaratan peraturan tertentu yang menghalangi Anda menggunakan opsi deployment lainnya.
- Model harga Amazon EC2 mencakup Instans Sesuai Permintaan, Instans Cadangan, Instans Spot, Instans Khusus, dan Host Khusus. Penagihan per detik tersedia untuk Instans Sesuai Permintaan, Instans Cadangan, dan Instans Spot yang hanya menggunakan Amazon Linux dan Ubuntu.
- Instans Spot dapat terganggu dengan pemberitahuan 2 menit. Namun, instans ini dapat menawarkan penghematan biaya yang signifikan dibanding Instans Sesuai Permintaan.
- Empat pilar pengoptimalan biaya adalah
  - Ukuran tepat
  - Meningkatkan elastisitas
  - Model harga optimal
  - Mengoptimalkan pilihan penyimpanan
## Container services
  Kontainermerupakan metode virtualisasi sistem operasiyang memungkinkan Anda menjalankan aplikasi dan dependensinya dalam proses yang sumber dayanya terisolasi. 
## Introduction to AWS Lambda
  AWS Lambda adalah layanan komputasi nirserver yang digerakkan event. Lambda memungkinkan Anda menjalankan kode tanpa menyediakan atau mengelola server. Fungsi Lambda, yaitu sumber daya AWS berisi kode yang Anda unggah. Anda kemudian mengatur fungsi Lambda untuk dipicu, baik secara terjadwal atau dalam merespons suatu peristiwa. Kode Anda hanya berjalan ketika dipicu.
Poin penting dari bagian modul ini:
- Komputasi nirserver memungkinkan Anda membangun dan menjalankan aplikasi serta layanan tanpa menyediakan atau mengelola server.
- AWS Lambda adalah layanan komputasi nirserver yang menyediakan toleransi kesalahan bawaan dan penskalaan otomatis.
- Sumber peristiwa adalah layanan AWS atau aplikasi buatan developer yang memicu jalannya fungsi Lambda.
- Alokasi memori maksimum untuk fungsi Lambda tunggal adalah 3.008 MB.
- Waktu eksekusi maksimum untuk fungsi Lambda adalah 15 menit
## Introduction to AWS Elastic Beanstalk
  AWS Elastic Beanstalk adalah opsi layanan komputasi AWS lain. Ini adalah platform as a service (atau PaaS) yang memfasilitasi deployment, penskalaan, dan manajemen cepat untuk aplikasi web dan layanan Anda.
  AWS Elastic Beanstalk memungkinkan Anda untuk men-deploy kode melalui AWS Management Console, AWS Command Line Interface (AWS CLI), Visual Studio, dan Eclipse. Layanan ini menyediakan semua layanan aplikasi yang dibutuhkan untuk aplikasi Anda. Satu-satunya hal yang harus Anda buat adalah kode Anda. Elastic Beanstalk dirancang untuk membuat deploy aplikasi Anda menjadi proses yang cepat dan mudah. Elastic Beanstalk mendukung berbagai platform. Platform yang didukung termasuk Docker, Go, Java, .NET, Node.js, PHP, Python, dan Ruby. 
  AWS Elastic Beanstalk men-deploy kode Anda di Apache Tomcatuntuk aplikasi Java; Apache HTTP Serveruntuk aplikasi PHP dan Python; NGINXatau Apache HTTP Server untuk aplikasi Node.js; Passengeratau Pumauntuk aplikasi Ruby; dan Microsoft Internet Information Services (IIS) untuk aplikasi .NET, Java SE, Docker, dan Go.
Poin penting dari bagian modul ini:
- AWS Elastic Beanstalk meningkatkan produktivitas developer.
- Menyederhanakan proses deploy aplikasi Anda.
- Mengurangi kompleksitas manajemen.
- Elastic Beanstalk mendukung Java, .NET, PHP, Node.js, Python, Ruby, Go, dan Docker.
- Tidak ada biaya untuk Elastic Beanstalk. Anda hanya membayar sumber daya AWS yang digunakan.
## Knowledge Chapter 6
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/98cf1567-c6b7-473f-8b7b-a172ecf71f1b)
