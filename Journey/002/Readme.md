
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/fad351af-5608-45d3-af95-6b8dec9e897e)


# CLOUD COMPUTING - Chapter 2 dan 3 [Pemateri: Tiara Dwi Maulita Sari]
  
## Chapter 2 - Cloud Economics and Billing

## Introduction
- Dasar-dasar harga
- Total Biaya Kepemilikan
- AWS Organizations
- Dukungan Teknis
  
### - Dasar-dasar harga

#### Model harga AWS
  Ada tiga pendorong dasar biaya dengan AWS, yaitu: **KOmputasi, Penyimpanan, Transfer data keluar**. Untuk karakteristikny bervariasi, tergantung produk AWS dan model harga yang dipilih.
- Komputasi: dikenai biaya per jam/detik, bervariasi sesuai tie instans
- Peyimpanan: biasanya dikenai biaya per GB
- Transfer data keluar: data keluar dijumlahkan dan dikenai biaya, data masuk tidak dikenai biaya, biasanya dikenai biaya per GB. Untuk transfer data keluar dijumlahkan di seluruh layanan kemudian dibebankan pada tarif transfer data kelar. Biaya ini akan terlihat pada laporan bulanan sebagai AWS Data Transfer Out.

#### How to pay for AWS?
  AWS menawarkan berbagai layanan cloud computing. Untuk setiap layanan nya, kita membayar persis dengan jumlah sumber daya yang benar-benar diperlukan. Model harga bergaya utilitas ini meliput:
  - **Bayar sesuai yang digunakan**. Hanya membayar untuk layanan yang dikonsumsi, tanpa biaya dimuka yang besar
  - **Bayar lebih sedikit ketika melakukan pemesanan**. Berinvestasi di instans terpesan, akan menerima diskon yang leih besar saat melakukan pembayaran di muka yang lebih besar
  - **Bayar lebih sedikit saat menggunakan lebih banyak**. Diskon berbasis volume. Dengan AWS, bisa mendapatkan diskon berbasis volume dan mewujudkan penghematan seiring meningkatnya penggunaan.
  - **Bayar jauh lebih sedikit seiring berkembangnya AWS**. Berfokus pada menurunkan biaya dalam menjalankan bisnis. Sumber daya berkinerja lebih tinggi di masa depan akan menggantikan sumber daya yang ada saat ini tanpa biaya tambahan.

####  Harga Khusus
  Penuhi kebutuhan melalui harga khusus. Tersedia untuk proyek bervolume tinggi dengan persyaratn yang unik.

####  AWS Tingkat Gratis
  Mendapatkan pengalaman langsung secara gratis dengan platform, produk, dan layanan AWS. Gratis selama 1 tahun untuk pelanggan baru.

#### Layanan tanpa biaya
  AWS juga menawaran layanan tanpa biaya tambahan.
  - **Amazon Virtual Private Cloud (Amazon VPC)**, menyediakan bagian yang terisolasi dari AWS Cloud secara logis.
  - **AWS Identity and Access Management (IAM)**, mengontrol akses pengguna ke layanan dan sumber daya AWS.
  - **Tagihan Terkonsolidasi**, fitur penagihan di AWS Organizations untuk menggabungkan pembayarn untuk beberapa akun AWS. Tagihan terkonsolidasi menyediakan:
      - satu tagihan untuk beberapa akun
      - kemamuan dengan mudah melacak biaya setiap akun
      - penggunaan gabungan
      - menggabubgkan semua akun
- **AWS Elastic Beanstalk**, cara yang lebih mudah untuk men-deploy dan mengelola apk dnegan cepat di AWS Cloud.
- **AWS CloudFormation**, menambahkan atau menghapus seumber daya secara otomatis sesuai dengan kondisi yang ditentukan.
- **AWS OpsWorks**, layanan pengelola apk yang memudahkan deploy dan mengoperaskan apk dengan berbagai bentuk dan ukuran.
  Meskioun tak ada biaya untuk layanan ini, mungkin akan ada biaya terkait dengan layanan AWS lain yang digunakan untuk layanan ini.  

