# Algoritme Dijkstra
## Background: Apa Itu Algoritme Dijkstra



Pathfinding menjadi terkenal di awal 1950-an dalam konteks routing; yaitu, menemukan jalur terpendek antara dua atau lebih node. Pada tahun 1956, insinyur perangkat lunak Belanda Edsger Wybe Dijkstra membua salah satu algoritme yang terkenal: Dijkstra.

Algoritme traversal seperti Breatdh-First-Search dan Depth-First-Search mengeksplorasi semua kemungkinan: mengulangi semua jalur yang memungkinkan sampai mencapai target. Namun, hal ini tidak efisien; Algoritme Dijkstra menghilangkan traversal yang tidak berguna menggunakan heuristik untuk menemukan jalur yang optimal.
Algoritme Dijkstra menemukan jalur terpendek dari node akar ke node lainnya (hingga target tercapai). Dijkstra adalah salah satu algoritma graph yang paling berguna; Selain itu, heuristik yang digunakan dapat dengan mudah dimodifikasi untuk menyelesaikan berbagai masalah.

## Kegunaan Dijkstra
- Banyak digunakan dalam protokol routing jaringan.
- Dalam layanan pemetaan digital seperti Google Maps.
- Dalam Biologi dengan mencari model network penyebaran penyakit menular.
- Dalam menentukan penjadwalan penerbangan yang optimal.
- Dalam perencanaan jalur untuk transportasi robot bergerak.
- Dalam navigasi kendaraan otomatis.
<!-- <img align="left" width="100" height="100" src="http://www.fillmurray.com/100/100"> -->
<!-- <img align="right" width="100" height="100" src="http://www.fillmurray.com/100/100"> -->
<div align="center">
  Implementasi Dijkstra dalam routing jaringan:
</div>
<div align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/66405353/119209952-d9ceb300-bad3-11eb-9d41-8ca111e1831f.png">
</div>
<div align="center">
  Implementasi Dijkstra: Model penyebaran penyakit menular.
</div>
<div align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/66405353/119209945-d3d8d200-bad3-11eb-83b5-4c21ba5abdfb.png">
</div>
<div align="center">
  Implementasi Dijkstra dalam penerbangan, untuk menentukan agenda penerbangan.
</div>
<div align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/66405353/119209947-d63b2c00-bad3-11eb-8900-18f6a824e23d.png">
</div>

## Cara Kerja Dijkstra
Algoritma Dijkstra bekerja dengan membuat jalur ke satu simpul optimal pada setiap langkah. Jadi pada langkah ke n, setidaknya ada n node yang sudah kita tahu jalur terpendek. Langkah-langkah algoritma Dijkstra dapat dilakukan dengan  langkah-langkah berikut:

1. Tentukan titik mana yang akan menjadi node awal, lalu beri bobot jarak pada node pertama ke node terdekat satu per satu, Dijkstra akan melakukan pengembangan pencarian dari satu titik ke titik lain dan ke titik selanjutnya tahap demi tahap.
2. Beri nilai bobot (jarak) untuk setiap titik ke titik lainnya, lalu set nilai 0 pada node awal dan nilai tak hingga terhadap node lain (belum terisi) 
3. Set semua node yang belum dilalui  dan set node awal sebagai “Node keberangkatan”
4. Dari node keberangkatan, pertimbangkan node tetangga yang belum dilalui dan hitung jaraknya dari titik keberangkatan. Jika jarak ini lebih kecil dari jarak sebelumnya (yang telah terekam sebelumnya) hapus data lama, simpan ulang data jarak dengan jarak yang baru
5. Saat kita selesai mempertimbangkan setiap jarak terhadap node tetangga, tandai node yang telah dilalui sebagai “Node dilewati”. Node yang dilewati tidak akan pernah di cek kembali, jarak yang disimpan adalah jarak terakhir dan yang paling minimal bobotnya.
6. Set “Node belum dilewati” dengan jarak terkecil (dari node keberangkatan) sebagai “Node Keberangkatan” selanjutnya dan ulangi langkah e.


Sebagai contoh hitunglah Jarak terdekat dari V1 ke V7 pada gambar berikut ini.
-------------------
![Vertex edge graph dijkstra](https://user-images.githubusercontent.com/66405353/119210519-c53fea00-bad6-11eb-9013-562596531212.png)
-------------------
Hasil setiap stepnya dapat dilihat pada tabel berikut ini.
-------------------
![Table dijkstra](https://user-images.githubusercontent.com/66405353/119210522-c6711700-bad6-11eb-864c-af70f3051b00.png)
-------------------
Dengan demikian jarak terpendek dari V1 ke V7 adalah 16 dengan jalur V1->V2->V3->V5->V6->V7
## 
