Oleh Kelompok C11

Aaron Astonvilla Rompis (0511184000131) <br>
Nikodemus Siahaan (05111840000151)


<b>Nomor 1<b>
 
Sebutkan webserver yang digunakan pada "testing.mekanis.me"!
 
filter http.host contains "testing.mekanis.me", lalu follow tcp stream

![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_123.png)

dan servernya: nginx/1.14.0 (Ubuntu)

<b>Nomor 2
 
Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

File -> export objects -> http
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_124.png)
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_125.png)

<b>Nomor 3<b>

Cari username dan password ketika login di "ppid.dpr.go.id"!
Cari http host yg contains nya ppid dpr go id dan request method nya post karena Login

![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_126.png)

Sehingga username adalah 10pemuda dan password adalah guncangdunia

4. Temukan paket dari web-web yang menggunakan basic authentication method!
Comand: http.authbasic
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_127.png)

5. Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng! 
tulis di filter http.host contains "aku.pengen.pw" && http.authorization

![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_128.png)
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_129.png)
Sehingga username kakakgamtenk dan password hartatahtabermuda

6. Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).

ftp-data , lalu cari Answer.zip dan follow tcp stream, lalu diubah dari ASCII ke Raw dan save as answer.txt. Setelah itu cari password di zipkey.txt lalu follow tcp stream.
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_130.png)

7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"

ftp-data , lalu cari Answer.zip dan follow tcp stream, lalu diubah dari ASCII ke Raw dan save as answer.txt. Setelah itu cari password di zipkey.txt lalu follow tcp stream.
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_131.png)

8. Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!

filter ftp.request.command == RETR
dan cari yang microsoft karena tersisa 2
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_132.png)
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_133.png)

9. Cari username dan password ketika login FTP pada localhost!

 Command : ftp.request.command == “USER”
 ![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_134.png)
 Ftp.request.command == “PASS”
 ![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_135.png)

10. Cari file .pdf di wireshark lalu download dan buka file tersebut!
clue: "25 50 44 46" 

Search filter dengan hex, lalu “25 50 44 46”, dan follow tcp stream, ubah ascii menjadi raw dan disave menjadi pdf
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_136.png)

11. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

Connect filezilla dulu, lalu pada wireshark port 21 pada adapter for loopback traffic capture
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_137.png)

12. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

tulis di display filter Src port 80
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_138.png)


13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

tulis di display filterDst port 443
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_139.png)

14. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

pertama cari ip kita lalu tuliskan di display filter  Src host (ip), src host 172.20.10.3
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_140.png)

15. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!

Command wireshark awal menggunakan wifi, monta.if.its.ac.id
![alt text](https://github.com/nicosiahaan/Jarkom_Modul1_Lapres_C11/blob/main/img/Screenshot_141.png)
