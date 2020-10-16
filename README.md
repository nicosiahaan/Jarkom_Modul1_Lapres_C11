Oleh Kelompok C11

Aaron Astonvilla Rompis (0511184000131) <br>
Nikodemus Siahaan (05111840000151)


<b>Nomor 1</b>
 
Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

<b>jawab</b> 

filter http.host contains "testing.mekanis.me", lalu follow tcp stream

![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_123.png)

dan servernya: nginx/1.14.0 (Ubuntu)

<b>Nomor 2</b>
 
Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

<b>jawab</b> 

File -> export objects -> http
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_124.png)
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_125.png)

<b>Nomor 3</b>

Cari username dan password ketika login di "ppid.dpr.go.id"!

<b>jawab</b> 

Cari http host yg contains nya ppid dpr go id dan request method nya post karena Login

![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_126.png)

Sehingga username adalah 10pemuda dan password adalah guncangdunia

<b>Nomor 4</b>

Temukan paket dari web-web yang menggunakan basic authentication method!

<b>jawab</b> 

Comand: http.authbasic
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_127.png)

<b>Nomor 5<b>

Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng! 

<b>jawab</b> 

tulis di filter http.host contains "aku.pengen.pw" && http.authorization

![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_128.png)
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_129.png)
Sehingga username kakakgamtenk dan password hartatahtabermuda

<b>Nomor 6</b>

Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).

<b>jawab</b> 

ftp-data , lalu cari Answer.zip dan follow tcp stream, lalu diubah dari ASCII ke Raw dan save as answer.txt. Setelah itu cari password di zipkey.txt lalu follow tcp stream.
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_130.png)

<b>Nomor 7</b>

Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"

<b>jawab</b> 

ftp-data , lalu cari Answer.zip dan follow tcp stream, lalu diubah dari ASCII ke Raw dan save as answer.txt. Setelah itu cari password di zipkey.txt lalu follow tcp stream.
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_131.png)

<b>Nomor 8</b>

Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

<b>jawab</b> 

filter ftp.request.command == RETR
dan cari yang microsoft karena tersisa 2
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_132.png)
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_133.png)

<b>Nomor 9</b>

Cari username dan password ketika login FTP pada localhost!

<b>jawab</b> 

 Command : ftp.request.command == “USER”
 ![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_134.png)
 Ftp.request.command == “PASS”
 ![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_135.png)

<b>Nomor 10</b>

Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46" 

<b>jawab</b> 

Search filter dengan hex, lalu “25 50 44 46”, dan follow tcp stream, ubah ascii menjadi raw dan disave menjadi pdf
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_136.png)

<b>Nomor 11</b>

Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

<b>jawab</b> 

Connect filezilla dulu, lalu pada wireshark port 21 pada adapter for loopback traffic capture
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_137.png)

<b>Nomor 12</b>

Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

<b>jawab</b> 

tulis di display filter Src port 80
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_138.png)

<b>Nomor 13</b>

Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

<b>jawab</b> 

tulis di display filterDst port 443
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_139.png)

<b>Nomor 14</b>

Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

<b>jawab</b> 

pertama cari ip kita lalu tuliskan di display filter  Src host (ip), src host 172.20.10.3
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_140.png)

<b>Nomor 15</b>

Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

<b>jawab</b> 

Command wireshark awal menggunakan wifi, monta.if.its.ac.id
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_141.png)
