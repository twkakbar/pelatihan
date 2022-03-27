<h1>Instalasi Apache2 dan Tunneling</h1>
<h2>Langkah 1 - Setting IP</h2>
1. Kita harus men-setting IP terlebih dahulu jika menggunakan jaringan bridge, maka kita gunakan IP dalam satu network dengan cara masukkan perintah berikut: <p>
  
```
sudo nano /etc/netplan/00-installer-config.yaml
```
Kemudian akan muncul sebagai berikut dan ubah IP nya<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar1.jpg" alt="Alt text" title="Gambar 1"><p>
2. Setelah selesai men-setting IP maka kita coba gunakan perintah `ping google.com` untuk mengetes koneksi dan jika berhasil maka akan muncul seperti gambar berikut<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar2.jpg" alt="Alt text" title="Gambar 2"><p>

<h2>Langkah 2 - Instalasi Apache2</h2>
1. Untuk mengecek IP yang sudah kita ubah tadi kita akan coba dengan remote server. Caranya dengan perintah berikut

```
ssh twk@192.168.1.6
```
Untuk twk kalian ganti dengan username Ubuntu Server kalian sendiri, jika ssh berhasil maka akan muncul seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar3.jpg" alt="Alt text" title="Gambar 3"><p>
2. Kembali ke Ubuntu Server, langkah pertama yang harus kita lakukan pada saat sedang di server yaitu update dan upgrade terlebih dahulu agar system kita up-to-date dengan cara
  
```
sudo apt update; sudo apt upgrade
```
3. Setelah update dan upgrade selanjutnya kita akan mulai menginstall Apache2 dengan menggunakan perintah:

```
sudo apt install apache2
```
ketika muncul "Do you want to continue?" ketik y dan enter maka instalasi akan mulai berjalan<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar6.jpg" alt="Alt text" title="Gambar 6"><p>
Jika sudah muncul seperti gambar berikut maka instalasi Apache2 sudah berhasil<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar7.jpg" alt="Alt text" title="Gambar 7"><p>
4. Selanjutnya kita akan mengecek status apache2 apa sudah aktif atau belum dengan perintah:

```
sudo systemctl status apache2
```
Jika apache2 berhasil Aktif/Running maka akan muncul seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar8.jpg" alt="Alt text" title="Gambar 8"><p>
Dan kita juga kita akan mengecek apache2 di web browser apakah berjalan<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar10.png" alt="Alt text" title="Gambar 10"><p>
Dan instalasi Apache2 Sukses!<p>

<h2>Langkah 3 - Localtunnel</h2>
1. Lakukan instalasi node.js menggunakan nvm, dan untuk melakukannya kita harus install curl terlebih dahulu menggunakan perintah berikut

```
sudo apt install curl
```
2. Kemudian setelah install curl maka kita akan mendownload nvm menggunakan curl dengan cara

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
3. Kemudian lakukan eksekusi bash dan instalasi nvm dengan cara

```
exec bash
```
```
nvm install 14
```
4. Untuk mengecek apakah instalasi node.js dan nvm berhasil maka gunakan perintah berikut

```
node -v
```
```
npm -v
```

<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar5.jpg" alt="Alt text" title="Gambar 5"><p>
5. Sekarang kita akan melakukan instalasi localtunnel dengan perintah berikut

```
npm install -g localtunnel
```
6. Jika instalasi localtunnel sudah selesai sekarang kita akan menjalankan localtunnel pada Apache2 kita dengan cara perintah berikut
  
```
lt --port 80
```
Dan dibawahnya akan muncul url localtunnel kita yang mana telah online dan bisa diakses di browser manapun seperti gambar berikut<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar9.jpg" alt="Alt text" title="Gambar 9"><p>
7. Dan sekarang kita coba URL localtunnel kita di browser, dan melalui HP
Web PC:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar11.png" alt="Alt text" title="Gambar 11"><p>
Browser HP:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%202/assets/gambar12.jpg" alt="Alt text" title="Gambar 12"><p>

<h1>Selesai</h1>
