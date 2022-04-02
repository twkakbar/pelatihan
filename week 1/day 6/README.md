# Day 5
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

#### 8. Move cursor
![Img 12](assets/16.jpg)

Kalau kita lihat disini saya memilik file bernama 1.html di dalam directory editor. Sekarang kita akan coba untuk mengambil isi dari file 1.html tersebut ke 
dalam file 2.html kita.

`CTRL + R` : untuk mengambil isi dari suatu file

![Img 12](assets/17.jpg)

Kemudian masukan lokasi yang sesuai dengan file yang isinya ingin kalian ambil

![Img 12](assets/18.jpg)

# 2. Text Manipulation
