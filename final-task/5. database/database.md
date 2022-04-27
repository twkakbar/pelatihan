# Database

1. Run database postgresql menggunakan docker dengan perintah berikut:

```
docker run -p 5432:5432 --name postgres -v /home/db/postgres:/var/lib/postgresql/data -e POSTGRES_PASSWORD=twk -d postgres:alpine3.15
```

![Img 1](assets/0.png)

2. Lihat isi container apakah postgres sudah berjalan

![Img 1](assets/1.png)

3. Sekarang masuk ke postgresql.conf dan ubah listen_address ke * agar server dapat di remote menggunakan server lain

![Img 1](assets/2.png)

![Img 1](assets/3.png)

4. Setelah mengubah postgresql.conf selanjutnya adalah mengijinkan postgre untuk menerima remote dari server lain dengan cara edit pg_hba.conf dan ubah method ke trust


![Img 1](assets/4.png)

![Img 1](assets/5.png)

5. Sekarang masuk ke container postgresql dan show database nya

```
docker exec -it postgres psql -U postgres
```

![Img 1](assets/6.png)

6. Sekarang buat database bernama dumbflix

![Img 1](assets/7.png)

7. Tambah user baru yang bernama twk beserta password nya dan berikan privileges atau izin user twk ke database dumbflix

![Img 1](assets/8.png)

8. Masuk lagi ke container database dengan menggunakan user twk dan database dumbflix

![Img 1](assets/9.png)

