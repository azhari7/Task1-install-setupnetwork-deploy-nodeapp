# Task1-install-setupnetwork-deploy-nodeapp

Install Ubuntu 18.04 pada VMware
- Membuat virtual machine baru pada New virtual machine wizard
- Pilih installer disk image dan arahkan pada direktori iso berada
- Isi personalize dan password
- Tentukan space disk yang akan dipakai untuk instalasi
- Klik finish dan VM machine akan booting iso yang sudah dikonfig
- Pilih bahasa
- Pada section storage configuration pilih custom storage
- Buat partisi "/" format: ex4 dan ukuran disk -> create
- Buat partisi swap -> konfig ukuran disk -> format: swap -> create
- Pilih continue, proses instalasi akan berjalan

Install Nginx pada Ubuntu 18.04
- apt install nginx


Setup network(ip statis) pada Ubuntu 18.04 VMware
Cara pertama :
- Konfig network pada saat section installasi
- Pilih interface -> enter
- Pilih manual 
- Isi Subnet, IP address, Gateway, dan nameserver

Cara Kedua :
- konfig network pada direktori netplan
- masuk ke direktori /etc/netplan
- edit 00-installer-config.yaml
- Format konfigurasi bisa dilihat pada screenshoot netplan
- ketikan perintah "netplan apply"


Deploy Frontend dumbplay
- install node js 
- Tambah repo node js
- apt-get install -y nodejs
- Git clone repo dumbplay
- masuk ke direktori dumbplay/frontend
- install package dengan perintah "npm install"
- deploy frontend dengan perintah "npm start"
