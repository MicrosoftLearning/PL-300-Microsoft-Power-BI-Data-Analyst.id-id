---
lab:
  title: Data Model di Power BI Desktop
  module: Module 4 - Design a Data Model in Power BI
ms.openlocfilehash: e6ffd23cf2b7861dad63a522734941b8f914bf88
ms.sourcegitcommit: 6853b027da7f5e739951c3eef54f4cd458854c66
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/12/2022
ms.locfileid: "146274823"
---
# <a name="model-data-in-power-bi-desktop"></a>**Membuat Model Data di Power BI Desktop**

**Perkiraan waktu untuk menyelesaikan lab adalah 45 menit**

Di lab ini Anda akan mulai mengembangkan model data. Lab ini akan melibatkan pembuatan hubungan antar tabel, dan kemudian mengonfigurasi properti tabel dan kolom untuk meningkatkan keramahan dan kegunaan model data. Anda juga akan membuat hierarki dan membuat tindakan cepat.

Di lab ini Anda mempelajari cara:

- Membuat hubungan model

- Mengonfigurasi properti tabel dan kolom

- Membuat hierarki


### <a name="lab-story"></a>**Cerita lab**

Lab ini adalah salah satu dari sekian banyak lab yang dirancang sebagai cerita lengkap, mulai dari persiapan data hingga publikasi sebagai laporan dan dasbor. Anda dapat menyelesaikan lab dalam urutan apa pun. Namun, jika Anda ingin mengerjakan beberapa lab sekaligus, untuk 10 lab pertama, sebaiknya Anda mengerjakannya dengan urutan berikut:

1. Mempersiapkan Data di Power BI Desktop

2. Muat Data di Power BI Desktop

3. **Membuat Model Data di Power BI Desktop**

5. Membuat Perhitungan DAX di Power BI Desktop, Bagian 1

6. Membuat Perhitungan DAX di Power BI Desktop, Bagian 2

7. Merancang Laporan di Power BI Desktop, Bagian 1

8. Merancang Laporan di Power BI Desktop, Bagian 2

9. Buat Dasbor Power BI

10. Menganalisis Data di Power BI Desktop

11. Terapkan Keamanan Tingkat Baris

## <a name="exercise-1-create-model-relationships"></a>**Latihan 1: Membuat Hubungan Model**

Dalam latihan ini Anda akan membuat hubungan model.

### <a name="task-1-get-started"></a>**Tugas 1: Mulai**

Dalam tugas ini Anda akan menyiapkan lingkungan untuk lab.

*Penting: Jika Anda melanjutkan dari lab sebelumnya (dan Anda berhasil menyelesaikan lab tersebut), jangan selesaikan tugas ini; sebagai gantinya, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Power BI Desktop, pada taskbar, klik pintasan Microsoft Power BI Desktop.

    ![Gambar 12](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image1.png)

1. Untuk menutup jendela memulai, di kiri atas jendela, klik **X**.

    ![Gambar 11](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image2.png)

1. Untuk membuka file Power BI Desktop pertama, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Buka Laporan**.

    ![Gambar 10](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image3.png)

1. Klik **Jelajahi Laporan**.

    ![Gambar 8](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image4.png)

1. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Labs\03-configure-data-model-in-power-bi-desktop\Starter**.

1. Pilih file **Analisis Penjualan**.

1. Klik **Buka**.

    ![Gambar 7](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image5.png)

1. Tutup semua jendela informasi yang mungkin terbuka.

1. Untuk membuat salinan file, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Simpan**.

    ![Gambar 5](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image6.png)

1. Jika diminta untuk menerapkan perubahan, klik **Terapkan**.

    ![Gambar 15](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image7.png)

1. Di jendela **Simpan Sebagai**, navigasikan ke folder **D:\PL300\MySolution**.

1. Klik **Simpan**.

    ![Gambar 3](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image8.png)

### <a name="task-2-create-model-relationships"></a>**Tugas 2: Membuat hubungan model**

Dalam tugas ini Anda akan membuat hubungan model.

1. Di Power BI Desktop, di sebelah kiri, klik ikon tampilan **Model**.

    ![Gambar 1](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image9.png)

