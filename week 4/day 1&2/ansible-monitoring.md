# Setup Ansible and Monitoring

## Langkah 1 - Ansible Installation (Dilakukan di local)

1. Lakukan update dan upgrade terlebih dahulu

```
sudo apt update; sudo apt upgrade
```

![Img 1](assets/1.png)

```
sudo apt install software-properties-common
```

```
sudo add-apt-repository --yes --update ppa:ansible/ansible
```

```
sudo apt install ansible
```

2. Cek apakah ansible sudah terinstall

```
ansible --version
```
![Img 1](assets/2.png)

## Langkah 1 - Setup Ansible (Dilakukan di local)
1. Buat directory baru dan file baru bernama Inventory yang berisi isi dari server kita nantinya yang akan dilakukan otomisasi

![Img 1](assets/3.png)

![Img 1](assets/4.png)

2. Kirim private key ke setiap server agar manage lebih mudah

![Img 1](assets/5.png)

3. Copy private key server dan paste di file baru yang bernama sshkey.pem di local

![Img 1](assets/6.png)

![Img 1](assets/7.png)

4. Buat file baru yang bernama ansible.cfg, file ini berfungsi untuk sebagai penghubung antara server yang ada di inventory ke local kita dengan private key tadi

![Img 1](assets/8.png)

![Img 1](assets/9.png)

5. Cek koneksi ke server tujuan dengan menggunakan perintah berikut:

```
ansible all -m ping
```

![Img 1](assets/10.png)

6. Buat dahulu sebuah folder baru dan didalamnya buat file-file yang berisi services node exporter dan prometheus

![Img 1](assets/11.png)

![Img 1](assets/12.png)

![Img 1](assets/13.png)

Di bagian sini jangan lupa untuk mengganti target ke ip server yang ingin kalian monitor

![Img 1](assets/14.png)

7. Hasil di dalam folder files seperti berikut

![Img 1](assets/15.png)

8. Kemudian kembali ke directory sebelumnya dan buat file baru bernama monitoring.yml, ini adalah file ansible playbook 

Untuk ansible playbook yang saya gunakan adalah seperti berikut:

```
- hosts: all
  become: true
  tasks:
    - name: "Update"
      apt:
        update_cache: yes

    - name: "Upgrade"
      apt:
        upgrade: yes

    - name: "Install node exporter"
      shell: "wget https://github.com/prometheus/node_exporter/releases/download/v0.15.2/node_exporter-0.15.2.linux-amd64.tar.gz; tar -xf node_exporter-0.15.2.linux-amd64.tar.gz; sudo mv node_exporter-0.15.2.linux-amd64/node_exporter /usr/local/bin; sudo useradd -rs /bin/false node_exporter"
      args:
        executable: /bin/bash

    - name: "Create service for node exporter"
      copy:
        src: node-exporter.service
        dest: /etc/systemd/system/node-exporter.service

    - name: "Reload service for node exporter"
      shell: "sudo systemctl daemon-reload; sudo systemctl enable node-exporter; sudo systemctl start node-exporter"
      args:
        executable: /bin/bash

- hosts: prometheus
  become: true
  tasks:
    - name: "Install prometheus"
      shell: "wget https://github.com/prometheus/prometheus/releases/download/v2.1.0/prometheus-2.1.0.linux-amd64.tar.gz; tar -xf prometheus-2.1.0.linux-amd64.tar.gz; sudo mv prometheus-2.1.0.linux-amd64/prometheus prometheus-2.1.0.linux-amd64/promtool /usr/local/bin; sudo mkdir /etc/prometheus /var/lib/prometheus; sudo mv prometheus-2.1.0.linux-amd64/consoles prometheus-2.1.0.linux-amd64/console_libraries /etc/prometheus"
      args:
        executable: /bin/bash

    - name: "Add node exporter to prometheus"
      copy:
        src: prometheus.yml
        dest: /etc/prometheus/prometheus.yml

    - name: "Add user prometheus"
      shell: "sudo useradd -rs /bin/false prometheus; sudo chown -R prometheus: /etc/prometheus /var/lib/prometheus"
      args:
        executable: /bin/bash

    - name: "Create service for prometheus"
      copy:
        src: prometheus.service
        dest: /etc/systemd/system/prometheus.service

    - name: "Reload service for prometheus"
      shell: "sudo systemctl daemon-reload; sudo systemctl enable prometheus; sudo systemctl start prometheus"
      args:
        executable: /bin/bash

    - name: "Install grafana"
      shell: 'sudo wget -q -O - https://packages.grafana.com/gpg.key | apt-key add -; sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"; sudo apt install grafana -y'
      args:
          executable: /bin/bash

    - name: "Reload service for grafana"
      shell: "sudo systemctl daemon-reload; sudo systemctl enable grafana-server; sudo systemctl start grafana-server"
      args:
        executable: /bin/bash
```

![Img 1](assets/16.png)

9. Cek ansible playbook kita apakah ada error dengan perintah berikut:

```
ansible-playbook --syntax-check monitoring.yml
```

![Img 1](assets/17.png)

10. Jika tidak ada error maka langsung kita jalankan ansible playbook kita dengan perintah berikut

```
ansible-playbook monitoring.yml
```

![Img 1](assets/18.png)

![Img 1](assets/19.png)

11. Testing Prometheus

![Img 1](assets/20.png)

Status server di prometheus

![Img 1](assets/21.png)

12. Testing Grafana

![Img 1](assets/22.png)

![Img 1](assets/23.png)

![Img 1](assets/24.png)

13. Tambahkan data source di grafana

![Img 1](assets/25.png)

Pilih prometheus

![Img 1](assets/26.png)

Isi kan host dari server yang kita install prometheus di bagian url, dan untuk konfigurasi lainnya tidak perlu diubah

![Img 1](assets/27.png)

Klik save & test

![Img 1](assets/28.png)

![Img 1](assets/29.png)

![Img 1](assets/30.png)
