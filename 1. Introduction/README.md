# Introduction

## Deployment
Deployment adalah permintaan untuk menerapkan referensi tertentu (cabang, SHA, tag). GitHub mengirimkan peristiwa penerapan yang dapat didengarkan dan ditindaklanjuti oleh layanan eksternal saat penerapan baru dibuat. Penerapan memungkinkan pengembang dan organisasi untuk membangun alat yang digabungkan secara longgar di sekitar penerapan, tanpa harus mengkhawatirkan detail penerapan dalam penyampaian berbagai jenis aplikasi (misalnya, web, asli). <br>
<br> Status deployment memungkinkan layanan eksternal menandai penerapan dengan status `error` , `failure` , `pending` , `in_progress` , `queued`, or `success` yang dapat digunakan oleh sistem yang mendengarkan peristiwa status deployment. <br>

Status deployment juga dapat menyertakan `description` opsional dan `log_url`, yang sangat disarankan karena membuat status deployment lebih berguna. `log_url` adalah URL lengkap ke keluaran deployment, dan `description` adalah ringkasan tingkat tinggi tentang apa yang terjadi dengan deployment tersebut. <br>
<br> 
Di bawah ini adalah diagram urutan sederhana tentang cara kerja deployment. <br>

![screenshot](diagram.png.jpg) <br>
## Stack
  Application stack adalah rangkaian atau kumpulan program aplikasi yang membantu dalam melakukan tugas tertentu. Aplikasi-aplikasi ini saling terkait erat dan data dapat diekspor atau diimpor di antara aplikasi-aplikasi tersebut dengan langkah minimal. Banyak aplikasi perkantoran menyertakan pengolah kata, spreadsheet, database, dan utilitas email dalam satu tumpukan aplikasi. <br> 
  Sejauh kita mulai membandingkan application technology stack dengan makanan, perlu diperhatikan bahwa tumpukan ini juga menyerupai burger yang terdiri dari beberapa lapisan: dua bagian roti, daging panggang, selada, keju, dan sebagainya. Sama seperti burger, tumpukan teknologi terdiri dari beberapa lapisan teknologi yang saling berhubungan yang membentuk sebuah aplikasi. <br>
  <br>
  ![screenshot](AS1.jpg) <br>
  <br>
  Sisi klien menampilkan semua yang dapat dilihat atau berinteraksi dengan pengguna di layar. Bagian aplikasi ini biasanya disebut front-end, dan dibuat dengan bantuan kerangka front-end dan bahasa markup seperti HTML, CSS, atau JavaScript. <br>

Sisi server aplikasi bertukar data dengan sisi klien dan disebut backend. Biasanya, ini terdiri dari beberapa komponen, termasuk kerangka kerja, API, sistem manajemen basis data, dan server web. Namun, beberapa aplikasi mungkin terdiri dari beberapa layanan mikro. Jika demikian, ada kebutuhan untuk memilih teknologi sisi server yang sesuai untuk masing-masing teknologi tersebut.<br>

Tumpukan teknologi aplikasi menentukan fungsionalitas produk dan apakah produk tersebut dapat ditingkatkan skalanya di masa mendatang. Hal ini juga mempengaruhi biaya pengembangan dan waktu yang dibutuhkan untuk membangun sebuah aplikasi. <br>

<br> 

berikut ada beberapa jenis dari application stack: <br>
### 1. The MEAN Stack
The MEAN stack development  adalah singkatan dari MongoDB, ExpressJS, AngularJS, dan Node.js. Ini adalah salah satu teknologi stack paling populer di pasar. Ini adalah stack JavaScript ujung ke ujung yang memungkinkan penggunaan satu bahasa di seluruh stack .
Kita dapat menggunakan kembali kode di seluruh aplikasi sehingga mengurangi upaya yang diperlukan dalam penemuan kembali seluruh kode. <br>
<br>
![screenshot](mean.jpg) <br>
<br>
#### Components of MEAN Stack
■ MongoDB (Database Manager)<br>
■ ExpressJS (Server-side application framework to support the function of Node.js)<br>
■ Angular.js (Front end application framework)<br>
■ Node.js (Cross-platform JavaScript framework)<br>

