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