2. Jika Anda tidak melihat ketujuh tabel, gulir secara horizontal ke kanan, lalu seret dan susun tabel lebih dekat bersama-sama sehingga semuanya dapat dilihat secara bersamaan.

    *Tips: Anda juga dapat menggunakan kontrol zoom yang terletak di bagian bawah jendela.*

    *Dalam tampilan Model, Anda dapat melihat setiap tabel dan hubungan (penghubung antar tabel). Saat ini, tidak ada hubungan karena di lab **Menyiapkan Data di Power BI Desktop**, Anda menonaktifkan opsi hubungan pemuatan data.*

3. Untuk kembali ke tampilan Laporan, di sebelah kiri, klik ikon tampilan **Laporan**.

    ![Gambar 327](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image10.png)

4. Untuk melihat semua bidang tabel, di panel **Bidang**, klik kanan area kosong, lalu pilih **Luaskan Semua**.

    ![Gambar 328](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image11.png)

5. Untuk membuat visual tabel, di panel **Bidang**, dari dalam tabel **Produk**, centang bidang **Kategori**.

    ![Gambar 329](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image12.png)

    *Lab menggunakan notasi steno untuk mereferensikan bidang. Ini akan terlihat seperti ini: **Produk \| Kategori**. Dalam contoh ini, **Produk** adalah nama tabel dan **Kategori** adalah nama bidang.*

6. Untuk menambahkan kolom tambahan ke tabel, di panel **Bidang**, centang bidang **Penjualan \| Penjualan**.

7. Perhatikan bahwa visual tabel mencantumkan empat kategori produk, dan nilai penjualannya sama untuk masing-masing kategori, dan sama untuk totalnya.

    ![Gambar 330](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image13.png)

    *Masalahnya adalah bahwa tabel didasarkan pada bidang dari tabel yang berbeda. Harapannya, setiap kategori produk menampilkan penjualan untuk kategori tersebut. Namun, karena tidak ada hubungan model antara tabel ini, tabel **Penjualan** tidak difilter. Sekarang Anda akan menambahkan hubungan untuk menyebarkan filter di antara tabel.*

8. Pada tab pita **Pemodelan**, dari dalam grup **Hubungan**, klik **Kelola Hubungan**.

    ![Gambar 331](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image14.png)

9. Di jendela **Kelola Hubungan**, perhatikan bahwa belum ada hubungan yang ditentukan.

10. Untuk membuat hubungan, klik **Baru**.

    ![Gambar 332](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image15.png)

11. Di jendela **Buat Hubungan**, dalam daftar dropdown pertama, pilih tabel **Produk**.

    ![Gambar 333](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image16.png)

12. Di daftar dropdown kedua (di bawah kisi tabel **Produk**), pilih tabel **Penjualan**.

    ![Gambar 334](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image17.png)

13. Perhatikan kolom **ProductKey** di setiap tabel telah dipilih secara otomatis.

    *Kolom dipilih karena memiliki nama dan tipe data yang sama.*

14. Dalam daftar dropdown **Kardinalitas**, perhatikan bahwa **Satu Ke Banyak (1:*)** dipilih.

    *Kardinalitas terdeteksi secara otomatis, karena Power BI memahami bahwa kolom **ProductKey** dari tabel **Produk** berisi nilai unik. Hubungan satu-ke-banyak adalah kardinalitas yang paling umum, dan semua hubungan yang Anda buat di lab ini akan menjadi jenis ini.*

15. Dalam daftar dropdown **Arah Filter Silang**, perhatikan bahwa **Tunggal** dipilih.

    *Satu arah filter berarti filter menyebar dari “satu sisi” ke “banyak sisi”. Dalam hal ini, ini berarti filter yang diterapkan ke tabel **Produk** akan menyebar ke tabel **Penjualan**, tetapi tidak ke arah yang berlawanan.*

16. Perhatikan bahwa **Tandai Hubungan Ini Aktif** dicentang.

    *Hubungan aktif menyebarkan filter. Anda dapat menandai hubungan sebagai tidak aktif sehingga filter tidak menyebar. Hubungan yang tidak aktif dapat terjadi ketika ada beberapa jalur hubungan antar tabel. Dalam hal ini, perhitungan model dapat menggunakan fungsi khusus untuk mengaktifkannya.*

