# Lapres Praktikum Modul 1 Jaringan Komputer
Kelompok A5 :
<li>05111840000138 - Gema Adi Perwira
<li>05111940000024 - Hanifa Fauziah
<li>05111940000111 - Evelyn Sierra

## Soal 1
## Soal 2
## Soal 3
## Soal 4
## Soal 5
## Soal 6
## Soal 7
## Soal 8
## Soal 9
## Soal 10

## Soal 11 
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80! 
### Jawaban : 
Ketik pada capture using this filter “Src port 80”. Lalu record dan buka website http bebas. Misalnya monta.if.its.ac.id, lalu lakukan aktivitas disana seperti mendownload file. Lalu paket akan otomatis muncul sesuai filter tadi seperti screenshot dibawah ini.

![soal11](https://user-images.githubusercontent.com/42856438/134634955-a6ffd64e-2e20-40c0-b5b0-bb774b920443.png)

## Soal 12
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
### Jawaban : 
Ketik “port 21” pada capture using this filter. Lalu klik 2x pada adapter for loopback traffic capture. Kemudian nyalakan filezilla pada xampp, lalu buka filezilla server.
![image](https://user-images.githubusercontent.com/42856438/134636368-c5d4ab40-f153-4f63-95ec-c60c8f27125a.png)

Lalu disitu kita klik menu edit dan add user dan password (bisa tanpa password). Kemudian buka filezilla client, ketik host “127.0.0.1”, username dan password yang telah dibuat, port “21”. Lalu klik quick connect. 
![image](https://user-images.githubusercontent.com/42856438/134636544-5f8ea596-514e-4c1d-8804-d00d4a54968b.png)

Lalu buka kembali wireshark dan akan otomatis muncul paket yang telah difilter.

![soal12](https://user-images.githubusercontent.com/42856438/134634977-7d44dcd4-c2e0-4861-bbb2-248f76dac47f.png)

## Soal 13
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
### Jawaban :
Jalankan dan record wireshark, lalu ketik pada display filter “tcp.dstport == 443”
![soal13](https://user-images.githubusercontent.com/42856438/134634986-b2831978-2ce7-444c-b3e6-7fa9cf105814.png)

## Soal 14
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
### Jawaban :
Ketik pada capture using this filter “Dst host kemenag.go.id”. Kemudian buka pada browser kalian websire kemenag.go.id, lalu kembali ke wireshark dan otomatis muncul paket yang telah difilter. 

![soal14](https://user-images.githubusercontent.com/42856438/134635027-08d430b3-cfa9-4e68-bec1-d7f29b85f552.png)

## Soal 15
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
### Jawaban : 
Cek IP melalui cmd dengan cara buka cmd lalu ketik ipconfig. 
![image](https://user-images.githubusercontent.com/42856438/134637041-292fc48e-153d-48d5-81e4-44ef9d5ce5c1.png)
IPv4 Address merupakan alamat IP kalian. IP bisa berbeda beda tergantung wifi yang digunakan. 
Kemudian buka wireshark dan ketik pada capture using this filter “Src host 192.168.1.28”(waktu itu IP saya 192.168.1.28). Kemudian jalankan, dan otomatis paket akan muncul sesuai filter. 
 
![soal15](https://user-images.githubusercontent.com/42856438/134635039-dd915d1c-d40c-47ae-9321-f940d2f40f31.png)
