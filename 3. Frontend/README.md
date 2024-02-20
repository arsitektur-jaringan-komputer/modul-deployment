<div align=center>

# Frontend Deployment

</div>

## Table of Contents
1. Package Installation


### Package Installation

Langkah pertama dalam melakukan *deployment* aplikasi *Frontend* adalah melakukan instalasi package yang digunakan.

Pertama, lakukan instalasi `nvm`. `nvm` merupakan *version manager* untuk node.js. Gunakan perintah di bawah ini untuk menginstall `nvm`.

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
source ~/.bashrc
```

Kemudian langkah selanjutnya adalah melakukan instalasi `yarn` yang merupakan *package manager* untuk JavaScript.

```sh
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update
sudo apt-get install yarn -y
```

Kemudian lakukan clone [repositori berikut](https://github.com/elshiraphine/fe-todo.git) pada direktori `/var/www/`. Setelah selesai melakukan clone, check versi aplikasi yang dibangun pada `package.json`.

![package](assets/package.png)

Karena pada `package.json` menunjukkan versi next adalah versi `14.1.0` maka berdasarkan [dokumentasi berikut](https://nextjs.org/docs/app/building-your-application/upgrading/version-14), versi `node` yang digunakan adalah **18**.

Lakukan instalasi node versi 18 dengan perintah berikut:

```sh
nvm install 18
nvm alias default 18
```

Selanjutnya lakukan instalasi `pm2`. `pm2` ini adalah *process manager* untuk aplikasi Node.js. Perintahnya adalah sebagai berikut:

```sh
sudo aot install npm
npm install pm2 -g
```