### - Total Biaya Kepemilikan
#### On-premise Vs Cloud
  Infrastruktur on-premise diinstall secara on-premise pada komputer server milik perusahaan. Ada beberapa biaya tetap yang juga dikenal sebagai biaya modal.

  Infrastruktur cloud dibeli dari penyedia layanan yang membangun dan memelihara fasilitas, perangkat keras, serta staf pemeliharaan. Pelanggan membayar sesuai yang digunakan

#### Apa itu Total Biaya Kepemilikan (TCO)?
  **Total Biaya Kepemilikan (TCO)** adalah perkiraan keuangan untuk membantu mengidentifikasi biaya langsung dan tidak langsung dari suatu sistem. 
  Digunakan untuk membandingkan biaya menjalankan seluruh lingkungan infrastruktu atau beban kerja spesifik on-premise versus di AWS. Perbandingan ini dilakukan untuk tujuan membuat penganggaran dan membangun kasus bisnis untuk berpindah ke cloud.
  Beberapa biaya terkait manajemen pusat data meliputi:
  - biaya server untuk perangkat keras dan perangkatlunak, serta biaya fasilitas untuk menyimpan peralatan.
  - Biaya penyimpanan untuk perangkat keras, administrasi, dan fasilitas.
  - Biaya jaringan untuk perangkat keras, administrasi, dan fasilitas.
  - Selain itu, biaya tenaga kerja IT yang diperlukan untuk mengelola seluruh solusi
    
Meskipun terkadang sulit untuk ditentukan, perhitungan biaya internal harus memperhitungkan semua:
• Biaya langsung yang menyertai pengoperasian server, seperti listrik, ruang lantai, penyimpanan, dan operasi IT untuk mengelola sumber daya tersebut.
• Biaya tidak langsung untuk menjalankan server, seperti infrastruktur jaringan dan penyimpanan

  #### **Pertimbangan manfaat tambahan**
  Manfaat langsungnya meliputi mengurangi pengeluaran komputasi, penyimpanan, jaringan, dan keamanan. Juga mencakup pengurangan pembelian perangkat keras dan perangkat lunak, pengurangan biaya operasional, pencadangan, pemulihan bencana, dan pengurangan personel operasi.
    Manfaat tidak langsung meliputi:
  - Menggunakan kembali layanan dan aplikasi yang memungkinkan kalian menentukan (dan menentukan ulang solusi) dengan menggunakan layanan cloud yang sama
  - Peningkatan produktivitas developer
  - Peningkatan kepuasan pelanggan
  - Proses bisnis yang tangkas dan dapat menanggapi peluang baru yang muncul dengan cepat
  - Peningkatan jangkauan global

### - AWS Organizations
  merupakan layanan manajemen akun yang memungkinkan kalian menggabungkan beberapa akun AWS ke sebuah **organisasi** yang dibuat dan dikelola secara terpusat. AWS Organizations meliputi tagihan terkonsolidasi dan kemampuan manajemen akun yang membantu kalian memenuhi anggaran, keamanan, dan kebutuhan kepatuhan bisnis dengan lebih baik.
  Manfaat utama AWS Organizations:
  - Mengelola kebijakan akses secara terpusat di beberapa akun AWS
  - Mengontrol akses ke layanan AWS
  - Mengautomasi pembuatan dan pengelolaan akun AWS
  - Tagihan terkonsolidasi di beberapa akun AWS

![th](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/59c13065-9ac4-44dd-87bc-525e22c14ff9)

