
# CLOUD COMPUTING - AWS Cloud Foundation Chapter 5 [Pemateri: Tiara Dwi Maulita Sari]
## Chapter 5 - Networking and Content Delivery
## Introduction
- Dasar-dasar jaringan
- Amazon VPC
- Jaringan VPC
- Keamanan VPC
- Amazon Route S3
- Amazon CloudFront

## - Dasar-dasar jaringan
  Jaringan komputer adalah dua mesin klien atau lebih yang terhubung bersama-sama untuk berbagi sumber daya. Sebuah jaringan dapat secara logis dipartisi menjadi subnet. Jaringan memerlukan perangkat jaringan (seperti perute atau switch) untuk menghubungkan semua klien bersama-sama dan memungkinkan komunikasi antarklien.
  Setiap mesin klien dalam jaringan memiliki alamat Internet Protocol (IP) yang unik yang mengidentifikasinya. Alamat IP adalah label numerik dalam format desimal. Mesin mengonversi angka desimal ke format biner.
  
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/c8598e0f-7458-42fb-9112-fb6fe0a18b46)

  Alamat IP 32 bit disebut sebagai alamat IPv4. Alamat IP 128 bit juga disebut sebagai alamat IPv6, alamat IPv6 dapat menampung lebih banyak perangkat pengguna.
  Alamat IPv6 terdiri dari 8 grup 4 huruf dan angka yang dipisahkan oleh titik dua (:). Masing-masing dari delapan grup alamat IPv6 yang dipisahkan titik dua mewakili 16 bit dalam format angka heksadesimal. Itu berarti masing-masing dari delapan grup tersebut bisa apa saja dari 0 sampai FFFF. Total gabungan dari delapan grup untuk alamat IPv6 adalah 128 bit dalam format biner
  Metode umum untuk mendeskripsikan jaringan adalah Classless Inter-Domain Routing (CIDR). Alamat CIDR dinyatakan sebagai berikut:
  - Alamat IP (yang merupakan alamat pertama jaringan)
  - Selanjutnya, karakter garis miring (/)
  - Terakhir, nomor yang memberitahu Anda berapa banyak bit awalan perutean yang harus ditetapkan atau dialokasikan untuk pengidentifikasi jaringan
  Bit yang tidak tetap diperbolehkan untuk berubah. CIDR adalah cara untuk mengekspresikan grup alamat IP yang berturut-turut satu sama lain. Jika CIDR adalah 192.0.2.0/16, angka terakhir (16) memberitahu Anda bahwa 16 bit pertama harus ditetapkan. 16 bit terakhir bersifat fleksibel, yang berarti bahwa 216(atau 65.536) alamat IP tersedia untuk jaringan dengan rentang 192.0.0.0 hingga 192.0.255.255. Angka desimal ketiga dan keempat masing-masing dapat berubah dari 0 hingga 255.

