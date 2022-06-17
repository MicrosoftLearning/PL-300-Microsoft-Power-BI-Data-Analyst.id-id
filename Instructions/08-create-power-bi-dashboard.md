---
lab:
  title: Buat Dasbor Power BI
  module: Module 8 - Create Dashboards
ms.openlocfilehash: 2ddb086b004fca3fa322e10570f9163342514808
ms.sourcegitcommit: f09183b2093a7f8de629f89b54d70bcad85598b6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/07/2022
ms.locfileid: "146109911"
---
# <a name="create-a-power-bi-dashboard"></a>**Membuat Dasbor Power BI**

**Perkiraan waktu untuk menyelesaikan lab adalah 45 menit**

Di lab ini Anda akan membuat dasbor **Pemantauan Penjualan**.

Di lab ini Anda mempelajari cara:

- Menyematkan visual ke dasbor

- Menggunakan Q&A untuk membuat petak peta dasbor

### <a name="lab-story"></a>**Cerita lab**

Lab ini adalah salah satu dari sekian banyak lab yang dirancang sebagai cerita lengkap, mulai dari persiapan data hingga publikasi sebagai laporan dan dasbor. Anda dapat menyelesaikan lab dalam urutan apa pun. Namun, jika Anda ingin mengerjakan beberapa lab sekaligus, untuk 10 lab pertama, sebaiknya Anda mengerjakannya dengan urutan berikut:

1. Mempersiapkan Data di Power BI Desktop

2. Muat Data di Power BI Desktop

3. Data Model di Power BI Desktop

5. Membuat Perhitungan DAX di Power BI Desktop, Bagian 1

6. Membuat Perhitungan DAX di Power BI Desktop, Bagian 2

7. Merancang Laporan di Power BI Desktop, Bagian 1

8. Merancang Laporan di Power BI Desktop, Bagian 2

9. **Membuat Dasbor Power BI**

10. Menganalisis Data di Power BI Desktop

11. Terapkan Keamanan Tingkat Baris

## <a name="exercise-1-create-a-dashboard"></a>**Latihan 1: Membuat Dasbor**

Dalam latihan ini Anda akan membuat dasbor **Pemantauan Penjualan**. Dasbor yang sudah selesai akan terlihat seperti berikut:

![Gambar dasbor yang telah selesai, terdiri dari tiga petak peta.](Linked_image_Files/09-create-power-bi-dashboard_image1.png)

### <a name="task-1-get-started--sign-in"></a>**Tugas 1: Memulai – Masuk**

Dalam tugas ini, Anda akan menyiapkan lingkungan untuk lab dengan masuk ke Power BI.

*Penting: Jika Anda sudah masuk ke Power BI di lab sebelumnya, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Microsoft Edge, pada bilah tugas, klik pintasan program Microsoft Edge.

    ![Gambar 42](Linked_image_Files/09-create-power-bi-dashboard_image2.png)

2. Di jendela browser Microsoft Edge, navigasikan ke **https://powerbi.microsoft.com** .

    *Tips: Anda juga dapat menggunakan favorit Layanan Power BI di bilah favorit Microsoft Edge.*

3. Klik **Masuk** (terletak di sudut kanan atas).

    ![Gambar 41](Linked_image_Files/09-create-power-bi-dashboard_image3.png)

4. Masukkan detail akun yang diberikan kepada Anda.

5. Jika diminta untuk memperbarui kata sandi, masukkan kembali kata sandi yang diberikan, lalu masukkan dan konfirmasikan kata sandi baru.

    *Penting: Pastikan untuk mencatat kata sandi baru Anda.*

6. Selesaikan proses masuk.

7. Jika diminta oleh Microsoft Edge untuk tetap masuk, klik **Ya**.

8. Di jendela browser Microsoft Edge, di layanan Power BI, di panel **Navigasi**, luaskan **Ruang Kerja Saya**.

    ![Gambar 40](Linked_image_Files/09-create-power-bi-dashboard_image4.png)