#### Fitur utama dan manfaat AWS Organizations
  AWS Organizations memungkinkan:
  - Membuat **service control policies (SCP)** yang secara terpusat mengontrol penggunaan layanan AWS di beberapa akun AWS.
  - Membuat **grup akun** dan kemudian melampirkan kebijakan ke dalam grup untuk memastikan kebijakan yang benar diterapkan di seluruh akun tersebut.
  - Menyederhanakan pengelolaan akun menggunakan **antarmuka pemrograman aplikasi (API)** untuk mengautomasi pembuatan dan pengelolaan akun AWS baru.
  - Menyederhanakan proses penagihan dengan menyiapkan metode pembayaran tunggal untuk semua akun AWS di organisasi kalian. Dengan tagihan terkonsolidasi, dapat melihat tampilan tagihan terkonsolidasi yang dikeluarkan oleh semua akun kalian, dan kalian dapat memanfaatkan keuntungan harga dari penggunaan gabungan. Tagihan terkonsolidasi menyediakan lokasi pusat untuk mengelola penagihan di semua akun AWS kalian, dan kemampuan untuk mendapatkan keuntungan dari diskon volume.
#### Keamanan dengab AWS Organizations
  AWS Organizations tidak menggantikan kebijakan AWS Identity dan Access Management (IAM) terkait dengan pengguna, grup, dan peran dalam akun AWS.
  Dengan kebijakan IAM, kalian dapat mengizinkan atau menolak akses ke layanan AWS (seperti Amazon S3), sumber daya AWS individu (seperti bucket S3 tertentu), atau tindakan API individu (seperti s3:CreateBucket). Kebijakan IAM hanya dapat diterapkan pada pengguna, grup, atau IAM role, dan tidak dapat membatasi root user akun AWS.
  Sedangkan Organizations, menggunakan **service control policies (SCP)** untuk mengizinkan atau menolak akses ke layanan AWS tertentu untuk akun AWS individu atau sekelompok akun di OU. Tindakan ini memengaruhi semua pengguna, grup, dan IAM role untuk akun, termasuk root user akun AWS.

#### Penyiapan Organisasi
  Langkah-langkah:
  1. Membuat organisasi, dengan akun AWS sebagai akun master.
  2. Membuat unit organisasi, membuat 2 unit organisasi dalam organisasi baru dan menempatkan akun anggota di OU tersebut.
  3. Membuat service control policies, yang memungkinkan menerapkan batasan tindakan apa yang dapat didelegasikan kepada pengguna dan peran dalam akun anggota.
  4. Pembatasan pengujian, menguji kebijakan organisasi dengan masuk sebagai pengguna untuk masing-masing peran dan lihat bagaimana service control policies ini memengaruhi akses akun.

#### Batas AWS Organizations
  Ada batasan pada nama yang dapat dibuat di AWS Organizations yang meliputi nama akun, OU, root, dan kebijakan. Nama harus terdiri dari karakter Unicode dan panjangnya tidak melebihi 250 karakter. AWS Organizations juga memeliki beberapa nilai maksimum dan minimum untuk entitas.

#### Mengakses AWS Organizations
  AWS Organizatioons dapat dikelola melalui antarmula yang berbeda.
  - AWS Management Console
  - AWS Command Line Interface (AWS CLI)
  - Kit pengembangan perangkat lunak (SDK)
  - Antarmuka pemrograman aplikasi (API) Kueri HTTPS
#### Dasbor Penagihan AWS
  Dasbor Penagihan AWS memungkinkan kalian melihat status pengeluaran AWS bulan ini sampai saat ini, dan mengidentifikasi layanan yang berkontribusi terhadap sebagian besar pengeluaran keseluruhan, dan memahami tren biaya dengan baik.
  Manajemen Penagihan dan Biaya AWS menyediakan alat untuk membantu Anda mengakses, memahami, mengalokasikan, mengontrol, dan mengoptimalkan biaya dan penggunaan AWS Anda. Alat ini meliputi Tagihan AWS, AWS Cost Explorer, AWS Budgets, dan Laporan Penggunaan dan Biaya AWS.
  Menggunakan Kalkulator Simpel Bulanan AWS untuk:
    - Memperkirakan biaya bulanan
    - Mengidentifikasi peluang untuk mengurangi biaya bulanan
    - Menggunakan templat untuk membandingkan layanan dan model deployment
  Gunakan Kalkulator TCO untuk:
    - Menganalisis laporan detail yang menunjukkan perbandingan TCO selama 3 tahun berdasarkan kategori biaya
    - Melihat laporan yang sesuai untuk dimasukkan dalam presentasi eksekutif
    - Mengubah asumsi untuk kebutuhan bisnis
    