17. Klik **OK**.

    ![Gambar 335](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image18.png)

18. Di jendela **Kelola Hubungan**, perhatikan bahwa hubungan baru terdaftar, lalu klik **Tutup**.

    ![Gambar 336](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image19.png)

19. Dalam laporan, perhatikan bahwa visual tabel diperbarui untuk menampilkan nilai yang berbeda untuk setiap kategori produk.

    ![Gambar 337](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image20.png)

    *Filter yang diterapkan ke tabel **Produk** sekarang menyebar ke tabel **Penjualan**.*

20. Beralih ke tampilan Model, lalu perhatikan sekarang ada konektor di antara dua tabel (tidak masalah jika tabel diposisikan bersebelahan).

    ![Gambar 338](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image21.png)

21. Dalam diagram, perhatikan bahwa Anda dapat menginterpretasikan kardinalitas yang diwakili oleh indikator **1** dan *****.

    *Arah filter diwakili oleh kepala panah. Garis solid mewakili hubungan aktif; garis putus-putus menunjukkan hubungan yang tidak aktif.*

22. Arahkan kursor ke atas hubungan untuk menyorot kolom terkait.

    *Ada cara yang lebih mudah untuk membuat hubungan. Dalam diagram model, Anda dapat menyeret dan meletakkan kolom untuk membuat hubungan baru.*

23. Untuk membuat hubungan baru menggunakan teknik yang berbeda, dari tabel **Pengecer**, seret kolom **ResellerKey** ke kolom **ResellerKey** di tabel **Penjualan**.

    ![Gambar 339](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image22.png)

    *Tips: Terkadang kolom tidak dapat diseret. Jika menemui masalah seperti ini, pilih kolom yang berbeda, lalu pilih kolom yang ingin Anda seret lagi, lalu coba lagi. Pastikan Anda melihat hubungan baru ditambahkan ke diagram.*

24. Gunakan teknik baru untuk membuat dua model hubungan berikut:

    - **Wilayah \| SalesTerritoryKey** ke **Penjualan \| SalesTerritoryKey**

    - **Penjual \| EmployeeKey** ke **Sales \| EmployeeKey**

25. Dalam diagram, atur tabel sehingga tabel **Penjualan** diposisikan di tengah diagram, dan tabel terkait diposisikan di atasnya. Posisikan tabel yang tidak terkait ke samping.

    ![Gambar 340](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image23.png)


26. Simpan file Power BI Desktop.

## <a name="exercise-2-configure-tables"></a>**Latihan 2: Mengonfigurasi Tabel**

Dalam latihan ini Anda akan mengonfigurasi setiap tabel dengan membuat hierarki, serta menyembunyikan, memformat, dan mengategorikan kolom.

### <a name="task-1-configure-the-product-table"></a>**Tugas 1: Mengonfigurasi tabel Produk**

Dalam tugas ini, Anda akan mengonfigurasi tabel **Produk**.

1. Dalam tampilan Model, di panel **Bidang**, jika perlu, luaskan tabel **Produk** untuk menampilkan semua bidang.

2. Untuk membuat hierarki, di panel **Bidang**, klik kanan kolom **Kategori**, lalu pilih **Buat Hierarki**.

    ![Gambar 341](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image24.png)

3. Di panel **Properti** (di sebelah kiri panel **Bidang**), di kotak **Nama**, ganti teks dengan **Produk**.

    ![Gambar 344](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image25.png)

4. Untuk menambahkan tingkat kedua ke hierarki, di panel **Properti**, di daftar dropdown **Hierarki**, pilih **Subkategori** (Anda mungkin perlu menggulir ke bawah di dalam panel ).

5. Untuk menambahkan tingkat ketiga ke hierarki, dalam daftar dropdown **Hierarki**, pilih **Produk**.

