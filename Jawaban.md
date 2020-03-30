# UTS Pengenalan Big Data
* Nama : A.M.Husna Ramadhan
* Nim : 195410252
---

## Cari dan sebutkan 3 DBMS yang bisa digunakan untuk mengelola big data
**Jawaban :**
### Apache HBase
`HBase` adalah database terdistribusi yang berorientasi pada kolom. HBase adalah program yang berjalan diatas Hadoop Distributed File System yang mampu memproses data dalam skala besar secara interaktif. HBase merupakan implementasi dari konsep Google Bigtable. HBase disebutkan berjalan pada HDFS, tapi tidak terbatas hanya pada HDFS, bisa juga pada distributed file system lain.
### MongoDB
`MongoDB` adalah database NoSQL yang berbasis dokumen yang bersifat cross-platform, open-source, dan dapat digunakan secara gratis. Adapun perusahaan-perusahaan besar yang telah menggunakan MongoDB diantaranya: Adobe, Facebook, eBay, video game FIFA, Foursquare, LinkedIn, McAfee, MetLife dan masih banya lagi.MongoDB adalah database multi-fungsi yang kuat, fleksibel, dan skalabel. MongoDB menggabungkan kemampuan bekerja dalam berbagai skala dengan fitur-fitur seperti secondary indexes (indeks tambahan selain indeks utama), range queries (penelisikan dalam suatu rentang tertentu), sorting (pengurutan data), aggregations (penggabungan dataset), dan geospatial indexes (indeks geospasial).
### Cassandra
`Cassandra` lengkap APACHE CASSANDRA adalah salah satu produk open source untuk menajemen database yang didistribusikan oleh Apache yang sangat scalable (dapat diukur) dan dirancang untuk mengelola data terstruktur yang berkapasitas sangat besar (Big Data) yang tersebar di banyak server. NoSQL merupakan konsep penyimpanan database dinamis yang tidak terikat pada relasi-relasi tabel yang kaku seperti RDBMS. Selain lebih scalable, NoSQL juga memiliki performa pengaksesan yang lebih cepat. Hal-hal itulah yang membuat NoSQL menjadi semakin populer beberapa tahun belakangan ini.
#
---
## Carilah contoh masalah big data yang bisa dikelola menggunakan salah satu DBMS tersebut, jelaskan mulai dari instalasi sampai CRUD untuk data menggunakan DBMS tersebut. Asumsikan anda akan memecahkan masalah big data yang sudah anda cari contoh tadi, jelaskan kira-kira bagaimana arsitektur dari solusi big data menggunakan DBMS tersebut, gambarkan diagramnya.
**Jawaban :**
Sebuah cluster HBase terdiri HMaster, RegionServer, ZooKeeper, dan HDFS. HMaster adalah server pada HBase yang bertugas men-start HBase, mendistribusikan Region ke RegionServer yang terdaftar, mendeteksi dan memulihkan RegionServer yang rusak. HMaster tidak menangani data yang disimpan pada HBase. RegionServer adalah server yang bertugas menyimpan dan mengelola Region-region yang diterimanya dari HMaster, menangani permintaan client, dan mempartisi Region yang sudah melewati ukuran maksimal, kemudian melaporkan Region yang telah dipartisi tersebut kepada HMaster. ZooKeeper bertugas mengelola informasi pokok tentang kondisi HBase itu sendiri. Ia senantiasa mengetahui kondisi terkini dari para RegionServer, kemudian memberikan informasi ini kepada HMaster. Berdasarkan informasi dari ZooKeeper ini lah HMaster mengatur pembagian Region ke RegionServer dan memulihkan RegionServer yang mengalami kerusakan. ZooKeeper juga menyimpan informasi tentang lokasi RootKatalog dan alamat HMaster. Bila suatu client hendak mengakses HBase untuk pertama kalinya, maka ia harus memulai koneksinya melalui ZooKeeper. HDFS (Hadoop Distributed File System) berfungsi sebagai media penyimpanan data bagi HBase. Semua data yang diloading ke HBase dan data log HBase disimpan dalam HDFS.