### - Dukungan Teknis
#### AWS Support
- Menyediakan kombinasi alat dan keahlian yang unik:
    - AWS Support
    - Paket AWS Support
- Dukungan disediakan untuk:
    - Bereksperimen dengan AWS
    - Pengguna produksi AWS
    - Penggunaan AWS untuk bisnis penting
- Panduan proaktif:
    - Manajer Akun Teknis (MAT)
- Praktik terbaik:
    - AWS Trusted Advisor
- Bantuan Akun:
    - AWS Support Concierge
#### Paket Support
  AWS Support menawarkan 4 paket dukungan:
- **Paket Basic Support menawarkan**:
   -Akses 7x24 jam ke layanan pelanggan, dokumentasi, whitepaper, dan forum dukungan.•Akses ke enam pemeriksaan Trusted Advisor inti.
   - Akses ke Personal Health Dashboard.
- **Paket Developer Support** menawarkan sumber daya bagi pelanggan yang menguji atau melakukan pengembangan awal di AWS, serta semua pelanggan yang:
   - Menginginkan akses ke panduan dan dukungan teknis.•Menjelajahi cara cepat untuk menggunakan AWS.
    - Menggunakan AWS untuk beban kerja atau aplikasi nonproduksi.
- **Paket Business Support** menawarkan sumber daya untuk pelanggan yang menjalankan beban kerja produksi di AWS dan semua pelanggan yang:
  - Menjalankan satu atau beberapa aplikasi di lingkungan produksi.
  - Mengaktifkan beberapa layanan, atau menggunakan layanan utama secara ekstensif.
  - Bergantung pada solusi bisnis mereka agar tersedia, dapat diskalakan, dan aman
- **Paket Enterprise Support** menawarkan sumber daya untuk pelanggan yang menjalankan bisnis dan beban kerja yang sangat penting di AWS dan semua pelanggan yang ingin:•
  - Berfokus pada manajemen proaktif untuk meningkatkan efisiensi dan ketersediaan.
  - Membangun dan mengoperasikan beban kerja yang mengikuti praktik terbaik AWS.
  - Menggunakan keahlian AWS untuk mendukung peluncuran dan migrasi.
  - Menggunakan Manajer Akun Teknis (MAT), yang menyediakan keahlian teknis untuk berbagai layanan AWS, serta memperoleh pemahaman detail tentang kasus penggunaan dan arsitektur teknologi Anda. Manajer Akun Teknis adalah kontak utama untuk kebutuhan dukungan yang sedang berjalan
### Knowledge Chapter 2



## Chapter 3 - AWS Global Infrastructure Overview
## Introduction
- Infrastruktur Global AWS
- Ikhtisar layanan AWS dan kategori layanan

