# CI CD With Jenkins

## Langkah 1 - Instalasi and Config Jenkins

1. Install Jenkins menggunakan perintah berikut:

Pertama kita install openjdk karena jenkins dibuat menggunakan java

```
sudo apt install openjdk-11-jdk
```

![Img 1](assets/1.png)

```
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
```

```
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
/etc/apt/sources.list.d/jenkins.list'
```

```
sudo apt update
```

![Img 2](assets/2.png)

Install jenkins menggunakan perintah berikut:

```
sudo apt install jenkins
```

![Img 3](assets/3.png)

2. Cek status jenkins menggunakan 

```
sudo systemctl status jenkins
```

![Img 4](assets/4.png)

3. Sekarang masuk ke jenkins menggunakan web browser dan jenkins menggunakan port 8080

![Img 5](assets/5.png)

4. Masukkan administrative password dengan cat seperti berikut:

```
sudo cat /var/lib/jenkins/secret/initialAdminPassword
```

![Img 2](assets/6.png)

5. Lalu masukkan secret nya dan klik Install suggested plugins

![Img 2](assets/7.png)

6. Berikut tampilan awal dari jenkins

![Img 2](assets/8.png)

7. Sekarang kita masuk ke plugin manaager dan install SSH Agent

![Img 2](assets/16.png)

![Img 2](assets/9.png)

8. Lalu kita cek apakah SSH agent sudah berhasil di install

![Img 2](assets/10.png)

9. Sekarang masuk ke server aplikasi dan config git kita

![Img 2](assets/11.png)

10. Kemudian copy id_rsa pub ke github kita

![Img 2](assets/12.png)

11. Cek koneksi ke github

![Img 2](assets/13.png)

12. Sekarang kita copy private key untuk dimasukkan ke jenkins kita

![Img 2](assets/14.png)

13. Masuk ke credential dan tambahkan credential kita dengan private key tadi

![Img 2](assets/16.png)

![Img 2](assets/17.png)

![Img 2](assets/18.png)

![Img 2](assets/19.png)

14. Sekarang kita akan menambahkan pipeline ke wayshub-frontend kita

![Img 2](assets/20.png)

![Img 2](assets/21.png)

15. Centang Github hook disini

![Img 2](assets/22.png)

16. Sekarang kita akan membuat file jenkinsfile untuk pipeline nya

![Img 2](assets/23.png)

17. Masukkan pipeline kita, untuk yang saya gunakan seperti berikut:

```
def secret = 'server'
def server = 'twk@103.174.114.240'
def directory = 'wayshub-frontend'
def branch = 'main'

pipeline{
    agent any
    stages{
        stage ('docker delete & git pull'){
            steps{
                sshagent([secret]) {
                    sh """ssh -o StrictHostKeyChecking=no ${server} << EOF
                    cd ${directory}
                    docker-compose down
                    docker system prune -f
                    git pull origin ${branch}
                    exit
                    EOF"""
                }
            }
        }
        stage ('docker build'){
            steps{
                sshagent([secret]) {
                    sh """ssh -o StrictHostKeyChecking=no ${server} << EOF
                    cd ${directory}
                    docker-compose build
                    exit
                    EOF"""
                }
            }
        }
        stage ('docker up'){
            steps{
                sshagent([secret]) {
                    sh """ssh -o StrictHostKeyChecking=no ${server} << EOF
                    cd ${directory}
                    docker-compose up -d
                    exit
                    EOF"""
                }
            }
        }
    }
}
```

![Img 2](assets/24.png)

![Img 2](assets/25.png)

18. Sekarang kita push wayshub-frontend nya ke github kita

![Img 2](assets/26.png)

19. Sekarang kita masukkan repository kita ke jenkins

![Img 2](assets/28.png)

20. Lalu apply dan savev

![Img 2](assets/29.png)

21. Sekarang masuk ke server aplikasi dan masuk ke directory .ssh dan masukkan key public ke authorized_keys agar jenkins bisa masuk ke dalam server kita

![Img 2](assets/30.png)

![Img 2](assets/31.png)

22. Jika sudah semua maka sekarang kita klik build now

![Img 2](assets/32.png)

23. Dan bisa dilihat proses build kita telah berhasil

![Img 2](assets/33.png)

24. Sekarang kita akan menambahkan webhooks agar repository github kita bisa di trigger oleh jenkins

![Img 2](assets/34.png)

25. Klik add webhooks

![Img 2](assets/35.png)

26. Masukkan link jenkins kita yang sudah https

![Img 2](assets/36b.png)

27. Berikut hasilnya

![Img 2](assets/37b.png)
