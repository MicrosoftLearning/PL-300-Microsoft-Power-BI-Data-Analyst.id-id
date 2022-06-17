---
lab:
  title: Menganalisis Data di Power BI Desktop
  module: Module 9 - Identify Patterns and Trends
ms.openlocfilehash: e58af011b5603e4cd6e5def7c4353156fc67c879
ms.sourcegitcommit: 6853b027da7f5e739951c3eef54f4cd458854c66
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/12/2022
ms.locfileid: "146274801"
---
# <a name="perform-data-analysis-in-power-bi-desktop"></a>**Menganalisis Data di Power BI Desktop**

**Perkiraan waktu untuk menyelesaikan lab adalah 45 menit**

Di lab ini Anda akan membuat laporan **Eksplorasi Penjualan**.

Di lab ini Anda mempelajari cara:

- Membuat bagan pencar animasi

- Gunakan visual untuk memperkirakan nilai



### <a name="lab-story"></a>**Cerita lab**

Lab ini adalah salah satu dari sekian banyak lab yang dirancang sebagai cerita lengkap, mulai dari persiapan data hingga publikasi sebagai laporan dan dasbor. Anda dapat menyelesaikan lab dalam urutan apa pun. Namun, jika Anda ingin mengerjakan beberapa lab sekaligus, untuk 10 lab pertama, sebaiknya Anda mengerjakannya dengan urutan berikut:

1. Mempersiapkan Data di Power BI Desktop

2. Muat Data di Power BI Desktop

3. Data Model di Power BI Desktop

5. Membuat Perhitungan DAX di Power BI Desktop, Bagian 1

6. Membuat Perhitungan DAX di Power BI Desktop, Bagian 2

7. Merancang Laporan di Power BI Desktop, Bagian 1

8. Merancang Laporan di Power BI Desktop, Bagian 2

9. Buat Dasbor Power BI

10. **Menganalisis Data di Power BI Desktop**

11. Terapkan Keamanan Tingkat Baris

## <a name="exercise-1-create-the-report"></a>**Latihan 1: Membuat Laporan**

Dalam latihan ini Anda akan membuat laporan **Eksplorasi Penjualan**.

### <a name="task-1-get-started--sign-in"></a>**Tugas 1: Memulai – Masuk**

Dalam tugas ini, Anda akan menyiapkan lingkungan untuk lab dengan masuk ke Power BI.

*Penting: Jika Anda sudah masuk ke Power BI di lab sebelumnya, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Microsoft Edge, pada bilah tugas, klik pintasan program Microsoft Edge.

    ![Gambar 7](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image1.png)

1. Di jendela browser Microsoft Edge, navigasikan ke **https://powerbi.microsoft.com** .

    *Tips: Anda juga dapat menggunakan favorit Layanan Power BI di bilah favorit Microsoft Edge.*

1. Klik **Masuk** (terletak di sudut kanan atas).

    ![Gambar 5](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image2.png)

1. Masukkan detail akun yang diberikan kepada Anda.

1. Jika diminta untuk memperbarui kata sandi, masukkan kembali kata sandi yang diberikan, lalu masukkan dan konfirmasikan kata sandi baru.

    *Penting: Pastikan untuk mencatat kata sandi baru Anda.*

1. Selesaikan proses masuk.

1. Jika diminta oleh Microsoft Edge untuk tetap masuk, klik **Ya**.

1. Di jendela browser Microsoft Edge, di layanan Power BI, di panel **Navigasi**, luaskan **Ruang Kerja Saya**.

    ![Gambar 4](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image3.png)

1. Biarkan jendela browser Microsoft Edge terbuka.

### <a name="task-2-get-started--create-a-dataset"></a>**Tugas 2: Memulai – Membuat himpunan data**

Dalam tugas ini, Anda akan menyiapkan lingkungan untuk lab dengan membuat himpunan data.

*Penting: Jika Anda telah menerbitkan himpunan data di lab **Membuat Dasbor Power BI**, lanjutkan dari tugas berikutnya.*

1. Di jendela browser Microsoft Edge, di layanan Power BI, di panel **Navigasi**, di bagian bawah, klik **Dapatkan Data**.

    ![Gambar 8](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image4.png)

2. Di petak peta **File**, klik **Dapatkan**.

    ![Gambar 10](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image5.png)

3. Klik petak peta **File Lokal**.

    ![Gambar 11](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image6.png)

4. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Labs\08-create-power-bi-dashboard\Solution**.

5. Pilih file **Sales Analysis.pbix**, lalu klik **Buka**.

6. Jika diminta untuk mengganti himpunan data, klik **Ganti**.

