
# CLOUD COMPUTING - AWS Cloud Foundation Chapter 4 [Pemateri: Tiara Dwi Maulita Sari]
## Chapter 4 - AWS Cloud Security
## Introduction
- Model tanggung jawab bersama AWS
- AWS Identity Access Management (IAM)
- Mengamankan akun AWS baru
- Mengamankan akun
- Mengamankan data di AWS
- Berupaya Memastikan Kepatuhan

## - Model tanggung jawab bersama AWS
  Keamanan dan kepatuhan merupakan tanggung jawab bersama antara **AWS** dan **pelanggan**. **AWS** mengoperasikan, mengelola, dan mengontrol komponen dari lapisan virtualisasi perangkat lunak ke keamanan fisik fasilitas di mana layanan AWS beroperasi. AWS bertanggung jawab melindungi infrastruktur yang menjalankan semua layanan yang ditawarkan di AWS Cloud. Infrastruktur ini terdiri atas perangkat keras, perangkat lunak, jaringan, dan fasilitas yang menjalankan layanan AWS Cloud. 
  **Pelanggan** bertanggung jawab atas enkripsi data saat istirahat dan data dalam transit. Pelanggan juga harus memastikan bahwa jaringan dikonfigurasi untuk keamanan dan kredensial keamanan dan login dikelola dengan aman. Juga bertanggung jawab atas konfigurasi grup keamanan dan konfigurasi sistem operasi yang berjalan pada instans komputasi yang mereka lunucurkan.

#### Tanggung Jawab AWS (dari cloud)
  AWS bertanggung jawab melindungi infrastruktur global yang menjalankan semua layanan yang ditawarkan di AWS Cloud . Infrastruktur global ini termasuk Wilayah AWS, Availability Zone, dan edge location. 
  AWS bertanggung jawab atas infrastruktur fisik yang menyediakan sumber daya, termasuk:
  - Keamanan fisik pusat data, dengan akses berbasis kebutuhan dan terkontrol.
  - Infrastruktur perangkat keras, seperti server, perangkat penyimpanan, dan peralatan lain yang diandalkan AWS.
  - Infrastruktur perangkat lunak, yang menyediakan sistem operasi, aplikasi layanan, dan perangkat lunak virtualisasi.
  - Infrastruktur Jaringan,seperti router, switch, load balancer, firewall, dan kabel. Mengamankan jalur akses, dan menyediakan infrastruktur redungan dengan deteksi gangguan.
  - Infrastruktur Virtualisasi, isolasi instans.
Melindungi infrastruktur merupakan prioritas utama untuk AWS.

#### Tanggung Jawab Pelanggan (di cloud)
  Pelanggan bertanggung jawab untuk keamanan semua yang mereka masukkan **ke dalam** cloud, juga bertanggung jawab atas apa yang dilaksanakan dengan menggunakan layanan AWS dan untuk apliaksi yang terhubung ke AWS. Tanggung jawab pelanggan termasuk memilih dan mengamankan sistem operasi instans, mengamankan aplikasi yang diluncurkan pada sumber daya AWS, konfigurasi grup keamanan, konfigurasi firewall, konfigurasi jaringan, dan manajemen akun aman.
  Pelanggan bertanggung jawab mengelola persyaratan keamanan konten sensitif, termasuk:
  - Konten yang pelanggan pilih untuk disimpan di AWS
  - Layanan AWS yang digunakan bersama konten
  - Di negara mana konten tersebut disimpan
  - Format dan struktur dari konten tersebut
  - Pelanggan yang memiliki akses ke konten tersebut serta bagaimana akses itu diberikan, dikelola, dan ditarik kembali.
  Pelanggan tetap memiliki kontrol atas layanan keamanan yang mereka pilih untuk diterapkan dalam melindungi data, lingkungan, aplikasi, konfigurasi IAM, dan sistem operasi mereka.

#### Karakteristik layanan dan tanggung jawab keamanan
  Infrastruktur as a Service (IaaS)
  - pelanggan memilki fleksibilitas lebih dalan mengonfigurasi pengaturan jaringan dan penyimpanan
  - Pelanggan bertanggung jawab untuk mengelola lebih banyak aspek keamanan
  - Pelanggan mengonfigurasi kontrol akses
  Platform as a Service (PaaS)
  - Pelanggan tidak perlu mengelola infrastruktur dasarnya
  - AWS menangani sistem operasi, basis data patch, konfigurasi firewall, dan disaster recovery
  - Pelanggan dapat fokus pada pengelolaan kode atau data
  Software as a Service (SaaS)
  - Perangkat lunak di hosting secara terpusat
  - Dilisensikan pada model langganan atau bayar sesuai pemakaian
  - Layanan biasanya diakses melalui peramban web, aplikasi seluler, atau antarmuka pemrograman aplikasi (API)
  - Pelanggan tidak perlu mengelola infrastruktur yang mendukung layanan
    

