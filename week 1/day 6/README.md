# Day 6
Pada hari ini kami mempelajari tentang text editor, text manipulation, monitoring, service management hingga network firewal

# 1. Text Editor Shortcut (Nano)
Text Editor adalah sebuah aplikasi yang berjalan di atas terminal, gunanya untuk melakukan manipulasi data pada sebuah file. Pada sebuah server kita wajib mengetahui penggunaan text editor karena di server tidak ada aplikasi yang bersifat GUI.

## Shortcut Nano
Secara default nano sudah terinstall pada sistem operasi linux, untuk memeriksanya kalian bisa gunakan perintah berikut :
```
nano --version
```
![Img 0](assets/0.jpg)

#### 1. Membuka Nano
cara membuka file nano dapat menggunakan perintah berikut
```
nano (file-name)
```
![Img 1](assets/1.jpg)
![Img 2](assets/2.jpg)
```
nano (location/folder/file-name)
```
![Img 3](assets/3.jpg)
![Img 4](assets/4.jpg)

keterangan : location/aplikasi-go-saya/index.go merupakan file yang lokasinya berada dalam folder/directory.

#### 2. Keluar dari text editor
`ctrl + X` untuk keluar dari editor. Jika melakukan perubahan maka akan dimintai konfirmasi apakah perubahan akan disimpan / tidak. Ketik Y untuk yes, dan N untuk No kemudian tekan Enter.

![Img 5](assets/5.jpg)

Jika kalian ingin mengubah nama dari file, kalian dapat mengubah nama dari yang sebelumnya index.go menjadi nama file yang kalian inginkan, jika
tidak kalian bisa langsung enter tanpa mengganti namanya seperti digambar berikut:

![Img 6](assets/6.jpg)

`ctrl + O` adalah untuk menyimpan perubahan file tanpa harus keluar dari text editor nano. Kemudian tekan Enter.

![Img 6](assets/6.jpg)

#### 3. Mencari text
`ctrl + W` adalah untuk mencari text. Masukkan value ke kolom pencarian kemudian tekan Enter.

![Img 7](assets/7.jpg)

#### 4. Choose text
`ALT + A` : adalah untuk memilih text, cukup arahkan cursor sesuai text yang ingin di select.

![Img 8](assets/8.jpg)

#### 5. Copy and Paste
`ALT + 6` : untuk melakukan copy text yang sudah di select

`CTRL + U` : untuk melakukan paste text yang sudah di copy

![Img 9](assets/9.jpg)
![Img 10](assets/10.jpg)

#### 6. Cut text and Paste
`CTRL + K` : untuk melakukan cut pada text yang sudah di select

![Img 11](assets/11.jpg)
![Img 12](assets/12.jpg)

`CTRL + U` : untuk melakukan paste text yang sudah di cut

![Img 12](assets/13.jpg)

#### 7. Move cursor
`CTRL + A` : untuk pindah cursor ke awal baris

![Img 12](assets/14.jpg)

`CTRL + E` : untuk pindah cursor ke akhir baris

![Img 12](assets/15.jpg)

#### 8. Ambil konten dari file lain
![Img 12](assets/16.jpg)

Kalau kita lihat disini saya memilik file bernama 1.html di dalam directory editor. Sekarang kita akan coba untuk mengambil isi dari file 1.html tersebut ke 
dalam file 2.html kita.

`CTRL + R` : untuk mengambil isi dari suatu file

![Img 12](assets/17.jpg)

Kemudian masukan lokasi yang sesuai dengan file yang isinya ingin kalian ambil

![Img 12](assets/18.jpg)

# 2. Text Manipulation

#### 1. cat
`Cat` adalah salah satu perintah yang berfungsi untuk membuat daftar konten atau isi file pada standard output (sdout). Yang kalian tahu pasti perintah `cat` hanya bisa untuk melihat isi dari suatu file, sebenarnya tidak hanya itu.

Contoh penggunaan :

Untuk melihat isi dari suatu file

```
cat (file-name)
```

![Img 12](assets/19.jpg)

Untuk membuat suatu file baru serta memasukkan teks, Jika sudah menambakan teks kalian dapat keluar dengan klik CTRL + C.

```
cat > (file-name)
```

![Img 19](assets/20.jpg)

Kemudian untuk menggabungkan dua buah file, dan menyimpannya ke dalam test3.go

```
cat test.go test2.go > test3.go
```

![Img 21](assets/21.jpg)

#### 2. sed
`Sed` adalah singkatan dari stream editor. Gunanya untuk memanipulasi teks dasar pada file. Dengan `sed` kita dapat mengganti teks dengan cepat.
```
sed -i 's/Hello/Holla/g' file3
```

Disini saya mengganti semua kata test menjadi testing pada test3.go

![Img 22](assets/22.jpg)

#### 3. grep
`Grep` merupakan perintah untuk melakukan pencarian sebuah text dalam sebuah file yang telah dibuat.

Contoh:

Saya akan mencari kata testing pada test3.go

```
grep testing test3.go
```

![Img 23](assets/23.jpg)

Untuk menghitung jumlah kata “testing” pada test3.go

```
grep -c testing test3.go
```

![Img 24](assets/24.jpg)

Untuk mencari semua file yang berisikan kata testing gunakan perintah berikut:

```
grep testing *
```

![Img 25](assets/25.jpg)

#### 4. sort
`Sort` untuk mengurutkan data, baik itu secara ascending atau descending.

Gunakan perintah berikut untuk mengurutkan berdasarkan ascending:

```
sort file1
```

![Img 26](assets/26.jpg)

Gunakan perintah berikut untuk mengurutkan berdasarkan descending

```
sort -r file1
```

![Img 27](assets/27.jpg)

#### 5. echo
`Echo` digunakan untuk mencetak string / pesan dari hasil perintah lain.

Gunakan perintah berikut untuk mencetak string Hallo Dunia!

```
echo "Hallo Dunia!"
```

![Img 28](assets/28.jpg)

Gunakan perintah berikut untuk mencetak kata Halo Dunia! di file2

```
echo "Hello Dumbways!" >> file3
```

![Img 29](assets/29.jpg)

Gunakan perintah berikut untuk mereplace semua data di file2 dan menggantinya dengan "Replace semua data di file2"

```
echo "Replace semua data di file2" > file2
```

![Img 30](assets/30.jpg)
