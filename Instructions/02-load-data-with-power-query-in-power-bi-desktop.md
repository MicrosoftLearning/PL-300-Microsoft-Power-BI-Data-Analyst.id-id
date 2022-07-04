---
lab:
  title: Muat Data di Power BI Desktop
  module: Module 3 - Clean, Transform, and Load Data in Power BI
ms.openlocfilehash: aced37b7bfdd2ccf94a9d3e7bdb8f8ff7013c125
ms.sourcegitcommit: 9ea1e7e21b9b3c718030c94b1693d153a2010ec7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/29/2022
ms.locfileid: "146650225"
---
# <a name="load-data-in-power-bi-desktop"></a>**Memuat Data di Power BI Desktop**

**Perkiraan waktu untuk menyelesaikan lab adalah 45 menit**

Di lab ini, Anda akan mulai menerapkan transformasi ke setiap kueri yang dibuat di lab sebelumnya. Anda kemudian akan menerapkan kueri untuk memuat masing-masing sebagai tabel ke model data.

Di lab ini Anda mempelajari cara:

- Menerapkan berbagai transformasi

- Menerapkan kueri untuk memuatnya ke model data

### <a name="lab-story"></a>**Cerita lab**

Lab ini adalah salah satu dari sekian banyak lab yang dirancang sebagai cerita lengkap, mulai dari persiapan data hingga publikasi sebagai laporan dan dasbor. Anda dapat menyelesaikan lab dalam urutan apa pun. Namun, jika Anda ingin mengerjakan beberapa lab sekaligus, sebaiknya Anda mengerjakannya dengan urutan berikut:

1. Mempersiapkan Data di Power BI Desktop

2. **Memuat Data di Power BI Desktop**

3. Data Model di Power BI Desktop


5. Membuat Perhitungan DAX di Power BI Desktop, Bagian 1

6. Membuat Perhitungan DAX di Power BI Desktop, Bagian 2

7. Merancang Laporan di Power BI Desktop, Bagian 1

8. Merancang Laporan di Power BI Desktop, Bagian 2

9. Buat Dasbor Power BI

10. Menganalisis Data di Power BI Desktop

11. Terapkan Keamanan Tingkat Baris

## <a name="exercise-1-load-data"></a>**Latihan 1: Memuat Data**

Dalam latihan ini Anda akan menerapkan transformasi ke setiap kueri yang dibuat di lab sebelumnya.

### <a name="task-1-get-started"></a>**Tugas 1: Mulai**

Dalam tugas ini Anda akan menyiapkan lingkungan untuk lab.

*Penting: Jika Anda melanjutkan dari lab sebelumnya (dan Anda berhasil menyelesaikan lab tersebut), jangan selesaikan tugas ini; sebagai gantinya, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Power BI Desktop, pada taskbar, klik pintasan Microsoft Power BI Desktop.

    ![Gambar 8](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image1.png)

1. Untuk menutup jendela memulai, di kiri atas jendela, klik **X**.

    ![Gambar 7](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image2.png)

1. Untuk membuka file Power BI Desktop pertama, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Buka Laporan**.

    ![Gambar 10](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image3.png)

1. Klik **Jelajahi Laporan**.

    ![Gambar 11](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image4.png)

1. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Labs\02-load-data-with-power-query-in-power-bi-desktop\Starter**.

1. Pilih file **Analisis Penjualan**.

1. Klik **Buka**.

    ![Gambar 12](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image5.png)

1. Tutup semua jendela informasi yang mungkin terbuka.

1. Perhatikan pesan peringatan kuning di bawah pita.

    *Pesan tersebut mengingatkan Anda tentang fakta bahwa kueri belum diterapkan untuk dimuat sebagai tabel model. Anda akan menerapkan kueri nanti di lab ini.*

1. Untuk menutup pesan peringatan, di sebelah kanan pesan peringatan kuning, klik **X**.

    ![Gambar 13](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image6.png)

1. Untuk membuat salinan file, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Simpan**.

    ![Gambar 18](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image7.png)

1. Jika diminta untuk menerapkan perubahan, klik **Terapkan Nanti**.

    ![Gambar 22](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image8.png)

1. Di jendela **Simpan Sebagai**, navigasikan ke folder **D:\PL300\MySolution**.

1. Klik **Simpan**.

    ![Gambar 15](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image9.png)

