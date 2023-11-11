
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


[link](link)