9. Biarkan jendela browser Microsoft Edge terbuka.

### <a name="task-2-get-started--open-report"></a>**Tugas 2: Memulai – Membuka laporan**

Dalam tugas ini, Anda akan menyiapkan lingkungan untuk lab dengan membuka laporan awal.

*Penting: Jika Anda melanjutkan dari lab sebelumnya (dan Anda berhasil menyelesaikan lab tersebut), jangan selesaikan tugas ini; sebagai gantinya, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Power BI Desktop, pada taskbar, klik pintasan Microsoft Power BI Desktop.

    ![Gambar 39](Linked_image_Files/09-create-power-bi-dashboard_image5.png)

2. Untuk menutup jendela memulai, di kiri atas jendela, klik **X**.

    ![Gambar 38](Linked_image_Files/09-create-power-bi-dashboard_image6.png)

3. Jika Power BI Desktop tidak masuk ke layanan Power BI, di kanan atas, klik **Masuk**.

    ![Gambar 37](Linked_image_Files/09-create-power-bi-dashboard_image7.png)

4. Selesaikan proses masuk menggunakan akun yang sama yang digunakan untuk masuk ke layanan Power BI.

5. Untuk membuka file Power BI Desktop pertama, klik tab pita **File** untuk membuka tampilan backstage.

6. Pilih **Buka Laporan**.

    ![Gambar 36](Linked_image_Files/09-create-power-bi-dashboard_image8.png)

7. Klik **Jelajahi Laporan**.

    ![Gambar 34](Linked_image_Files/09-create-power-bi-dashboard_image9.png)

8. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Labs\08-create-power-bi-dashboard\Starter**.

9. Pilih file **Analisis Penjualan**.

10. Klik **Buka**.

    ![Gambar 32](Linked_image_Files/09-create-power-bi-dashboard_image10.png)

11. Tutup semua jendela informasi yang mungkin terbuka.

12. Untuk membuat salinan file, klik tab pita **File** untuk membuka tampilan backstage.

13. Pilih **Simpan**.

    ![Gambar 29](Linked_image_Files/09-create-power-bi-dashboard_image11.png)

14. Jika diminta untuk menerapkan perubahan, klik **Terapkan**.

    ![Gambar 10](Linked_image_Files/09-create-power-bi-dashboard_image12.png)

15. Di jendela **Simpan Sebagai**, navigasikan ke folder **D:\PL300\MySolution**.

16. Klik **Simpan**.

    ![Gambar 9](Linked_image_Files/09-create-power-bi-dashboard_image13.png)

### <a name="task-3-get-started--publish-the-report"></a>**Tugas 3: Memulai – Menerbitkan laporan**

Dalam tugas ini, Anda akan menyiapkan lingkungan untuk lab dengan membuat himpunan data.

*Penting: Jika Anda telah menerbitkan laporan di lab **Merancang Laporan di Power BI Desktop, Bagian 2**, lanjutkan dari tugas berikutnya.*

1. Di jendela browser Microsoft Edge, di layanan Power BI, di panel **Navigasi**, di bagian bawah, klik **Dapatkan Data**.

    ![Gambar 8](Linked_image_Files/09-create-power-bi-dashboard_image14.png)

2. Di petak peta **File**, klik **Dapatkan**.

    ![Gambar 2](Linked_image_Files/09-create-power-bi-dashboard_image15.png)

3. Klik petak peta **File Lokal**.

    ![Gambar 5](Linked_image_Files/09-create-power-bi-dashboard_image16.png)

4. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Labs\08-create-power-bi-dashboard\Solution**.

5. Pilih file **Sales Analysis.pbix**, lalu klik **Buka**.

6. Jika diminta untuk mengganti himpunan data, klik **Ganti**.

### <a name="task-4-create-a-dashboard"></a>**Tugas 4: Membuat dasbor**

