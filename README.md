# Eksekusi-Numerik-MPI
Membahas penggunaan Numerik python pada MPI melalui Ubuntu Desktop.

## Topologi MPI Cluster
![TOPOLOGI](https://github.com/intnprmtahti/Eksekusi-Numerik---MPI/assets/150001747/119c8e03-fac5-46a7-83cb-a5f2aa04e9cd)


## 1. New User
## 1.1 Buat User
` sudo adduser <nama user> `

## 1.2 Beri Akses Root
` sudo usermod -aG <nama user> `

## 1.3 Login ke User yang Dibuat
` su - <nama user `

## 2. Buat File
## 2.1 Buat File pada user menggunakan perintah
` touch <nama file.py> `

## 2.2 Edit File
` sudo nano <nano file> `

## 2.3 Masukkan Program Numerik..py ke Dalam File yang Sudah Dibuat
![image](https://github.com/intnprmtahti/Eksekusi-Numerik---MPI/assets/150001747/0ff21390-314b-413a-9443-a34b4612be79)

## 3. Perbedaan Waktu Eksekusi pada Multinode dan Singlenode
## 3.1 Multinode
`mpiexec -n 1 -host master,worker1,worker2 python3 numerik.py`

## 3.2 Singlenode
`Python3 numerik.py`

Saat menjalankan MPI, waktu eksekusi tercatat sekitar 0.0003039836883544922 sementara jika dijalankan secara mandiri dengan python3, waktu yang diperlukan adalah sekitar 0.0003161430358886719.

Perbedaan dalam waktu eksekusi antara penggunaan MPI dan mandiri dengan Python3 dapat dipengaruhi oleh beberapa faktor, salah satunya kinerja jaringan antar node. MPI sebagai protokol komunikasi untuk komputasi paralel sangat bergantung pada efisiensi komunikasi di antara node-node tersebut.
