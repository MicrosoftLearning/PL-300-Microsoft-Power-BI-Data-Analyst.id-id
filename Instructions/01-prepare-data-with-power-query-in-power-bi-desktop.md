---
lab:
  title: Mempersiapkan Data di Power BI Desktop
  module: Module 2 - Get Data in Power BI
ms.openlocfilehash: 56cc5b93dfb545367ae8f5fe3996a9318203f151
ms.sourcegitcommit: 9ea1e7e21b9b3c718030c94b1693d153a2010ec7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2022
ms.locfileid: "147015347"
---
# <a name="prepare-data-in-power-bi-desktop"></a>**Mempersiapkan Data di Power BI Desktop**

**Perkiraan waktu untuk menyelesaikan lab adalah 45 menit**

Di lab ini Anda memulai pengembangan solusi Power BI Desktop untuk perusahaan Adventure Works. Lab ini melibatkan koneksi ke data sumber, melihat pratinjau data, dan menggunakan teknik pratinjau data untuk memahami karakteristik dan kualitas data sumber.

Di lab ini Anda mempelajari cara:

- Membuka Power BI Desktop

- Mengatur opsi Power BI Desktop

- Menghubungkan ke data sumber

- Melihat pratinjau data sumber

- Menggunakan teknik pratinjau data untuk lebih memahami data

### <a name="lab-story"></a>**Cerita lab**

Lab ini adalah salah satu dari sekian banyak lab yang dirancang sebagai cerita lengkap, mulai dari persiapan data hingga publikasi sebagai laporan dan dasbor. Anda dapat menyelesaikan lab dalam urutan apa pun. Namun, jika Anda ingin mengerjakan beberapa lab sekaligus, sebaiknya Anda mengerjakannya dengan urutan berikut:

1. **Mempersiapkan Data di Power BI Desktop**

2. Muat Data di Power BI Desktop

3. Data Model di Power BI Desktop

5. Membuat Perhitungan DAX di Power BI Desktop, Bagian 1

6. Membuat Perhitungan DAX di Power BI Desktop, Bagian 2

7. Merancang Laporan di Power BI Desktop, Bagian 1

8. Merancang Laporan di Power BI Desktop, Bagian 2

9. Buat Dasbor Power BI

10. Menganalisis Data di Power BI Desktop

11. Terapkan Keamanan Tingkat Baris

## <a name="exercise-1-prepare-data"></a>**Latihan 1: Mempersiapkan Data**

Dalam latihan ini Anda akan membuat delapan kueri Power BI Desktop. Enam kueri akan mengambil data dari SQL Server, dan dua dari file CSV.

### <a name="task-1-save-the-power-bi-desktop-file"></a>**Tugas 1: Menyimpan file Power BI Desktop**

Dalam tugas ini Anda akan menyimpan file Power BI Desktop terlebih dahulu.

1. Untuk membuka Power BI Desktop, pada taskbar, klik pintasan Microsoft Power BI Desktop.

    ![Gambar 2](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image1.png)

1. Untuk menutup jendela memulai, di kanan atas jendela, klik **X**.

    ![Gambar 3](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image2.png)

1. Untuk menyimpan file, klik tab pita **File** untuk membuka tampilan di backstage.

1. Pilih **Simpan**.

    ![Gambar 4](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image3.png)

1. Di jendela **Simpan Sebagai**, navigasikan ke folder **D:\PL300\MySolution**.

1. Di kotak **Nama File**, masukkan **Analisis Penjualan**.

    ![Gambar 14](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image4.png)

1. Klik **Simpan**.

    ![Gambar 17](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image5.png)

    Tips: Anda juga dapat menyimpan file dengan mengeklik ikon **Simpan** yang terletak di kiri atas.

    ![Gambar 18](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image6.png)

### <a name="task-2-set-power-bi-desktop-options"></a>**Tugas 2: Mengatur opsi Power BI Desktop**

Dalam tugas ini Anda akan mengatur opsi Power BI Desktop.

1. Di Power BI Desktop, klik tab pita **File** untuk membuka tampilan backstage.

1. Di sebelah kiri, pilih **Opsi dan Pengaturan**, lalu pilih **Opsi**.

    ![Gambar 1](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image7.png)

1. Di jendela **Opsi**, di sebelah kiri, dalam grup **File Saat Ini**, pilih **Pemuatan Data**.

    ![Gambar 5](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image8.png)

    Pengaturan **Pemuatan Data** untuk file saat ini memungkinkan opsi pengaturan yang menentukan perilaku default saat membuat model.