6. Untuk menyelesaikan desain hierarki, klik **Terapkan Perubahan Tingkat**.

    ![Gambar 343](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image26.png)

    *Tips: Jangan lupa untuk mengeklik **Terapkan Perubahan Tingkat**—mengabaikan langkah ini adalah kesalahan yang sering dilakukan.*

7. Di panel **Bidang**, perhatikan hierarki **Produk**.

    ![Gambar 347](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image27.png)

8. Untuk menampilkan tingkat hierarki, perluas hierarki **Produk**.

    ![Gambar 346](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image28.png)

9. Untuk mengatur kolom ke dalam folder tampilan, di panel **Bidang**, pilih kolom **Format Warna Latar Belakang** terlebih dahulu.

10. Sambil menekan tombol **Ctrl**, pilih kolom **Format Warna Fon**.

11. Di panel **Properti**, di kotak **Folder Tampilan**, masukkan **Pemformatan**.

    ![Gambar 348](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image29.png)

12. Di panel **Bidang**, perhatikan bahwa kedua kolom sekarang berada di dalam folder.

    ![Gambar 349](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image30.png)

    *Menampilkan folder adalah cara yang bagus untuk mendeklarasikan tabel—terutama untuk tabel yang terdiri dari banyak bidang.*

### <a name="task-2-configure-the-region-table"></a>**Tugas 2: Mengonfigurasi tabel Wilayah**

Dalam tugas ini, Anda akan mengonfigurasi tabel **Wilayah**.

1. Dalam tabel **Wilayah**, buat hierarki bernama **Wilayah**, dengan tiga tingkat berikut:

    - Grup

    - Negara

    - Wilayah

    ![Gambar 350](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image31.png)

2. Pilih kolom **Negara** (bukan tingkat hierarki **Negara**).

3. Di panel **Properti**, luaskan bagian **Tingkat Lanjut** (di bagian bawah panel), lalu di daftar dropdown **Kategori Data**, pilih **Negara /Wilayah**.

    ![Gambar 352](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image32.png)

    *Kategorisasi data dapat memberikan petunjuk kepada perancang laporan. Dalam hal ini, mengategorikan kolom sebagai negara atau wilayah memberikan informasi yang lebih akurat ke Power BI saat membuat visualisasi peta.*

### <a name="task-3-configure-the-reseller-table"></a>**Tugas 3: Mengonfigurasi tabel Pengecer**

Dalam tugas ini, Anda akan mengonfigurasi tabel **Pengecer**.

1. Di tabel **Pengecer**, buat hierarki bernama **Pengecer**, dengan dua tingkat berikut:

    - Jenis Bisnis

    - Pengecer

    ![Gambar 351](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image33.png)

2. Buat hierarki kedua bernama **Geografi**, dengan empat tingkat berikut:

    - Negara-Wilayah

    - Negara Bagian-Provinsi

    - Kota

    - Pengecer

    ![Gambar 353](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image34.png)

3. Atur **Kategori Data** untuk kolom **Negara-Wilayah**, **Negara-Provinsi**, dan **Kota** (bukan tingkat hierarki) ke **Negara/Wilayah**, **Negara Bagian atau Provinsi**, dan **Kota**. 

### <a name="task-4-configure-the-sales-table"></a>**Tugas 4: Mengonfigurasi tabel Penjualan**

Dalam tugas ini, Anda akan mengonfigurasi tabel **Penjualan**.

1. Di tabel **Penjualan**, pilih kolom **Biaya**.

2. Di panel **Properti**, di kotak **Deskripsi**, masukkan: **Berdasarkan biaya standar**

    ![Gambar 358](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image35.png)

    *Deskripsi dapat diterapkan ke tabel, kolom, hierarki, atau ukuran. Di panel **Bidang**, teks deskripsi ditampilkan dalam tipsalat saat penulis laporan mengarahkan kursor ke bidang tersebut.*

3. Pilih kolom **Kuantitas**.

4. Di panel **Properti**, dari dalam bagian **Pemformatan**, geser properti **Pemisah Ribuan** ke **Ya**.

    ![Gambar 357](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image36.png)

5. Pilih kolom **Harga Satuan**.

6. Di panel **Properti**, dari dalam bagian **Pemformatan**, atur properti **Tempat Desimal** ke **2**.