Dalam tugas ini, Anda akan membuat dasbor **Pemantauan Penjualan**. Anda akan menyematkan visual dari laporan, dan menambahkan petak peta berdasarkan URI data gambar, dan menggunakan Q&A untuk membuat petak peta.

1. Di jendela browser Microsoft Edge, di layanan Power BI, buka laporan **Analisis Penjualan**.

2. Di halaman **Ringkasan**, atur pemotong **Tahun** ke **FY2020**.

    ![Gambar 4](Linked_image_Files/09-create-power-bi-dashboard_image17.png)

3. Atur pemotong **Wilayah** ke **Pilih Semua**.

    *Saat menyematkan visual ke dasbor, mereka akan menggunakan konteks filter saat ini. Setelah disematkan, konteks filter tidak dapat diubah. Untuk filter berbasis waktu, sebaiknya gunakan pemotong tanggal relatif (atau, Q&A menggunakan pertanyaan berbasis waktu relatif).*

4. Untuk membuat dasbor dan menyematkan visual, arahkan kursor ke visual **Penjualan dan Margin Keuntungan berdasarkan Bulan** (kolom/baris).

5. Di pojok kanan bawah, klik tombol paku payung.

    ![Gambar 43](Linked_image_Files/09-create-power-bi-dashboard_image18.png)

6. Di jendela **Sematkan ke Dasbor**, di kotak **Nama Dasbor**, masukkan **Pemantauan Penjualan**.

    ![Gambar 3](Linked_image_Files/09-create-power-bi-dashboard_image19.png)

7. Klik **Sematkan**.

    ![Gambar 1](Linked_image_Files/09-create-power-bi-dashboard_image20.png)

8. Buka panel **Navigasi**, pilih **Ruang Kerja Saya**, lalu buka dasbor **Pemantauan Penjualan**.

    ![Gambar 44](Linked_image_Files/09-create-power-bi-dashboard_image21.png)

9. Perhatikan bahwa dasbor memiliki satu petak peta.

    ![Gambar 45](Linked_image_Files/09-create-power-bi-dashboard_image22.png)

10. Untuk menambahkan petak peta berdasarkan pertanyaan, di kiri atas dasbor, klik **Ajukan Pertanyaan Tentang Data Anda**.

    ![Gambar 7](Linked_image_Files/09-create-power-bi-dashboard_image23.png)

    *Anda dapat menggunakan fitur Q&A untuk mengajukan pertanyaan, dan Power BI akan merespons secara visual.*

11. Klik salah satu pertanyaan yang disarankan di bawah kotak Q&A, dalam kotak biru.

12. Tinjau responsnya.

13. Hapus semua teks dari kotak Q&A.

14. Di kotak Q&A, masukkan yang berikut ini: **YTD Penjualan**

    ![Gambar 11](Linked_image_Files/09-create-power-bi-dashboard_image24.png)

15. Perhatikan respons dari **(Kosong)** .

    ![Gambar 14](Linked_image_Files/09-create-power-bi-dashboard_image25.png)

    *Anda mungkin ingat bahwa Anda menambahkan ukuran **Penjualan YTD** di lab **Membuat Perhitungan DAX di Power BI Desktop, Bagian 2**. Ukuran ini adalah ekspresi Inteligensi Waktu dan karenanya memerlukan filter pada tabel **Tanggal** untuk menghasilkan hasil.*

16. Perpanjang pertanyaan dengan: **pada tahun FY2020**.

    ![Gambar 12](Linked_image_Files/09-create-power-bi-dashboard_image26.png)

17. Perhatikan responsnya sekarang **$33 juta**.

    ![Gambar 13](Linked_image_Files/09-create-power-bi-dashboard_image27.png)

18. Untuk menyematkan respons ke dasbor, di sudut kanan atas, klik **Sematkan Visual**.

    ![Gambar 15](Linked_image_Files/09-create-power-bi-dashboard_image28.png)

19. Saat diminta untuk menyematkan petak peta ke dasbor, klik **Sematkan**.

    ![Gambar 17](Linked_image_Files/09-create-power-bi-dashboard_image29.png)

