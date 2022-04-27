# CICD

1. Untuk CICD juga saya sudah melakukan instalasi on top docker menggunakan ansible, berikut playbooknya:

```
- hosts: jenkins
  become: true
  tasks:
  - name: jenkins volume dir
    file:
     path: /home/jenkins/jenkins_home
     state: directory
     owner: 1000
     group: 1000

  - name: Pull jenkins
    docker_image:
     name: jenkins/jenkins:lts
     source: pull

  - name: Container jenkins
    docker_container:
     name: jenkins
     image: jenkins/jenkins
     ports:
      - 8080:8080
      - 50000:50000
     volumes: /home/jenkins/jenkins_home:/var/jenkins_home
```

2. Karena sebelumnya di nginx sudah setup reverse proxy, maka masukkan link nya ke browser dan akan diminta password seperti ini, maka masukkan saja password yang ada di server kita

![Img 1](assets/1.png)

![Img 1](assets/2.png)

3. Berikut halaman utama jenkins

![Img 1](assets/3.png)

4. Masuk ke plugin manager dan download ssh agent

![Img 1](assets/4.png)

5. Juga download publish over ssh sesuai tugas final task

![Img 1](assets/5.png)

6. Sekarang kita akan konfigurasi publish over ssh, masuk ke configure system dan pada bagian publish over ssh, masukkan private key nya dan host server app kita

![Img 1](assets/6.png)

![Img 1](assets/7.png)

Lalu tes koneksi

![Img 1](assets/8.png)

7. Sekarang konfigurasi user untuk ke github dengan cara masuk ke manage credential

![Img 1](assets/15.png)

![Img 1](assets/16.png)

![Img 1](assets/17.png)

![Img 1](assets/18.png)

8. Sekarang kita akan buat job baru CICD yaitu untuk dumbflix-frontend dan dumbflix-backend, klik new item dan masukkan nama project kita, disini saya menggunakan freestyle project untuk menggunakan publish over ssh dan discord notifier

![Img 1](assets/9.png)

9. Disini pilih git dan masukkan url kita dan credential yang kita buat di step 7 tadi

![Img 1](assets/10.png)

Centang GitHub hook trigger for GITScm polling agar dapat di trigger di perubahan github

![Img 1](assets/11.png)

Nah disini masukkan publish over ssh yang kita buat tadi, pilih ssh server kita seperti gambar berikut

![Img 1](assets/12.png)

Dan disini tambahkan Discord Notifier agar notifikasi dapat dikirim di discord

![Img 1](assets/13.png)

![Img 1](assets/19.png)

Berikut hasil notifikasi dari discord notifier ketika trigger di github

![Img 1](assets/12.png)

10. Agar CICD dapat trigger di github, kita tambahkan webhook jenkins di github kita

![Img 1](assets/20.png)

![Img 1](assets/21.png)
