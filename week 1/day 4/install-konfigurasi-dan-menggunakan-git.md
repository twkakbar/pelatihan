<h1>Instalasi, Konfigurasi dan Menggunakan GIT</h1>
<h2>Langkah 1 - Konfigurasi GIT</h2>
1. Jika menggunakan sistem operasi Linux-Ubuntu/Mac OS maka kita tidak perlu install GIT lagi karena GIT sudah ada secara default, maka langkah pertama yang kita
lakukan adalah konfigurasi GIT kita dengan menetapkan username dan email akun Github kita dengan menggunakan perintah<p>
  
```
git config --global user.name " *your.github-user.name* "
```
```
git config --global user.email " *your.github-user.email* "
```
Ubah kata berbintang dengan username dan email kalian dan pastikan sesuai dengan akun github kalian<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar1.jpg" alt="Alt text" title="Gambar 1"><p>

<h2>Langkah 2 - SSH </h2>
1. SSH key berguna untuk mengintegrasikan antara repository local kita dengan platform github, kita akan generate SSH dengan menggunakan perintah berikut:

```
ssh-keygen
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar2.jpg" alt="Alt text" title="Gambar 2"><p>
2. Kemudian kita masuk ke directory ssh yang telah kita buat tadi dengan perintah berikut:
```
cat .ssh/id_rsa.pub
```
Dan copy isi dari file id_rsa.pub yang dilingkari merah tersebut untuk kita pakai di step 4 nanti<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar3.jpg" alt="Alt text" title="Gambar 3"><p>
3. Kemudian masuk ke Web github dan pilih settings di pojok kanan atas profil kita kemudan klik settings. Setelah itu pada halaman settings masuk ke tab
  SSH and GPG keys kemudian klik New SSH Key seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar4.jpg" alt="Alt text" title="Gambar 4"><p>
4. Kemudian masukkan title sesuai keinginan kita dan key SSH yang telah kita copy di step 2 tadi di kolom Key dan klik Add SSH key<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar5.jpg" alt="Alt text" title="Gambar 5"><p>
5. Jika berhasil maka akan muncul seperti ini di halaman SSH Keys kalian
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar6.jpg" alt="Alt text" title="Gambar 6"><p>
6. Sekarang kita akan cek koneksi antara Local kita dengan Github dengan perintah berikut:
```
ssh -T git@github.com
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar7.jpg" alt="Alt text" title="Gambar 7"><p>
