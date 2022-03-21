<h1>Langkah 1</h1>
<h2>Download VMware dan Ubuntu Server</h2>
Langkah awal adalah mendownload Ubuntu server dan Aplikasi VMware <p>
Buka link https://ubuntu.com/download/server dan klik "Option 2 - Manual server installation"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/Screenshot%20(1140).jpg" alt="Alt text" title="Gambar 1"><p>
Dan download aplikasi VMware di https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/Screenshot%20(1141).jpg" alt="Alt text" title="Gambar 2"><p>
  
<h1>Langkah 2</h1>
<h2>Instalasi dan konfigurasi VMware</h2>
Setelah selesai mendownload maka langsung di install dan jalankan VMware dan klik "Create a New Virtual Machine"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar3.jpg" alt="Alt text" title="Gambar 3"><p>
Kemudian pilih "Installer disc image (iso)" untuk memasukkan file iso Ubuntu server kita kemudian browse dan pilih file Ubuntu Server yang telah di download tadi<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar4.jpg" alt="Alt text" title="Gambar 4"><p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar5.jpg" alt="Alt text" title="Gambar 5"><p>
Kemudian masukkan nama kita dan password nya, sebenarnya disini tidak terlalu diperlukan karena yang kita install adalah Ubuntu Server, nanti ketika instalasi didalam Ubuntu Server akan diminta memasukkan nama dan password yang akan kita gunakan<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar6.jpg" alt="Alt text" title="Gambar 6"><p>
Masukkan berapa size storage yang akan kita gunakan, disini saya memasukkan 10GB, kemudian next<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar7.jpg" alt="Alt text" title="Gambar 7"><p>
Pilih "Customize Hardware" untuk mengkonfigurasi Virtual Machine Ubuntu Server kita<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar8.jpg" alt="Alt text" title="Gambar 8"><p>
Kemudian untuk Memory masukkan 2GB, Processor 2 Core, dan pada bagian Network Adapter pilih "NAT" kemudian close<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar9.jpg" alt="Alt text" title="Gambar 9"><p>
Klik Finish jika sudah melakukan konfigurasi<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar10.jpg" alt="Alt text" title="Gambar 10"><p>
Kemudian kita jalankan server yang telah kita buat dengan menekan salah satu dari 2 tombol berikut<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar11.jpg" alt="Alt text" title="Gambar 11"><p>
Pilih Bahasa Inggris dan tekan tombol Space di keyboard<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar12.jpg" alt="Alt text" title="Gambar 12"><p>
Pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar13.jpg" alt="Alt text" title="Gambar 13"><p>
Disini kita akan mengkonfigurasi jaringan menjadi Statis, klik di bagian ens33 eth<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar14.jpg" alt="Alt text" title="Gambar 14"><p>
Kemudian pilih "Edit IPv4"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar15.jpg" alt="Alt text" title="Gambar 15"><p>
Kemudian masukkan ip statis sesuai device kita masing-masing dengan cara jika di windows ketik ipconfig di cmd<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar16.jpg" alt="Alt text" title="Gambar 16"><p>
Jika sudah selesai maka pilih done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar17.jpg" alt="Alt text" title="Gambar 17"><p>
Pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar18.jpg" alt="Alt text" title="Gambar 18"><p>
Pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar19.jpg" alt="Alt text" title="Gambar 19"><p>
Pilih "Custom Storage Layout"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar20.jpg" alt="Alt text" title="Gambar 20"><p>
Pilih "Free Space -> Add GPT Partition"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar21.jpg" alt="Alt text" title="Gambar 21"><p>
Disini kita buat storage untuk Root, masukkan size maksimal kemudian Create<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar22.jpg" alt="Alt text" title="Gambar 22"><p>
Jika sudah selesai pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar23.jpg" alt="Alt text" title="Gambar 23"><p>
Nah disini kita masukkan nama dan password yang ingin digunakan untuk login di Ubuntu Server nantinya, pastikan untuk mengingat Username dan Password yang kita buat kemudian pilih done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar24.jpg" alt="Alt text" title="Gambar 24"><p>
Pilih Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar25.jpg" alt="Alt text" title="Gambar 25"><p>
Pilih "Install OpenSSH Server" dan Done<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar26.jpg" alt="Alt text" title="Gambar 26"><p>
Karena disini hanya instalasi dan konfigurasi Ubuntu Server, kita masih belum memerlukan aplikasi disini maka pilih Done untuk melanjutkan<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar27.jpg" alt="Alt text" title="Gambar 27"><p>
Disini proses instalasi berjalan silahkan ditunggu sebentar<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar28.jpg" alt="Alt text" title="Gambar 28"><p>
Jika sudah selesai akan muncul seperti ini dan pilih "Reboot Now"<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar29.jpg" alt="Alt text" title="Gambar 29"><p>
Disini masukkan username dan password yang telah kita buat tadi<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar30.jpg" alt="Alt text" title="Gambar 30"><p>
VOILAA!! Dan instalasi dan konfigurasi Ubuntu Server di VMware selesai!<p>
<img src="https://raw.githubusercontent.com/twkakbar/pelatihan/main/week%201/day%201/assets/gambar31.jpg" alt="Alt text" title="Gambar 31"><p>
