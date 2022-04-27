# Deployment


1. Sebelumnya saya sudah clone backend dan frontend, sekarang saya akan setup keduanya, untuk frontend edit api.js di bagian baseURL untuk menghubungkan frontend ke backend

![Img 1](assets/1.png)

![Img 1](assets/2.png)

2. Untuk backend edit config.json dan masukkan credential postgtresql yang sudah saya setup tadi dan masukkan ip private nya

![Img 1](assets/3.png)

![Img 1](assets/4.png)

3. Sekarang saya akan melakukan migrasi ke database, agar menggunakan environtment production gunakan `export NODE_ENV=production` kemudian lakukan migrasi menggunakan sequelize dengan perintah npx sequelize db:migrate

![Img 1](assets/5.png)

4. Sekarang cek tabel nya apakah sudah di migrasi

![Img 1](assets/6.png)

5. Sekarang buat dockerfile untuk build si aplikasi seperti gambar berikut:

backend:

![Img 1](assets/7.png)

frontend:

![Img 1](assets/8.png)

6. Sekarang kita buat file docker-compose.yml, docker compose ini digunakan untuk mempercepat dan mempermudah pembuatan service atau aplikasi pada sebuah container

backend:

![Img 1](assets/9.png)

frontend:

![Img 1](assets/10.png)

7. Jika sudah jalankan menggunakan perintah berikut:

```
docker-compose up -d
```

Hasil frontend

![Img 1](assets/11.png)

Hasil backend

![Img 1](assets/12.png)