1. Di grup **Hubungan**, hapus centang pada dua opsi yang sudah dicentang.

    ![Gambar 7](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image9.png)

    Meskipun mengaktifkan kedua opsi ini dapat membantu saat mengembangkan model data, Anda telah menonaktifkannya sebelumnya untuk mendukung pengalaman lab. Saat Anda membuat hubungan di lab **Memuat Data di Power BI Desktop**, Anda akan mempelajari mengapa Anda menambahkan masing-masing hubungan.

1. Klik **OK**.

    ![Gambar 9](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image10.png)

1. Simpan file Power BI Desktop.

### <a name="task-3-get-data-from-sql-server"></a>**Tugas 3: Mendapatkan data dari SQL Server**

Dalam tugas ini Anda akan membuat kueri berdasarkan tabel SQL Server.

1. Pada tab pita **Beranda**, dari dalam grup **Data**, klik **SQL Server**.

    ![Gambar 19](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image11.png)

2. Di jendela **SQL Server Database**, di kotak **Server**, masukkan **localhost**.

    ![Gambar 21](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image12.png)

    Di lab ini Anda akan terhubung ke database SQL Server dengan menggunakan **localhost**. Ini bukan praktik yang disarankan saat membuat solusi Anda sendiri. Itu karena sumber data gateway tidak dapat menyelesaikan **localhost**.

3. Klik **OK**.

    ![Gambar 22](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image13.png)

4. Jika dimintai kredensial, di jendela **SQL Server Database**, pilih **Gunakan kredensial saya saat ini**. Kemudian **Hubungkan**.

4. Di jendela **Navigator**, di sebelah kiri, luaskan database **AdventureWorksDW2020**.

    Database **AdventureWorksDW2020** didasarkan pada database sampel **AdventureWorksDW2017**. Database ini telah dimodifikasi untuk mendukung tujuan pembelajaran dari laboratorium kursus.

    ![Gambar 28](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image17.png)

5. Pilih—tetapi jangan centang—tabel **DimEmployee**.

    ![Gambar 29](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image18.png)

6. Di panel kanan, perhatikan pratinjau data tabel.

    Data pratinjau memungkinkan Anda menentukan kolom dan sampel baris.

7. Untuk membuat kueri, pilih kotak centang di samping enam tabel berikut:

    - DimEmployee

    - DimEmployeeSalesTerritory

    - DimProduct

    - DimReseller

    - DimSalesTerritory

    - FactResellerSales

8. Untuk menerapkan transformasi pada data tabel yang dipilih, klik **Transformasi Data**.

    Anda tidak akan mengubah data di lab ini. Tujuan lab ini berfokus pada penjelajahan dan pembuatan profil data di jendela **Editor Power Query**.

    ![Gambar 30](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image19.png)

### <a name="task-4-preview-sql-server-queries"></a>**Tugas 4: Melihat pratinjau kueri SQL Server**

Dalam tugas ini Anda akan melihat pratinjau data kueri SQL Server. Pertama, Anda akan mempelajari informasi yang relevan tentang data. Anda juga akan menggunakan alat kualitas kolom, distribusi kolom, dan profil kolom untuk memahami data dan menilai kualitas data.

1. Di jendela **Editor Power Query**, di sebelah kiri, perhatikan panel **Kueri**.

    ![Gambar 31](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image20.png)

    Panel **Kueri** berisi satu kueri untuk setiap tabel yang Anda periksa.

2. Pilih kueri pertama—**DimEmployee**.

    ![Gambar 33](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image21.png)

    Tabel **DimEmployee** di database SQL Server menyimpan satu baris untuk setiap karyawan. Subset baris dari tabel ini mewakili penjual, yang akan relevan dengan model yang akan Anda kembangkan.

3. Di kiri bawah, di bilah status, perhatikan statistik tabel—tabel memiliki 33 kolom, dan 296 baris.

    ![Gambar 36](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image22.png)

4. Di panel pratinjau data, gulir secara horizontal untuk meninjau semua kolom.

5. Perhatikan bahwa lima kolom terakhir berisi tautan **Tabel** atau **Nilai**.

    Lima kolom ini mewakili hubungan ke tabel lain dalam database. Kolom tersebut dapat digunakan untuk menggabungkan tabel bersama. Anda akan menggabungkan tabel di lab **Memuat Data di Power BI Desktop**.

