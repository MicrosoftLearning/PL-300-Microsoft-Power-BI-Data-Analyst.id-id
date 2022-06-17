---
lab:
  title: Membuat Perhitungan DAX di Power BI Desktop, Bagian 1
  module: Module 5 - Create Model Calculations using DAX in Power BI
ms.openlocfilehash: 3bbdf3dfb4b302a9b3c28005976ff34764c1c542
ms.sourcegitcommit: d88b7941fe3805f0bc2979ea864c5483ec289c75
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/04/2022
ms.locfileid: "146071703"
---
# <a name="create-dax-calculations-in-power-bi-desktop-part-1"></a>**Membuat Perhitungan DAX di Power BI Desktop, Bagian 1**

**Perkiraan waktu untuk menyelesaikan lab adalah 45 menit**

Di lab ini Anda akan membuat tabel terhitung, kolom terhitung, dan pengukuran sederhana menggunakan Data Analysis Expressions (DAX).

Di lab ini Anda mempelajari cara:

- Membuat tabel terhitung

- Membuat kolom terhitung

- Buat langkah-langkah

### <a name="lab-story"></a>**Cerita lab**

Lab ini adalah salah satu dari sekian banyak lab yang dirancang sebagai cerita lengkap, mulai dari persiapan data hingga publikasi sebagai laporan dan dasbor. Anda dapat menyelesaikan lab dalam urutan apa pun. Namun, jika Anda ingin mengerjakan beberapa lab sekaligus, untuk 10 lab pertama, sebaiknya Anda mengerjakannya dengan urutan berikut:

1. Mempersiapkan Data di Power BI Desktop

2. Muat Data di Power BI Desktop

3. Data Model di Power BI Desktop

5. **Membuat Perhitungan DAX di Power BI Desktop, Bagian 1**

6. Membuat Perhitungan DAX di Power BI Desktop, Bagian 2

7. Merancang Laporan di Power BI Desktop, Bagian 1

8. Merancang Laporan di Power BI Desktop, Bagian 2

9. Buat Dasbor Power BI

10. Menganalisis Data di Power BI Desktop

11. Terapkan Keamanan Tingkat Baris

## <a name="exercise-1-create-calculated-tables"></a>**Latihan 1: Membuat Tabel Terhitung**

Dalam latihan ini Anda akan membuat dua tabel terhitung. Yang pertama adalah tabel **Penjual**, untuk memungkinkan hubungan langsung antara tabel tersebut dan tabel **Penjualan**. Yang kedua adalah tabel **Tanggal**.

### <a name="task-1-get-started"></a>**Tugas 1: Mulai**

Dalam tugas ini Anda akan menyiapkan lingkungan untuk lab.

*Penting: Jika Anda melanjutkan dari lab sebelumnya (dan Anda berhasil menyelesaikan lab tersebut), jangan selesaikan tugas ini; sebagai gantinya, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Power BI Desktop, pada taskbar, klik pintasan Microsoft Power BI Desktop.

    ![Gambar 50](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image1.png)

1. Untuk menutup jendela memulai, di kiri atas jendela, klik **X**.

    ![Gambar 49](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image2.png)

1. Untuk membuka file Power BI Desktop pertama, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Buka Laporan**.

    ![Gambar 48](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image3.png)

1. Klik **Jelajahi Laporan**.

    ![Gambar 47](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image4.png)

1. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Labs\04-create-dax-calculations-in-power-bi-desktop\Starter**.

1. Pilih file **Analisis Penjualan**.

1. Klik **Buka**.

    ![Gambar 35](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image5.png)

1. Tutup semua jendela informasi yang mungkin terbuka.

1. Untuk membuat salinan file, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Simpan**.

    ![Gambar 34](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image6.png)

1. Jika diminta untuk menerapkan perubahan, klik **Terapkan**.

    ![Gambar 25](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image7.png)

1. Di jendela **Simpan Sebagai**, navigasikan ke folder **D:\PL300\MySolution**.

