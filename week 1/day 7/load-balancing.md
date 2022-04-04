# Load Balancing Aplikasi Wayshub 

## Langkah 1 - Instalasi Yarn

1. Langkah pertama adalah saya clone aplikasi wayshub dan install Yarn Karena aplikasi yang saya gunakan menggunakan yarn dan react maka terlebih dahulu kita 
install yarn nya 

Install yarn menggunakan NPM:

```
npm install --global yarn
```

![Img 1](assets/1.jpg)


## Langkah 2 - Reverse Proxy

1. Masuk ke folder nginx setelah itu buat suatu directory baru telebih dahulu

Masuk ke folder nging

```
cd /etc/nginx
```

Buat directory baru bernama wayshub

```
sudo mkdir wayshub
```

Masuk ke directory wayshub kemudian buat file baru dan masukkan konfigurasi nya

```
cd wayshub
```

```
sudo nano my.reverse-proxy.conf
```

![Img 5](assets/5.jpg)

2. Masukkan konfigurasi berikut:

```
server { 
    server_name wayshub.xyz; 
  
    location / { 
             proxy_pass http://127.0.0.1:3000;
    }
}
```

![Img 4](assets/4.jpg)


2. Keluar dari directory wayshub kemudian masuk ke dalam file `nginx.conf`

Keluar dari directory

```
cd ..
```

edit file `nging.conf`

```
sudo nano nginx.conf
```

![Img 6](assets/6.jpg)

Scroll kebawah sampai menemukan include dan masukkan konfigurasi berikut:

```
include /etc/nginx/wayshub/*;
```

![Img 21](assets/21.jpg)

3. Kemudian kita akan melakukan pengecekan konfigurasi dengan menjalankan perintah:

```
sudo nginx -t
```

4. Restart nginx kita dengan perintah:

```
sudo systemctl restart nginx
```

![Img 22](assets/22.jpg)

5. Sekarang edit file host, karena saya menggunakan windows host ada di c:\Windows\System32\Drivers\etc\hosts

![Img 7](assets/7.jpg)

6. Sekarang kita akan test apakah reverse proxy kita berhasil dengan mengecek di browser menggunakan domain

Jika muncul seperti gambar berikut artinya reverse proxy berhasil!

![Img 8](assets/8.jpg)

7. Sekarang kita akan menjalankan aplikasi di domain kita

Dan berhasil!

![Img 12](assets/12.jpg)

## Langkah 3 - Load Balancing