## - Amazon VPC
![image](https://github.com/fiakholida/100DaysOfCloud/assets/140806089/e1f3dced-c3d9-4a9e-8580-24136fb0df61)
  Amazon Virtual Private Cloud (VPC) adalah layanan yang memungkinkan menyediakan bagian yang terisolasi secara logis dari AWS Cloud tempat kalian dapat meluncurkan sumber daya AWS pada jaringan virtual yang di tentukan.
  Amazon VPC memberikan kontrol atas sumber daya jaringan virtual, termasuk pemilihan rentang alamat IP, pembuatan subnet, serta konfigurasi tabel rute dan gateway jaringan. Memungkinkan kustomisasi konfigurasi jaringan untuk VPC. Juga dapat menggunakan beberapa lapis keamanan untuk mengontrol akses ke instans Amazon Elastic Compute Cloud (Amazon EC2) dalam setiap subnet.

### VPC & Subnet
  - VPC
    - Terisolasi secara logis dari VPC lain
    - Didedikasikan untuk akun AWS
    - Bagian dari satu Wilayah AWS dan dapat menjangkau beberapa Availabilit Zone
  - Subnet
    - Rentang alamat IP yang membagi VPC
    - Bagian dari satu Availability Zone
    - Diklasifikasikan sebagai publik atau privat

### Pemberian alamat IP
  - Menetapkan ke blok CIDR IPv4 (rentang alamat IPv4 privat)
  - Tidak dapat mengubah rentang alamat setelah membuat VPC
  - Ukuran blok CIDR IPv4 terbesar yaitu /16
  - Ukuran blok CIDR IPv4 terkecil yaitu /28
  - IPv6 juga didukung (dengan batas ukuran blok yang berbeda)
  - Blok CIDR subnet tidak dapat tumpang tindih

### Alamat IP yang dicadangkan
AWS mencadangkan alamat IP untuk:
- Alamat jaringan
- Perute lokal VPC (komunikasi internal)
- Resolusi Domain Name System (DNS)
- Penggunaan di masa mendatang
- Alamat siaran jaringan

### Jenis alamat IP publik
Alamat IPv4 publik
- Ditetapkan secara manual melalui alamat IP Elastis
- Ditetapkan secara otomatis melalui pengaturan penetapan alamat IP publik otomatis di tingkat subnet

Alamat IP elastis
  - Berkaitan dengan akun AWS
  - Dapat dialokasikan dan dipetakan ulang kapan saja
  - Biaya tambahan mungkin berlaku
### Antarmuka jaringan elastis
  Antarmuka jaringan elastis adalah antarmuka jaringan virtual yang dapat di lampirkan ke sebuah instans, juga dilepaskan dari instans dan dilampirkan ke instans lain untuk mengarahkan lalu lintas jaringan.
  Setiap instans dalam VPC memliki antarmuka jaringan default yang ditetapkan alamat IPv4 pribadi dari rentang alamat IPv4 dari VPC, tidak dapat melepaskan antarmuka jaringan utama dari instans tetapi dapat membuat dan melampirkan antarmuka jaringan tambahan untuk setiap instans di VPC.

### Tabel rute dan rute
  Tabel rute berisi sekumpulan aturan (atau rute) yang dapat dikonfigurasikan untuk mengarahkan lalu lintas jaringan dari subnet. Setiap rute menentukan tujuan dan target. Secara default, setiap tabel rute berisi rute lokal untuk komunikasi di dalam VPC. Setiap subnet dalam VPC harus diasosiasikan dengan tabel rute (maks 1).

## Jaringan VPC
### Gateway Internet
  gateway internet adalah komponen VPC yang dapat diskalakan, redundan, dan tersedia dengan sangat baik yang memungkinkan komunikasi antara instans di VPC dan internet. Gateway internet memiliki dua tujuan: untuk memberikan target dalam tabel rute VPC Anda untuk lalu lintas yang dapat dirutekan internet, dan untuk melakukan penerjemahan alamat jaringan untuk instans yang telah ditetapkan alamat IPv4 publik.
### Gateway network address translation (NAT)
  Gatewaynetwork address translation (NAT)  memungkinkan instans dalam subnet privat untuk terhubung ke internet atau layanan AWS lainnya, tetapi mencegah internet untuk memulai koneksi dengan instans.
  Untuk membuat gateway NAT, Anda harus menentukan subnet publik di mana gateway NAT seharusnya berada. Anda juga harus menentukan alamat IP Elastis untuk mengaitkannya dengan gateway NAT saat Anda membuatnya. Setelah Anda membuat gateway NAT, Anda harus memperbarui tabel rute yang terkait dengan satu atau lebih subnet privat Anda untuk mengarahkan lalu lintas yang terikat internet ke gateway NAT. Dengan demikian, instans di subnet privat Anda dapat berkomunikasi dengan internet.
### Berbagi  VPC
  Berbagi VPC memungkinkan pelanggan berbagi subnet dengan akun AWS lainnya dalam organisasi yang sama di AWS Organizations. Berbagi VPC memungkinkan beberapa akun AWS untuk membuat sumber daya aplikasi mereka -seperti Amazon EC2 instance, basis data Amazon Relational Database Service (Amazon RDS), kluster Amazon Redshift, dan fungsi AWS Lambda—ke dalam VPC bersama yang dikelola secara terpusat. Berbagi VPC menawarkan beberapa manfaat:
  - Pemisahan tugas, struktur VPC yang dikendalikan secara terpussat, perutean, alokasi alamat IP
  - Kepemilikan, pemilik apk terus memiliki sumber daya, akun, dan grup keamanan.
  - Grup keamanan, peserta berbagi VPC dapat mereferensikan ID grup keamanan satu sama lain
  - Efisiensi, Kepadatan yang lebih tinggi di subnet, penggunaan VPN dan AWS Direct Connect
  - Tanpa batas langsung, batas langsung dapat dihindari, misal 50 antarmuka virtual per koneksi AWS Direct Connect melalui arsitektur jaringan yang disederhanakan
  - Pengoptimalan biaya -Biaya dapat dioptimalkan melalui penggunaan kembali gateway NAT, endpoint antarmuka VPC, dan lalu lintas antar-Availability Zone
[link](link)