1. Klik **Simpan**.

    ![Gambar 13](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image8.png)

### <a name="task-2-create-the-salesperson-table"></a>**Tugas 2: Membuat tabel Penjual**

Dalam tugas ini, Anda akan membuat tabel **Penjual** (hubungan langsung dengan **Penjualan**).

1. Di Power BI Desktop, dalam tampilan Laporan, pada pita **Pemodelan**, dari dalam grup **Perhitungan**, klik **Tabel Baru**.

    ![Gambar 1](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image9.png)

2. Di bilah rumus (yang terbuka langsung di bawah pita saat membuat atau mengedit perhitungan), ketik **Penjual =** , tekan **Shift+Enter**, ketik **'Penjual (Performa)'** , lalu tekan **Enter**.

    ![Gambar 4](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image10.png)

    *Demi kenyamanan Anda, semua definisi DAX di lab ini dapat disalin dari file cuplikan, yang terletak di **D:\PL300\Labs\04-create-dax-calculations-in-power-bi-desktop\Assets \Snippets.txt**.*

    *Tabel terhitung dibuat dengan terlebih dahulu memasukkan nama tabel, diikuti dengan simbol sama dengan (=), diikuti dengan rumus DAX yang mengembalikan tabel. Perhatikan bahwa nama tabel tidak boleh ada dalam model data.*

    *Bilah rumus mendukung memasukkan rumus DAX yang valid. Ini mencakup fitur seperti pelengkapan otomatis, Intellisense, dan kode warna, memungkinkan Anda memasukkan rumus dengan cepat dan akurat.*

    *Definisi tabel ini membuat salinan tabel **Penjual (Performa)** . Definisi ini hanya menyalin data, namun properti model seperti visibilitas, pemformatan, dll. tidak disalin.*

    *Tips: Anda dianjurkan untuk memasukkan "white space" (yaitu carriage return dan tab) ke rumus tata letak dalam format yang intuitif dan mudah dibaca—terutama jika rumus panjang dan rumit. Untuk memasukkan carriage return, tekan **Shift+Enter**. “White space” bersifat opsional.*

3. Di panel **Bidang**, perhatikan bahwa ikon tabel berwarna biru (menunjukkan tabel terhitung).

    ![Gambar 10](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image11.png)

    *Tabel terhitung ditentukan dengan menggunakan rumus DAX yang mengembalikan tabel. Penting untuk dipahami bahwa tabel terhitung meningkatkan ukuran model data karena tabel terhitung mewujudkan dan menyimpan nilai. Tabel terhitung dihitung ulang setiap kali dependensi formula direfresh, seperti yang akan terjadi pada model data ini ketika nilai tanggal baru (yang akan datang) dimuat ke dalam tabel.*

    *Tidak seperti tabel yang bersumber dari Power Query, tabel terhitung tidak dapat digunakan untuk memuat data dari sumber data eksternal. Tabel terhitungn hanya dapat mengubah data berdasarkan apa yang telah dimuat ke dalam model data.*

4. Beralih ke tampilan Model.

5. Perhatikan bahwa tabel **Penjual** tersedia (hati-hati, tabel mungkin disembunyikan dalam tampilan, dalam hal ini gulir secara horizontal untuk menemukannya).

6. Buat hubungan dari kolom **Penjual \| EmployeeKey** ke kolom **Penjualan \| EmployeeKey**.

7. Klik kanan hubungan tidak aktif antara tabel **Penjual (Performa)** dan **Penjualan**, lalu pilih **Hapus**.

    ![Gambar 2](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image12.png)

8. Saat diminta untuk mengonfirmasi penghapusan, klik **OK**.

    ![Gambar 3](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image13.png)

9. Di tabel **Penjual**, pilih beberapa kolom berikut, lalu sembunyikan (atur properti **Tersembunyi** ke **Ya**):

    - IDKaryawan

    - EmployeeKey

    - UPN

10. Dalam diagram model, pilih tabel **Penjual**.

