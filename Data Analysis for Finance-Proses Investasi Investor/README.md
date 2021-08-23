LATAR BELAKANG

DQLab Finance merupakan perusahaan peer to peer lending, sehingga DQLab Finance membutuhkan investor untuk memberikan pinjaman kepada calon borrower.

Setiap ada borrower yang mengajukan pinjaman, DQLab Finance akan mengupload loan itu ke marketplace lalu kemudian investor yang sudah mendaftar akan melihat loan tersebut, jika ada yang cocok maka mereka akan order lalu bayar. Sehingga investor tersebut membiayai loan yang tadi dipilih.

Pada project kali ini, akan dilakukan analisis terhadap proses investasi dari investor tersebut.

LANGKAH-LANGKAH PENGERJAAN

menganalisis proses investasi dari investor yang terdaftar di DQLab Finance dan bagaimana behaviornya

1. Eksplorasi data
2. Manipulasi data
3. Analisis proses investasi
4. Analisis waktu sampai investasi pertama
5. Analisis retention invest

DATA

Data yang digunakan diperoleh dari :'https://storage.googleapis.com/dqlab-dataset/event.csv'

+ loan_id : unik ID dari loan yang diupload ke marketplace
+ investor_id : unik ID dari investor yang terdaftar
+ nama_event : kegiatan yang dilakukan oleh investor dan perubahan status loan
+ created_at : waktu (sampai detik) event terjadi

Keterangan nama_event :

+ investor_register : Event saat Investor register. Jumlah event sama dengan unik investor, artinya setiap investor melakukan event ini hanya 1 kali. Jumlah loan hanya 1, ini isinya NA, karena register ini tidak memerlukan loan.
+ loan_to_marketplace : Event saat loan diupload ke marketplace, Jumlah event sama dengan jumlah loan, artinya setiap loan diupload hanya 1 kali. Jumlah investor hanya 1, ini isi NA, karena saat upload ke marketplace tidak berhubungan dengan investor
+ investor_view_loan : Event saat investor melihat detail loan di marketplace. Jumlah event nya tidak sama dengan unik loan maupun unik investor, artinya 1 investor dapat melihat loan yang sama beebrapa kali, dan 1 loan bisa dilihat oleh beberapa investor berbeda
+ investor_order_loan : Event saat investor memesan loan, menunggu pembayaran. Jumlah event nya tidak sama dengan unik loan maupun unik investor, artinya 1 loan bisa dipesan oleh beberapa investor berbeda (jika pemesanan sebelumnya tidak dibayar)
+ investor_pay_loan : Event saat investor membayar loan dari pesanan sebelumnya. Jumlah Event nya sama dengan unik loan, artinya 1 loan ini hanya bisa dibayar oleh 1 investor. Jumlah investor lebih sedikit daripada jumlah loan artinya 1 investor bisa membeli banyak loan
