---
lab:
  title: Membuat Perhitungan DAX di Power BI Desktop, Bagian 2
  module: Module 5 - Create Model Calculations using DAX in Power BI
ms.openlocfilehash: 064f5bb2c313448f7d15b01bd0e69a84aa85811f
ms.sourcegitcommit: 9ea1e7e21b9b3c718030c94b1693d153a2010ec7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/29/2022
ms.locfileid: "146650198"
---
# <a name="create-dax-calculations-in-power-bi-desktop-part-2"></a>**Membuat Perhitungan DAX di Power BI Desktop, Bagian 2**

**Perkiraan waktu untuk menyelesaikan lab adalah 45 menit**

Di lab ini Anda akan membuat pengukuran dengan ekspresi DAX yang melibatkan manipulasi konteks filter.

Di lab ini Anda mempelajari cara:

- Menggunakan fungsi CALCULATE() untuk memanipulasi konteks filter

- Menggunakan fungsi Inteligensi Waktu

### <a name="lab-story"></a>**Cerita lab**

Lab ini adalah salah satu dari sekian banyak lab yang dirancang sebagai cerita lengkap, mulai dari persiapan data hingga publikasi sebagai laporan dan dasbor. Anda dapat menyelesaikan lab dalam urutan apa pun. Namun, jika Anda ingin mengerjakan beberapa lab sekaligus, sebaiknya Anda mengerjakannya dengan urutan berikut:

1. Mempersiapkan Data di Power BI Desktop

2. Muat Data di Power BI Desktop

3. Data Model di Power BI Desktop

5. Membuat Perhitungan DAX di Power BI Desktop, Bagian 1

6. **Membuat Perhitungan DAX di Power BI Desktop, Bagian 2**

7. Merancang Laporan di Power BI Desktop, Bagian 1

8. Merancang Laporan di Power BI Desktop, Bagian 2

9. Buat Dasbor Power BI

10. Menganalisis Data di Power BI Desktop

11. Terapkan Keamanan Tingkat Baris

## <a name="exercise-1-work-with-filter-context"></a>**Latihan 1: Bekerja dengan Konteks Filter**

Dalam latihan ini Anda akan membuat pengukuran dengan ekspresi DAX yang melibatkan manipulasi konteks filter.

### <a name="task-1-get-started"></a>**Tugas 1: Mulai**

Dalam tugas ini Anda akan menyiapkan lingkungan untuk lab.

*Penting: Jika Anda melanjutkan dari lab sebelumnya (dan Anda berhasil menyelesaikan lab tersebut), jangan selesaikan tugas ini; sebagai gantinya, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Power BI Desktop, pada taskbar, klik pintasan Microsoft Power BI Desktop.

    ![Gambar 12](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image1.png)

1. Untuk menutup jendela memulai, di kiri atas jendela, klik **X**.

    ![Gambar 11](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image2.png)

1. Untuk membuka file Power BI Desktop pertama, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Buka Laporan**.

    ![Gambar 10](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image3.png)

1. Klik **Jelajahi Laporan**.

    ![Gambar 9](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image4.png)

1. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Labs\05-create-dax-calculations-in-power-bi-desktop-advanced\Starter**.

1. Pilih file **Analisis Penjualan**.

1. Klik **Buka**.

    ![Gambar 8](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image5.png)

1. Tutup semua jendela informasi yang mungkin terbuka.

1. Untuk membuat salinan file, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Simpan**.

    ![Gambar 7](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image6.png)

1. Jika diminta untuk menerapkan perubahan, klik **Terapkan**.

    ![Gambar 6](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image7.png)

1. Di jendela **Simpan Sebagai**, navigasikan ke folder **D:\PL300\MySolution**.

1. Klik **Simpan**.

    ![Gambar 2](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image8.png)

### <a name="task-2-create-a-matrix-visual"></a>**Tugas 2: Membuat visual matriks**

Dalam tugas ini, Anda akan membuat visual matriks untuk mendukung pengujian pengukuran baru Anda.

1. Di Power BI Desktop, dalam tampilan Laporan, buat halaman laporan baru.

    ![Gambar 1](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image9.png)

2. Pada **Halaman 3**, tambahkan visual matriks.

    ![Gambar 13](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image10.png)

3. Ubah ukuran visual matriks untuk mengisi seluruh halaman.

