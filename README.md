# Jarkom-Modul-1-IT25-2023

## Modul 1 Jarkom IT25

### Anggota :

- ANDYANA MUHANDHATUL NABILA - 5027211029
- ANDREAS TIMOTIUS PARHORASAN SIHOMBING - 5027211019

## No 1

### Soal

User melakukan berbagai aktivitas dengan menggunakan protokol FTP, untuk mendapatkan flagnya kita diminta untuk mengakses nc 10.21.78.111 12345 dan muncul soal Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?

### Analisis Soal

Dari soal, kita diminta untuk mencari sequence number (raw) dari aktivitas user yang menggunakan FTP

### Jawaban

Dalam menyelesaikan soal ini langkah pertama adalah mengakses nc untuk mendapatkan jawaban berupa flag. Dimana setelah memasukkan nc muncul soal yang harus dijawab untuk mendapatkan flagnya. Selanjutnya download file yang disediakan di soal dan buka file dengan wireshark.

[![JJTt02s.md.jpg](https://iili.io/JJTt02s.md.jpg)](https://freeimage.host/i/JJTt02s)
[![JJTtGp4.md.jpg](https://iili.io/JJTtGp4.md.jpg)](https://freeimage.host/i/JJTtGp4)

Karena kita diminta menganalisis user yang menggunakan protokol FTP jadi kita dapat mengfilter langsung dengan kata kunci ftp dalam wiresharknya dan kemudian muncul banyak aktivitas berupa request dan respon dalam protokol FTP. Kemudian kita cari satu" dan saya menemukannya di sini dalam line 147 berupa request karena bentuknya file zip sehingga saya mencoba memasukkan sequence number (raw) dan didapatkan petunjuk selanjutnya. dan didapatkan flagnya

[![JJTtEvf.md.jpg](https://iili.io/JJTtEvf.md.jpg)](https://freeimage.host/i/JJTtEvf)

## No 2

### Soal

Sebutkan web server yang digunakan pada portal praktikum jaringan komputer.

### Analisis Soal

dari soal kita diminta untuk mencari server apa sih yang digunakan portal praktikum jaringan komputer

### Jawaban

hal pertama adalah download file soal2. kemudian buka filenya dengan wireshark. selanjutnya adalah kita filter http untuk menemukan paket httpnya sehingga diketahui server apa yang digunakan

[![JJTm03F.md.jpg](https://iili.io/JJTm03F.md.jpg)](https://freeimage.host/i/JJTm03F)
[![JJTmc41.md.jpg](https://iili.io/JJTmc41.md.jpg)](https://freeimage.host/i/JJTmc41)

kemudian coba akses ncnya untuk mengetahui soal yang harus dijawab untuk mendapatkan flagnya

[![JJTm5QV.md.jpg](https://iili.io/JJTm5QV.md.jpg)](https://freeimage.host/i/JJTm5QV)

setelah ditemukan yaitu gunicorn maka kita inputkan sehingga mendapatkan flagnya

[![JJTmYCB.md.jpg](https://iili.io/JJTmYCB.md.jpg)](https://freeimage.host/i/JJTmYCB)

## No 3
#### Soal
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
nc 10.21.78.111 13590
#### Analisis Soal
Pada saat kita melakukan nc 10.21.78.111 13590 pada terminal diminta untuk menghitung banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702
#### Jawaban
dengan menggunakan query  (ip.src == 239.255.255.250 || ip.dst == 239.255.255.250) && udp.port == 3702 untuk memfilter paket, terdapat 16 


<a href="https://ibb.co/qW3Qb3d"><img src="https://i.ibb.co/xftTVtD/Screenshot-158.png" alt="Screenshot-158" border="0"></a>

Lalu ditanyakan juga protokal yang digunakan yaitu UDP
<a href="https://ibb.co/QvCZbLY"><img src="https://i.ibb.co/hFZk7b2/Screenshot-157.png" alt="Screenshot-157" border="0"></a>



## No 4

### Soal

Berapa nilai checksum yang didapatkan dari header pada paket nomor 130?

### Analisis Soal

dari soal kita diminta untuk mencari berapa sih nilai dari checksum pada header paket nomor 130

### Jawaban

Download terlebih dahulu file pada soal nomor 4 kemudian buka di wireshark. kemudian lakukan filter untuk menemukan paket nomor 130 dengan queri "frame.number == 130". Selanjutnya buka paket 130 dan lihat pada user diagram protokol kemudian ditemukan checksum 0x18e5.

[![JJTyemG.md.jpg](https://iili.io/JJTyemG.md.jpg)](https://freeimage.host/i/JJTyemG)

buka nc soal, dan masukkan checksum value yang telah ditemukan tadi sehingga flag didapatkan.

[![JJTyOes.md.jpg](https://iili.io/JJTyOes.md.jpg)](https://freeimage.host/i/JJTyOes)

## No 5
### Soal

### Analisis Soal
Pada soal 5 diberi 2 file yaitu file pcap dan zipfile yang berisi file .txt yang dikunci dengan sandi. 

### Jawaban
Pada saat TCP stream akan memberikan password yang sudah di enkripsi dengan base64

<a href="https://ibb.co/RDTqqrk"><img src="https://i.ibb.co/87gHHvL/Screenshot-159.png" alt="Screenshot-159" border="0"></a>

Pertama tama deskripsikan dulu dengan menggunakan base 64

<a href="https://ibb.co/BKc74mR"><img src="https://i.ibb.co/rfFLbgJ/Screenshot-160.png" alt="Screenshot-160" border="0"></a>

Masukan password pada file txt akan mendapatkan seperti gambar dibawah ini

<a href="https://ibb.co/mXzkK4m"><img src="https://i.ibb.co/VQBRGTd/Screenshot-161.png" alt="Screenshot-161" border="0"></a>

Pada saat connect akan ditanya beberapa pertanyaan

<a href="https://ibb.co/k41w0PY"><img src="https://i.ibb.co/X78KpGm/Screenshot-163.png" alt="Screenshot-163" border="0"></a>

Jawabannya ada pada wireshark yang pertama packet yang ditangkap ada 60 lalu soal kedua ditanyakan port apa yang digunakan yaitu port 25 dan yang terakhir ditanyakan ip public yang ada di pcap adalah 74.53.140.153

<a href="https://ibb.co/VYJMbL4"><img src="https://i.ibb.co/TMYPJw3/Screenshot-162.png" alt="Screenshot-162" border="0"></a>

## No 6
### Soal
PESAN TERSEMBUNYI

Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

### Analisis Soal
Pada soal diberitahukan server source address 7812 is invalid, dan ketika ditelusuri google menghasilkan a1 e5 u21

### Jawaban
coba lihat ip pada packet ke 7812, karena diberikan hint SOURCE ADDRESS ADALAH KUNCI SEMUANYA. lalu decode menggunakan A1Z26 yang diberikan pada hint

<a href="https://ibb.co/SB4Mcv0"><img src="https://i.ibb.co/rHRz3yM/Screenshot-171.png" alt="Screenshot-171" border="0"></a>

Masukan hasil dari chiper A1

<a href="https://ibb.co/qY8Z6Q3"><img src="https://i.ibb.co/7tD9hmd/Screenshot-169.png" alt="Screenshot-169" border="0"></a>

 


## No 7

### Soal

Berapa jumlah packet yang menuju IP 184.87.193.88?

### Analisis Soal

diminta untuk mencari jumlah packet pada IP 184.87.193.88?

### Jawaban

Download dan buka file pada soal di wireshark kemudian lakukan filtering dengan memasukkan kueri ip.dst == 184.87.193.88 dan hitung ada berapa packet, setelah dihitung kita mendapatkan jumlahnya ada 6 packet.

[![JJu9LFI.md.jpg](https://iili.io/JJu9LFI.md.jpg)](https://freeimage.host/i/JJu9LFI)

kemudian akses nc untuk memasukkan jawabannya sehingga kita dapatkan flagnya

[![JJu9i6N.md.jpg](https://iili.io/JJu9i6N.md.jpg)](https://freeimage.host/i/JJu9i6N)

## No 8
### Soal
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)!

### Jawaban 
tcp.dstport == 80 || udp.dstport == 80

<a href="https://ibb.co/Db1bqxg"><img src="https://i.ibb.co/VNLNK7p/Screenshot-164.png" alt="Screenshot-164" border="0"></a>

## No 9
### Soal
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
### Jawabannya

ip.src == 10.51.40.1 && ip.dst != 10.39.55.34

<a href="https://ibb.co/cxC7QMT"><img src="https://i.ibb.co/52nfLtc/Screenshot-165.png" alt="Screenshot-165" border="0"></a>

## No 10
### Soal
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet!

### Analisis soal
Soal berada pada kategori stream dan pada soal menyebutkan protokol Telnet

### Jawaban 
Melakukan TCP Stream pada protocol Telnet

<a href="https://ibb.co/gjCqc71"><img src="https://i.ibb.co/r7J8XtP/Screenshot-166.png" alt="Screenshot-166" border="0"></a>

Terdapat beberapa kredetial pada yang terlihat. Pada stream ke 15 bisa dilihat berbeda dari yang lain dengan password kesayangannyak0k0

<a href="https://ibb.co/6tD2xX7"><img src="https://i.ibb.co/94yJLZk/Screenshot-167.png" alt="Screenshot-167" border="0"></a>

untuk menemukan kredential yang tepat adalah menyamakan password yang ada pada stream ke 15

<a href="https://ibb.co/PgCynb9"><img src="https://i.ibb.co/qp18f4W/Screenshot-168.png" alt="Screenshot-168" border="0"></a>