20. Untuk kembali ke dasbor, di sudut kiri atas, klik **Keluar dari Q&amp;A**.

    ![Gambar 16](Linked_image_Files/09-create-power-bi-dashboard_image30.png)

21. Untuk menambahkan logo perusahaan, pada bilah menu, klik **Edit**, lalu pilih **Tambahkan Petak Peta**.

    ![Gambar 46](Linked_image_Files/09-create-power-bi-dashboard_image31.png)

    *Menggunakan teknik ini untuk menambahkan petak peta dasbor memungkinkan Anda menghiasi dasbor dengan media, termasuk konten web, gambar, kotak teks berformat kaya, dan video (menggunakan tautan YouTube atau Vimeo).*

22. Di panel **Tambahkan Petak Peta** (terletak di sebelah kanan), pilih petak peta **Gambar**.

    ![Gambar 47](Linked_image_Files/09-create-power-bi-dashboard_image32.png)

23. Klik **Berikutnya**.

    ![Gambar 48](Linked_image_Files/09-create-power-bi-dashboard_image33.png)

24. Di panel **Tambahkan Petak Peta Gambar**, di kotak **URL**, masukkan URL lengkap yang ada di file **D:\PL300\Resources\AdventureWorksLogo_DataURL.txt**.

    *Anda dapat menyematkan gambar dengan menggunakan URL-nya, atau Anda dapat menggunakan URL data, yang menyematkan konten sebaris.*

25. Di bagian bawah panel, klik **Terapkan**.

    ![Gambar 49](Linked_image_Files/09-create-power-bi-dashboard_image34.png)

26. Untuk mengubah ukuran petak peta logo, seret sudut kanan bawah, dan ubah ukuran petak peta menjadi lebar satu unit, dan tinggi dua unit.

    *Ukuran petak peta dibatasi menjadi bentuk persegi panjang. Anda hanya dapat mengubah ukuran menjadi beberapa bentuk persegi panjang.*

27. Atur petak peta sehingga logo muncul di kiri atas, dengan petak peta **Penjualan YTD** di bawahnya, dan petak peta **Penjualan, Margin Keuntungan** di sebelah kanan.

    ![Gambar 52](Linked_image_Files/09-create-power-bi-dashboard_image35.png)

### <a name="task-5-edit-tile-details"></a>**Tugas 5: Mengedit detail petak peta**

Dalam tugas ini Anda akan mengedit detail dua petak peta.

1. Arahkan kursor ke petak peta **Penjualan YTD**, lalu di kanan atas petak peta, klik elipsis, lalu pilih **Edit Detail**.

    ![Gambar 50](Linked_image_Files/09-create-power-bi-dashboard_image36.png)

2. Di panel **Detail Petak Peta** (terletak di sebelah kanan), di kotak **Subjudul**, masukkan **FY2020**.

    ![Gambar 19](Linked_image_Files/09-create-power-bi-dashboard_image37.png)

3. Klik **Terapkan**.

    ![Gambar 20](Linked_image_Files/09-create-power-bi-dashboard_image38.png)

4. Perhatikan bahwa petak peta **Penjualan YTD** menampilkan subtitel.

    ![Gambar 21](Linked_image_Files/09-create-power-bi-dashboard_image39.png)

5. Edit detail petak peta untuk petak peta **Penjualan, Margin Keuntungan**.

6. Di panel **Detail Petak Peta**, di bagian **Fungsionalitas**, centang **Tampilkan Waktu Refresh Terakhir**.

    ![Gambar 22](Linked_image_Files/09-create-power-bi-dashboard_image40.png)

7. Klik **Terapkan**.

    ![Gambar 23](Linked_image_Files/09-create-power-bi-dashboard_image41.png)