4. Untuk mengonfigurasi bidang visual matriks, dari panel **Bidang**, seret hierarki **Wilayah \| Wilayah**, dan letakkan di dalam visual.

    *Lab menggunakan notasi steno untuk mereferensikan bidang atau hierarki. Ini akan terlihat seperti ini: **Wilayah \|Wilayah**. Dalam contoh ini, **Wilayah** adalah nama tabel dan **Wilayah** adalah nama hierarkinya.*

5. Tambahkan juga bidang **Penjualan \| Penjualan**.

6. Untuk memperluas seluruh hierarki, di kanan atas visual matriks, klik ikon panah bercabang dua kali.

    ![Gambar 47](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image11.png)

    *Anda mungkin ingat bahwa hierarki **Wilayah** memiliki tingkat **Grup**, **Negara**, dan **Wilayah**.*

7. Untuk memformat visual, di panel **Visualisasi**, pilih panel **Format**.

    ![Gambar 14](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image12.png)

8. Di kotak **Pencarian**, masukkan **Bertahap**.

9. Atur properti **Tata Letak Bertahap** ke **Nonaktif**.

    ![Gambar 49](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image14.png)

10. Verifikasi bahwa visual matriks sekarang memiliki empat header kolom.

    ![Gambar 50](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image15.png)

    *Di Adventure Works, wilayah penjualan diatur ke dalam grup, negara, dan wilayah. Semua negara—kecuali Amerika Serikat—hanya memiliki satu wilayah, yang diberi nama berdasarkan nama negara tersebut. Karena Amerika Serikat adalah wilayah penjualan yang sangat besar, maka Amerika Serikat dibagi menjadi lima wilayah penjualan.*

    *Anda akan membuat beberapa ukuran dalam latihan ini, lalu mengujinya dengan menambahkannya ke visual matriks.*

### <a name="task-3-manipulate-filter-context"></a>**Tugas 3: Memanipulasi konteks filter**

Dalam tugas ini Anda akan membuat beberapa pengukuran dengan ekspresi DAX yang menggunakan fungsi CALCULATE() untuk memanipulasi konteks filter.

1. Tambahkan ukuran ke tabel **Penjualan**, berdasarkan ekspresi berikut:

    *Demi kenyamanan Anda, semua definisi DAX di lab ini dapat disalin dari **D:\PL300\Labs\05-create-dax-calculations-in-power-bi-desktop-advanced\Assets\Snippets. file txt**.*


    **DAX**


    ```
    Sales All Region =

    CALCULATE(SUM(Sales[Sales]), REMOVEFILTERS(Region))
    ```


    *Fungsi CALCULATE() adalah fungsi canggih yang digunakan untuk memanipulasi konteks filter. Argumen pertama mengambil ekspresi atau ukuran (ukuran hanyalah ekspresi bernama). Argumen berikutnya memungkinkan modifikasi konteks filter.*

    *Fungsi REMOVEFILTERS() menghapus filter aktif. Tidak ada argumen, atau tabel, kolom, atau beberapa kolom sebagai argumennya.*

    *Dalam rumus ini, ukuran mengevaluasi jumlah kolom **Penjualan** dalam konteks filter yang dimodifikasi, yang menghapus filter apa pun yang diterapkan ke kolom tabel **Wilayah**.*

2. Tambahkan ukuran **Penjualan Semua Wilayah** ke visual matriks.

    ![Gambar 52](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image16.png)

3. Perhatikan bahwa ukuran **Penjualan Semua Wilayah** menghitung total semua penjualan wilayah untuk setiap wilayah, negara (subtotal), dan grup (subtotal).

    *Tindakan baru ini belum memberikan hasil yang bermanfaat. Jika penjualan untuk grup, negara, atau wilayah dibagi dengan nilai ini, akan menghasilkan rasio berguna yang dikenal sebagai “persen dari total keseluruhan”.*