### - Infrastruktur Global AWS
  **Infrastruktur Global AWS** dirancang dan dibangun untuk memberikan lingkungan cloud computing yang **fleksibel, dapat diandalkan, dan aman** dengan kinerja jaringan global berkualitas tinggi.
  ![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/687aa5f3-eb70-4c5d-89f9-7729b499b58e)
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/ce20564b-ab9f-4b1c-b1da-51d6a0f0747e)
#### Wilayah AWS
  Infrastruktur AWS Cloud dibangun di sekitar Wilayah. AWS memiliki 22 Wilayah di seluruh dunia. Satu Wilayah AWS adalah lokasi geografis fisik dengan satu atau beberapa Availability Zone. Availability Zone terdiri dari satu atau beberapa pusat data. Untuk mencapai toleransi kesalahan dan stabilitas, Wilayah diisolasi dari satu sama lain. Sumber daya di satu Wilayah tidak secara otomatis direplikasi ke Wilayah lain. Saat menyimpan data di Wilayah tertentu, data Anda tidak direplikasi di luar Wilayah tersebut
  Wilayah AWS yang diperkenalkan sebelum 20 Maret 2019diaktifkansecara default. Wilayah yang diperkenalkan setelah 20 Maret 2019—seperti Asia Pasifik (Hong Kong) dan Timur Tengah (Bahrain)—dinonaktifkansecara default. Anda harus mengaktifkan Wilayah ini sebelum Anda dapat menggunakannya. Anda dapat menggunakan AWS Management Console untuk mengaktifkan atau menonaktifkan Wilayah. Beberapa wilayah memiliki akses terbatas seperti akun Amazon AWS (Tiongkok) hanya menyediakan akses ke wilayah Beijing dan Ningxia.

#### Availability Zone
  Setiap wilayah memiliki banyak lokasi terisolasi yang dikenal sebagai *Availabilty Zone*. Setiap Availability Zone menyediakan kemampuan untuk mengoperasikan aplikasi dan basis data yang tersedia dengan sangat baik, toleran terhadap kesalahan, dan dapat diskalakan daripada yang mungkin dilakukan dengan satu pusat data. Availability Zone merupakan partisi Infrastruktur Global AWS yang terisolasi penuh. Availability Zone memiliki infrastruktur daya tersendiri, dan secara fisik berjarak sangat jauh dari Availability Zone lainnya—tetapi semua Availability Zone berjarak 100 km satu sama lain.

#### Pusat Data AWS
- Pusat data AWS dirancang demi keamanan.
- Pusat data adalah tempat data berada dan pemrosesan data terjadi.
- Setiap pusat data memiliki daya, jaringan, dan konektivitas berlebih, dan ditempatkan di fasilitas yang terpisah.
- Pusat data biasanya memiliki 50.000 sampai 80.000 server fisik.
  Dasar untuk infrastruktur AWS adalah pusat data. Pelanggan tidak menentukan pusat data untuk deployment sumber daya. Sebaliknya, Availability Zone adalah tingkat spesifikasi paling granular yang dapat dibuat pelanggan. Namun, pusat data adalah lokasi tempat data aktual berada. Amazon mengoperasikan pusat data mutakhir yang tersedia dengan sangat baik. Meskipun jarang, kegagalan yang memengaruhi ketersediaan instans di lokasi yang sama dapat terjadi. Jika Anda meng-host semua instans Anda di satu lokasi yang terpengaruh oleh kegagalan tersebut, tidak ada instans Anda yang akan tersedia. AWS menggunakan peralatan jaringan khusus yang bersumber dari beberapa Produsen Perangkat Asli yang juga dikenal sebagai ODM. ODM merancang dan membuat produk berdasarkan spesifikasi dari perusahaan kedua. Perusahaan kedua kemudian mengubah merek produk untuk dijual.

#### Point of Presence
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/c1806a07-5c95-4175-a05d-6c34316b8c65)