7. Di grup **Tingkat Lanjut** (Anda mungkin perlu menggulir ke bawah untuk menemukannya), dalam daftar dropdown **Ringkas Berdasarkan**, pilih **Rata-rata**.

    ![Gambar 354](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image37.png)

    *Secara default, kolom numerik akan diringkas dengan menjumlahkan nilai. Perilaku default ini tidak sesuai untuk kolom seperti **Harga Satuan**, yang menunjukkan tarif. Mengatur peringkasan default ke rata-rata akan membuahkan hasil yang berarti.*

### <a name="task-5-bulk-update-properties"></a>**Tugas 5: Memperbarui properti secara massal**

Dalam tugas ini Anda akan memperbarui beberapa kolom menggunakan pembaruan massal tunggal. Anda akan menggunakan pendekatan ini untuk menyembunyikan kolom, dan memformat nilai kolom.

1. Di panel **Bidang**, pilih kolom **Produk \| ProductKey**.

2. Saat menekan tombol **Ctrl**, pilih 13 kolom berikut (mencakup beberapa tabel):

    - Wilayah \| SalesTerritoryKey

    - Pengecer \| ResellerKey

    - Penjualan \| EmployeeKey
    
    - Penjualan \| ProductKey

    - Penjualan \| ResellerKey

    - Penjualan \| SalesOrderNumber

    - Penjualan \| SalesTerritoryKey

    - Penjual \| EmployeeID

    - Penjual \| EmployeeKey

    - Penjual \| UPN

    - SalespersonRegion \| EmployeeKey

    - SalespersonRegion \| SalesTerritoryKey

    - Target \| EmployeeID

3. Di panel **Properti**, geser properti **Tersembunyi** ke **Ya**.

    ![Gambar 355](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image38.png)

    *Kolom disembunyikan karena digunakan oleh hubungan atau akan digunakan dalam konfigurasi keamanan tingkat baris atau logika perhitungan.*

    *Anda akan menggunakan **SalesOrderNumber** dalam perhitungan di lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 1**.*

4. Pilih tiga kolom berikut:

    - Produk \| Biaya Standar

    - Penjualan \| Biaya

    - Penjualan \| Penjualan

5. Di panel **Properti**, dari dalam bagian **Pemformatan**, atur properti **Tempat Desimal** ke **0** (nol).

    ![Gambar 356](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image39.png)

## <a name="exercise-3-review-the-model-interface"></a>**Latihan 3: Meninjau Antarmuka Model**

Dalam latihan ini Anda akan beralih ke tampilan Laporan, dan meninjau antarmuka model.

### <a name="task-1-review-the-model-interface"></a>**Tugas 1: Meninjau antarmuka model**

Dalam tugas ini Anda akan beralih ke tampilan Laporan, dan meninjau antarmuka model.

1. Beralih ke tampilan Laporan.

2. Di panel **Bidang**, perhatikan hal berikut:

    - Kolom, hierarki, dan levelnya adalah bidang, yang dapat digunakan untuk mengonfigurasi visual laporan

    - Hanya bidang yang relevan dengan penulisan laporan yang terlihat

    - Tabel **SalespersonRegion** tidak terlihat—karena semua bidangnya disembunyikan

    - Bidang spasial di tabel **Wilayah** dan **Pengecer** dihiasi dengan ikon spasial

    - Bidang yang dihiasi dengan simbol sigma (Ʃ) akan diringkas, secara default

    - Keterangan alat muncul saat mengarahkan kursor ke bidang **Penjualan \| Biaya**

3. Perluas bidang **Penjualan \|OrderDate**, lalu perhatikan bahwa bidang tersebut mengungkapkan hierarki tanggal.

    ![Gambar 359](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image40.png)

    *Bidang **Target \| TargetMonth** memberikan hierarki yang serupa. Hierarki ini tidak dibuat oleh Anda. Hierarki dibuat secara otomatis. Sayangnya, ada satu masalah. Tahun keuangan Adventure Works dimulai pada 1 Juli setiap tahun. Namun, dalam hierarki tanggal yang dibuat secara otomatis ini, tahun hierarki tanggal dimulai pada 1 Januari setiap tahun.*

    *Sekarang Anda akan menonaktifkan perilaku otomatis ini. Di lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 1**, Anda akan menggunakan DAX untuk membuat tabel tanggal, dan mengonfigurasinya untuk menentukan kalender Adventure Works.*