### <a name="task-3-create-the-report"></a>**Tugas 3: Membuat laporan**

Dalam tugas ini, Anda akan membuat laporan **Eksplorasi Penjualan**.

1. Untuk membuka Power BI Desktop, pada taskbar, klik pintasan Microsoft Power BI Desktop.

    *Penting: Jika Anda sudah membuka Power BI Desktop (dari lab sebelumnya), tutup instans tersebut.*

    ![Gambar 14](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image7.png)

2. Untuk menutup jendela memulai, di kiri atas jendela, klik **X**.

    ![Gambar 13](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image8.png)

3. Jika Power BI Desktop tidak masuk ke layanan Power BI, di kanan atas, klik **Masuk**.

    ![Gambar 16](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image9.png)

4. Selesaikan proses masuk menggunakan akun yang sama yang digunakan untuk masuk ke layanan Power BI.

5. Untuk menyimpan file, klik tab pita **File** untuk membuka tampilan di backstage.

6. Pilih **Simpan**.

    ![Gambar 12](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image10.png)

7. Di jendela **Simpan Sebagai**, navigasikan ke folder **D:\PL300\MySolution**.

8. Di kotak **Nama File**, masukkan **Eksplorasi Penjualan** dan klik **Simpan**.

    ![Gambar 1](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image11.png)

9. Untuk membuat koneksi langsung ke himpunan data **Analisis Penjualan**, pada tab pita **Beranda**, dari dalam grup **Data**, klik **Himpunan Data Power BI**.

    ![Gambar 15](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image12.png)

10. Di jendela **Pilih Himpunan Data untuk Membuat Laporan**, pilih himpunan data **Analisis Penjualan**.

11. Klik **Buat**.

    ![Gambar 17](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image13.png)

12. Simpan file Power BI Desktop.

    *Sekarang Anda akan membuat dua halaman laporan, dan di setiap halaman Anda akan bekerja dengan visual yang berbeda untuk menganalisis dan menjelajahi data.*

## <a name="exercise-2-create-a-scatter-chart"></a>**Latihan 2: Membuat Diagram Tebar**

Dalam latihan ini Anda akan membuat diagram tebar yang dapat diberi animasi.

### <a name="task-1-create-an-animated-scatter-chart"></a>**Tugas 1: Membuat diagram tebar yang diberi animasi**

Dalam tugas ini Anda akan membuat diagram tebar yang dapat diberi animasi.

1. Ganti nama **Halaman 1** sebagai **Diagram Tebar**.

    ![Gambar 67](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image14.png)

2. Tambahkan visual **Diagram Tebar** ke halaman laporan, lalu posisikan dan ubah ukurannya sehingga memenuhi seluruh halaman.

    ![Gambar 18](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image15.png)

    ![Gambar 75](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image16.png)

3. Tambahkan bidang berikut ke sumber/area visual:

    Lab menggunakan notasi steno untuk mereferensikan bidang. Ini akan terlihat seperti ini: **Pengecer** **\|** **Jenis Bisnis**. Dalam contoh ini, **Pengecer** adalah nama tabel dan **Jenis Bisnis** adalah nama bidang.

    

    - Sumbu X: **Penjualan \| Penjualan** 

    - Sumbu Y: **Penjualan \| Margin Keuntungan**

    - Legenda: **Pengecer \| Jenis Bisnis**

    - Ukuran: **Penjualan \| Kuantitas**

    - Sumbu Putar: **Tanggal \| Kuartal**

    ![Gambar 39](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image17.png)

    *Bagan dapat diberi animasi jika bidang ditambahkan ke sumber/area **Sumbu Putar**.*

4. Di panel **Filter**, tambahkan bidang **Produk \| Kategori** ke sumber/area **Filter Di Halaman Ini**.

5. Di kartu filter, filter berdasarkan **Sepeda**.

    ![Gambar 40](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image18.png)

6. Untuk memberi animasi pada bagan, di sudut kiri bawah, klik **Putar**.

    ![Gambar 41](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image19.png)

7. Tonton seluruh siklus animasi dari **FY2018 Q1** hingga **FY2020 Q4**.

    *Diagram tebar memungkinkan pemahaman nilai ukuran secara bersamaan: dalam hal ini, jumlah pesanan, pendapatan penjualan, dan margin keuntungan.*

    *Setiap balon mewakili jenis bisnis pengecer. Perubahan ukuran gelembung mencerminkan peningkatan atau penurunan jumlah pesanan. Sementara pergerakan horizontal menunjukkan kenaikan/penurunan pendapatan penjualan, dan pergerakan vertikal menunjukkan peningkatan/penurunan profitabilitas.*

