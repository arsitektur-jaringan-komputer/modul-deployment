<div align=center>

# Prerequisites

</div>

## Table of Contents

1. [Topologi](#topologi)
2. [Akses Instance](#akses-instance)
3. [Membuat VM di Virtual Box dan VMWare Workstation](#membuat-vm-di-membuat-vm-di-virtual-box-dan-vmware-workstation)
    - [Menggunakan Vagrant](#menggunakan-vagrant)
    - [Clone VM](#clone-vm)
4. [Basic Command](#basic-command)

## Topologi

Topologi yang akan kita gunakan pada pelatihan kali ini adalah seperti berikut:

![Topologi](assets/topologi.jpg)

Dimana topologi atau arsitektur yang kita gunakan, bakalan terdiri dari 3 VM atau instances.

1. `Load Balancer`, VM ini akan kita gunakan untuk penerapan load balancing dan server ini akan kita gunakan juga sebagai database utama.
2. `App 1`, adalah server yang akan kita gunakan untuk mendeploy aplikasi frontend dan backend. Kita juga akan menginstal webserver.
3. `App 2`, server ini memiliki fungsi yang sama persis dengan `App 1` dan nantinya bisa menjadi server backup ketika server `App 1` tidak bisa digunakan.

## Akses Instance

Untuk akses ke setiap VM atau instance kita bisa menggunakan `SSH (Secure Shell)`.

A. SSH Menggunakan Windows

B. SSH Menggunakan Linux

1. Download file `.pem` pada link yang telah disediakan.

2. Buka terminal atau console yang kalian miliki. Pastikan kalian membuka terminal di lokasi yang sama dengan file `.pem` yang telah didownload. Terakhir jalankan command `chmod 400 <file_pem>` untuk memberikan permission.

![CHMOD](https://private-user-images.githubusercontent.com/69733783/303817314-1e45b1c5-3d30-44f7-9ebd-8a5da2677900.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDc1NDIwNTMsIm5iZiI6MTcwNzU0MTc1MywicGF0aCI6Ii82OTczMzc4My8zMDM4MTczMTQtMWU0NWIxYzUtM2QzMC00NGY3LTllYmQtOGE1ZGEyNjc3OTAwLmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMTAlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjEwVDA1MDkxM1omWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTU1OTlmZDAzZjczM2ZlMWYxZTEyY2Y1ODZkYTQ1NTMyNWU1MDQ4NjI2ODk3NWE0ZGQ3ZGUwNGZiZTFlNzQ4Y2UmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.NtHy6PQhOuXMqevjxPSBvy2lB1O6Laj2Eb7zEVZ0bg8)

3. Langkah terakhir yaitu akses ke VM atau instance menggunakan `.pem` file dengan menjalankan command `ssh -i <file_pem> <username@ip_address>`.

![Akses ke VM](https://private-user-images.githubusercontent.com/69733783/303817822-6280f468-7845-4de0-b9ab-9816f99c4d76.gif?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MDc1NDI5NzIsIm5iZiI6MTcwNzU0MjY3MiwicGF0aCI6Ii82OTczMzc4My8zMDM4MTc4MjItNjI4MGY0NjgtNzg0NS00ZGUwLWI5YWItOTgxNmY5OWM0ZDc2LmdpZj9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFWQ09EWUxTQTUzUFFLNFpBJTJGMjAyNDAyMTAlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjQwMjEwVDA1MjQzMlomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTZhYjRlMzY4ZTk1NjZlMmJhZThiMWViOTAyNGM4NDc5MmMwYmM3MGJmMTg4YzJlYWI3MjgyZGM5MWUxNzEyZGMmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.voz9Gzs_uWh0fQ7TRkrKMu1fkfq9We58aEsz3__GRvg)

## Membuat VM di Membuat VM di Virtual Box dan VMWare Workstation

Untuk mempercepat pembuatan VM baik di Virtual Box atau VMWare Workstation kalian bisa mengikuti langkah berikut.

### Menggunakan Vagrant

Requirements:

- [ ] Install [Vagrant >= 2.4.1](https://developer.hashicorp.com/vagrant/install)
- [ ] Install Virtual Box atau VMWare Workstation
- [ ] Silahkan membaca modul [LBE-AJK-2022](https://github.com/arsitektur-jaringan-komputer/lbe-ajk-2022/tree/master/Modul%202#vagrant) untuk langkah-langkah menginstall Vagrant.
- [ ] Pastikan kalian menginstall plugin untuk VMWare: `vagrant plugin install vagrant-vmware`
- [ ] Jangan Lupa mengatur IP di interface `Host-Only` menjadi Static : 192.168.1.1
- [ ] Harap memakai WSL untuk menggunakan command `wget`, jika memakai CMD harap menginstall wget terlebih dahulu: [Install Wget Windows](https://www.niagahoster.co.id/blog/contoh-penggunaan-wget-command/)

- Download Vagrant file melalui link berikut:

Untuk Virtual Box:

```bash
wget https://raw.githubusercontent.com/danielcristho/modul-deployment/master/0.%20Prerequisites/vagrant/Vagrantfile-Vbox -O Vagrantfile
```

Untuk VMWare:

```bash
wget https://raw.githubusercontent.com/danielcristho/modul-deployment/master/0.%20Prerequisites/vagrant/Vagrantfile-VMWare -O Vagrantfile
```

- Selanjutnya jalankan command `vagrant up` untuk membuat vm menggunakan vagrant.

![Vagrant Up](assets/vagrant-up.png)

- Selanjutnya untuk mengakses VM yang telah dibuat, bisa menggunakan command `vagrant ssh <hostname_vm>`.

![Vagrant SSH](assets/vagrant-ssh.gif)

Catatan:

- Untuk mematikan VM bisa menggunakan command `vagrant halt`.
- Untuk destroy VM bisa menggunakan command `vagrant destroy`

#### Virtual Box

![IP Static Virtual Box](assets/static-ip-vbox.gif)

#### VMWare Workstation

![IP Static VMWare](assets/static-ip-vmware.gif)

### Clone VM

Silahkan baca modul [Prerequisites Pelatihan Linux](https://github.com/arsitektur-jaringan-komputer/Pelatihan-Linux/tree/master/0.%20Prerequisites) untuk menginstall Ubuntu di VM. Jika sudah kalian bisa meng-clone VM sesuai dengan aplikasi yang digunakan.

#### 1. Virtual Box

![Clone VM Virtual Box](assets/clone-vm-vbox.gif)

#### 2. VMWare

![Clone VM VMWare](assets/clone-vm-ware.gif)

## Basic Command

Silahkan membaca modul **[Pelatihan Linux](https://github.com/arsitektur-jaringan-komputer/Pelatihan-Linux)**.