1. Untuk membuka jendela **Editor Power Query**, pada tab pita **Beranda**, dari dalam grup **Kueri**, klik ikon **Transformasi Data**.

    ![Gambar 20](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image10.png)

### <a name="task-2-configure-the-salesperson-query"></a>**Tugas 2: Mengonfigurasi kueri Penjual**

Dalam tugas ini, Anda akan mengonfigurasi kueri **Penjual**.

1. Di jendela **Editor Power Query**, di panel **Kueri**, pilih kueri **DimEmployee**.

    ![Gambar 1](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image11.png)

2. Untuk mengganti nama kueri, di panel **Pengaturan Kueri** (terletak di sebelah kanan), di kotak **Nama**, ganti teks dengan **Penjual**, lalu tekan **Enter**.

    *Nama kueri akan menentukan nama tabel model. Disarankan untuk mendefinisikan nama yang ringkas, namun mudah diingat.*

3. Di panel **Kueri**, verifikasi bahwa nama kueri telah diperbarui.

    ![Gambar 87](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image12.png)

    *Sekarang Anda akan memfilter baris kueri untuk mengambil hanya karyawan yang merupakan penjual.*

4. Untuk menemukan kolom tertentu, pada tab pita **Beranda**, klik panah bawah **Kelola Kolom**, klik panah bawah **Pilih Kolom**, lalu pilih **Buka Kolom**.

    ![Gambar 88](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image13.png)

    *Tips: Teknik ini berguna ketika kueri berisi banyak kolom. Jika kolomnya tidak terlalu banyak, Anda cukup menggulir secara horizontal untuk menemukan kolom yang diinginkan.*

5. Di jendela **Buka Kolom**, untuk mengurutkan daftar berdasarkan nama kolom, klik tombol urutkan **AZ**, lalu pilih **Nama**.

    ![Gambar 94](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image14.png)

6. Pilih kolom **SalesPersonFlag**, lalu klik **OK**.

7. Untuk memfilter kueri, di header kolom **SalesPersonFlag**, klik panah bawah, lalu hapus centang **FALSE**.

    ![Gambar 95](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image15.png)

8. Klik **OK**.

    ![Gambar 96](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image16.png)

9. Di panel **Pengaturan Kueri**, dalam daftar **Langkah yang Diterapkan**, perhatikan penambahan langkah **Baris yang Difilter**.

    ![Gambar 98](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image17.png)

    *Setiap transformasi yang Anda buat menghasilkan logika langkah tambahan. Anda dapat mengedit atau menghapus langkah. Anda juga dapat memilih langkah untuk melihat pratinjau hasil kueri pada tahap transformasi kueri tersebut.*

10. Untuk menghapus kolom, pada tab pita **Beranda**, klik grup **Kelola Kolom**, klik ikon **Pilih Kolom**.

    ![Gambar 99](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image18.png)

11. Di jendela **Pilih Kolom**, untuk menghapus centang semua kolom, hapus centang item **(Pilih Semua Kolom)** .

    ![Gambar 102](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image19.png)

12. Untuk menyertakan kolom, periksa enam kolom berikut:

    - EmployeeKey

    - EmployeeNationalIDAlternateKey

    - NamaDepan

    - NamaBelakang

    - Judul

    - EmailAddress

13. Klik **OK**.

    ![Gambar 104](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image20.png)

14. Dalam daftar **Langkah yang Diterapkan**, perhatikan penambahan langkah kueri lainnya.

    ![Gambar 112](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image21.png)

15. Untuk membuat satu kolom nama, pertama-tama pilih header kolom **FirstName**.

16. Sambil menekan tombol **Ctrl**, pilih kolom **LastName**.

    ![Gambar 116](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image22.png)

17. Klik kanan salah satu header kolom yang dipilih, lalu di menu konteks, pilih **Gabungkan Kolom**.

    ![Gambar 117](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image23.png)

    *Banyak transformasi umum dapat diterapkan dengan mengeklik kanan header kolom, lalu memilihnya dari menu konteks. Perhatikan, bagaimanapun, lebih banyak transformasi tersedia di pita.*

18. Di jendela **Gabungkan Kolom**, dalam daftar dropdown **Pemisah**, pilih **Spasi**.

19. Di kotak **Nama Kolom Baru**, ganti teks dengan **Penjual**.

    ![Gambar 119](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image24.png)

