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
![screenshot](mean.jpg) <br>