6. Untuk menilai kualitas kolom, pada tab pita **Lihat**, dari dalam grup **Pratinjau Data**, centang **Kualitas Kolom**.

    ![Gambar 35](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image23.png)

    Fitur kualitas kolom memungkinkan Anda dengan mudah menentukan persentase nilai valid, kesalahan, atau kosong yang ditemukan di kolom.

7. Untuk kolom **Posisi** (kolom terakhir keenam), perhatikan bahwa 94% baris kosong (null).

    ![Gambar 38](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image24.png)

8. Untuk menilai distribusi kolom, pada tab pita **Lihat**, dari dalam grup **Pratinjau Data**, centang **Distribusi Kolom**.

    ![Gambar 40](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image25.png)

9. Tinjau kembali kolom **Posisi**, dan perhatikan bahwa ada empat nilai berbeda, dan satu nilai unik.

10. Tinjau distribusi kolom untuk kolom **EmployeeKey** (pertama)—ada 296 nilai berbeda, dan 296 nilai unik.

    ![Gambar 43](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image26.png)

    Ketika jumlah yang berbeda dan unik sama, itu berarti kolom tersebut berisi nilai unik. Saat membuat model, beberapa tabel model harus memiliki kolom unik. Kolom unik ini dapat digunakan untuk membuat hubungan satu-ke-banyak, yang akan Anda lakukan di lab **Membuat Model Data in Power BI Desktop**.

11. Di panel **Kueri**, pilih kueri **DimEmployeeSalesTerritory**.

    ![Gambar 44](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image27.png)

    Tabel **DimEmployeeSalesTerritory** menyimpan satu baris untuk setiap karyawan dan wilayah teritori penjualan yang dikelola. Tabel mendukung menghubungkan banyak wilayah ke satu karyawan. Beberapa karyawan mengelola satu, dua, atau mungkin lebih banyak wilayah. Saat membuat model data ini, Anda harus mendefinisikan hubungan banyak ke banyak.

12. Di panel **Kueri**, pilih kueri **DimProduct**.

    ![Gambar 46](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image28.png)

    Tabel **DimProduct** berisi satu baris per produk yang dijual oleh perusahaan.

13. Gulir secara horizontal untuk membuka kolom terakhir.

14. Perhatikan kolom **DimProductSubcategory**.

    Saat menambahkan transformasi ke kueri ini di lab **Memuat Data di Power BI Desktop**, Anda akan menggunakan kolom **DimProductSubcategory** untuk menggabungkan tabel.

15. Di panel **Kueri**, pilih kueri **DimReseller**.

    ![Gambar 49](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image29.png)

    Tabel **DimReseller** berisi satu baris per pengecer. Pengecer menjual, mendistribusikan, atau menambah nilai produk Adventure Works.

16. Untuk melihat nilai kolom, pada tab pita **Lihat**, dari dalam grup **Pratinjau Data**, centang **Profil Kolom**.

    ![Gambar 41](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image30.png)

17. Pilih header kolom **BusinessType**.

18. Perhatikan panel baru di bawah panel pratinjau data.

19. Tinjau statistik kolom dan distribusi nilai di panel pratinjau data.

20. Perhatikan masalah kualitas data: ada dua label untuk gudang (**Gudang**, dan **Gu dang** yang salah eja).

    ![Gambar 51](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image31.png)

21. Arahkan kursor ke bilah **Gu dang**, dan perhatikan bahwa ada lima baris dengan nilai ini.

    Anda akan menerapkan transformasi untuk memberi label ulang pada lima baris ini di lab **Memuat Data di Power BI Desktop**.

22. Di panel **Kueri**, pilih kueri **DimSalesTerritory**.

    ![Gambar 52](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image32.png)

    Tabel **DimSalesTerritory** berisi satu baris per wilayah penjualan, termasuk **Kantor Pusat Perusahaan** (kantor pusat). Wilayah ditetapkan ke suatu negara, dan negara-negara ditetapkan ke grup. Di lab **Membuat Model Data in Power BI Desktop**, Anda akan membuat hierarki untuk mendukung analisis di tingkat wilayah, negara, atau grup.

23. Di panel **Kueri**, pilih kueri **FactResellerSales**.

    ![Gambar 54](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image33.png)

    Tabel **FactResellerSales** berisi satu baris per baris pesanan penjualan—pesanan penjualan berisi satu atau beberapa item baris.

