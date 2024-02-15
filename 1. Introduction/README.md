# Intoroduction

## Deployment
Deployment adalah permintaan untuk menerapkan referensi tertentu (cabang, SHA, tag). GitHub mengirimkan peristiwa penerapan yang dapat didengarkan dan ditindaklanjuti oleh layanan eksternal saat penerapan baru dibuat. Penerapan memungkinkan pengembang dan organisasi untuk membangun alat yang digabungkan secara longgar di sekitar penerapan, tanpa harus mengkhawatirkan detail penerapan dalam penyampaian berbagai jenis aplikasi (misalnya, web, asli). <br>
+---------+             +--------+            +-----------+        +-------------+
| Tooling |             | GitHub |            | 3rd Party |        | Your Server |
+---------+             +--------+            +-----------+        +-------------+
     |                      |                       |                     |
     |  Create Deployment   |                       |                     |
     |--------------------->|                       |                     |
     |                      |                       |                     |
     |  Deployment Created  |                       |                     |
     |<---------------------|                       |                     |
     |                      |                       |                     |
     |                      |   Deployment Event    |                     |
     |                      |---------------------->|                     |
     |                      |                       |     SSH+Deploys     |
     |                      |                       |-------------------->|
     |                      |                       |                     |
     |                      |   Deployment Status   |                     |
     |                      |<----------------------|                     |
     |                      |                       |                     |
     |                      |                       |   Deploy Completed  |
     |                      |                       |<--------------------|
     |                      |                       |                     |
     |                      |   Deployment Status   |                     |
     |                      |<----------------------|                     |
     |                      |                       |                     |

## Stack