4. Di panel **Bidang**, pastikan bahwa ukuran **Penjualan Semua Wilayah** dipilih (jika dipilih, akan memiliki latar belakang abu-abu gelap), lalu di bilah rumus, ganti nama ukuran dan rumus dengan rumus sebagai berikut:

    *Tips: Untuk mengganti rumus yang ada, salin dulu cuplikannya. Kemudian, klik di dalam bilah rumus dan tekan **Ctrl+A** untuk memilih semua teks. Kemudian, tekan **Ctrl+V** untuk menempelkan cuplikan guna menimpa teks yang dipilih. Lalu tekan **Enter**.*


    **DAX**


    ```
    Sales % All Region =  
    ‎DIVIDE(  
    ‎ SUM(Sales[Sales]),  
    ‎ CALCULATE(  
    ‎ SUM(Sales[Sales]),  
    ‎ REMOVEFILTERS(Region)  
    ‎ )  
    ‎)
    ```


    *Ukuran telah diganti namanya untuk secara akurat mencerminkan formula yang diperbarui. Fungsi DIVIDE() membagi ukuran **Penjualan** (tidak diubah oleh konteks filter) dengan ukuran **Penjualan** dalam konteks yang dimodifikasi, yang menghapus semua filter yang diterapkan ke tabel **Wilayah**.*

5. Dalam visual matriks, perhatikan bahwa ukuran telah diubah namanya dan nilai yang berbeda sekarang muncul untuk setiap grup, negara, dan wilayah.

6. Format ukuran **Penjualan % Semua Wilayah** sebagai persentase dengan dua tempat desimal.

7. Dalam visual matriks, tinjau nilai ukuran **Penjualan % Semua Wilayah**.

    ![Gambar 53](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image17.png)

8. Tambahkan ukuran lain ke tabel **Penjualan**, berdasarkan ekspresi berikut, dan format sebagai persentase:


    **DAX**

    ```
    Sales % Country =  
    ‎DIVIDE(  
    ‎ SUM(Sales[Sales]),  
    ‎ CALCULATE(  
    ‎ SUM(Sales[Sales]),  
    ‎ REMOVEFILTERS(Region[Region])  
    ‎ )  
    ‎)
    ```


9. Perhatikan bahwa rumus ukuran **Penjualan % Negara** sedikit berbeda dari rumus ukuran **Penjualan % Semua Wilayah**.

    *Perbedaannya adalah penyebut mengubah konteks filter dengan menghapus filter pada kolom **Wilayah** tabel **Wilayah**, tidak semua kolom tabel **Wilayah**. Artinya, filter apa pun yang diterapkan ke kolom grup atau negara akan dipertahankan. Ini akan mencapai hasil yang mewakili penjualan sebagai persentase negara.*

10. Tambahkan ukuran **Penjualan % Negara** ke visual matriks.

11. Perhatikan bahwa hanya wilayah Amerika Serikat yang menghasilkan nilai yang tidak 100%.

    ![Gambar 54](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image18.png)

    *Anda mungkin ingat bahwa hanya Amerika Serikat yang memiliki beberapa wilayah. Semua negara lain terdiri dari satu wilayah, yang menjelaskan mengapa semuanya 100%.*

12. Untuk meningkatkan keterbacaan pengukuran ini secara visual, timpa ukuran **Negara % Penjualan** dengan formula yang ditingkatkan ini.


    **DAX**


    ```
    Sales % Country =  
    ‎IF(  
    ‎ ISINSCOPE(Region[Region]),  
    ‎ DIVIDE(  
    ‎ SUM(Sales[Sales]),  
    ‎ CALCULATE(  
    ‎ SUM(Sales[Sales]),  
    ‎ REMOVEFILTERS(Region[Region])  
    ‎ )  
    ‎ )  
    ‎)
    ```


    *Disematkan dalam fungsi IF(), fungsi ISINSCOPE() digunakan untuk menguji apakah kolom region adalah tingkat dalam hierarki tingkat. Jika benar, fungsi DIVIDE() dievaluasi. Tidak adanya bagian yang salah berarti bahwa kosong dikembalikan ketika kolom wilayah tidak dalam cakupan.*

13. Perhatikan bahwa ukuran **Penjualan % Negara** sekarang hanya mengembalikan nilai jika suatu wilayah berada dalam cakupannya.

    ![Gambar 55](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image19.png)

14. Tambahkan ukuran lain ke tabel **Penjualan**, berdasarkan ekspresi berikut, dan format sebagai persentase:


    **DAX**


    ```
    Sales % Group =  
    ‎DIVIDE(  
    ‎ SUM(Sales[Sales]),  
    ‎ CALCULATE(  
    ‎ SUM(Sales[Sales]),  
    ‎ REMOVEFILTERS(  
    ‎ Region[Region],  
    ‎ Region[Country]  
    ‎ )  
    ‎ )  
    ‎)
    ```


    *Untuk mencapai penjualan sebagai persentase grup, dua filter dapat diterapkan untuk menghapus filter secara efektif pada dua kolom.*