11. Di panel **Properti**, di kotak **Deskripsi**, masukkan: **Penjual yang terkait dengan Penjualan**

    *Anda mungkin ingat bahwa deskripsi muncul sebagai tipsalat di panel **Bidang** saat pengguna mengarahkan kursor ke tabel atau bidang.*

12. Untuk tabel **Penjual (Performa)** , atur deskripsi ke: **Penjual yang terkait dengan wilayah**

    *Model data sekarang memberikan dua alternatif saat menganalisis penjual. Tabel **Penjual** memungkinkan analisis penjualan yang dilakukan oleh staf penjualan, sedangkan tabel **Penjual (Performa)** memungkinkan analisis penjualan yang dilakukan di wilayah penjualan yang ditetapkan untuk staf penjualan.*

### <a name="task-3-create-the-date-table"></a>**Tugas 3: Membuat tabel Tanggal**

Dalam tugas ini Anda akan membuat tabel **Tanggal**.

1. Beralih ke tampilan Data.

    ![Gambar 29](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image14.png)

2. Pada tab pita **Beranda**, dari dalam grup **Perhitungan**, klik **Tabel Baru**.

    ![Gambar 5](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image15.png)

3. Di bilah rumus, masukkan berikut ini:


    **DAX**


    ```
    Date =  
    CALENDARAUTO(6)
    ```


    ![Gambar 6](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image16.png)

    
    *Fungsi CALENDARAUTO() mengembalikan tabel kolom tunggal yang terdiri dari nilai tanggal. Perilaku "otomatis" memindai semua kolom tanggal model data untuk menentukan nilai tanggal paling awal dan terbaru yang disimpan dalam model data. Perilaku ini kemudian membuat satu baris untuk setiap tanggal dalam rentang ini, memperluas rentang di kedua arah untuk memastikan bahwa data selama satu tahun penuh disimpan.*

    *Fungsi ini dapat mengambil satu argumen opsional yang merupakan angka bulan terakhir dalam setahun. Jika dihilangkan, nilainya adalah 12, artinya Desember adalah bulan terakhir dalam setahun. Dalam hal ini, 6 dimasukkan, artinya Juni adalah bulan terakhir dalam setahun.*

4. Perhatikan kolom nilai tanggal.

    ![Gambar 7](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image17.png)

    *Tanggal yang ditampilkan diformat menggunakan pengaturan regional AS (yaitu bb/hh/tttt).*

5. Di sudut kiri bawah, di bilah status, perhatikan statistik tabel, yang mengonfirmasi bahwa 1.826 baris data telah dibuat, yang mewakili data lima tahun penuh.

    ![Gambar 9](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image18.png)

### <a name="task-4-create-calculated-columns"></a>**Tugas 4:** **Membuat kolom terhitung**

Dalam tugas ini, Anda akan menambahkan kolom tambahan untuk mengaktifkan pemfilteran dan pengelompokan berdasarkan periode waktu yang berbeda. Anda juga akan membuat kolom terhitung untuk mengontrol urutan kolom lainnya.

*Demi kenyamanan Anda, semua definisi DAX di lab ini dapat disalin dari file cuplikan, yang terletak di **D:\PL300\Labs\04-create-dax-calculations-in-power-bi-desktop\Assets \Snippets.txt**.*

1. Pada pita kontekstual **Alat Tabel**, dari dalam grup **Perhitungan**, klik **Kolom Baru**.

    ![Gambar 11](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image19.png)

2. Di bilah rumus, ketik berikut ini (atau salin dari file cuplikan), lalu tekan **Enter**:


    **DAX**


    ```
    Year =
    "FY" & YEAR('Date'[Date]) + IF(MONTH('Date'[Date]) > 6, 1)
    ```


    *Kolom terhitung dibuat dengan terlebih dahulu memasukkan nama kolom, diikuti dengan simbol sama dengan (=), diikuti dengan rumus DAX yang mengembalikan hasil nilai tunggal. Nama kolom tidak boleh ada di tabel.*

    *Rumusnya menggunakan nilai tahun tanggal tetapi menambahkan satu ke nilai tahun saat bulannya setelah Juni. Begitulah cara menghitung tahun fiskal di Adventure Works.*

