# Jarkom-Modul-1-E12-2023

## Anggota Kelompok
- Andhika Lingga Mariano (5025211161)
- Beauty Valen Fajri (5025211227)

## Soal 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
- Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 
- Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 
- Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
- Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

### Jawaban

### Kendala yang dialami

## Soal 2
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

### Jawaban

### Kendala yang dialami

## Soal 3
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
- Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
- Protokol layer transport apa yang digunakan?

### Jawaban

### Kendala yang dialami

## Soal 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?

### Jawaban

Untuk menyelesaikan permasalahan tersebut, dalam file yang telah dibuka pada wireshark maka lakukan pengecekan header pada paket nomor 130

<img width="1440" alt="Screen Shot 2023-09-21 at 13 33 11" src="https://github.com/Deekuh/Jarkom-Modul-1-E12-2023/assets/114421539/93d25fe5-a738-4214-9828-ab8b8840119d">

Didapatkan paket nomor 130 dengan beberapa rincian yang ada. Untuk melihat nilai checksum. Maka bisa dilihat lebih rinci pada 'User Datagram Protocol'. Checksum adalah sebuah nilai numerik yang dihasilkan dari data yang digunakan untuk memeriksa integritas data tersebut. Checksum sangat berguna untuk memastikan keintegritasan data dalam berbagai situasi, termasuk pengiriman data melalui jaringan, penyimpanan data di perangkat penyimpanan, dan verifikasi integritas berkas yang diunduh dari internet. Rincian data seperti berikut

<img width="459" alt="Screen Shot 2023-09-21 at 13 33 11" src="https://github.com/Deekuh/Jarkom-Modul-1-E12-2023/assets/114421539/36c72ae4-194b-4a96-a4a5-c0167ba90f89">

Maka didapatkan untuk nilai checksum yang terdapat pada paket nomor 130 yakni 0x18e5. Berikut hasil percobaan pada terminal

<img width="572" alt="Screen Shot 2023-09-21 at 13 33 51" src="https://github.com/Deekuh/Jarkom-Modul-1-E12-2023/assets/114421539/74b93dc4-9056-492e-b1c5-1878a2d8f681">

### Kendala yang dialami

## Soal 5
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
- Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
- Port berapakah pada server yang digunakan untuk service SMTP?
- Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

### Jawaban

### Kendala yang dialami

## Soal 6
Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan **"server SOURCE ADDRESS 7812 is invalid"**. ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

### Jawaban

### Kendala yang dialami

## Soal 7
Berapa jumlah packet yang menuju IP 184.87.193.88?

### Jawaban

Untuk menyelesaikan permasalahan tersebut, dalam file yang telah dibuka pada wireshark maka lakukan filter menggunakan ip.dst == 184.87.193.88 seperti pada bukti berikut

<img width="1440" alt="Screen Shot 2023-09-21 at 13 43 23" src="https://github.com/Deekuh/Jarkom-Modul-1-E12-2023/assets/114421539/6d4229de-5b33-4757-85af-80781eca26be">

Dalam konteks ip.dst == 184.87.193.88 memiliki penjabaran yaitu :
  - "ip" mengacu pada protokol IP (Internet Protocol).
  - "dst" merupakan singkatan dari "destination" yang berarti alamat tujuan.
  - "==" digunakan untuk membandingkan apakah alamat tujuan dari paket tersebut sama dengan "184.87.193.88."

Dengan menggunakan konteks tersebut sebagai kueri filter, maka akan mendapatkan semua paket yang ditujukan ke alamat IP 184.87.193.88. 

<img width="1440" alt="Screen Shot 2023-09-21 at 13 43 37" src="https://github.com/Deekuh/Jarkom-Modul-1-E12-2023/assets/114421539/dcfef30e-efd1-4771-be30-06cbcabf3509">

Dari hasil diatas, didapatkan jumlah paket yang ditujukan ke alamat IP 184.87.193.88 ada sebanyak 6. Berikut hasil percobaan pada terminal

<img width="567" alt="Screen Shot 2023-09-21 at 13 44 06" src="https://github.com/Deekuh/Jarkom-Modul-1-E12-2023/assets/114421539/4cd3b42b-d2a8-4494-9d8a-c8f1190cb528">

### Kendala yang dialami

## Soal 8
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

### Jawaban

### Kendala yang dialami


## Soal 9
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

### Jawaban

### Kendala yang dialami


## Soal 10
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

### Jawaban

### Kendala yang dialami