20. Klik **OK**.

    ![Gambar 5636](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image25.png)

21. Untuk mengganti nama kolom **EmployeeNationalIDAlternateKey**, klik dua kali header kolom **EmployeeNationalIDAlternateKey**.

22. Ganti teks dengan **EmployeeID**, lalu tekan **Enter**.

    *Penting: Saat dipetunjukkan untuk mengganti nama kolom, Anda harus mengganti namanya persis seperti yang dijelaskan.*

23. Gunakan langkah sebelumnya untuk mengganti nama kolom **EmailAddress** menjadi **UPN**.

    *UPN adalah singkatan dari Nama Prinsipal Pengguna.*

24. Di kiri bawah, di bilah status, verifikasi bahwa kueri memiliki lima kolom dan 18 baris.

    ![Gambar 5638](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image26.png)

    *Penting: Penting agar Anda tidak melanjutkan jika kueri tidak menghasilkan hasil yang benar—lab selanjutnya tidak dapat diselesaikan. Jika kolom atau baris kueri tidak cocok, lihat kembali langkah-langkah dalam tugas ini untuk memperbaiki masalah apa pun.*

### <a name="task-3-configure-the-salespersonregion-query"></a>**Tugas 3: Mengonfigurasi kueri SalespersonRegion**

Dalam tugas ini, Anda akan mengonfigurasi kueri **SalespersonRegion**.

1. Di panel **Kueri**, pilih kueri **DimEmployeeSalesTerritory**.

    ![Gambar 5639](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image27.png)

2. Di panel **Pengaturan Kueri**, ganti nama kueri menjadi **SalespersonRegion**.

3. Untuk menghapus dua kolom terakhir, pertama-tama pilih header kolom **DimEmployee**.

4. Saat menekan tombol **Ctrl**, pilih header kolom **DimSalesTerritory**.

5. Klik kanan salah satu header kolom yang dipilih, lalu di menu konteks, pilih **Hapus Kolom**.

    ![Gambar 5640](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image28.png)

6. Di bilah status, verifikasi bahwa kueri memiliki dua kolom dan 39 baris.

    ![Gambar 5641](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image29.png)

### <a name="task-4-configure-the-product-query"></a>**Tugas 4: Mengonfigurasi kueri Produk**

Dalam tugas ini, Anda akan mengonfigurasi kueri **Produk**.

*Penting: Ketika detail petunjuk telah diberikan, langkah-langkah lab sekarang akan memberikan petunjuk yang lebih ringkas. Jika Anda memerlukan detail petunjuk, Anda dapat mengacu kembali ke langkah-langkah tugas sebelumnya.*

1. Pilih kueri **DimProduct**.

    ![Gambar 5643](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image30.png)

2. Ganti nama kueri menjadi **Produk**.

3. Cari kolom **FinishedGoodsFlag**, lalu filter kolom tersebut untuk mengambil produk yang merupakan barang jadi (yaitu TRUE).

4. Hapus semua kolom, kecuali yang berikut ini:

    - ProductKey

    - EnglishProductName

    - StandardCost

    - Warna

    - DimProductSubcategory

5. Perhatikan bahwa kolom **DimProductSubcategory** mewakili tabel terkait (berisi tautan **Nilai**).

6. Di header kolom **DimProductSubcategory**, di sebelah kanan nama kolom, klik tombol perluas.

    ![Gambar 5644](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image31.png)

7. Untuk menghapus centang semua kolom, hapus centang pada item **(Pilih Semua Kolom)** .

8. Periksa kolom **EnglishProductSubcategoryName** dan **DimProductCategory**.

    ![Gambar 5646](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image32.png)

    *Dengan memilih dua kolom ini, transformasi akan diterapkan untuk bergabung ke tabel **DimProductSubcategory**, lalu menyertakan kolom ini. Kolom **DimProductCategory** sebenarnya adalah tabel terkait lainnya di sumber data.*

9. Hapus centang pada kotak centang **Gunakan Nama Kolom Asli sebagai Awalan**.

    ![Gambar 5647](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image33.png)

    *Nama kolom kueri harus selalu unik. Jika dibiarkan dicentang, kotak centang ini akan mengawali setiap kolom dengan nama kolom yang diperluas (dalam hal ini **DimProductSubcategory**). Karena diketahui bahwa nama kolom yang dipilih tidak bertabrakan dengan nama kolom di kueri **Produk**, opsi tersebut tidak dipilih.*