3. Verifikasi bahwa kolom baru telah ditambahkan.

    ![Gambar 12](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image20.png)

4. Gunakan definisi file cuplikan untuk membuat dua kolom terhitung berikut untuk tabel **Tanggal**:

    - Kuartal

    - Bulan

    ![Gambar 14](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image21.png)

5. Untuk memvalidasi perhitungan, alihkan ke tampilan Laporan.

6. Untuk membuat halaman laporan baru, di kiri bawah, klik ikon plus.

    ![Gambar 15](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image22.png)

7. Untuk menambahkan visual matriks ke halaman laporan baru, di panel **Visualisasi**, pilih jenis visual matriks.

    *Tips: Anda dapat mengarahkan kursor ke setiap ikon untuk menampilkan tipsalat yang menjelaskan jenis visual.*

    ![Gambar 51](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image23.png)

8. Di panel **Bidang**, dari dalam tabel **Tanggal**, seret bidang **Tahun** ke dalam sumber/area **Baris**.

    ![Gambar 17](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image24.png)

9. Seret bidang **Bulan** ke dalam sumber/area **Baris**, tepat di bawah bidang **Tahun**.

    ![Gambar 18](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image25.png)

10. Di kanan atas visual matriks (atau bawah, tergantung pada lokasi visual), klik ikon panah bercabang-ganda (yang akan memperluas sepanjang tahun ke bawah satu tingkat).

    ![Gambar 19](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image26.png)

11. Perhatikan bahwa tahun berkembang menjadi bulan, dan bulan diurutkan berdasarkan abjad, bukan kronologis.

    ![Gambar 20](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image27.png)

    *Secara default, nilai teks diurutkan berdasarkan abjad, angka diurutkan dari terkecil ke terbesar, dan tanggal diurutkan dari yang paling awal hingga yang terbaru.*

12. Untuk menyesuaikan urutan sortir bidang **Bulan**, alihkan ke tampilan Data.

13. Tambahkan kolom **MonthKey** ke tabel **Tanggal**.


    **DAX**


    ```
    MonthKey =
    (YEAR('Date'[Date]) * 100) + MONTH('Date'[Date])
    ```


    *Rumus ini menghitung nilai numerik untuk setiap kombinasi tahun/bulan.*

14. Dalam tampilan Data, verifikasi bahwa kolom baru berisi nilai numerik (misalnya 201707 untuk Juli 2017, dll.).

    ![Gambar 21](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image28.png)

15. Beralih kembali ke tampilan Laporan.

16. Di panel **Bidang**, pastikan bahwa bidang **Bulan** dipilih (jika dipilih, bidang tersebut akan memiliki latar belakang abu-abu gelap).

17. Pada pita kontekstual **Alat Kolom**, dari dalam grup **Urutkan**, klik **Urutkan berdasarkan Kolom**, lalu pilih **MonthKey**.

    ![Gambar 22](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image29.png)

18. Dalam visual matriks, perhatikan bahwa bulan-bulan sekarang diurutkan secara kronologis.

    ![Gambar 23](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image30.png)

### <a name="task-5-complete-the-date-table"></a>**Tugas 5:** **Melengkapi tabel Tanggal**

Dalam tugas ini Anda akan menyelesaikan desain tabel **Tanggal** dengan menyembunyikan kolom dan membuat hierarki. Anda kemudian akan membuat hubungan ke tabel **Penjualan** dan **Target**.

1. Beralih ke tampilan Model.

2. Di tabel **Tanggal**, sembunyikan kolom **MonthKey** (atur **Tersembunyi** ke **Ya**).

3. Pada panel sisi kanan **Bidang**, pilih tabel **Tanggal**, klik kanan pada kolom **Tahun**, dan pilih **buat hierarki**. 