- AWS menyediakan jaringan global 187 lokasi Point of Presence
- Terdiri dari 176 edge location ddan 11 Cache edge Regional
- Digunakan dengan Amazon CloudFront
- Cache edge Regional digunakan untuk konten dengan akses jarang
  **Amazon CloudFront** adalah jaringan penyampaian konten(CDN) yang digunakan untuk mendistribusikan konten ke pengguna akhir untuk mengurangi latensi. Amazon Route 53 adalah layanan Domain Name System (DNS). Permintaan ke salah satu layanan ini akan dialihkan ke edge locationterdekat secara otomatis untuk menurunkan latensi.
  Points of Presence AWS terleta kdi sebagian besar kota besar di (total 69 kota) di 30 negaradi seluruh dunia. Dengan terus mengukur konektivitas internet, kinerja, dan komputasi untuk menemukan cara terbaik untuk merutekan permintaan, Points of Presence memberikan pengalaman pengguna yang lebih baik hampir secara real-time. Titik kehadiran ini digunakan oleh banyak layanan AWS, termasuk layanan Amazon CloudFront, Amazon Route 53, AWS Shield, dan AWS Web Application Firewall (AWS WAF).
  Cache Edge Wilayahl digunakan secara default dengan Amazon CloudFront. Cache edge regional digunakan saat Anda memiliki konten yang tidak cukup sering diakses untuk tetap berada di edge location.

#### Fitur infrastruktur AWS
AWS Global Infrastructure memiliki beberapa fitur berharga:
- Elastis dan sklabilitas.
  - elastis; adaptasi kapasitas yang dinamis
  - skalabilitas; adaptasi untuk mengakomodasi pertumbuhan
- Toleransi kesalahan.
  - terus beroperasi meskipun terjadi kegagalan
  - redundansi komponen terintegrasi
- Ketersediaan tinggi.
  - kinerja operasional tingkat tinggi
  - pengurangan waktu henti
  - tanpa campur tangan manusia
    
### - Ikhtisar layanan AWS dan kategori layanan
#### Layanan dasar AWS
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/d866dc69-e728-4821-b8d8-91b517ba34d6)
Seperti yang dibahas sebelumnya, Infrastruktur Global AWS dapat dibagi menjadi tiga elemen: Wilayah, Availability Zone, dan Points of Presence, yang disertai edge location. Infrastruktur ini menyediakan platform untuk serangkaian layanan yang luas, seperti jaringan, penyimpanan, layanan komputasi, dan basis data—serta layanan ini dikirimkan sebagai utilitas sesuai permintaan yang tersedia dalam hitungan detik, dengan harga sesuai pemakaian.

#### Kategori layanan AWS
  ![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/e078f95c-1a96-4b0b-bb64-d522165a5de0)
  AWS menawarkan serangkaian layanan berbasis cloud. Ada 23 kategori produk atau layanan yang berbeda, dan masing-masing kategori terdiri dari satu atau beberapa layanan. Kursus ini tidak akan mencoba untuk memperkenalkan Anda ke setiap layanan. Sebaliknya, fokus dari kursus ini adalah pada layanan yang paling banyak digunakan dan menawarkan pengenalan terbaik ke AWS Cloud. Kursus ini juga berfokus pada layanan yang kemungkinan besar akan dibahas dalam ujian AWS Certified Cloud Practitioner.

#### Kategori layanan penyimpanan
  ![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/c2c20bc2-e2d0-4e76-92b1-490afea91db6)