10. Klik **OK**.

    ![Gambar 5648](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image34.png)

11. Perhatikan bahwa transformasi menghasilkan penambahan dua kolom, dan kolom **DimProductSubcategory** telah dihapus.

12. Luaskan kolom **DimProductCategory**, lalu perkenalkan hanya kolom **EnglishProductCategoryName**.

13. Ganti nama empat kolom berikut:

    - **EnglishProductName** menjadi **Product**

    - **StandardCost** menjadi **Standard Cost** (termasuk spasi)

    - **EnglishProductSubcategoryName** menjadi **Subcategory**

    - **EnglishProductCategoryName** menjadi **Category**

14. Di bilah status, verifikasi bahwa kueri memiliki enam kolom dan 397 baris.

    ![Gambar 5651](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image35.png)

### <a name="task-5-configure-the-reseller-query"></a>**Tugas 5: Mengonfigurasi kueri Pengecer**

Dalam tugas ini, Anda akan mengonfigurasi kueri **Pengecer**.

1. Pilih kueri **DimReseller**.

    ![Gambar 5653](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image36.png)

2. Ganti nama kueri menjadi **Pengecer**.

3. Hapus semua kolom, kecuali yang berikut ini:

    - ResellerKey

    - BusinessType

    - ResellerName

    - DimGeography

4. Luaskan kolom **DimGeography**, untuk hanya menyertakan tiga kolom berikut:

    - Kota

    - StateProvinceName

    - EnglishCountryRegionName

    ![Gambar 5656](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image37.png)

5. Di header kolom **Jenis Bisnis**, klik panah bawah, lalu tinjau nilai kolom yang berbeda, dan perhatikan ejaan gudang yang salah.

    ![Gambar 2](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image38.png)

  

6. Klik kanan header kolom **Jenis Bisnis**, lalu pilih **Ganti Nilai**.

    ![Gambar 4](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image39.png)

7. Di jendela **Ganti Nilai**, konfigurasikan nilai berikut:

    - Di kotak **Nilai yang akan Dicari**, masukkan **Gu Dang**

    - Di kotak **Ganti Dengan**, masukkan **Gudang**

    ![Gambar 5](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image40.png)

8. Klik **OK**.

    ![Gambar 6](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image41.png)

9. Ganti nama empat kolom berikut:

    - **BusinessType** menjadi **Jenis Bisnis** (termasuk spasi)

    - **ResellerName** menjadi **Pengecer**

    - **StateProvinceName** menjadi **Negara-Wilayah**

    - **EnglishCountryRegionName** menjadi **Country-Region**

10. Di bilah status, verifikasi bahwa kueri memiliki enam kolom dan 701 baris.

    ![Gambar 5657](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image42.png)

### <a name="task-6-configure-the-region-query"></a>**Tugas 6: Konfigurasikan kueri Wilayah**

Dalam tugas ini, Anda akan mengonfigurasi kueri **Wilayah**.

1. Pilih kueri **DimSalesTerritory**.

    ![Gambar 5659](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image43.png)

2. Ganti nama kueri menjadi **Wilayah**.

3. Terapkan filter ke kolom **SalesTerritoryAlternateKey** untuk menghapus nilai 0 (nol).

    ![Gambar 5660](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image44.png)

4. Hapus semua kolom, kecuali yang berikut ini:

    - SalesTerritoryKey

    - SalesTerritoryRegion

    - SalesTerritoryCountry

    - SalesTerritoryGroup

5. Ganti nama tiga kolom berikut:

    - **SalesTerritoryRegion** menjadi **Wilayah**

    - **SalesTerritoryCountry** menjadi **Negara**

    - **SalesTerritoryGroup** menjadi **Grup**

6. Di bilah status, verifikasi bahwa kueri memiliki empat kolom dan 10 baris.

    ![Gambar 5661](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image45.png)

### <a name="task-7-configure-the-sales-query"></a>**Tugas 7: Mengonfigurasi kueri Penjualan**

Dalam tugas ini, Anda akan mengonfigurasi kueri **Penjualan**.

1. Pilih kueri **FactResellerSales**.

    ![Gambar 5663](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image46.png)

2. Ganti nama kueri menjadi **Penjualan**.