4. Untuk mematikan waktu otomatis/tanggal, klik tab pita **File** untuk membuka tampilan backstage.

5. Di sebelah kiri, pilih **Opsi dan Pengaturan**, lalu pilih **Opsi**.

    ![Gambar 360](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image41.png)

6. Di jendela **Opsi**, di sebelah kiri, dalam grup **File Saat Ini**, pilih **Pemuatan Data**.

    ![Gambar 361](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image42.png)

7. Di bagian **Inteligensi Waktu**, hapus centang **Tanggal/Waktu Otomatis**.

    ![Gambar 362](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image43.png)

8. Klik **OK**.

    ![Gambar 9](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image44.png)

9. Di panel **Bidang**, perhatikan bahwa hierarki tanggal tidak lagi tersedia.

    ![Gambar 363](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image45.png)


## <a name="exercise-4-create-quick-measures"></a>**Latihan 4: Membuat Tindakan Cepat**

Dalam latihan ini Anda akan membuat dua langkah cepat.

### <a name="task-1-create-quick-measures"></a>**Tugas 1: Membuat tindakan cepat**

Dalam tugas ini Anda akan membuat dua langkah cepat untuk menghitung keuntungan dan margin keuntungan.

1. Di panel **Bidang**, klik kanan tabel **Penjualan**, lalu pilih **Pengukuran Cepat Baru**.

    ![Gambar 366](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image46.png)

2. Di jendela **Pengukuran Cepat**, dalam daftar dropdown **Perhitungan**, dari dalam grup **Operasi Matematika**, pilih **Pengurangan**.

    ![Gambar 367](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image47.png)

3. Di panel **Bidang** dari jendela **Tindakan Cepat**, luaskan tabel **Penjualan**.

4. Seret bidang **Penjualan** ke dalam kotak **Nilai Dasar**.

5. Seret bidang **Biaya** ke dalam kotak **Nilai yang akan Dikurangi**.

    ![Gambar 368](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image48.png)

6. Klik **OK**.

    ![Gambar 369](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image49.png)

    *Pengukuran cepat membuat rumus perhitungan untuk Anda. Pengukuran ini mudah dan cepat dibuat untuk perhitungan sederhana dan umum. Anda akan membuat pengukuran tanpa menggunakan alat ini di lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 1**.*

7. Di panel **Bidang**, di dalam tabel **Penjualan**, perhatikan pengukuran baru tersebut.

    ![Gambar 370](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image50.png)

    *Ukuran dilapisi dengan ikon kalkulator.*

8. Untuk mengganti nama ukuran, klik kanan, lalu pilih **Ganti nama**.

    ![Gambar 371](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image51.png)

    *Tips: Untuk mengganti nama bidang, Anda juga dapat mengekliknya dua kali, atau memilihnya dan menekan **F2**.*

9. Ganti nama ukuran menjadi **Keuntungan**, lalu tekan **Enter**.

10. Di tabel **Penjualan**, tambahkan pengukuran cepat kedua, berdasarkan persyaratan berikut:

    - Gunakan operasi matematika **Pembagian**

    - Atur **Pembilang** ke bidang **Penjualan \| Keuntungan**

    - Atur **Penyebut** ke bidang **Penjualan \| Penjualan**

    - Ganti nama ukuran menjadi **Margin Keuntungan**

    ![Gambar 372](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image52.png)

    ![Gambar 373](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image53.png)

11. Pastikan ukuran **Margin Keuntungan** dipilih, lalu pada pita kontekstual **Alat Pengukuran**, atur format ke **Persentase**, dengan dua tempat desimal.

    ![Gambar 374](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image54.png)

12. Untuk menguji kedua ukuran tersebut, pertama-tama pilih visual tabel pada halaman laporan.