15. Tambahkan ukuran **Grup % Penjualan** ke visual matriks.

16. Untuk meningkatkan keterbacaan pengukuran ini secara visual, timpa ukuran **Grup % Penjualan** dengan rumus yang ditingkatkan ini.


    **DAX**


    ```
    Sales % Group =  
    ‎IF(  
    ‎ ISINSCOPE(Region[Region])  
    ‎ || ISINSCOPE(Region[Country]),  
    ‎ DIVIDE(  
    ‎ SUM(Sales[Sales]),  
    ‎ CALCULATE(  
    ‎ SUM(Sales[Sales]),  
    ‎ REMOVEFILTERS(  
    ‎ Region[Region],  
    ‎ Region[Country]  
    ‎ )  
    ‎ )  
    ‎ )  
    ‎)
    ```


17. Perhatikan bahwa ukuran **Penjualan % Grup** sekarang hanya mengembalikan nilai jika wilayah atau negara berada dalam cakupannya.

18. Dalam tampilan Model, tempatkan tiga ukuran baru ke dalam folder tampilan bernama **Rasio**.

    ![Gambar 56](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image20.png)

19. Simpan file Power BI Desktop.

    *Ukuran yang ditambahkan ke tabel **Penjualan** telah mengubah konteks filter untuk mencapai navigasi hierarki. Perhatikan bahwa pola untuk mencapai perhitungan subtotal memerlukan penghapusan beberapa kolom dari konteks filter, dan untuk mencapai total keseluruhan, semua kolom harus dihapus.*

## <a name="exercise-2-work-with-time-intelligence"></a>**Latihan 2: Bekerja dengan Inteligensi Waktu**

Dalam latihan ini Anda akan membuat ukuran penjualan tahun-ke-tanggal (YTD) dan ukuran pertumbuhan penjualan tahun-ke-tahun (YoY).

### <a name="task-1-create-a-ytd-measure"></a>**Tugas 1: Membuat ukuran YTD**

Dalam tugas ini Anda akan membuat ukuran YTD penjualan.

1. Dalam tampilan Laporan, pada **Halaman 2**, perhatikan visual matriks yang menampilkan berbagai ukuran dengan tahun dan bulan yang dikelompokkan pada baris.

2. Tambahkan ukuran ke tabel **Penjualan**, berdasarkan ekspresi berikut, dan diformat ke nol tempat desimal:


    **DAX**


    ```
    Sales YTD =  
    ‎TOTALYTD(SUM(Sales[Sales]), 'Date'[Date], "6-30")
    ```


    *Fungsi TOTALYTD() mengevaluasi ekspresi—dalam hal ini jumlah kolom **Penjualan**—pada kolom tanggal tertentu. Kolom tanggal harus dimiliki oleh tabel tanggal yang ditandai sebagai tabel tanggal, seperti yang dilakukan di lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 1**.*

    *Fungsi ini juga dapat mengambil argumen opsional ketiga yang mewakili tanggal terakhir dalam satu tahun. Tidak adanya tanggal ini berarti bahwa 31 Desember adalah tanggal terakhir tahun ini. Untuk Adventure Works, Juni di bulan terakhir tahun mereka, jadi "6-30" digunakan.*

3. Tambahkan bidang **Penjualan** dan ukuran **Penjualan YTD** ke visual matriks.

4. Perhatikan akumulasi nilai penjualan dalam setahun.

    ![Gambar 59](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image21.png)

    *Fungsi TOTALYTD() melakukan manipulasi filter, khususnya manipulasi filter waktu. Misalnya, untuk menghitung penjualan YTD untuk September 2017 (bulan ketiga tahun fiskal), semua filter pada tabel **Tanggal** dihapus dan diganti dengan filter baru tanggal yang dimulai pada awal tahun (1 Juli 2017) dan diperpanjang hingga tanggal terakhir periode tanggal dalam konteks (30 September 2017).*

    *Perhatikan bahwa banyak fungsi Inteligensi Waktu tersedia di DAX untuk mendukung manipulasi filter waktu yang umum.*

### <a name="task-2-create-a-yoy-growth-measure"></a>**Tugas 2: Membuat ukuran pertumbuhan YoY**

Dalam tugas ini Anda akan membuat ukuran pertumbuhan penjualan YoY.