3. Hapus semua kolom, kecuali yang berikut ini:

    - SalesOrderNumber

    - OrderDate

    - ProductKey

    - ResellerKey

    - EmployeeKey

    - SalesTerritoryKey

    - OrderQuantity

    - UnitPrice

    - TotalProductCost

    - SalesAmount

    - DimProduct

    *Anda mungkin ingat di lab **Mempersiapkan Data di Power BI Desktop** bahwa sebagian kecil dari baris **FactResellerSales** tidak memiliki nilai **TotalProductCost**. Kolom **DimProduct** telah disertakan untuk mengambil kolom biaya standar produk guna membantu memperbaiki nilai yang hilang.*

4. Luaskan kolom **DimProduct**, hapus centang semua kolom, lalu sertakan hanya kolom **StandardCost**.

5. Untuk membuat kolom kustom, pada tab pita **Tambahkan Kolom**, dari dalam grup **Umum**, klik **Kolom Kustom**.

    ![Gambar 5664](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image47.png)

6. Di jendela **Kolom Kustom**, dalam kotak **Nama Kolom Baru**, ganti teks dengan **Biaya**.

    ![Gambar 5665](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image48.png)

7. Di kotak **Rumus Kolom Kustom**, masukkan ekspresi berikut (setelah simbol sama dengan):

8. Untuk kenyamanan Anda, Anda dapat menyalin ekspresi dari file **D:\PL300\Labs\02-load-data-with-power-query-in-power-bi-desktop\Assets\Snippets.txt**.


   **Power Query**
   ```
   if [TotalProductCost] = null then [OrderQuantity] * [StandardCost] else [TotalProductCost]
   ```


*Ekspresi ini menguji apakah nilai **TotalProductCost** tidak ada. Jika ya, buat nilai dengan mengalikan nilai **OrderQuantity** dengan nilai **StandardCost**; jika tidak, nilai tersebut akan menggunakan nilai **TotalProductCost** yang ada.*

9. Klik **OK**.

    ![Gambar 5666](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image49.png)

10. Hapus dua kolom berikut:

    - TotalProductCost

    - StandardCost

11. Ganti nama tiga kolom berikut:

    - **OrderQuantity** menjadi **Kuantitas**

    - **UnitPrice** menjadi **Harga Satuan** (termasuk spasi)

    - **SalesAmount** menjadi **Penjualan**

12. Untuk mengubah tipe data kolom, di header kolom **Kuantitas**, di sebelah kiri nama kolom, klik ikon **1.2**, lalu pilih **Bilangan Bulat**.

    ![Gambar 5667](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image50.png)

    *Penting untuk mengonfigurasi tipe data yang benar. Jika kolom berisi nilai numerik, penting juga untuk memilih jenis yang benar jika Anda ingin melakukan perhitungan matematis.*

13. Ubah tiga tipe data kolom berikut menjadi **Angka Desimal Tetap**.

    - Harga Satuan

    - Sales

    - Biaya

    ![Gambar 5668](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image51.png)

    *Tipe data angka desimal tetap menyimpan nilai dengan presisi penuh, sehingga membutuhkan lebih banyak ruang penyimpanan angka desimal tersebut. Penting untuk menggunakan jenis angka desimal tetap untuk nilai keuangan, atau nilai tukar (seperti nilai tukar).*

14. Di bilah status, verifikasi bahwa kueri memiliki 10 kolom dan 999+ baris.

    ![Gambar 5669](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image52.png)

    *Maksimum 1000 baris akan dimuat sebagai data pratinjau untuk setiap kueri.*

### <a name="task-8-configure-the-targets-query"></a>**Tugas 8: Mengonfigurasi kueri Target**

Dalam tugas ini, Anda akan mengonfigurasi kueri **Target**.

1. Pilih kueri **ResellerSalesTargets**.

    ![Gambar 5672](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image53.png)

2. Ganti nama kueri menjadi **Target**.

3. Untuk membatalkan pivot kolom 12 bulan (**M01**-**M12**), pertama-tama pilih beberapa header kolom **Tahun** dan **EmployeeID**.

    ![Gambar 5673](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image54.png)

4. Klik kanan salah satu header kolom yang dipilih, lalu di menu konteks, pilih **Batalkan Pivot Kolom Lain**.

    ![Gambar 5674](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image55.png)

5. Perhatikan bahwa nama kolom sekarang muncul di kolom **Atribut**, dan nilai muncul di kolom **Nilai**.

