<h1>Langkah 1</h1>
<h2>Download VMware dan Ubuntu Server</h2>
Langkah awal adalah mendownload Ubuntu server dan Aplikasi VMware <p>
1. Buka link https://ubuntu.com/download/server dan klik "Option 2 - Manual server installation"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/Screenshot%20(1140).jpg" alt="Alt text" title="Gambar 1"><p>
2. Download aplikasi VMware di https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/Screenshot%20(1141).jpg" alt="Alt text" title="Gambar 2"><p>
  
<h1>Langkah 2</h1>
<h2>Instalasi dan konfigurasi VMware</h2>
1. Setelah selesai mendownload maka langsung di install dan jalankan VMware dan klik "Create a New Virtual Machine"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar3.jpg" alt="Alt text" title="Gambar 3"><p>
2. Kemudian pilih "Installer disc image (iso)" untuk memasukkan file iso Ubuntu server kita kemudian browse dan pilih file Ubuntu Server yang telah di download tadi<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar4.jpg" alt="Alt text" title="Gambar 4"><p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar5.jpg" alt="Alt text" title="Gambar 5"><p>
3. Kemudian masukkan nama kita dan password nya, sebenarnya disini tidak terlalu diperlukan karena yang kita install adalah Ubuntu Server, nanti ketika instalasi didalam Ubuntu Server akan diminta memasukkan nama dan password yang akan kita gunakan<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar6.jpg" alt="Alt text" title="Gambar 6"><p>
4. Masukkan berapa size storage yang akan kita gunakan, disini saya memasukkan 10GB, kemudian next<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar7.jpg" alt="Alt text" title="Gambar 7"><p>
5. Pilih "Customize Hardware" untuk mengkonfigurasi Virtual Machine Ubuntu Server kita<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar8.jpg" alt="Alt text" title="Gambar 8"><p>
6. Kemudian untuk Memory masukkan 2GB, Processor 2 Core, dan pada bagian Network Adapter pilih "NAT" kemudian close<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar9.jpg" alt="Alt text" title="Gambar 9"><p>
7. Klik Finish jika sudah melakukan konfigurasi<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar10.jpg" alt="Alt text" title="Gambar 10"><p>
8. Kemudian kita jalankan server yang telah kita buat dengan menekan salah satu dari 2 tombol berikut<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar11.jpg" alt="Alt text" title="Gambar 11"><p>
9. Pilih Bahasa Inggris dan tekan tombol Space di keyboard<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar12.jpg" alt="Alt text" title="Gambar 12"><p>
10. Pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar13.jpg" alt="Alt text" title="Gambar 13"><p>
11. Disini kita akan mengkonfigurasi jaringan menjadi Statis, klik di bagian ens33 eth<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar14.jpg" alt="Alt text" title="Gambar 14"><p>
12. Kemudian pilih "Edit IPv4"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar15.jpg" alt="Alt text" title="Gambar 15"><p>
13. Kemudian masukkan ip statis sesuai device kita masing-masing dengan cara jika di windows ketik ipconfig di cmd<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar16.jpg" alt="Alt text" title="Gambar 16"><p>
14. Jika sudah selesai maka pilih done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar17.jpg" alt="Alt text" title="Gambar 17"><p>
15. Pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar18.jpg" alt="Alt text" title="Gambar 18"><p>
16. Pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar19.jpg" alt="Alt text" title="Gambar 19"><p>
17. Pilih "Custom Storage Layout"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar20.jpg" alt="Alt text" title="Gambar 20"><p>
18. Pilih "Free Space -> Add GPT Partition"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar21.jpg" alt="Alt text" title="Gambar 21"><p>
19. Disini kita buat storage untuk Root, masukkan size maksimal kemudian Create<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar22.jpg" alt="Alt text" title="Gambar 22"><p>
20. Jika sudah selesai pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar23.jpg" alt="Alt text" title="Gambar 23"><p>
21. Nah disini kita masukkan nama dan password yang ingin digunakan untuk login di Ubuntu Server nantinya, pastikan untuk mengingat Username dan Password yang kita buat kemudian pilih done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar24.jpg" alt="Alt text" title="Gambar 24"><p>
22. Pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar25.jpg" alt="Alt text" title="Gambar 25"><p>
23. Pilih "Install OpenSSH Server" dan Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar26.jpg" alt="Alt text" title="Gambar 26"><p>
24. Karena disini hanya instalasi dan konfigurasi Ubuntu Server, kita masih belum memerlukan aplikasi disini maka pilih Done untuk melanjutkan<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar27.jpg" alt="Alt text" title="Gambar 27"><p>
25. Disini proses instalasi berjalan silahkan ditunggu sebentar<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar28.jpg" alt="Alt text" title="Gambar 28"><p>
26. Jika sudah selesai akan muncul seperti ini dan pilih "Reboot Now"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar29.jpg" alt="Alt text" title="Gambar 29"><p>
27. Disini masukkan username dan password yang telah kita buat tadi<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar30.jpg" alt="Alt text" title="Gambar 30"><p>
28. VOILAA!! Dan instalasi dan konfigurasi Ubuntu Server di VMware selesai!<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar31.jpg" alt="Alt text" title="Gambar 31"><p>