24. Tinjau kualitas kolom untuk kolom **TotalProductCost**, dan perhatikan bahwa 8% baris kosong.

    ![Gambar 63](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image34.png)

    Nilai kolom **TotalProductCost** yang hilang merupakan masalah kualitas data. Untuk mengatasi masalah tersebut, di lab **Memuat Data di Power BI Desktop**, Anda akan menerapkan transformasi untuk mengisi nilai yang hilang dengan menggunakan biaya standar produk, yang disimpan di tabel **DimProduct** terkait.


### <a name="task-5-get-data-from-a-csv-file"></a>**Tugas 5: Mendapatkan data dari file CSV**

Dalam tugas ini Anda akan membuat kueri berdasarkan file CSV.

1. Untuk menambahkan kueri baru, di jendela **Editor Power Query**, pada tab pita **Beranda**, dari dalam grup **Kueri Baru**, klik ikon **Sumber Baru** panah bawah, lalu pilih **Teks/CSV**.

    ![Gambar 70](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image35.png)

2. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Resources**, dan pilih file **ResellerSalesTargets.csv**.

3. Klik **Buka**.

4. Di jendela **ResellerSalesTargets.csv**, tinjau data pratinjau.

5. Klik **OK**.

    ![Gambar 71](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image36.png)
 

6. Di panel **Kueri**, perhatikan penambahan kueri **ResellerSalesTargets**.

    ![Gambar 72](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image37.png)

    File CSV **ResellerSalesTargets** berisi satu baris per staf penjualan, per tahun. Setiap baris mencatat 12 target penjualan bulanan (dinyatakan dalam ribuan). Perhatikan bahwa tahun bisnis untuk perusahaan Adventure Works dimulai pada 1 Juli.

7. Perhatikan bahwa tidak ada kolom yang berisi nilai kosong.

    Jika tidak ada target penjualan bulanan, karakter tanda hubung disimpan sebagai gantinya.

8. Tinjau ikon di setiap header kolom, di sebelah kiri nama kolom.

    ![Gambar 74](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image38.png)

    Ikon mewakili tipe data kolom. **123** adalah bilangan bulat, dan **ABC** adalah teks.

    Anda akan menerapkan banyak transformasi untuk mencapai hasil berbentuk berbeda yang hanya terdiri dari tiga kolom: **Tanggal**, **EmployeeKey**, dan **TargetAmount** di lab **Memuat Data di Power BI Desktop**.

### <a name="task-6-get-additional-data-from-a-csv-file"></a>**Tugas 6: Mendapatkan data tambahan dari file CSV**

Dalam tugas ini, Anda akan membuat kueri tambahan berdasarkan file CSV yang berbeda.

1. Gunakan langkah-langkah di tugas sebelumnya untuk membuat kueri berdasarkan file **D:\PL300\Resources\ColorFormats.csv**.

    ![Gambar 75](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image39.png)

    File CSV **ColorFormats** berisi satu baris per warna produk. Setiap baris mencatat kode HEX untuk memformat latar belakang dan warna fon. Anda akan mengintegrasikan data ini dengan data kueri **DimProduct** di lab **Memuat Data di Power BI Desktop**.

### <a name="task-7-finish-up"></a>**Tugas 7: Selesaikan**

Dalam tugas ini Anda akan menyelesaikan lab.

1. Pada tab pita **Lihat**, dari dalam grup **Pratinjau Data**, hapus centang pada tiga opsi pratinjau data yang sebelumnya diaktifkan di lab ini:

    - Kualitas kolom

    - Distribusi kolom

    - Profil kolom

    ![Gambar 76](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image40.png)

2. Untuk menyimpan file Power BI Desktop, di jendela **Editor Power Query**, pada tampilan **File** di belakang layar, pilih **Simpan**.

    ![Gambar 77](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image41.png)

3. Saat diminta untuk menerapkan kueri, klik **Terapkan Nanti**.

    ![Gambar 86](Linked_image_Files/01-prepare-data-with-power-query-in-power-bi-desktop_image42.png)

    Menerapkan kueri akan memuat datanya ke model data. Anda belum siap untuk melakukan itu, karena ada banyak transformasi yang harus diterapkan terlebih dahulu.

4. Jika Anda ingin memulai lab berikutnya, biarkan Power BI Desktop tetap terbuka.

    Anda akan menerapkan berbagai transformasi ke kueri, lalu menerapkan kueri untuk memuatnya ke model data di lab **Memuat Data di Power BI Desktop**.