6. Terapkan filter ke kolom **Nilai** untuk menghapus nilai tanda hubung (-).

    *Anda mungkin ingat bahwa karakter tanda hubung digunakan dalam file CSV sumber untuk mewakili nol (0).*

7. Ganti nama dua kolom berikut:

    - **Atribut** menjadi **MonthNumber** (tidak ada spasi di antara dua kata—ini akan dihapus nanti)

    - **Nilai** untuk **Target**

    *Sekarang Anda akan menerapkan transformasi untuk menghasilkan kolom tanggal. Tanggal akan diambil dari kolom **Tahun** dan **MonthNumber**. Anda akan membuat kolom dengan menggunakan fitur **Kolom Dari Contoh**.*

8. Untuk menyiapkan nilai kolom **MonthNumber**, klik kanan header kolom **MonthNumber**, lalu pilih **Ganti Nilai**.

    ![Gambar 5676](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image56.png)

9. Di jendela **Ganti Nilai**, di kotak **Nilai yang Akan Dicari**, masukkan **M**.

    ![Gambar 5677](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image57.png)

10. Klik **OK**.

11. Ubah tipe data kolom **MonthNumber** menjadi **Bilangan Bulat**.

    ![Gambar 5678](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image58.png)

12. Pada tab pita **Tambahkan Kolom**, dari dalam grup **Umum**, klik ikon **Kolom Dari Contoh**.

    ![Gambar 5675](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image59.png)

13. Perhatikan bahwa baris pertama adalah untuk tahun **2017** dan nomor bulan **7**.

14. Di kolom **Column1**, di sel kisi pertama, masukkan **1/7/2017**, lalu tekan **Enter**.

    *Mesin virtual menggunakan pengaturan regional AS, jadi tanggal ini sebenarnya adalah 1 Juli 2017.*

15. Perhatikan bahwa sel kisi diperbarui dengan nilai yang diprediksi.

    *Fitur ini telah memperkirakan secara akurat bahwa Anda menggabungkan nilai dari kolom **Tahun** dan **MonthNumber**.*

16. Perhatikan juga rumus yang disajikan di atas kisi kueri.

    ![Gambar 5679](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image60.png)

17. Untuk mengganti nama kolom baru, klik dua kali header kolom **Gabungan**.

18. Ganti nama kolom menjadi **TargetMonth**.

    ![Gambar 5680](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image61.png)

19. Untuk menambahkan kolom baru, klik **Oke**.

    ![Gambar 5681](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image62.png)

20. Hapus kolom berikut:

    - Tahun

    - MonthNumber

21. Ubah tipe data kolom berikut:

    - **Target** sebagai angka desimal tetap

    - **TargetMonth** sebagai tanggal

22. Untuk mengalikan nilai **Target** dengan 1000, pilih header kolom **Target**, lalu pada tab pita **Transformasi**, dari dalam grup **Kolom Angka**, klik **Standar**, lalu pilih **Kalikan**.

    *Anda mungkin ingat bahwa nilai target disimpan dalam ribuan.*

    ![Gambar 5682](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image63.png)

23. Di jendela **Kalikan**, di kotak **Nilai**, masukkan **1000**.

    ![Gambar 5683](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image64.png)

24. Klik **OK**.

    ![Gambar 5684](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image65.png)

25. Di bilah status, verifikasi bahwa kueri memiliki tiga kolom dan 809 baris.

    ![Gambar 5685](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image66.png)

### <a name="task-9-configure-the-colorformats-query"></a>**Tugas 9: Mengonfigurasi kueri ColorFormats**

Dalam tugas ini, Anda akan mengonfigurasi kueri **ColorFormats**.

1. Pilih kueri **ColorFormats**.

    ![Gambar 5687](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image67.png)

2. Perhatikan bahwa baris pertama berisi nama kolom.

3. Pada tab pita **Beranda**, dari dalam grup **Transformasi**, klik **Gunakan Baris Pertama sebagai Header**.

    ![Gambar 5688](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image68.png)

4. Di bilah status, verifikasi bahwa kueri memiliki tiga kolom dan 10 baris.

    ![Gambar 5689](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image69.png)

### <a name="task-10-update-the-product-query"></a>**Tugas 10: Perbarui kueri Produk**

Dalam tugas ini, Anda akan memperbarui kueri **Produk** dengan menggabungkan kueri **ColorFormats**.