- Amazon Simple Storage Service (Amazon S3) adalah layanan penyimpanan objek yang menawarkan skalabilitas, ketersediaan data, keamanan, dan kinerja. Gunakan layanan ini untuk menyimpan dan melindungi sejumlah data untuk situs web, aplikasi seluler, pencadangan dan pemulihan, arsip, aplikasi perusahaan, perangkat Internet of Things (IoT), dan analitik big data
- Amazon Elastic Block Store (Amazon EBS)adalah penyimpanan blok berkinerja tinggi, yang dirancang untuk digunakan dengan Amazon EC2 untuk beban kerja intensif throughput dan transaksi. Layanan ini digunakan untuk beragam beban kerja, seperti basis data relasional dan non-relasional, aplikasi perusahaan, aplikasi kontainer, mesin analitik big data, sistem file, dan alur kerja media
- Amazon Elastic File System (Amazon EFS)menyediakan Sistem File Jaringan (NFS) elastis, dapat diskalakan, dan terkelola sepenuhnya untuk digunakan dengan layanan AWS Cloud dan sumber daya on-premise. Amazon EFS dibuat untuk menskalakan sesuai permintaan hingga petabyte, tumbuh dan menyusut secara otomatis ketika Anda menambahkan dan menghapus file. Layanan ini mengurangi kebutuhan untuk menyediakan dan mengelola kapasitas guna mengakomodasi pertumbuhan
- Amazon Simple Storage Services Glacieradalah kelas penyimpanan cloud Amazon S3 yang aman, tahan lama, dan berbiaya sangat rendah untuk pengarsipan data dan pencadangan jangka panjang. Dirancang untuk memberikan daya tahan sebesar 99,999999999%, dan untuk menyediakan kemampuan keamanan dan kepatuhan menyeluruh untuk memenuhi persyaratan hukum yang paling ketat.

#### Kategori layanan komputasi
  ![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/a228d1c4-9399-4253-8daf-e817d84bbc43)

- Amazon Elastic Compute cloud (Amazon EC2) menyediakan kapasitas komputasi yang aman dan fleksibel sebagai mesin virtual di cloud.
- Amazon EC2 Auto Scaling memungkinkan Anda menambah atau menghapus EC2 instance secara otomatis sesuai dengan kondisi yang Anda tetapkan.
- Amazon Elastic Container Service (Amazon ECS) adalah layanan orkestrasi kontainer berkinerja tinggi dan sangat mudah diskalakan yang mendukung kontainer Docker.
- Amazon Elastic Container Registry (Amazon ECR) merupakan registri kontainer Docker yang dikelola sepenuhnya yang memudahkan developer menyimpan, mengelola, dan men-deploy gambar kontainer Docker.
- AWS Elastic Beanstalk adalah layanan untuk men-deploy dan menskalakan aplikasi dan layanan web di server yang sudah dikenal, seperti Apache dan Microsoft Internet Information Services (IIS).
- AWS Lambda memungkinkan Anda menjalankan kode tanpa menyediakan atau mengelola server. Anda hanya membayar untuk waktu komputasi yang Anda gunakan. Tidak ada biaya ketika kode Anda tidak berjalan.
- Amazon Elastic Kubernetes Service (Amazon EKS) memudahkan untuk men-deploy, mengelola, dan menskalakan aplikasi dalam kontainer yang menggunakan Kubernetes di AWS.
- AWS Fargate adalah mesin komputasi untuk Amazon ECS yang memungkinkan Anda menjalankan kontainer tanpa harus mengelola server atau kluster

#### Kategori layanan basis data
- Amazon Relational Database Service (Amazon RDS)memudahkan penyiapan, pengoperasian, dan penskalaan basis data relasional di cloud.
- Amazon Auroraadalah basis data relasional yang kompatibel dengan MySQL dan PostgreSQL.
- Amazon Redshift memungkinkan Anda menjalankan pertanyaan analitik terhadap data berjumlah petabyte yang disimpan secara lokal di Amazon Redshift, dan langsung terhadap data berjumlah exabyte yang disimpan di Amazon S3.
- Amazon DynamoDB adalah basis data nilai kunci dan dokumen yang memberikan kinerja milidetik satu digit pada skala apa pun, dengan keamanan bawaan, pencadangan dan pemulihan, serta cache dalam memori.

