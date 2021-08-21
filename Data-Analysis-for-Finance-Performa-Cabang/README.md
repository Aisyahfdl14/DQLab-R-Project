LATAR BELAKANG

DQLab Finance merupakan perusahaan finance yang sudah mempunyai banyak cabang tersebar dimana-mana. Sejak berdiri pada Januari 2020, DQLab Finance konsisten menyalurkan pembiayaan untuk masyarakat dan semakin berkembang setiap bulannya dengan membuka cabang baru.

Walaupun berumur kurang dari 1 tahun, DQLab Finance sudah mempunyai banyak cabang, oleh karena itu perlu dipantau bagaimana performa dari cabang - cabang tersebut.

Pada masing-masing cabang, terdapat agen-agen yang bertugas mencari dan mendata calon mitra yang akan mengajukan pinjaman kepada DQLab Finance. Lalu jika sudah disetujui, agen juga yang akan memberikan uang tersebut kepada mitra.

LANGKAH-LANGKAH PENGERJAAN

Pada project kali ini, akan dianalisis bagaimana performa cabang pada Mei 2020.
Langkah yang akan dilakukan adalah:
1. Memfilter data untuk bulan Mei 2020
2. Membuat summary per cabang untuk melihat data 5 cabang terbaik dan terburuk
3. Karena cabang bertambah setiap bulannya, maka perlu dicek umur cabang dan performa Mei
4. Mencari cabang terburuk untuk masing - masing kelompok umur
5. Mennganalisis performa agen pada cabang dengan performa terendah

DATA

Data yang digunakan diperoleh dari 'https://storage.googleapis.com/dqlab-dataset/loan_disbursement.csv'
Data terdiri dari 5 kolom yaitu:
+ loan_id : ID dari data ini
+ tanggal_cair : tanggal uang diberikan kepada mitra
+ cabang : lokasi agen bekerja dan tempat mitra terdaftar
+ agen : petugas lapangan yang melakukan pencairan
+ amount : jumlah uang yang dicairkan