## - AWS Identity and Access Management (IAM)
  AWS Identity and Access Management (IAM) memungkinkan Anda mengontrol akses ke komputasi, penyimpanan, basis data, dan layanan aplikasi di AWS Cloud. IAM dapat digunakan untuk menangani autentikasi, dan untuk menentukan dan menegakkan kebijakan otorisasi sehingga Anda dapat menentukan pengguna yang dapat mengakses layanan.
  IAM adalah alat yang secara terpusat mengelola akses untuk meluncurkan, mengonfigurasi, mengelola, dan mengakhiri sumber daya di akun AWS Anda. Ini memberikan kontrol detail atas akses ke sumber daya, termasuk kemampuan untuk menentukan dengan tepat panggilan API mana yang diizinkan untuk dilakukan pengguna ke setiap layanan.
  Dengan IAM, Anda dapat mengelola sumber daya yangdapat diakses oleh siapa, dan bagaimanasumber daya ini dapat diakses. Anda dapat memberikan izin yang berbeda kepada orang yang berbeda untuk sumber daya yang berbeda. Misalnya, Anda mungkin mengizinkan beberapa pengguna akses penuh ke Amazon EC2, Amazon S3, Amazon DynamoDB, Amazon Redshift, dan layanan AWS lainnya. Namun, untuk pengguna lain, Anda mungkin hanya mengizinkan akses hanya-baca ke beberapa bucket S3. Juga memebrikan izin kepada pengguna lain untuk hanya mengelola instance EC2.
#### IAM Komponen Penting
**Pengguna IAM**, seseorang atau aplikasi yang dapat mengautentikasi dengan akun AWS.
**Grup IAM**, Kumpulan pengguna IAM yang diberikan otorisasi identik.
**Kebijakan IAM**, dokumen yang menetapkan izin untuk menentukan apa yang dapat dilakukan pengguna di akun AWS. 
**IAM role**, alat untuk memberikan akses sementara ke sumber daya AWS tertentu dalam akun AWS.

#### IAM MFA
  Layanan dan sumber daya AWS dapat diakses dengan menggunakan AWS Management Console, AWS CLI, atau melalui SDK dan API. Untuk keamanan yang meningkat, sebaiknya aktifkan MFA. Dengan MFA, pengguna dan sistem harus memberikan token MFA—selain kredensial masuk biasa—sebelum mereka dapat mengakses layanan dan sumber daya AWS.
  Pilihan untuk membuat token autentikasi MFA mencakup aplikasi yang kompatibel dengan MFA virtual(seperti Google Authenticator atau Authy 2-Factor Authentication), perangkat kunci keamanan U2F, dan perangkat MFA perangkat keras.

#### Otorisasi tindakan apa saja yang diizinkan
  Otorisasi adalah proses menentukan izinapa yang harus diberikan oleh pengguna, layanan, atau aplikasi. Setelah pengguna diautentikasi, mereka harus diotorisasi untuk dapat mengakses layanan AWS. Pengguna IAM tidak memiliki izin untuk mengakses sumber daya atau data apa pun di akun AWS. Sebaliknya, Anda harus secara eksplisit memberikan izin kepada pengguna, grup, atau peran dengan membuatkebijakan,yang merupakan dokumen dalam format JavaScript Object Notation (JSON). Kebijakan daftar izin yang memungkinkanatau memblokir akses ke sumber daya di akun AWS.

#### IAM: Otorisasi
  Menetapkan izin kepada pengguna, grup, atau peran dengan membuat kebijakan IAM (atau menemukan kebijakan yang ada di akun). Tidak ada izin default, smua tindakan dalam akun ditolak untuk pengguna secara default (pemblokiran implisit) kecuali tindakan tersebut diizinkan secara eksplisit. Tindakan apapun yang tidak diizinkan secara eksplisit akan ditolak.

#### Kebijakan IAM
  Kebijakan IAM adalah dokumen yang mendefinisikan isin yang memberikan kontrol akses ketat.