### 2. The MERN Stack
The MERN stack adalah versi terbaru dari stack MEAN, yang menggunakan React.js, bukan Angular.js. Ini juga merupakan stack JavaScript yang digunakan untuk pengembangan komponen perangkat lunak yang efisien dan cepat. MERN menggunakan JSX, yang merupakan modifikasi JavaScript dan memungkinkan kerja komponen tanpa hambatan yang sangat disukai oleh para pengembang. Ia menggunakan React untuk membangun aplikasi web front-end, yang merupakan salah satu Perpustakaan paling populer yang digunakan untuk membangun aplikasi kelas atas bersama dengan Antarmuka Pengguna interaktif. <br>
<br>

#### Components of MERN Stack
■ MongoDB (Database Manager)<br>
■ Express.js (Server-side application framework to support the function of Node.js)<br>
■ React (A JavaScript front-end library for building user interfaces)<br>
■ Node.js (Cross-platform JavaScript framework)<br>

### 3. The MEVN Stack
Stack ini menggunakan Vue.js sebagai kerangka pengembangan front-end. Kerangka kerja ini sangat populer di kalangan pengembang karena Vue.js menawarkan pengembangan dan efektivitas yang cepat dibandingkan dengan Angular.js dan React.js. Vue.js menawarkan beberapa fungsi dasar yang dapat diperluas menggunakan layanan pihak ketiga. Bisa dibilang, Vue.js menyediakan fitur terbaik dari Angular dan React yang memberikan kinerja luar biasa bersama dengan seperangkat alat yang sangat kaya. Ia menggunakan ExpressJS, untuk mengelola semua operasi terkait server-end.
Ini memiliki komponen berikut, yang dapat digunakan untuk merancang komponen frontend dan backend yang efektif dan meningkatkan fungsionalitas situs web atau aplikasi Anda secara drastis.
 <br> 

 ![screenshot](mevn.jpg) <br>
 <br>
#### Components of MEVN Stack
■ MongoDB (Database Manager)<br>
■ ExpressJS (Server-side application framework to support the function of Node.js)<br>
■ Vue.js (A front end development framework)<br>
■ Node.js (Cross-platform JavaScript framework)<br>
<br>
### 4. The LAMP Stack
LAMP adalah teknologi klasik dan salah satu teknologi tertua (Linux, Apache, MySQL dan PHP). Ini adalah yang terdepan dalam stack perangkat lunak sumber terbuka, pemimpin pasar yang memulai semuanya dan masih dicintai oleh pengembang karena keandalan dan fleksibilitasnya. Ia menawarkan stabilitas dan kesederhanaan yang luar biasa ditambah dengan kekuatan, yang menjadikan LAMP platform paling cocok untuk mengembangkan aplikasi. <br> 
![screenshot](lamp.jpg) <br>
 <br>
Popularitasnya tidak tertandingi, karena beberapa aplikasi web sumber terbuka populer seperti WordPress dan Drupal didasarkan pada LAMP. Ia dikenal karena kemampuannya yang luar biasa dalam menangani halaman dinamis. LAMP adalah stack sumber terbuka, memungkinkan pengembang dan organisasi untuk memilih komponen berbeda berdasarkan kebutuhan bisnis tertentu. Ia menawarkan fleksibilitas untuk menggunakan MS Windows untuk membuat (Windows, Apache, MySQL, dan PHP) tumpukan atau MAC Apple untuk membuat stack (Mac, Apache, MySQL, dan PHP) untuk mengembangkan aplikasi yang sesuai untuk masing-masing platform. LAMP menawarkan fleksibilitas untuk memilih Perl atau Python daripada PHP untuk mengembangkan beragam aplikasi. Ini memiliki platform yang kuat, yang paling cocok untuk mengembangkan dan menghosting aplikasi berskala besar.
Muncul dengan komunitas pengembang terbesar ditambah dengan sejumlah besar perpustakaan dan alat, yang memberikan dukungan dan sumber daya yang besar untuk pengembangan aplikasi. <br>
<br>
#### Components of LAMP Stack
■ Linux (Operating System) <br>
■ Apache (a dedicated Webserver)<br>
■ MySQL (for Data persistence)<br>
■ PHP (Programming language)<br>
