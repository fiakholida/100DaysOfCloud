**Add a cover photo like:**
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



✍️ Describe what you think you think you want to do next.

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
