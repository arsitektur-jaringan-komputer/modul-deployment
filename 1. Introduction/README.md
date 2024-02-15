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

Berikut kelebihan dan kekurangan dari Application stack : <br>
### 1. Kelebihan<br>
* membantu mengelola data dengan metode LIFO
* secara otomatis membersihkan objek
* tidak mudah rusak
* ukuran variabel tidak dapat diubah
* mengontrol memori secara mandiri