1. Pilih kueri **Produk**.

    ![Gambar 5690](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image70.png)

2. Untuk menggabungkan kueri **ColorFormats**, pada tab pita **Beranda**, klik panah bawah **Gabungkan**, lalu klik **Gabungkan Kueri**.

    ![Gambar 5654](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image71.png)

    *Penggabungan kueri memungkinkan pengintegrasian data, dalam hal ini dari sumber data yang berbeda (SQL Server dan file CSV).*

3. Di jendela **Gabungkan**, di kisi kueri **Produk**, pilih header kolom **Warna**.

    ![Gambar 5655](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image72.png)

4. Di bawah kisi kueri **Produk**, dalam daftar dropdown, pilih kueri **ColorFormats**.

    ![Gambar 21](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image73.png)

5. Di kisi kueri **ColorFormats**, pilih header kolom **Warna**.

6. Saat jendela **Tingkat Privasi** terbuka, untuk masing-masing dari dua sumber data, di daftar dropdown yang sesuai, pilih **Organisasi**.

    ![Gambar 5691](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image74.png)

    *Tingkat privasi dapat dikonfigurasi untuk sumber data guna menentukan apakah data dapat dibagikan antar sumber. Mengatur setiap sumber data sebagai **Organisasi** memungkinkan mereka berbagi data, jika perlu. Perhatikan bahwa sumber data pribadi tidak pernah dapat dibagikan dengan sumber data lain. Ini tidak berarti bahwa data Pribadi tidak dapat dibagikan; artinya mesin Power Query tidak dapat berbagi data antar sumber.*

7. Klik **Simpan**.

    ![Gambar 5692](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image75.png)

8. Di jendela **Gabungkan**, gunakan default **Jenis Gabungan** - pertahankan pilihan Kiri Luar dan klik **OK**.

    ![Gambar 5693](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image76.png)

9. Luaskan kolom **ColorFormats** untuk menyertakan dua kolom berikut:

    - Format Warna Latar Belakang

    - Format Warna Huruf

    ![Gambar 5694](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image77.png)

10. Di bilah status, verifikasi bahwa kueri sekarang memiliki delapan kolom dan 397 baris.

    ![Gambar 5695](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image78.png)

### <a name="task-11-update-the-colorformats-query"></a>**Tugas 11: Memperbarui kueri ColorFormats**

Dalam tugas ini, Anda akan memperbarui **ColorFormats** untuk menonaktifkan pemuatannya.

1. Pilih kueri **ColorFormats**.

    ![Gambar 321](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image79.png)

2. Di panel **Pengaturan Kueri**, klik tautan **Semua Properti**.

    ![Gambar 322](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image80.png)

3. Di jendela **Properti Kueri**, hapus centang pada kotak **Aktifkan Pemuatan Ke Laporan**.

    ![Gambar 323](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image81.png)

    Menonaktifkan pemuatan berarti tidak akan memuat sebagai tabel ke model data. Ini dilakukan karena kueri digabungkan dengan kueri **Produk**, yang diaktifkan untuk memuat ke model data.

4. Klik **OK**.

    ![Gambar 324](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image82.png)

### <a name="task-12-finish-up"></a>**Tugas 12: Selesaikan**

Dalam tugas ini Anda akan menyelesaikan lab.

1. Verifikasi bahwa Anda memiliki delapan kueri, dengan nama yang benar sebagai berikut:

    - Penjual

    - SalespersonRegion

    - Produk

    - Pengecer

    - Wilayah

    - Sales

    - Target

    - ColorFormats (yang tidak akan dimuat ke model data)

2. Untuk memuat model data, pada tampilan **File** di tampilan backstage, pilih **Tutup &amp; Terapkan**.

    ![Gambar 326](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image83.png)

    *Semua kueri yang mendukung pemuatan sekarang dimuat ke model data.*

3. Di panel **Bidang** (terletak di sebelah kanan), perhatikan tujuh tabel yang dimuat ke model data.

    ![Gambar 3](Linked_image_Files/02-load-data-with-power-query-in-power-bi-desktop_image84.png)

4. Simpan file Power BI Desktop.

5. Jika Anda ingin memulai lab berikutnya, biarkan Power BI Desktop tetap terbuka.

    *Anda akan mengonfigurasi tabel dan hubungan model data di lab **Membuat Model Data di Power BI Desktop**.*