#### Kategori layanan jaringan dan penyampaian konten
- Amazon Virtual Private Cloud (Amazon VPC) memungkinkan Anda menyediakan bagian yang terisolasi secara logis dari AWS Cloud.
- Elastic Load Balancing secara otomatis mendistribusikan lalu lintas aplikasi yang masuk di beberapa target, seperti Amazon EC2 instance, kontainer, alamat IP, dan fungsi Lambda.
- Amazon CloudFront adalah layanan jaringan penyampaian konten (CDN) cepat yang memberikan data, video, aplikasi, dan antarmuka pemrograman aplikasi (API) dengan aman kepada pelanggan secara global dengan latensi rendah dan kecepatan transfer tinggi.
- AWS Transit Gateway adalah layanan yang memungkinkan pelanggan menghubungkan Amazon Virtual Private Cloud (VPC) dan jaringan on-premise mereka ke satu gateway.
- Amazon Route 53 adalah layanan web Domain Name System (DNS) cloud yang dapat diskalakan yang dirancang untuk memberikan cara yang dapat diandalkan untuk merutekan pengguna akhir ke aplikasi internet.
- AWS Direct Connect menyediakan cara untuk membuat koneksi jaringan pribadi khusus dari pusat data atau kantor Anda ke AWS, yang dapat mengurangi biaya jaringan dan meningkatkan throughput bandwidth.
- AWS VPN menyediakan terowongan pribadi yang aman dari jaringan atau perangkat Anda ke jaringan global AWS.

#### Kategori layanan keamanan, identitas, dan kepatuhan
- AWS Identity and Access Management (IAM)memungkinkan Anda mengelola akses layanan dan sumber daya AWS secara aman. Dengan menggunakan IAM, Anda dapat membuat dan mengelola pengguna dan grup AWS. Anda dapat menggunakan izin IAM untuk mengizinkan dan menolak akses pengguna dan grup ke sumber daya AWS.
- AWS Organizations memungkinkan Anda membatasi layanan dan tindakan apa yang diizinkan di akun Anda.
- Amazon Cognito memungkinkan Anda menambahkan fungsi daftar, masuk, dan kontrol akses pengguna ke aplikasi web dan seluler Anda.
- AWS Artifact memberikan akses sesuai permintaan ke laporan keamanan dan kepatuhan AWS dan perjanjian online tertentu.
- AWS Key Management Service (AWS KMS) memungkinkan Anda membuat dan mengelola kunci. Anda dapat menggunakan AWS KMS untuk mengontrol penggunaan enkripsi di berbagai layanan AWS dan di aplikasi Anda.
- AWS Shield adalah layanan perlindungan Distributed Denial of Service (DDoS) terkelola yang melindungi aplikasi yang berjalan di AWS.

#### Kategori layanan manajemen biaya AWS
- Laporan Penggunaan dan Biaya AWS berisi kumpulan data biaya dan penggunaan AWS terlengkap yang tersedia, termasuk metadata tambahan tentang layanan, harga, dan reservasi AWS.
- AWS Budgets memungkinkan Anda mengatur anggaran kustom yang akan memberi Anda peringatan saat biaya atau penggunaan Anda melebihi (atau diprakirakan akan melebihi) jumlah yang Anda anggarkan.
- AWS Cost Explorer memiliki antarmuka yang mudah digunakan yang memungkinkan Anda memvisualisasikan, memahami, serta mengelola biaya dan penggunaan AWS Anda dari waktu ke waktu.

#### Kategori layanan manajemen dan tata kelola
- AWS Management Console memberikan antarmuka pengguna berbasis web untuk mengakses akun AWS Anda.
- AWS Config menyediakan layanan yang membantu Anda melacak inventaris dan perubahan sumber daya.
- Amazon CloudWatch memungkinkan Anda memantau sumber daya dan aplikasi.AWS Auto Scaling menyediakan fitur yang memungkinkan Anda menskalakan beberapa sumber daya untuk memenuhi permintaan.
- AWS Command Line Interface menyediakan alat terpadu untuk mengelola layanan AWS.
- AWS Trusted Advisor membantu Anda mengoptimalkan kinerja dan keamanan.
- AWS Well-Architected Tool menyediakan bantuan dalam meninjau dan meningkatkan beban kerja Anda.
- AWS CloudTrail melacak aktivitas pengguna dan penggunaan API.
