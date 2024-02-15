# Intoroduction

## Deployment
Deployment adalah permintaan untuk menerapkan referensi tertentu (cabang, SHA, tag). GitHub mengirimkan peristiwa penerapan yang dapat didengarkan dan ditindaklanjuti oleh layanan eksternal saat penerapan baru dibuat. Penerapan memungkinkan pengembang dan organisasi untuk membangun alat yang digabungkan secara longgar di sekitar penerapan, tanpa harus mengkhawatirkan detail penerapan dalam penyampaian berbagai jenis aplikasi (misalnya, web, asli). <br>
<br> Status deployment memungkinkan layanan eksternal menandai penerapan dengan status 'error' , 'failure' , 'pending' , 'in_progress' , 'queued' , or 'success' yang dapat digunakan oleh sistem yang mendengarkan peristiwa status deployment. <br>

Status deployment juga dapat menyertakan 'description' opsional dan 'log_url', yang sangat disarankan karena membuat status deployment lebih berguna. 'log_url' adalah URL lengkap ke keluaran deployment, dan 'description' adalah ringkasan tingkat tinggi tentang apa yang terjadi dengan deployment tersebut. <br>
<br> 
Di bawah ini adalah diagram urutan sederhana tentang cara kerja deployment. <br>

![screenshot](diagram.png)
## Stack
