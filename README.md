# Jarkom-Modul-1-E12-2023

## Anggota Kelompok
- Andhika Lingga Mariano (5025211161)
- Beauty Valen Fajri (5025211227)

## Daftar Isi
- [Soal 1](#soal-1)
- [Soal 2](#soal-2)
- [Soal 3](#soal-3)
- [Soal 4](#soal-4)
- [Soal 5](#soal-5)
- [Soal 6](#soal-6)
- [Soal 7](#soal-7)
- [Soal 8](#soal-8)
- [Soal 9](#soal-9)
- [Soal 10](#soal-10)

## Soal 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
- Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 
- Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 
- Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
- Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

### Jawaban
Untuk mengambil packet dengan protokol FTP, dilakukan filter dengan menggunakan query **ftp**. 

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154668064466554980/image.png">

Setelah ditelusuri, diperoleh packet request dengan command STOR beserta packet response nya.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154668365781147720/image.png">

Packet request tersebut memiliki Sequence number (raw) **258040667** dan Acknowledge number (raw) **1044861039**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154667569047949322/image.png">

Sementara packet response nya memiliki Sequence number (raw)  **1044861039** dan Acknowledge number (raw) **258040696**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154667568825638922/image.png">

Berikut hasil percobaan pada terminal.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154670163405320233/image.png">

### Kendala yang dialami
Sempat kesulitan dalam mencari packet yang sesuai.

## Soal 2
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

### Jawaban
Pertama dilakukan filter dengan menggunakan query **http**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154675517425991701/image.png">

Diperoleh server yang digunakan adalah **gunicorn**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154675313842847744/image.png">

Berikut hasil percobaan pada terminal.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154676509265641563/image.png">

### Kendala yang dialami
Tidak ada, karena nama server yang digunakan dapat langsung diketahui dari packet http.

## Soal 3
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
- Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
- Protokol layer transport apa yang digunakan?

### Jawaban
Untuk menangkap packet dengan IP source maupun destination address 239.255.255.250 dan port 3702, dilakukan filter dengan query **(ip.src == 239.255.255.250 && udp.port == 3702) || (ip.dst == 239.255.255.250 && udp.port == 3702)**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154678455678550058/image.png">

Sementara untuk protokol yang digunakan dapat dilihat pada bagian protocol.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154678762919710760/image.png">

Berikut hasil percobaan pada terminal.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154678455942774855/image.png">

### Kendala yang dialami
Sempat kesulitan dalam menemukan syntax yang sesuai untuk melakukan filter.

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

Tidak ada, karena ketentuan nilai checksum tertera langsung pada paket nomor 130.

## Soal 5
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
- Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
- Port berapakah pada server yang digunakan untuk service SMTP?
- Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

### Jawaban
Untuk mendapatkan password zip file, follow TCP stream dari packet yang bertuliskan "*Pass: ...*".

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154691139895566377/image.png">

Diperoleh pesan sebagai berikut.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154691351842148392/image.png">

Password yang diperoleh adalah **NWltcGxlUGFzNXdvcmQ**, namun harus didecode terlebih dahulu menggunakan Base64.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154694124381929513/image.png">

Diperoleh password untuk membuka zip file adalah **5implePas5word**. Di dalam zip file tersebut terdapat sebuah txt file berisi instance yang diperlukan untuk menjawab pertanyaan.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154695449714905170/image.png">

Terdapat **60 packet** yang tercapture di dalam file pcap.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154695961239633983/image.png">

Port yang digunakan untuk service SMTP adalah **25**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154696461670424606/image.png">

Sementara IP yang merupakan public IP adalah **74.53.140.153**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154697054703067156/image.png">

Berikut hasil percobaan pada terminal.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154697359452803092/image.png">

### Kendala yang dialami
Sempat kesulitan dalam mencari paket yang mengandung password karena harus dicek satu per satu.

## Soal 6
Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan **"server SOURCE ADDRESS 7812 is invalid"**. ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

### Jawaban
Dari soal di atas, terdapat 2 buah petunjuk yang dapat digunakan untuk menyelesaikan soal.

- Dapat dilihat bahwa beberapa huruf kapital yang tersebar secara acak. Jika digabungkan, maka akan diperoleh kata "SUBSTITUSI".
- Dari hasil pencarian yang hanya menampilkan a1 e5 u21, dapat diambil kesimpulan bahwa perlu dilakukan substitusi dari huruf menjadi angka atau dari angka menjadi huruf.

Pada soal juga disebutkan bahwa terdapat kode invalid yang bertuliskan "server SOURCE ADDRESS 7812 is invalid". Dengan begitu, kita perlu mengambil source address dari packet nomor 7812 di dalam file pcapng.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154699050327736360/image.png">

Diperoleh source address nya adalah 104.18.14.101. Address ini selanjutnya akan disubstitusi ke dalam huruf.

10 = J <br>
4 = D <br>
18 = R <br>
14 = N <br>
10 = J <br>
1 = A

Kode yang diperoleh adalah **JDRNJA**.

Berikut hasil percobaan pada terminal. 

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154703037546373241/image.png">

### Kendala yang dialami
Sudah menemukan clue untuk melakukan substitusi namun tidak kepikiran untuk mengambil source address dari packet nomor 7812. 

## Soal 7
Berapa jumlah packet yang menuju IP 184.87.193.88?

### Jawaban

Untuk menyelesaikan permasalahan tersebut, dalam file yang telah dibuka pada wireshark maka lakukan filter menggunakan ip.dst == 184.87.193.88 seperti pada bukti berikut

<img width="1440" alt="Screen Shot 2023-09-21 at 13 43 23" src="https://github.com/Deekuh/Jarkom-Modul-1-E12-2023/assets/114421539/6d4229de-5b33-4757-85af-80781eca26be">

Dalam konteks ip.dst == 184.87.193.88 memiliki penjabaran yaitu :
  - "ip" mengacu pada protokol IP (Internet Protocol).
  - "dst" merupakan singkatan dari "destination" yang berarti alamat tujuan.
  - "==" digunakan untuk membandingkan apakah alamat tujuan dari paket tersebut sama dengan "184.87.193.88."

Dengan menggunakan konteks tersebut sebagai query filter, maka akan mendapatkan semua paket yang ditujukan ke alamat IP 184.87.193.88. 

<img width="1440" alt="Screen Shot 2023-09-21 at 13 43 37" src="https://github.com/Deekuh/Jarkom-Modul-1-E12-2023/assets/114421539/dcfef30e-efd1-4771-be30-06cbcabf3509">

Dari hasil diatas, didapatkan jumlah paket yang ditujukan ke alamat IP 184.87.193.88 ada sebanyak 6. Berikut hasil percobaan pada terminal

<img width="567" alt="Screen Shot 2023-09-21 at 13 44 06" src="https://github.com/Deekuh/Jarkom-Modul-1-E12-2023/assets/114421539/4cd3b42b-d2a8-4494-9d8a-c8f1190cb528">

### Kendala yang dialami

Tidak ada, karena setelah kita filter menggunakan query pada file tersebut maka packet-packet yang menuju IP 184.87.193.88 akan ditampilkan dan akan langsung bisa menghitung jumlah packet yang menuju IP 184.87.193.88.

## Soal 8
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)

### Jawaban
Untuk mengambil semua protokol paket yang menuju port 80, dilakukan filter dengan menggunakan query **tcp.dstport == 80 || udp.dstport == 80**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154703595694989362/image.png">

Berikut hasil percobaan pada terminal. 

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154703851857911908/image.png">

### Kendala yang dialami
Sempat kesulitan dalam menemukan syntax yang sesuai untuk melakukan filter.


## Soal 9
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!

### Jawaban
Untuk mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34, dilakukan filter dengan menggunakan query **ip.src == 10.51.40.1 && ip.dst != 10.39.55.34**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154704886605291550/image.png">

Berikut hasil percobaan pada terminal. 

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154704886366208000/image.png">

### Kendala yang dialami
Sempat kesulitan dalam menemukan syntax yang sesuai untuk melakukan filter.

## Soal 10
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet

### Jawaban
Pertama dilakukan filter dengan menggunakan query **telnet**.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154705605785821274/image.png">

Setelah ditelusuri, diperoleh kredensial berupa username dan password sebagai berikut.

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154705606016512032/image.png">

Berikut hasil percobaan pada terminal. 

<img src="https://cdn.discordapp.com/attachments/1102231088945963098/1154706184574599209/image.png">

### Kendala yang dialami
Sempat kesulitan dalam mencari paket yang mengandung kredensial karena harus dicek satu per satu.