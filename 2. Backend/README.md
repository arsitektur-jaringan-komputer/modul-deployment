<div align=center>

# Backend Deployment

</div>

## Table of Contents

## LEMP (Laravel, Nginx, MySQL & PHP) Stack

LEMP stack adalah sekumpulan perangkat lunak yang dapat digunakan untuk menyajikan laman web dan aplikasi web dinamis yang ditulis dalam PHP. Ini adalah akronim yang mendeskripsikan sistem operasi Linux, dengan web server Nginx (diucapkan seperti “Engine-X”). Data backend disimpan di dalam database MySQL, dan pemrosesan dinamis ditangani oleh PHP.

Prasyarat untuk modul ini, kalian perlu mengakses ke server pastinya sebagai `sudo` non-root reguler.

## Web Server Nginx

### Instalasi Nginx

Untuk menampilkan laman web kepada pengunjung situs kita, kita akan menggunakan [Nginx](https://nginx.org/en/), yang merupakan server web berkinerja tinggi, untuk menginstal Nginx kita bisa menggunakan package manager `apt`. Jika sebelumnya kalian belum melakukan `update`, maka jalankan perintah `sudo apt update`.

```bash
sudo apt update
sudo apt install nginx -y
```

### UFW Simple Setup

Apa itu `UFW (Uncomplicated Firewall)` merupakan firewall bawaan pada Linux, terutama distibusi Ubuntu. Firewall ini cukup sederhana jadi mudah untuk digunakan.

#### 1 - Mengaktifkan UFW

Pertama-tama kalian bisa mengcek status dari ufw dengan menggunakan perintah:

```bash
sudo ufw status
```

Jika sebelumnya belum diaktifkan, maka muncul pesan `Status: inactive`, untuk mengaktifkan ufw cukup dengan perintah:

```bash
sudo ufw enable
```

#### 2 - Memberikan Akses HTTP dan SSH

Selanjutnya kita bakal memberikan akses untuk penggunaan `HTTP` dan `SSH`, caranya yaitu dengan mengetikan perintah:

```bash
sudo ufw allow 'Nginx HTTP'
sudo ufw allow 'OpenSSH'
```

Atau bisa juga dengan menggunakan port:

```bash
sudo ufw allow 80
sudo ufw allow 22
```

![UFW Meme](Assets/ufw-meme.jpg)

Untuk sekarang konfigurasi `ufw` sudah cukup, tapi jika nanti kalian menggunakan `SSL` berarti kalian perlu mengaktifkan akses untuk `HTTPS` atau port `443`. **Perlu diperhatikan karena kita bakal menginstal database atau aplikasi frontend yang berjalan diport tertentu, jika ingin diakses dari luar maka kita perlu mengizinkan (allow) dulu portnya di ufw**.

Selanjutnya jika kalian ingin mengakses laman dari Nginx, dapat dilakukan dengan mengetikan IP Public di browser yang kalian miliki.

```bash
http://<ip_address or domain>
```

![Halaman Nginx](Assets/nginx-1.png)

## MySQL

### Instalasi MySQL

Setelah berhasil menginstall Nginx, selanjutnya kita perlu menginstall database yang nanti dapat digunakan sebagai penyimpanan dan pengelolaan data yang kita miliki.

```bash
sudo apt install mysql-server -y
```

### Setup Database & User

Untuk mengakses console mysql, cukup menggunakan perintah:

```bash
sudo mysql
```

![MySQL Console](Assets/mysql-1.png)

#### Membuat Database

Untuk membuat database baru, kalian kita bisa menggunakan perintah:

```sql
CREATE DATABASE laravel;
```

```sql
SHOW DATABASES;
```

![Show Database](Assets/mysql-2.png)

Selanjutnya kita perlu membuat user baru dan memberikan akses ke databasenya.

```bash
CREATE USER 'USER'@'%' IDENTIFIED BY 'PASSWORD';
GRANT ALL PRIVILEGES ON laravel.* TO 'USER'@'%' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```

#### Testing

Kalian perlu login menggunakan user yang telah dibuat, untuk memastikan apakah usernya dapat mengakses databasenya.

```bash
mysql -u USER -p
```

## PHP

### Instalasi PHP

Selanjutnya perlu menginstall PHP, dimana akan kita gunakan sebagai penghubung ke database dan juga untuk menyajikan konten yang lebih dinamis. Yang perlu perlu diperhatikan pada saat menginstall PHP, yaitu kalian perlu menginstall dependesi tambahan seperti `php-fpm` yang bertugas sebagai penghubung ke Nginx (web server), lalu ada `php-mysql` yang bertugas menjadi penghubung ke database MySQL dan dependensi lainnya sesuai kebutuhan kalian.

Tambahkan repository PHP terlebih dahulu:

```bash
sudo add-apt-repository ppa:ondrej/php -y
sudo apt update
```

```bash
sudo apt-get install php8.1-common php8.1-cli php8.1-mbstring php8.1-xml unzip composer php8.1-curl php8.1-mysql php8.1-fpm php8.1-intl -y
```

Verifikasi instalasi

```bash
php -v
```

### Setup Laravel Project

Untuk backend yang akan kita gunakan yaitu `Laravel`. Laravel sendiri adalah framework PHP yang open-source dan berisi banyak modul dasar untuk mengoptimalkan kinerja PHP dalam pengembangan aplikasi web, apalagi PHP adalah bahasa pemrograman yang dinamis dan Laravel disini bisa bertindak untuk membuat web development lebih cepat, lebih aman, dan lebih simpel.

#### Clone Project

```bash
cd /var/www
sudo git clone https://github.com/elshiraphine/be-todo.git && cd be-todo
```

#### Composer

Apa itu `composer`? Composer adalah sebuah tools manajemen dependensi untuk bahasa pemrograman PHP. Dalam konteks pemrograman, Composer adalah sebuah aplikasi yang digunakan untuk mengelola dan mengatur dependensi seperti library, framework, atau paket lain yang diperlukan dalam proyek PHP.

#### Install

Pastikan kalian berada di direktori `be-todo`, lalu kalian perlu menginstal beberapa library menggunakan `composer`.

```bash
composer install
```

#### Update & Upgrade (optional)

```bash
sudo composer update
```

```bash
sudo which composer
sudo php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
sudo php composer-setup.php --install-dir=/usr/bin --filename=composer
```

#### Artisan

Artisan adalah sebuah file yang berisi command-line interface (CLI) yang disediakan oleh Laravel untuk membantu pengembangan aplikasi dengan menyediakan berbagai perintah yang dapat digunakan untuk melakukan tugas-tugas umum seperti membuat model, controller, migrasi database, menjalankan unit test, dan masih banyak lagi.


