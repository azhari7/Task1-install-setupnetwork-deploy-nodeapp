# Task1-install-setupnetwork-deploy-nodeapp
Screenshoot ada pada Folder Screenshoot


Install Ubuntu 18.04 pada VMware
- Membuat virtual machine baru pada New virtual machine wizard
- Pilih installer disk image dan arahkan pada direktori iso berada
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Create%20VM/01create%20virtual%20machine.jpg)
- Isi personalize dan password Linux 

![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Create%20VM/02-create%20virtual%20machine1.jpg)
- Tentukan space disk yang akan dipakai untuk instalasi
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Create%20VM/03-create%20virtual%20machine2%20-%20create%20capacity.jpg)
- Klik finish dan VM machine akan booting iso yang sudah dikonfig
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Create%20VM/04-create%20virtual%20machine3%20-%20finish.jpg)
- Pilih bahasa yang digunakan untuk instalasi
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Install%20Ubuntu%2018.04/01-install%20ubuntu%20-%20pilih%20bahasa.jpg)
- Pada section storage configuration pilih custom storage
- Buat partisi "/" format: ex4 dan ukuran disk -> create
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Install%20Ubuntu%2018.04/02-root%20partition.jpg)
- Buat partisi swap -> konfig ukuran disk -> format: swap -> create
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Install%20Ubuntu%2018.04/03-create%20partition%20swap.jpg)
- Pilih continue, proses instalasi akan berjalan
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Install%20Ubuntu%2018.04/04-process%20install.jpg)


Install Nginx pada Ubuntu 18.04
- apt install nginx

![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Install%20Ubuntu%2018.04/05-install%20nginx.jpg)
- testing nginx pada browser
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Install%20Ubuntu%2018.04/06-nginx%20success.jpg)

Setup network(ip statis) pada Ubuntu 18.04 VMware

- setup NAT to brige pada vmware
- Pilih VM -> Edit Virtual machine setting
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Setup%20network/00-vmware%20bridge.jpg)
- pada network adapter -> pilih bridge
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Setup%20network/01-setup%20network%20static.jpg)


Cara pertama :
- Konfig network pada saat section installasi
- Pilih interface -> enter
- Pilih manual 
- Isi Subnet, IP address, Gateway, dan nameserver
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Setup%20network/01-setup%20network%20static.jpg)

Cara Kedua :
- konfig network pada direktori netplan
- masuk ke direktori /etc/netplan
- edit 00-installer-config.yaml
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Setup%20network/02-netplans.jpg)
- ketikan perintah "netplan apply"


Deploy Frontend dumbplay
- install node js 
- penambahan repo node js
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Deploy%20Frontend%20Dumbplay/01-penambahan%20repo%20node%20js%20v12.jpg)
- install nodejs dengan command "apt-get install -y nodejs"
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Deploy%20Frontend%20Dumbplay/02-install%20node%20js.jpg)
- Clone repository frontend dumbplay pada git  
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Deploy%20Frontend%20Dumbplay/03-clone%20app.jpg)
- masuk ke direktori dumbplay/frontend
- install package dengan perintah "npm install"
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Deploy%20Frontend%20Dumbplay/05-npm%20install.jpg)
- deploy frontend dengan perintah "npm start"
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Deploy%20Frontend%20Dumbplay/06-npm%20start.jpg)
- Cek apakah frontend sudah terdeploy dengan -> Buka browser -> IPSERVER:3000
![alt text](https://github.com/azhari7/Task1-install-setupnetwork-deploy-nodeapp/blob/main/Screenshoot/Deploy%20Frontend%20Dumbplay/07-deploy%20frontend%20berhasil.jpg)
