<h1>Konfigurasi CI/CD menggunakan Cloudflare</h1>
<h2>Langkah 1 - Daftar Akun Cludflare</h2>
1. Sebelum mulai kita harus mendaftar terlebih dahulu pada link https://dash.cloudflare.com/sign-up kemudian masukkan email dan password yang akan kalian daftarkan<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%205/assets/gambar1.jpg" alt="Alt text" title="Gambar 1"><p>

<h2>Langkah 2 - Konfigurasi dan menggunakan CI/CD Cloudflare </h2>
1. Login terlebih dahulu menggunakan akun yang kalian daftarkan tadi kemudian setelah login berikut halaman awal dan klik pages di tab sebelah kiri seperti
gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar2.jpg" alt="Alt text" title="Gambar 2"><p>
2. Setelah itu klik "Create a project" seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar3.jpg" alt="Alt text" title="Gambar 3"><p>
3. Kemudian kita akan mengkoneksikan antara cloudflare dengan akun github kita dengan cara klik "Connect Github" seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar4.jpg" alt="Alt text" title="Gambar 4"><p>
4. Kemudian kita akan diarahkan ke website Github dan kalian pilih "Only select repositories" kemudian pilih repository yang ingin kalian gunakan 
di cloudflare pages seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar5.jpg" alt="Alt text" title="Gambar 5"><p>
5. Jika sudah selesai klik "Install & authorize"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar6.jpg" alt="Alt text" title="Gambar 6"><p>
6. Kemudian masukkan password Github kalian<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar7.jpg" alt="Alt text" title="Gambar 7"><p>
7. Jika sudah maka kita akan kembali ke halaman Cloudflare, jangan lupa di centang pada bagian repository kalian dan klik "Begin setup"
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar8.jpg" alt="Alt text" title="Gambar 8"><p>
8. Disini kita akan mengkonfigurasi CI/CD kita, masukkan project name yang kalian inginkan kemudian pilih branch kalian<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar9.jpg" alt="Alt text" title="Gambar 9"><p>
Disini kita akan konfigurasi build nya, pilih framework yang kalian gunakan di repository yang sudah kalian pilih tadi, disini saya menggunakan
React maka saya memilih Create React App, kemudian di "Build Command" akan terganti sesuai rekomendasi framework yang kita pilih tadi, dan untuk build biarkan default
rekomendasi<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar10.jpg" alt="Alt text" title="Gambar 10"><p>
Pada bagian ini Root directory saya sudah benar berada di "/" dan Untuk "Environment variables" saya kosongkan karena tidak ada backend didalam project ini hanya
front end saja<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar11.jpg" alt="Alt text" title="Gambar 11"><p>
9. Sekarang kita tunggu sampai proses build selesai dan di deploy
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar12.jpg" alt="Alt text" title="Gambar 12"><p>
10. Jika proses build dan deploy berhasil maka akan muncul gambar berikut dan kita akan copy link yang telah diberikan untuk di tes 
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar13.jpg" alt="Alt text" title="Gambar 13"><p>
11. Dan setelah di tes proses deploy berhasil, web dapat diakses dengan sempurna<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar14.jpg" alt="Alt text" title="Gambar 14"><p>
12. Dan seperti ini status dari CI/CD kita tadi
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar15.jpg" alt="Alt text" title="Gambar 15"><p>
13. Kemudian saya akan melakukan perubahan di Github untuk melihat apakah CI/CD kita berjalan dengan baik dengana mengubah Title menjadi 
Wayshub - Twk Muhammad Akbar Nahyadi<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar16.jpg" alt="Alt text" title="Gambar 16"><p>
14. Dan secara otomatis CI/CD kita akan melakukan proses build dan deploy dengan sendirinya dapat dilihat di status berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar17.jpg" alt="Alt text" title="Gambar 17"><p>
15. Dapat dilihat Log dari proses build kita
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar18.jpg" alt="Alt text" title="Gambar 18"><p>
16. Dan jika proses CI/CD berhasil maka Log kita akan memberitahu kita seperti gambar berikut:
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar19.jpg" alt="Alt text" title="Gambar 19"><p>
17. Dapat dilihat hasil CI/CD berjalan dengan baik dan web yang tadinya title hanya "Wayshub" sekarang berubah menjadi "Wayshub - Twk Muhammad Akbar Nahyadi"
yang artinya proses CI/CD kita berhasil!
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%204/assets/gambar20.jpg" alt="Alt text" title="Gambar 20"><p>