4. Ganti nama hierarki yang baru dibuat menjadi **Fiskal** dengan mengeklik kanan dan **Ganti nama**. 
5. Tambahkan dua bidang berikutnya yang tersisa ke hierarki Fiskal dengan memilihnya di panel bidang, mengeklik kanan, memilih **Tambahkan ke hierarki** -> **Fiskal**.
    
    - Kuartal

    - Bulan

    ![Gambar 24](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image31.png)

6. Buat dua model hubungan berikut:

    - **Tanggal \| Tanggal** ke **Penjual \| OrderDate**

    - **Tanggal \| Tanggal** ke **Target \| TargetMonth**

7. Sembunyikan dua kolom berikut:

    - Penjualan \| OrderDate

    - Target \| TargetMonth

### <a name="task-6-mark-the-date-table"></a>**Tugas 6: Tandai tabel Tanggal**

Dalam tugas ini, Anda akan menandai tabel **Tanggal** sebagai tabel tanggal.

1. Beralih ke tampilan Laporan.

2. Di panel **Bidang**, pilih tabel **Tanggal** (bukan bidang **Tanggal**).

3. Pada pita kontekstual **Alat Tabel**, dari dalam grup **Kalender**, klik **Tandai sebagai Tabel Tanggal**, lalu pilih **Tandai sebagai Tabel Tanggal**.

    ![Gambar 8](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image32.png)

4. Di jendela **Tandai sebagai Tabel Tanggal**, dalam daftar dropdown **Kolom Tanggal**, pilih **Tanggal**.

    ![Gambar 37](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image33.png)

5. Klik **OK**.

    ![Gambar 26](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image34.png)

6. Simpan file Power BI Desktop.

    *Power BI Desktop sekarang memahami bahwa tabel ini menentukan tanggal (waktu). Ini penting ketika mengandalkan perhitungan inteligensi waktu. Anda akan bekerja dengan perhitungan inteligensi waktu di lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 2**.*

    *Perhatikan bahwa pendekatan desain untuk tabel tanggal ini cocok jika Anda tidak memiliki tabel tanggal di sumber data Anda. Jika Anda memiliki gudang data, akan lebih tepat untuk memuat data tanggal dari tabel dimensi tanggalnya, bukan "mendefinisikan ulang" logika tanggal dalam model data Anda.*

## <a name="exercise-2-create-measures"></a>**Latihan 2: Membuat Pengukuran**

Dalam latihan ini Anda akan membuat dan memformat beberapa ukuran.

### <a name="task-1-create-simple-measures"></a>**Tugas 1: Membuat pengukuran sederhana**

Dalam tugas ini Anda akan membuat pengukuran sederhana. Pengukuran ini mengukur nilai agregat dalam satu kolom atau menghitung baris tabel.

1. Dalam tampilan Laporan, pada **Halaman 2**, di panel **Bidang**, seret bidang **Penjualan \| Harga Satuan** ke dalam visual matriks.

    *Lab menggunakan notasi steno untuk mereferensikan bidang. Ini akan terlihat seperti ini: **Penjualan \| Harga Satuan**. Dalam contoh ini, **Penjualan** adalah nama tabel dan **Harga Satuan** adalah nama bidangnya.*

    ![Gambar 27](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image35.png)

    *Anda mungkin ingat bahwa di lab **Model Data in Power BI Desktop**, Anda mengatur kolom **Harga Satuan** untuk diringkas berdasarkan **Rata-rata**. Hasil yang Anda lihat dalam visual matriks adalah harga satuan rata-rata bulanan (jumlah nilai harga satuan dibagi dengan jumlah harga satuan).*

2. Di panel bidang visual (terletak di bawah panel **Visualisasi**), di bidang sumber/area **Nilai**, perhatikan bahwa **Harga Satuan** tercantum.

    ![Gambar 28](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image36.png)

