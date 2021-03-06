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
7. Sekarang kita akan membuat repository di masing-masing 3 directory yaitu di directory aplikasi NodeJS,Golang, dan Python kita. Untuk sekarang kita akan membuat
  repository di directory Nodejs kita dengan perintah berikut:

```
git init
```
Dan secara otomatis GIT akan membuat repository di directory aplikasi NodeJS kita<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar8.jpg" alt="Alt text" title="Gambar 8"><p>
8. Kemudian kita buat juga repository di web Github kita dengan klik pada pojok kanan atas dan klik "New Repository" seperti gambar dibawah ini
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar9.jpg" alt="Alt text" title="Gambar 9"><p>
9. Masukkan nama repository nya dan klik "Create Repository
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar10.jpg" alt="Alt text" title="Gambar 10"><p>
Jika muncul seperti gambar berikut maka repository telah berhasil dibuat dan copy pada bagian git remote add untuk digunakan pada step 10<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar11.jpg" alt="Alt text" title="Gambar 11"><p>
10. Sekarang kita buat git remote dengan perintah yang telah kita copy tadi yaitu:

```
git remote add origin git@github.com:twkakbar/nodejs.git
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar12.jpg" alt="Alt text" title="Gambar 12"><p>
11. Sekarang kita akan membuat .gitignore untuk node modules yang mana fungsinya untuk mengecualikan file/folder yang tidak akan di deploy ke github,
  dikarenakan node modules ini mempunyai banyak isi yang tidak diperlukan untuk di deploy dengan perintah berikut:<p>

Pertama kita buat terlebih dahulu file .gitignore<p>
```
touch .gitignore
```
Kemudian edit file .gitignore nya
```
nano .gitignore
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar13.jpg" alt="Alt text" title="Gambar 13"><p>
Kemudian kita masukkan nama file/folder yang akan kita jadikan pengecualian seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar14.jpg" alt="Alt text" title="Gambar 14"><p>
Kemudian kita cek di git status dan node modules sudah ada di pengecualian dan tidak akan di deploy ke github<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar15.jpg" alt="Alt text" title="Gambar 15"><p>
12. Sekarang kita git add semua file di dalam folder NodeJS kita dengan perintah berikut:<p>
Fungsi . adalah semua file didalam folder itu akan ditambah dan siap untuk di commit<p>
```
git add .
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar16.jpg" alt="Alt text" title="Gambar 16"><p>
13. Sekarang kita akan melakukan commit untuk persiapan ke tahap production dengan perintah berikut:
```
git commit -m "first commit"
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar17.jpg" alt="Alt text" title="Gambar 17"><p>
14. Sebelum melakukan push, kita lihat branch yang kita gunakan terlebih dahulu dan push ke branch tersebut dengan perintah berikut:<p>
```
git branch -a
```
Dan lakukan push dengan perintah berikut:<p>
```
git push origin master
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar18.jpg" alt="Alt text" title="Gambar 18"><p>
Dan aplikasi kita berhasil di push.<p>
15. Kita cek di Github kita apakah aplikasi telah berhasil di push apa tidak<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar19.jpg" alt="Alt text" title="Gambar 19"><p>
Dan jika seperti gambar diatas berarti push berhasil<p>
16. Sekarang kita akan berpindah ke branch development menggunakan perintah berikut:<p>
```
git branch -m development
```
Dan kita cek apakah perpindahan berhasil dengan perintah<p>
```
git branch -a
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar20.jpg" alt="Alt text" title="Gambar 20"><p>
17. Sekarang kita akan membuat 2 branch lagi yaitu staging dan production dengan perintah berikut:
```
git branch *nama branch*
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar21.jpg" alt="Alt text" title="Gambar 21"><p>
Dan cek lagi dengan `git branch -a`<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar22.jpg" alt="Alt text" title="Gambar 22"><p>
18. Kemudian lakukan push ke branch development,staging dan production<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar23.jpg" alt="Alt text" title="Gambar 23"><p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar24.jpg" alt="Alt text" title="Gambar 24"><p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar25.jpg" alt="Alt text" title="Gambar 25"><p>
19. Kita cek 3 branch tadi apakah sudah selesai dengan membuka github kita dan jika berhasil seperti gambar dibawah ini<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar26.jpg" alt="Alt text" title="Gambar 26"><p>
20. Dan untuk berpindah ke branch lainnya menggunakan<p>
```
git checkout production
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar27.jpg" alt="Alt text" title="Gambar 27"><p>
21. Sekarang kita akan beralih ke directory golang kita<p>
Disini saya melakukan inisialisasi git menggunakan perintah `git init` kemudian membuat file .gitignore dan menambahkan file gol1.16.5.linux-amd64.tar.gz, 
jadi file tersebut tidak akan di deploy, kemudian saya melakukan `git add .` dan `git commit -m "first commit"`<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar28.jpg" alt="Alt text" title="Gambar 28"><p>
22. Setelah itu saya membuat 3 branch yaitu development, staging dan production<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar29.jpg" alt="Alt text" title="Gambar 29"><p>
23. Setelah itu disini saya membuat remote origin ke repository pytohn kita, kemudian saya melakukan push ke setiap branch dengan menggunakan remote
  origin<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar30.jpg" alt="Alt text" title="Gambar 30"><p>
Lalu kita cek apakah branch nya sudah ada dan berhasil di push 
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar31.jpg" alt="Alt text" title="Gambar 31"><p>
24. Sekarang kita akan beralih ke directory python kita<p>
Disini saya melakukan inisialisasi git dengan perintah `git init`, kemudian saya melakukan `git add .` dan `git commit -m "first commit"`<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar32.jpg" alt="Alt text" title="Gambar 32"><p>
25. Setelah itu saya membuat 3 branch yaitu development, staging dan production<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar33.jpg" alt="Alt text" title="Gambar 33"><p>
26. Kemudian saya lakukan push ke branch development,staging dan production<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar34.jpg" alt="Alt text" title="Gambar 34"><p>
27. Lalu kita cek apakah branch nya sudah ada dan berhasil di push<p>
Dan di gambar berikut terbukti sudah berhasil di push<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar35.jpg" alt="Alt text" title="Gambar 35"><p>
Dan 3 branch juga berhasil dibuat dan di push<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar36.jpg" alt="Alt text" title="Gambar 36"><p>