Ada 2 jenis kebijakan, yaitu: **berbasis identitas** dan **berbasis sumber daya**.
- **Kebijakan berbasis identitas**, yang dilampirkan pada pelaku (atau identitas), seperti pengguna, peran, atau grup IAM. Kebijakan ini mengontrol tindakan apa yang dapat dilakukan identittas, pada sumber daya apa, dan dalam kondisi apa. Kebijakan identitas dapat dikategorikan lebih lanjut sebagai:
    - Kebijakan terkelola, kebijakan berbasis ientittas yang mandiri yang dapat diapmirkan pada beberapa pengguna, grup, dan peran dalam akun AWS.
    - Kebijakan inline, kebijakan yang dibuat dan kelola, dan yang tertaman secara langsung dalam grup atau peran pengguna tunggal.
- **Kebijakan berbasis sumber daya**,  yang dilampirkan pada sumber daya, seperti bucket Amazon S3. Kebijakan ini menentukan siapa yang dapat mengakses sumber daya dan tindakan apa yang dapat mereka lakukan padanya. Ditentukan sebagai **inline** saja, yang berarti bahwa kita menentukan kebijakan pada sumber daya itu sendiri, bukan membuat dokumen kebijakan IAM terpisah yang dilampirkan. 

#### Grup IAM
  Grup IAM adalah kumpulan pengguna IAM, digunakan untuk memberikan izin yang sama untuk beberapa pengguna, yang mempermudah pengelolaan izin ysng diberikan dengan melampirkan kebijakan atau kebijakan IAM ke grup. Karakteristik grup IAM:
  - dapat berisi banyak user, dan user dapat menjadi milik beberapa grup
  - grup tidak dapat ditumpuk, hanya dapat berisi user dan tidak dapat beriis grup lain.
  - tidak ada grup default yang secara oomatis menackup semua user di akun AWS.

#### IAM role
  IAM role adalah identitas IAM dengan izin khusus. IAM role dapat memiliki kebijakan izin yang melekat padanya, dan dapat digunakan untuk mendelegasikan akses sementara kepada pengguna atau aplikasi. IAM role mirip dengan pengguna IAM, yang dapat melampirkan kebijakan izinnya. IAM role berbeda dari pengguna IAM, yang tidak terkait secara khusu dengan satu orang dan ditujukan untuk dapat diasumsikan oleh orang, aplikasi, atau layanan. Dapat menggunakan peran yang menyeiakan kredensial keamanan sementara.

## - Mengamankan akun AWS baru
  Cara terbaik untuk mengamankan akun AWS:
- Amankan  login dengan otentikasi multifaktor (MFA).
- Hapus access key pengguna root akun.
- Membuat pengguna IAM individu dan memberikan izin sesuai dengan prinsip hak istimewa paling minim.
- Gunakan grup untuk menetapkan izin kepada pengguna IAM.
- Mengonfigurasi kebijakan kata sandi yang kuat.
- Delegasikan penggunaan peran, alih-alih pembagian kredensial.
- Pantau aktivitas akun menggunakan AWS CloudTrail.
## - Mengamankan akun 
  AWS Organizations adalah layanan manajemen akun yang memungkinkan Anda mengonsolidasikan beberapa akun AWS ke sebuahorganisasiyang Anda buat dan kelola secara terpusat. Di sini, fokusnya adalah pada fitur keamanan yang disediakan AWS Organizations. Salah satu fitur keamanan yang berguna adalah bahwa Anda dapat mengelompokkan akun ke unit organisasi(OU) dan melekatkan kebijakan akses yang berbeda untuk setiap OU.
  SCP menawarkan kontrol pusat atas izin maksimum yang tersediauntuk semua akun di organisasi Anda, sehingga memungkinkan Anda memastikan bahwa akun Anda tetap berada dalam pedoman kontrol akses organisasi Anda. SCP hanya tersedia di organisasi yang mengaktifkan semua fitur, termasuk tagihan terkonsolidasi.
  AWS Key Management Service (AWS KMS) adalah layanan yang memungkinkan Anda membuat dan mengelola kunci enkripsi, dan untuk mengontrol penggunaan enkripsi di berbagai layanan AWS dan aplikasi Anda. AWS KMS adalah layanan aman dan tangguh yang menggunakan modul keamanan perangkat keras (HSM) yang divalidasi di bawah Standar Pemrosesan Informasi Federal (FIPS) 140-2(atau sedang dalam proses divalidasi) untuk melindungi kunci Anda. AWS KMS juga terintegrasi dengan AWS CloudTrail guna menyediakan log untuk semua penggunaan kunci Anda untuk membantu memenuhi kebutuhan peraturan dan kepatuhan.
  Amazon Cognito membantu Anda memenuhi beberapa persyaratan keamanan dan kepatuhan, termasuk persyaratan untuk organisasi yang sangat diatur seperti perusahaan kesehatan dan perdagangan. Amazon Cognito memenuhi syarat untuk digunakan dengan US Health Insurance Portability and Accountability Act (HIPAA).
  AWS Shield adalah layanan perlindungan distributed denial of service (DDoS) terkelola yang melindungi aplikasi yang berjalan di AWS. AWS Shield menyediakan deteksi yang selalu aktif dan mitigasi inline otomatis yang meminimalkan waktu henti dan latensi aplikasi, jadi tidak perlu melibatkan AWS Support untuk mendapatkan manfaat dari perlindungan DDoS.
  AWS Shield Standard secara otomatis diaktifkan untuk semua pelanggan AWS tanpa biaya tambahan apa pun.AWS Shield Advanced adalah layanan berbayar opsional. AWS Shield Advanced memberikan perlindungan tambahan terhadap serangan yang lebih canggih dan lebih besar terhadap aplikasi Anda yang berjalan di Amazon EC2, Elastic Load Balancing, Amazon CloudFront, AWS Global Accelerator, dan Amazon Route 53. AWS Shield Advanced tersedia untuk semua pelanggan.