8. Perhatikan bahwa petak peta menjelaskan waktu refresh terakhir (yang dilakukan saat memuat model data di Power BI Desktop).



    *Anda akan merefresh himpunan data di latihan berikutnya. Biasanya, hal ini akan dicapai dengan menggunakan refresh terjadwal, dalam hal ini Power BI akan menggunakan gateway untuk terhubung ke database SQL Server. Namun, karena kendala dalam penataan ruang kelas, tidak ada gateway. Jadi, Anda akan membuka Power BI Desktop, merefresh data manual, lalu mengunggah file ke ruang kerja Anda.*

## <a name="exercise-2-refresh-the-dataset"></a>**Latihan 2: Merefresh Himpunan Data**

Dalam latihan ini, pertama-tama Anda akan memuat data pesanan penjualan untuk bulan Juni 2020 ke dalam database **AdventureWorksDW2020**. Anda kemudian akan membuka file Power BI Desktop, merefresh data, lalu mengunggah file ke ruang kerja Anda.

### <a name="task-1-update-the-lab-database"></a>**Tugas 1: Memperbarui database lab**

Dalam tugas ini Anda akan menjalankan skrip PowerShell untuk memperbarui data di database **AdventureWorksDW2020**.

1. Di File Explorer, di dalam folder **D:\PL300\Setup**, klik kanan file **UpdateDatabase-2-AddSales.ps1**, lalu pilih **Jalankan dengan PowerShell**.

    ![Gambar 28](Linked_image_Files/09-create-power-bi-dashboard_image46.png)

2. Jika diminta untuk mengubah kebijakan eksekusi, tekan **A**.

3. Saat diminta untuk menekan tombol apa saja untuk menutup, tekan **Enter** lagi.

    *Database **AdventureWorksDW2020** sekarang menyertakan pesanan penjualan yang dibuat pada Juni 2020.*

### <a name="task-2-refresh-the-power-bi-desktop-file"></a>**Tugas 2: Refresh file Power BI Desktop**

Dalam tugas ini, Anda akan membuka file **Analisis Penjualan** Power BI Desktop, merefresh data, lalu mengunggah file ke ruang kerja **Analisis Penjualan** Anda.

1. Di file Power BI Desktop, di panel **Bidang**, klik kanan tabel **Penjualan**, lalu pilih **Refresh Data**.

    ![Gambar 55](Linked_image_Files/09-create-power-bi-dashboard_image47.png)

2. Setelah refresh selesai, simpan file Power BI Desktop.

3. Untuk menerbitkan file ke ruang kerja Anda, pada tab pita **Beranda**, dari dalam grup **Bagikan**, klik **Terbitkan** lalu klik **Pilih** untuk menerbitkan.

    ![Gambar 59](Linked_image_Files/09-create-power-bi-dashboard_image48.png)

4. Saat diminta untuk mengganti himpunan data, klik **Ganti**.

    ![Gambar 31](Linked_image_Files/09-create-power-bi-dashboard_image49.png)

    *Himpunan data di layanan Power BI sekarang memiliki data penjualan Juni 2020.*

5. Dapatkan Power BI Desktop.

## <a name="exercise-3-review-the-dashboard"></a>**Latihan 3: Meninjau Dasbor**

Dalam latihan ini Anda akan meninjau dasbor untuk melihat penjualan yang diperbarui.

### <a name="task-1-review-the-dashboard"></a>**Tugas 1: Meninjau dasbor**

Dalam tugas ini Anda akan meninjau dasbor untuk melihat penjualan yang diperbarui.

1. Di jendela browser Microsoft Edge, di layanan Power BI, tinjau dasbor **Pemantauan Penjualan**.

2. Di petak peta **Penjualan, Margin Keuntungan**, di subtitel, perhatikan bahwa data telah direfresh **SEKARANG**.

3. Perhatikan juga bahwa sekarang ada kolom untuk **Juni 2020**.

    *Jika Anda tidak melihat data Juni 2020, Anda mungkin perlu menekan **F5** untuk memuat ulang browser web.*

    ![Gambar 33](Linked_image_Files/09-create-power-bi-dashboard_image50.png)

    

4. Untuk menutup panel, klik **Tutup**.