3. Klik panah bawah untuk **Harga Satuan**, lalu perhatikan opsi menu yang tersedia.

    ![Gambar 30](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image37.png)

    *Kolom numerik yang terlihat memungkinkan penulis laporan pada waktu desain laporan untuk memutuskan bagaimana nilai kolom akan diringkas (atau tidak). Hal ini dapat mengakibatkan pelaporan yang tidak tepat. Namun, beberapa pemodel data tidak suka membiarkan hal-hal terjadi secara kebetulan, dan memilih untuk menyembunyikan kolom ini dan sebagai gantinya mengekspos logika agregasi yang ditentukan dalam ukuran. Ini adalah pendekatan yang sekarang akan Anda ambil di lab ini.*

4. Untuk membuat ukuran, di panel **Bidang**, klik kanan tabel **Penjualan**, lalu pilih **Ukuran Baru**.

    ![Gambar 31](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image38.png)

5. Di bilah rumus, tambahkan definisi ukuran berikut:


    **DAX**


    ```
    Avg Price =  
    ‎AVERAGE(Sales[Unit Price])
    ```


6. Tambahkan ukuran **Harga Rata-Rata** ke visual matriks.

7. Perhatikan bahwa ukuran ini menampilkan hasil yang sama dengan kolom **Harga Satuan** (tetapi dengan format yang berbeda).

8. Di sumber **Nilai**, buka menu konteks untuk bidang **Harga Rata-Rata**, dan perhatikan bahwa teknik agregasi tidak dapat diubah.

    ![Gambar 32](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image39.png)

    *Perilaku agregasi suatu ukuran tidak dapat diubah.*

9. Gunakan definisi file cuplikan untuk membuat lima ukuran berikut untuk tabel **Penjualan**:

    - Harga Median

    - Harga Minimal

    - Harga Maks

    - Pesanan

    - Baris Pesanan

    *Fungsi DISTINCTCOUNT() yang digunakan dalam pengukuran **Pesanan** akan menghitung pesanan hanya sekali (mengabaikan duplikat). Fungsi COUNTROWS() yang digunakan dalam ukuran **Baris Pesanan** beroperasi di atas tabel.*

    *Dalam hal ini, jumlah pesanan dihitung dengan menghitung nilai kolom **SalesOrderNumber** yang berbeda, sedangkan jumlah baris pesanan hanyalah jumlah baris tabel (setiap baris adalah baris pesanan).*

10. Beralih ke tampilan Model, lalu pilih empat ukuran harga: **Harga Rata-Rata**, **Harga Maks.** , **Harga Median**, dan **Harga Minimum**.

11. Untuk memilih beberapa tindakan, konfigurasikan persyaratan berikut:

    - Atur format ke dua tempat desimal

    - Tetapkan ke folder tampilan bernama **Harga**

    ![Gambar 33](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image40.png)

12. Sembunyikan kolom **Harga Satuan**.

    *Kolom **Harga Satuan** sekarang tidak tersedia untuk penulis laporan. Kolom harus menggunakan ukuran penetapan harga yang telah Anda tambahkan ke model. Pendekatan desain ini memastikan bahwa penulis laporan tidak akan mengagregasi harga secara tidak tepat, misalnya, dengan menjumlahkannya.*

13. Pilih beberapa tindakan **Baris Pesanan** dan **Pesanan**, lalu konfigurasikan persyaratan berikut:

    - Atur formatnya menggunakan pemisah ribuan

    - Tetapkan ke folder tampilan bernama **Jumlah**

    ![Gambar 36](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image41.png)

14. Dalam tampilan Laporan, di sumber/area **Nilai** dari visual matriks, untuk bidang **Harga Satuan**, klik **X** untuk menghapusnya.

    ![Gambar 38](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image42.png)

15. Tingkatkan ukuran visual matriks untuk mengisi lebar dan tinggi halaman.

16. Tambahkan lima ukuran berikut ke visual matriks:

    - Harga Median

    - Harga Minimal

    - Harga Maks

    - Pesanan

    - Baris Pesanan

17. Verifikasi bahwa hasilnya terlihat masuk akal dan diformat dengan benar.

    ![Gambar 39](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image43.png)

