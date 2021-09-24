# Lapres Praktikum Modul 1 Jaringan Komputer
Kelompok A5 :
<li>05111840000138 - Gema Adi Perwira
<li>05111940000024 - Hanifa Fauziah
<li>05111940000111 - Evelyn Sierra


## Soal 1
Sebutkan webserver yang digunakan pada "ichimarumaru.tech"
### Jawaban : 
Pada kolom display filter tuliskan `http.host == "ichimarumaru.tech"`. Setelah itu klik salah satu paket http yang ada, klik kanan lalu pilih follow. Lalu, pilih HTTP stream. 
Nantinya akan muncul kotak dialog seperti gambar yang dibawah ini.
![image](https://user-images.githubusercontent.com/80946219/134697547-facaf6d1-3e69-472e-8a2f-41d6e603bcff.png)

Web server yang digunakan oleh ichimarumaru.tech ada dibagian dengan tulisan server.
![image](https://user-images.githubusercontent.com/80946219/134697682-8b49e5ba-ee6d-4999-a579-2504b1295262.png)

Dari gambar diatas, bisa dilihat bahwa ichimarumaru.tech menggunakan webserver **nginx/1.18.0 (Ubuntu)**.
 
## Soal 2
Temukan paket dari web-web yang menggunakan basic authentication method!
### Jawaban : 
Pada kolom display filter tuliskan `http.authbasic`. Setelah itu, tekan enter, maka akan muncul 3 paket yang ada.
![image](https://user-images.githubusercontent.com/80946219/134698252-f100b7bd-ce57-42ab-a6a6-359ae14f1b55.png)

## Soal 3
Ikuti perintah di `basic.ichimarumaru.tech`! Username dan password bisa didapatkan dari file .pcapng!
### Jawaban : 
Pada kolom display filter ketik `http.authbasic && http.host contains "basic.ichimarumaru.tech"` lalu pilih bagian meme.png. Maka akan muncul tampilan seperti dibawah ini.
![image](https://user-images.githubusercontent.com/80946219/134699298-f6d36ca7-af77-444e-a33a-adddace1f069.png)

Setelah itu, dropdown pada bagian Hypertext Transfer Protocol, lalu dropdown lagi pada bagian authorization. Maka akan muncul username dan passwordnya.
![image](https://user-images.githubusercontent.com/80946219/134699660-2b3d7989-59ba-4da5-b9e0-57ac3436d160.png)

Bisa dilihat dari gambar diatas,
 
Username : kuncimenujulautan
 
Password : tQKEJFbgNGC1NCZlWAOjhyCOm6o3xEbPkJhTciZN
 
Ketika username dan password dimasukkan pada portal `basic.ichimarumaru.tech`. 
![image](https://user-images.githubusercontent.com/80946219/134700042-2a856944-d88d-4041-9017-8d65ba53221c.png)
 
Maka akan muncul tampilan seperti berikut ini.
![image](https://user-images.githubusercontent.com/80946219/134700162-9318e240-4d7c-4cb7-be2c-3e565bf516e6.png)

Jawaban dari pertanyaan yang ditampilkan adalah sebagai berikut.
![image](https://user-images.githubusercontent.com/80946219/134700630-b667832e-400f-4a5b-911a-2d1bbd959ba1.png)

Referensi jawabnya berasal dari modul 1 berikut ini.
 
![image](https://user-images.githubusercontent.com/80946219/134700487-6528ae6f-5c6a-4d83-8763-3962cd8e161d.png)

## Soal 4
Temukan paket mysql yang mengandung perintah query select!
### Jawaban : 
Pada kolom display filter ketik `mysql.query contains SELECT || mysql.query contains select` lalu enter. Maka akan muncul tampilan seperti dibawah ini.
![image](https://user-images.githubusercontent.com/80946219/134701912-7c0e5fd8-00bc-4c3b-a68c-48b660081ab6.png)

Ketiga paket yang ada di gambar merupakan paket yang mengandung perintah query select.
 
## Soal 5
Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!
### Jawaban : 
Pada kolom display filter ketik `mysql.query contains INSERT || mysql.query contains insert` lalu enter. Maka akan muncul tampilan seperti dibawah ini.
![image](https://user-images.githubusercontent.com/80946219/134702387-ed689d30-37a5-4a5b-b8f5-d6ffb1b5cf75.png)

Dropdown bagian MySQL Protocol dan Request Command Query.
![image](https://user-images.githubusercontent.com/80946219/134702547-463b4fbc-fde3-42bb-a6c6-921669e19266.png)

Terlihat dari gambar diatas bahwa,
 
Username : akakanomi
 
Password : pemisah4lautan

Ketika username dan password dimasukkan pada portal `portal.ichimarumaru.tech`.
![image](https://user-images.githubusercontent.com/80946219/134702930-59c42ba4-0dd9-433f-a864-18d1feade6a7.png)

Maka akan muncul tampilan seperti berikut.
![image](https://user-images.githubusercontent.com/80946219/134702998-babd4df4-f7d3-4fa6-b267-e1ae1ced0163.png)

Jawaban dari pertanyaan yang ditampilkan adalah sebagai berikut.
![image](https://user-images.githubusercontent.com/80946219/134703359-80a67209-f719-4ada-a102-5de82f30081a.png)

Referensi jawabnya berasal dari modul 1 berikut ini.
 
![image](https://user-images.githubusercontent.com/80946219/134703101-42259d3e-a857-4918-bd22-64493c44ac6b.png)
 
## Soal 6
Cari username dan password ketika melakukan login ke FTP Server!
### Jawaban :
 ftp.request.command == USER || ftp.request.command == PASS
 
## Soal 7
Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")
 ### Jawaban :
 Frame contains “Real.pdf”, klik kanan tekan follow -> tcp stream -> show data as Raw. Simpan file Save as [nama].zip
 
## Soal 8
Cari paket yang menunjukan pengambilan file dari FTP tersebut!
 ### Jawaban :
 ftp.request.command contains "RETR"
 
## Soal 9
Dari paket-paket yang menuju FTP terdapat indikasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!
 ### Jawaban :
 ketik ftp-data, cari secret.zip, klik kanan, follow -> tcp stream, show and save data as RAW, dan simpan dengan nama secret.zip
 
## Soal 10
Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!
 ### Jawaban :
 ketik ftp-data, cari secret.zip, klik kanan, follow -> tcp stream, show and save data as RAW, dan simpan dengan nama secret.zip
ketik ftp-data, cari history.txt. 

 Isi file wanted.pdf
 

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