1. Tambahkan ukuran tambahan ke tabel **Penjualan**, berdasarkan ekspresi berikut:


    **DAX**


    ```
    Sales YoY Growth =  
    ‎VAR SalesPriorYear =  
    ‎ CALCULATE(  
    ‎ SUM(Sales[Sales]),  
    ‎ PARALLELPERIOD(  
    ‎ 'Date'[Date],  
    ‎ -12,  
    ‎ MONTH  
    ‎ )  
    ‎ )  
    ‎RETURN  
    ‎ SalesPriorYear
    ```


    *Rumus ukuran **Pertumbuhan Penjualan YoY** mendeklarasikan variabel. Variabel dapat berguna untuk menyederhanakan logika rumus, dan lebih efisien ketika ekspresi perlu dievaluasi beberapa kali dalam rumus (yang akan menjadi kasus logika pertumbuhan YoY). Variabel dideklarasikan dengan nama unik, dan ekspresi ukuran kemudian harus dikeluarkan setelah kata kunci **RETURN**.*

    *Variabel **SalesPriorYear** diberi ekspresi yang menghitung jumlah kolom **Penjualan** dalam konteks yang dimodifikasi yang menggunakan fungsi PARALLELPERIOD() untuk menggeser 12 bulan ke belakang dari setiap tanggal dalam konteks filter.*

2. Tambahkan ukuran **Pertumbuhan Penjualan YoY** ke visual matriks.

3. Perhatikan bahwa ukuran baru mengembalikan KOSONG untuk 12 bulan pertama (karena tidak ada penjualan yang dicatat sebelum tahun fiskal 2017).

4. Perhatikan bahwa nilai ukuran **Pertumbuhan Penjualan YoY** untuk **Juli 2018** adalah nilai **Penjualan** untuk **Juli 2017**.

    ![Gambar 61](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image22.png)

    *Sekarang setelah “bagian yang sulit” dari rumus telah diuji, Anda dapat menimpa ukuran dengan rumus akhir yang menghitung hasil pertumbuhan.*

5. Untuk menyelesaikan pengukuran, timpa ukuran **Pertumbuhan Penjualan YoY** dengan rumus ini, format sebagai persentase dengan dua tempat desimal:


    **DAX**


    ```
    Sales YoY Growth =  
    ‎VAR SalesPriorYear =  
    ‎ CALCULATE(  
    ‎ SUM(Sales[Sales]),  
    ‎ PARALLELPERIOD(  
    ‎ 'Date'[Date],  
    ‎ -12,  
    ‎ MONTH  
    ‎ )  
    ‎ )  
    ‎RETURN  
    ‎ DIVIDE(  
    ‎ (SUM(Sales[Sales]) - SalesPriorYear),  
    ‎ SalesPriorYear  
    ‎ )
    ```


6. Dalam rumus, dalam klausa **RETURN**, perhatikan bahwa variabel direferensikan dua kali.

7. Verifikasi bahwa pertumbuhan YoY untuk **Juli 2018** adalah **392.83%** .

    ![Gambar 62](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image23.png)

    *Ini berarti bahwa penjualan Juli 2018 ($2.411.559) menunjukkan peningkatan hampir 400% (hampir 4x) dibandingkan penjualan yang dicapai pada waktu yang sama tahun sebelumnya ($489.328).*

8. Dalam tampilan Model, tempatkan dua ukuran baru ke dalam folder tampilan bernama **Inteligensi Waktu**.

    ![Gambar 63](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image24.png)

### <a name="task-3-finish-up"></a>**Tugas 3: Selesaikan**

Dalam tugas ini Anda akan menyelesaikan lab.

1. Untuk membersihkan solusi yang siap untuk pengembangan laporan, di kiri bawah, klik kanan tab **Halaman 2**, lalu pilih halaman **Hapus**.

    ![Gambar 17](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image25.png)

2. Saat diminta untuk menghapus halaman, klik **Hapus**.

    ![Gambar 18](Linked_image_Files/06-create-dax-calculations-in-power-bi-desktop-advanced_image26.png)

3. Hapus juga **Halaman 3**.

4. Pada halaman yang tersisa, untuk mengosongkan halaman, pilih visual tabel, lalu tekan tombol **Hapus**.

5. Simpan file Power BI Desktop.

6. Jika Anda ingin memulai lab berikutnya, biarkan Power BI Desktop tetap terbuka.

    *Anda akan membuat laporan berdasarkan model data di lab **Merancang Laporan di Power BI Desktop, Bagian 1**.*