### <a name="task-2-create-additional-measures"></a>**Tugas 2: Membuat tindakan tambahan**

Dalam tugas ini Anda akan membuat ukuran tambahan yang menggunakan rumus lebih rumit.

1. Dalam tampilan Laporan, pilih **Halaman 1**.

    ![Gambar 40](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image44.png)

2. Tinjau visual tabel, perhatikan total untuk kolom **Target**.

    ![Gambar 41](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image45.png)

    

3. Pilih visual tabel, lalu di panel **Visualisasi**, hapus bidang **Target**.

    ![Gambar 42](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image46.png)

4. Ganti nama kolom **Target \| Target** menjadi **Target \| TargetAmount**.

    *Tips: Ada beberapa cara untuk mengganti nama kolom dalam tampilan Laporan: Di panel **Bidang**, Anda dapat mengeklik kanan kolom, lalu memilih **Ganti nama**—atau, klik dua kali kolom, atau tekan **F2**.*

    *Anda akan membuat ukuran bernama **Target**. ANda tidak dapat memiliki kolom dan ukuran dalam tabel yang sama dengan nama yang sama.*

5. Buat ukuran berikut pada tabel **Target**:


    **DAX**


    ```
    Target =

    IF(

    HASONEVALUE('Salesperson (Performance)'[Salesperson]),

    SUM(Targets[TargetAmount])

    )
    ```


    *Fungsi HASONEVALUE() menguji apakah satu nilai di kolom **Penjual** difilter. Jika true, ekspresi akan mengembalikan jumlah total target (hanya untuk penjual tersebut). Jika false, ekspresi akan mengembalikan KOSONG.*

6. Format ukuran **Target** untuk nol tempat desimal.

    *Tips: Anda dapat menggunakan pita kontekstual **Alat Pengukuran**.*

7. Sembunyikan kolom **TargetAmount**.

    *Tips: Anda dapat mengeklik kanan kolom di panel **Bidang**, lalu memilih **Sembunyikan**.*

8. Tambahkan ukuran **Target** ke visual tabel.

9. Perhatikan bahwa total kolom **Target** sekarang KOSONG.

    ![Gambar 43](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image47.png)

10. Gunakan definisi file cuplikan untuk membuat dua ukuran berikut untuk tabel **Target**:

    - Varian

    - Margin Varians

11. Format ukuran **Varians** untuk nol tempat desimal.

12. Format ukuran **Margin Varians** sebagai persentase dengan dua tempat desimal.

13. Tambahkan ukuran **Varians** dan **Margin Varians** ke visual tabel.

14. Ubah ukuran visual tabel sehingga semua kolom dan baris dapat dilihat.

    ![Gambar 44](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image48.png)

    *Meskipun tampaknya semua penjual tidak memenuhi target, ingatlah bahwa visual tabel belum difilter berdasarkan jangka waktu tertentu. Anda akan membuat laporan performa penjualan yang difilter berdasarkan periode waktu yang dipilih pengguna di lab **Merancang Laporan di Power BI Desktop, Bagian 1**.*

15. Di pojok kanan atas panel **Bidang**, ciutkan, lalu luaskan, buka panel.

    ![Gambar 45](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image49.png)

    *Menciutkan dan membuka kembali panel akan mengatur ulang konten.*

16. Perhatikan bahwa tabel **Target** sekarang muncul di bagian atas daftar.

    ![Gambar 46](Linked_image_Files/05-create-dax-calculations-in-power-bi-desktop_image50.png)

    *Tabel yang hanya terdiri dari pengukuran yang terlihat secara otomatis dicantumkan di bagian atas daftar.*

### <a name="task-3-finish-up"></a>**Tugas 3: Selesaikan**

Dalam tugas ini Anda akan menyelesaikan lab.

1. Simpan file Power BI Desktop.

2. Jika Anda ingin memulai lab berikutnya, biarkan Power BI Desktop tetap terbuka.

    *Anda akan menyempurnakan model data dengan perhitungan lebih lanjut menggunakan DAX di lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 2**.*