## - Mengamankan data di AWS
  Enkripsi data adalah alat penting untuk digunakan ketika tujuan Anda adalah untuk melindungi data digital. Enkripsi data mengambil data yang dapat dibaca dan mengodekannya sehingga tidak dapat dibaca oleh siapa pun yang tidak memiliki akses ke kunci rahasia yang dapat digunakan untuk memecahkan kode itu. Jadi, bahkan jika penyerang mendapatkan akses ke data Anda, mereka tidak bisa melakukan apa pun.Data saat istirahat mengacu pada data yang tersimpan secara fisik pada disk atau pita.
## - Berupaya Memastikan Kepatuhan
  AWS terlibat dengan badan penyertifikasi eksternal dan auditor independen untuk memberi pelanggan informasi yang memadai tentang kebijakan, proses, dan kontrol yang ditetapkan dan dioperasikan oleh AWS.Sebuah CantumanAWS Program Kepatuhantersedia secara lengkap. Juga, terkait detail tentang layanan AWS yang berada dalam lingkup program jaminan AWS, lihat Layanan AWS dalam Cakupan oleh Program Kepatuhan.
  AWS Config adalah layanan yang memungkinkan Anda mengakses, mengaudit, dan mengevaluasi konfigurasi sumber daya AWS Anda. AWS Config terus memantau dan mencatat konfigurasi sumber daya AWS Anda dan memungkinkan Anda mengautomasi evaluasi konfigurasi tercatat terhadap konfigurasi yang diinginkan. Dengan Aws Config, Anda dapat meninjau perubahan dalam konfigurasi dan hubungan antara sumber daya AWS, meninjau riwayat konfigurasi sumber daya detail, dan menentukan kepatuhan Anda secara keseluruhan terhadap konfigurasi yang ditentukan dalam pedoman internal Anda. Ini memungkinkan Anda menyederhanakan audit kepatuhan, analisis keamanan, manajemen perubahan, dan pemecahan masalah operasional.
  AWS Artifact menyediakan pengunduhan dokumen keamanan dan kepatuhan AWS sesuai permintaan, seperti sertifikasi ISO AWS, Payment Card Industry (PCI), dan laporan Service Organization Control (SOC). Anda dapat mengirimkan dokumen keamanan dan kepatuhan (juga dikenal sebagaiartefak audit) kepada auditor atau regulator Anda untuk menunjukkan keamanan dan kepatuhan infrastruktur dan layanan AWS yang Anda gunakan. Anda juga dapat menggunakan dokumen-dokumen ini sebagai pedoman untuk mengevaluasi arsitektur cloud Anda sendiri dan menilai keefektifan kontrol internal perusahaan Anda. AWS Artifact menyediakan dokumen tentang AWS saja. Pelanggan AWS bertanggung jawab mengembangkan atau memperoleh dokumen yang menunjukkan keamanan dan kepatuhan perusahaan mereka.

## ☁️ Knowledge Chapter 4
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/efe1d8d0-cd16-4f34-aadf-89f6c3514a3a)