8. Saat animasi berhenti, klik salah satu gelembung untuk menampilkan pelacakannya dari waktu ke waktu.

9. Arahkan kursor ke gelembung mana pun untuk menampilkan tipsalat yang menjelaskan nilai ukuran untuk jenis pengecer pada saat itu.

10. Di panel **Filter**, filter berdasarkan **Pakaian** saja, dan perhatikan bahwa pakaian menghasilkan hasil yang sangat berbeda.

11. Simpan file Power BI Desktop.

## <a name="exercise-3-create-a-forecast"></a>**Latihan 3: Membuat Perkiraan**

Dalam latihan ini Anda akan membuat perkiraan untuk menentukan kemungkinan pendapatan penjualan di masa mendatang.

### <a name="task-1-create-a-forecast"></a>**Tugas 1: Membuat perkiraan**

Dalam tugas ini, Anda akan membuat perkiraan untuk menentukan kemungkinan pendapatan penjualan di masa mendatang.

1. Tambahkan halaman baru, lalu ganti nama halaman menjadi **Prakiraan**.

    ![Gambar 66](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image20.png)

2. Tambahkan visual **Diagram Garis** ke halaman laporan, lalu posisikan dan ubah ukurannya sehingga memenuhi seluruh halaman.

    ![Gambar 19](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image21.png)

    ![Gambar 74](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image22.png)

  

3. Tambahkan bidang berikut ke sumber/area visual:

    - sumbu X: **Tanggal \| Tanggal**

    - sumbu Y: **Penjualan \| Penjualan** 

    ![Gambar 46](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image23.png)

4. Di panel **Filter**, tambahkan bidang **Tanggal \| Tahun** ke sumber/area **Filter Di Halaman Ini**.

5. Di kartu filter, filter berdasarkan dua tahun: **FY2019** dan **FY2020**.

    ![Gambar 47](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image24.png)

    *Saat membuat prakiraan berdasarkan garis waktu, Anda memerlukan setidaknya dua siklus (tahun) data untuk membuat perkiraan yang akurat dan stabil.*

  

6. Tambahkan juga bidang **Produk \| Kategori** ke area **Filter Pada Halaman Ini**, dan filter berdasarkan **Sepeda**.

    ![Gambar 48](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image25.png)

7. Untuk menambahkan perkiraan, di bawah panel **Visualisasi**, pilih panel **Analitik**.

    ![Gambar 20](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image26.png)

8. Luaskan bagian **Prakiraan**.



    *Jika bagian **Prakiraan** tidak tersedia, mungkin karena visual belum dikonfigurasi dengan benar. Prakiraan hanya tersedia jika dua kondisi terpenuhi: sumbu memiliki satu bidang jenis tanggal, dan hanya ada satu bidang nilai.*

9. Ubah opsi **Prakiraan** ke **Aktif**.

    ![Gambar 51](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image28.png)

10. Konfigurasikan properti prakiraan berikut:

    - Unit: Bulan

    - Panjang prakiraan: 1 bulan

    - Musiman: 365
    
    - Interval keyakinan: 80%



11. Klik **Terapkan**.

    ![Gambar 52](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image29.png)

12. Dalam visual garis, perhatikan bahwa prakiraan telah diperpanjang satu bulan di luar data riwayat.

    *Area abu-abu mewakili keyakinan. Semakin luas keyakinannya, semakin tidak stabil—dan oleh karena itu semakin kurang akurat—prakiraan tersebut kemungkinan besar akan terjadi.*

    *Jika Anda mengetahui panjang siklus, dalam hal ini tahunan, Anda harus memasukkan poin musiman. Terkadang bisa mingguan (7), atau bulanan (30).*

13. Di panel **Filter**, filter berdasarkan **Pakaian** saja, dan perhatikan bahwa filter menampilkan hasil yang berbeda.

14. Simpan file Power BI Desktop.


### <a name="task-2-finish-up"></a>**Tugas 2: Selesaikan**

Dalam tugas ini Anda akan menyelesaikan lab.

1. Pilih halaman **Diagram Tebar**.

2. Simpan file Power BI Desktop.

3. Untuk menerbitkan file ke **Ruang kerja saya**, pada tab pita **Beranda**, dari dalam grup **Bagikan**, klik **Terbitkan** lalu klik **Pilih** untuk menerbitkan.

    ![Gambar 23](Linked_image_Files/10-perform-data-analysis-in-power-bi-desktop_image46.png)

4.  Dapatkan Power BI Desktop.
