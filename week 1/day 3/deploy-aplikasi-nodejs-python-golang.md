<h1>Build dan Running aplikasi NodeJS, Golang dan Python3</h1>
<h2>Langkah 1 - Instalasi, Build dan Run Aplikasi NodeJS</h2>
1. Install terlebih dahulu engine NodeJS dengan cara perintah berikut:<p>
  
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar1.jpg" alt="Alt text" title="Gambar 1"><p>
Keterangan: disini kita menggunakan nvm<p>
nvm merupakan singkatan dari Node Version Manager. nvm adalah sebuah program yang akan membantu kita untuk menggunakan lebih dari satu versi Nodejs di dalam satu komputer.<p>
Jika nvm belum terdeteksi gunakan perintah berikut:<p>

```
exec bash
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gamba2.jpg" alt="Alt text" title="Gambar 2"><p>
Kemudian lakukan instalasi dengan perintah berikut:<p>
  
```
nvm install 16
```
Lalu untuk menggunakan nvm versi 16 kita gunakan perintah berikut<p>
```
nvm use 16
```
Untuk mengecek versi node menggunakan perintah berikut:<p>
```
node -v
```
Dan untuk mengecek versi npm menggunakan perintah berikut:<p>
```
npm -v
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar3.jpg" alt="Alt text" title="Gambar 3"><p>
2. Kemudian disini saya membuat directory untuk aplikasi NodeJS saya kemudian menggunakan perintah `npm init -y` untuk menginisiasi project saya, 
  hasilnya adalah perintah tersebut akan membuat file baru dengan nama package.json, package.json ini berisikan isi informasi dari aplikasi yang akan kita buat<p>

```
npm init -y
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar4.jpg" alt="Alt text" title="Gambar 4"><p>
3. Selanjutnya saya akan menginstall ExpressJS. Express JS adalah framework dari NodeJS yang dirancang secara fleksibel dan sederhana untuk membantu tahap pengembangan aplikasi back end, untuk menginstall express js gunakan perintah berikut:<p>

```
npm install express --save
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar5.jpg" alt="Alt text" title="Gambar 5"><p>
4. Sekarang kita akan membuat file baru dengan nama index.js dengan perintah berikut:<p>

```
touch index.js
```
Dan untuk edit file index.js gunakan perintah berikut:<p>
```
nano index.js
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar6.jpg" alt="Alt text" title="Gambar 6"><p>
Kemudian masukkan script berikut:<p>

```
const express = require("express");
const app = express();
const port = 3000;

app.get("/", (req, res) => {
  res.send("Hello World!");
});

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`);
});
```
Dan tekan ctrl+x dan y dan enter untuk save<p><p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar7.jpg" alt="Alt text" title="Gambar 7"><p>
5. Dan file berhasil dibuat! Sekarang kita akan menjalankan file index.js tadi dengan perintah berikut:<p>
  
```
node index.js
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar8.jpg" alt="Alt text" title="Gambar 8"><p>
6. Dan jika sudah muncul seperti gambar diatas maka aplikasi sudah berhasil dijalankan, untuk mengetes kita akan mencoba di web browser local seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar9.jpg" alt="Alt text" title="Gambar 9"><p>
Dan dapat dilihat di gambar diatas aplikasi kita berhasil berjalan di web browser tanpa masalah<p>
  
<h2>Langkah 2 - Instalasi, Build dan Run Aplikasi Golang</h2>
1. Kembali ke halaman root, disini saya membuat directory baru untuk aplikasi golang kita dan mendownload engine Golang dengan perintah berikut:<p>

Untuk membuat directory:<p>

```
mkdir aplikasi-go-saya
```
Untuk mendonwnload engine Golang:<p>

```
wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar10.jpg" alt="Alt text" title="Gambar 10"><p>
2. Kemudian masuk ke path go pada `.bashrc` dengan perintah berikut:<p>
  
```
sudo nano .bashrc
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar12.jpg" alt="Alt text" title="Gambar 12"><p>
3. Tambahkan `export PATH=$PATH:/usr/local/go/bin` di bagian paling bawa pada file .bashrc seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar13.jpg" alt="Alt text" title="Gambar 13"><p>
4. Kemudian kita check apakah Go sudah terinstall dengan baik, jika sudah maka akan seperti gambar berikut:<p>

```
go version
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar16.jpg" alt="Alt text" title="Gambar 16"><p>
5. Sekarang saya akan membuat file go dan meng-editnya dengan menggunakan perintah berikut:<p>
Untuk membuat file index.go:<p>
```
touch index.go
```
Untuk mengedit gunakan perintah berikut:<p>
```
nano index.go
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar17.jpg" alt="Alt text" title="Gambar 17"><p>
6. Kemudian masukkan script berikut kedalam file index.go tadi:<p>

```
package main

import "fmt"

func main() {
    fmt.Println("Hello World!")
}
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar18.jpg" alt="Alt text" title="Gambar 18"><p>
7. Lalu kita coba run aplikasi go tadi dengan perintah berikut:<p>

```
go run index.go
```
Jika berhasil akan seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar19.jpg" alt="Alt text" title="Gambar 19"><p>
8. Untuk build aplikasi go gunakan perintah berikut:<p>

```
go build index.go
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar31.jpg" alt="Alt text" title="Gambar 31"><p>
9. Lalu jalankan aplikasi go yang telah kita build tadi dengan perintah berikut:<p>

```
./index
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar32.jpg" alt="Alt text" title="Gambar 32"><p>

<h2>Langkah 3 - Instalasi, Build dan Run Aplikasi Python3</h2>
1. Aplikasi python telah di install secara default pada Ubuntu, maka kita tidak perlu mendownload nya lagi, untuk mengecek apakah python3 sudah ada gunakan
perintah berikut:<p>

```
python3
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar20.jpg" alt="Alt text" title="Gambar 20"><p>
2. Sekarang kita akan menginstall package manager dari python yaitu PIP dengan perintah berikut:<p>
  
```
sudo apt install python3-pip
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar20.jpg" alt="Alt text" title="Gambar 21"><p>
3. Setelah itu kita akan menginstall flask dengan perintah berikut:<p>

```
pip install flask
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar22.jpg" alt="Alt text" title="Gambar 22"><p>
Catatan:<p>
PIP adalah sebuah package management system yang biasa digunakan untuk mengatur dan menginstall package yang berisi modul-modul Python. PIP digunakan untuk menginstall Flask karena Flask ditulis dan dikembangkan dengan bahasa dan modul-modul pemrograman Python. Dengan menggunakan PIP, semua hal yang dibutuhkan untuk instalasi Flask akan diunduh dan dipasang dalam satu perintah.<p>
4. Sekarang kita akan membuat file python kita dan mengedit nya<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar23.jpg" alt="Alt text" title="Gambar 23"><p>
5. Masukkan script berikut kedalam file index.py kita <p>

```
from flask import Flask
app = Flask(__name__)
@app.route("/")
def helloworld():
    return "Hello World"
if __name__ == "__main__":
    app.run()
```
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar24.jpg" alt="Alt text" title="Gambar 24"><p>
6. kemudian jalankan file index.py kita tadi dengan menggunakan perintah berikut:<p>

```
python3 index.py
```
Dan jika berhasil akan seperti gambar berikut:<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%203/assets/gambar24.jpg" alt="Alt text" title="Gambar 25"><p>