13. Di panel **Bidang**, centang kedua ukuran.

    ![Gambar 375](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image55.png)

14. Klik dan seret panduan yang tepat untuk memperlebar visual tabel.

    ![Gambar 376](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image56.png)

15. Verifikasi bahwa langkah-langkah tersebut membuahkan hasil yang masuk akal yang diformat dengan benar.

    ![Gambar 378](Linked_image_Files/03-configure-data-model-in-power-bi-desktop_image57.png)

### <a name="task-2-create-a-many-to-many-relationship"></a>**Tugas 2: Membuat hubungan banyak-ke-banyak**

Dalam tugas ini, Anda akan membuat hubungan banyak ke banyak antara tabel **Penjual** dan tabel **Penjualan**.

1. Di Power BI Desktop, dalam tampilan Laporan, di panel **Bidang**, centang dua bidang berikut untuk membuat visual tabel:

    - Penjual \| Penjual

    - Penjualan \| Penjualan

    *Lab menggunakan notasi steno untuk mereferensikan bidang. Ini akan terlihat seperti ini: **Penjual \| Penjual**. Dalam contoh ini, **Penjual** adalah nama tabel dan **Penjual** adalah nama bidang.*

    ![Gambar 1](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image9.png)

    *Tabel menampilkan penjualan yang dilakukan oleh setiap penjual. Namun, ada hubungan lain antara penjual dan penjualan. Beberapa penjual termasuk dalam satu, dua, atau mungkin lebih banyak wilayah penjualan. Selain itu, wilayah penjualan dapat memiliki beberapa penjual yang ditugaskan dalam wilayah tersebut.*

    *Dari perspektif manajemen performa, penjualan penjual (berdasarkan wilayah yang ditetapkan) perlu dianalisis dan dibandingkan dengan target penjualan. Anda akan membuat hubungan untuk mendukung analisis ini pada latihan berikutnya.*

2. Perhatikan bahwa Michael Blythe telah menjual hampir $9 juta.

3. Beralih ke tampilan Model.

    ![Gambar 10](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image10.png)

4. Seret tabel **SalespersonRegion** untuk memosisikannya di antara tabel **Wilayah** dan **Penjual**.

5. Gunakan teknik seret dan letakkan untuk membuat dua hubungan model berikut:

    - **Penjual \| EmployeeKey** ke **SalespersonRegion \| EmployeeKey**

    - **Wilayah \| SalesTerritoryKey** ke **SalespersonRegion \| SalesTerritoryKey**

    *Tabel **SalespersonRegion** dapat dianggap sebagai tabel penghubung.*

6. Beralih ke tampilan Laporan, lalu perhatikan bahwa visualnya belum diperbarui—hasil penjualan untuk Michael Blythe tidak berubah.

7. Beralih kembali ke tampilan Model, lalu ikuti arah filter hubungan (panah) dari tabel **Penjual**.

    *Pertimbangkan bahwa tabel **Penjual** memfilter tabel **Penjualan**. Tabel ini juga memfilter tabel **SalespersonRegion**, tetapi tidak melanjutkan dengan menyebarkan filter ke tabel **Wilayah** (panah menunjuk ke arah yang salah).*

    ![Gambar 380](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image11.png)

8. Untuk mengedit hubungan antara tabel **Wilayah** dan **SalespersonRegion**, klik dua kali hubungan tersebut.

9. Di jendela **Edit Hubungan**, dalam daftar dropdown **Arah Filter Silang**, pilih **Keduanya**.

10. Centang kotak **Terapkan Filter Keamanan di Kedua Arah**.

    ![Gambar 381](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image12.png)

11. Klik **OK**.

    ![Gambar 335](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image13.png)

12. Perhatikan bahwa hubungan memiliki panah ganda.

    ![Gambar 382](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image14.png)

13. Beralih ke tampilan Laporan, lalu perhatikan bahwa nilai penjualan masih belum berubah.

    *Masalahnya sekarang berkaitan dengan fakta bahwa ada dua kemungkinan jalur penyebaran filter antara tabel **Penjual** dan **Penjualan**. Ambiguitas ini diselesaikan secara internal, berdasarkan penilaian “jumlah tabel paling sedikit”. Untuk memperjelas, Anda tidak boleh merancang model dengan jenis ambiguitas ini—masalah ini akan dibahas sebagian nanti di lab ini, dan setelah menyelesaikan lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 1**.*

14. Beralih ke tampilan Model.

15. Untuk memaksa penyebaran filter melalui tabel penghubung, edit (klik dua kali) hubungan antara tabel **Penjual** dan **Penjualan**.

16. Di jendela **Edit Hubungan**, hapus centang pada kotak **Buat Hubungan Ini Aktif**.

    ![Gambar 383](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image15.png)

17. Klik **OK**.

    ![Gambar 5696](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image16.png)

    *Propagasi filter sekarang akan mengikuti satu-satunya jalur yang aktif.*

18. Dalam diagram, perhatikan bahwa hubungan tidak aktif diwakili oleh garis putus-putus.

    ![Gambar 5697](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image17.png)

19. Beralih ke tampilan Laporan, lalu perhatikan bahwa penjualan Michael Blythe sekarang hampir $22 juta.

    ![Gambar 5698](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image18.png)

20. Perhatikan juga, bahwa penjualan untuk setiap penjual—jika ditambahkan—akan melebihi total tabel.

    *Ini adalah pengamatan umum dari hubungan banyak ke banyak karena penghitungan hasil penjualan regional dua kali lipat, tiga kali lipat, dll. Pertimbangkan Brian Welcker, penjual kedua yang terdaftar. Jumlah penjualannya sama dengan jumlah total penjualan. Ini adalah hasil yang benar hanya karena dia adalah Direktur Penjualan; penjualannya diukur dengan penjualan semua wilayah.*

    *Sementara hubungan banyak-ke-banyak sekarang berfungsi, sekarang tidak mungkin untuk menganalisis penjualan yang dilakukan oleh penjual (karena hubungan tidak aktif). Anda akan dapat mengaktifkan kembali hubungan saat memperkenalkan tabel terhitung yang akan memungkinkan analisis penjualan yang dilakukan di wilayah penjualan yang ditetapkan ke penjual (untuk analisis performa) di lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 1**.*

21. Beralih ke tampilan Pemodelan, lalu dalam diagram, pilih tabel **Penjual**.

22. Di panel **Properti**, di kotak **Nama**, ganti teks dengan **Penjual (Performa)** .

    *Tabel yang diganti namanya sekarang mencerminkan tujuannya: digunakan untuk melaporkan dan menganalisis performa penjual berdasarkan penjualan di wilayah penjualan yang ditetapkan untuk mereka.*

### <a name="task-3-relate-the-targets-table"></a>**Tugas 3: Membuat hubungan tabel Target**

Dalam tugas ini Anda akan membuat hubungan ke tabel **Target**

1. Buat hubungan dari kolom **Penjual (Performa) \| EmployeeID** dan kolom **Target \| EmployeeID**.

2. Dalam tampilan Laporan, tambahkan bidang **Target \| Target** ke visual tabel.

3. Ubah ukuran visual tabel sehingga semua kolom terlihat.

    ![Gambar 5699](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image19.png)

    *Tabel sekarang memvisualisasikan penjualan dan target—tetapi berhati-hatilah dengan dua alasan berikut. Pertama, tidak ada filter pada periode waktu, sehingga target juga mencakup jumlah target di masa mendatang. Kedua, target tidak aditif, sehingga total tidak boleh ditampilkan. Total dapat dinonaktifkan dengan memformat visual atau dihapus dengan menggunakan logika perhitungan. Anda akan mengikuti pendekatan kedua dengan membuat ukuran target di lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 2** yang akan mengembalikan BLANK saat lebih dari satu staf penjualan difilter.*

### <a name="task-4-finish-up"></a>**Tugas 4: Selesaikan**

Dalam tugas ini Anda akan menyelesaikan lab.

1. Simpan file Power BI Desktop.

2. Jika diminta untuk menerapkan kueri, klik **Terapkan Nanti**.

3. Jika Anda ingin memulai lab berikutnya, biarkan Power BI Desktop tetap terbuka.
