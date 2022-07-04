---
lab:
  title: Merancang Laporan di Power BI Desktop, Bagian 2
  module: Module 7 - Create Reports
ms.openlocfilehash: 72d571e81320d4c0311f9e566d1805725439f961
ms.sourcegitcommit: 9ea1e7e21b9b3c718030c94b1693d153a2010ec7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/29/2022
ms.locfileid: "146650207"
---
# <a name="design-a-report-in-power-bi-desktop-part-2"></a>**Merancang Laporan di Power BI Desktop, Bagian 2**

**Perkiraan waktu untuk menyelesaikan lab adalah 45 menit**

Di lab ini, Anda akan menyempurnakan **Analisis Penjualan** dengan fitur desain tingkat lanjut.

Di lab ini Anda mempelajari cara:

- Menyinkronkan pemotong

- Membuat halaman drillthrough

- Menerapkan pemformatan bersyarat

- Membuat dan menggunakan bookmark

### <a name="lab-story"></a>**Cerita lab**

Lab ini adalah salah satu dari sekian banyak lab yang dirancang sebagai cerita lengkap, mulai dari persiapan data hingga publikasi sebagai laporan dan dasbor. Anda dapat menyelesaikan lab dalam urutan apa pun. Namun, jika Anda ingin mengerjakan beberapa lab sekaligus, sebaiknya Anda mengerjakannya dengan urutan berikut:

1. Mempersiapkan Data di Power BI Desktop

2. Muat Data di Power BI Desktop

3. Data Model di Power BI Desktop

5. Membuat Perhitungan DAX di Power BI Desktop, Bagian 1

6. Membuat Perhitungan DAX di Power BI Desktop, Bagian 2

7. Merancang Laporan di Power BI Desktop, Bagian 1

8. **Merancang Laporan di Power BI Desktop, Bagian 2**

9. Buat Dasbor Power BI

10. Menganalisis Data di Power BI Desktop

11. Terapkan Keamanan Tingkat Baris

## <a name="exercise-1-configure-sync-slicers"></a>**Latihan 1: Mengonfigurasi Sinkronisasi Pemotong**

Dalam latihan ini Anda akan menyinkronkan pemotong halaman laporan.

### <a name="task-1-get-started--sign-in"></a>Tugas 1: Memulai – Masuk

Dalam tugas ini, Anda akan menyiapkan lingkungan untuk lab dengan masuk ke Power BI.

*Penting: Jika Anda sudah masuk ke Power BI, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Microsoft Edge, pada bilah tugas, klik pintasan program Microsoft Edge.

    ![Gambar 12](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image1.png)

1. Di jendela browser Microsoft Edge, navigasikan ke **https://powerbi.microsoft.com** .

    *Tips: Anda juga dapat menggunakan favorit Layanan Power BI di bilah favorit Microsoft Edge.*

1. Klik **Masuk** (terletak di sudut kanan atas).

    ![Gambar 11](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image2.png)

1. Masukkan detail akun yang diberikan kepada Anda.

1. Jika diminta untuk memperbarui kata sandi, masukkan kembali kata sandi yang diberikan, lalu masukkan dan konfirmasikan kata sandi baru.

    *Penting: Pastikan untuk mencatat kata sandi baru Anda.*

1. Selesaikan proses masuk.

1. Jika diminta oleh Microsoft Edge untuk tetap masuk, klik **Ya**.

1. Di jendela browser Microsoft Edge, di layanan Power BI, di panel **Navigasi**, luaskan **Ruang Kerja Saya**.

    ![Gambar 22](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image3.png)

1. Biarkan jendela browser Microsoft Edge terbuka.

### <a name="task-2-get-started--open-report"></a>Tugas 2: Memulai – Membuka laporan

Dalam tugas ini, Anda akan menyiapkan lingkungan untuk lab dengan membuka laporan awal.

*Penting: Jika Anda melanjutkan dari lab sebelumnya (dan Anda berhasil menyelesaikan lab tersebut), jangan selesaikan tugas ini; sebagai gantinya, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Power BI Desktop, pada taskbar, klik pintasan Microsoft Power BI Desktop.

    ![Gambar 10](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image4.png)

2. Untuk menutup jendela memulai, di kiri atas jendela, klik **X**.

    ![Gambar 9](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image5.png)

3. Untuk masuk ke layanan Power BI, di kanan atas, klik **Masuk**.

    ![Gambar 8](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image6.png)

4. Selesaikan proses masuk menggunakan akun yang sama yang digunakan untuk masuk ke layanan Power BI.

5. Untuk membuka file Power BI Desktop pertama, klik tab pita **File** untuk membuka tampilan backstage.

6. Pilih **Buka Laporan**.

    ![Gambar 7](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image7.png)

7. Klik **Jelajahi Laporan**.

    ![Gambar 6](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image8.png)

8. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Labs\07-design-report-in-power-bi-desktop-enhanced\Starter**.

9. Pilih file **Analisis Penjualan**.

10. Klik **Buka**.

    ![Gambar 5](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image9.png)

11. Tutup semua jendela informasi yang mungkin terbuka.

12. Untuk membuat salinan file, klik tab pita **File** untuk membuka tampilan backstage.

13. Pilih **Simpan**.

    ![Gambar 4](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image10.png)

14. Jika diminta untuk menerapkan perubahan, klik **Terapkan**.

    ![Gambar 3](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image11.png)

15. Di jendela **Simpan Sebagai**, navigasikan ke folder **D:\PL300\MySolution**.

16. Klik **Simpan**.

    ![Gambar 2](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image12.png)

### <a name="task-3-sync-slicers"></a>**Tugas 3: Menyinkronkan pemotong**

Dalam tugas ini, Anda akan menyinkronkan pemotong **Tahun** dan **Wilayah**.

*Anda akan melanjutkan pengembangan laporan yang dibuat di lab **Merancang Laporan di Power BI Desktop, Bagian 1**.*

1. Di Power BI Desktop, pada halaman **Ringkasan**, atur pemotong **Tahun** ke **FY2018**.

2. Buka halaman **Performa Saya**, lalu perhatikan bahwa pemotong **Tahun** adalah nilai yang berbeda.

    *Jika pemotong tidak disinkronkan, pemotong dapat menyebabkan kesalahan penyajian data dan frustrasi bagi pengguna laporan. Sekarang Anda akan menyinkronkan pemotong laporan.*

3. Kembali ke halaman **Ringkasan**, lalu pilih pemotong **Tahun**.

4. Pada tab pita **Lihat**, dari dalam grup **Tampilkan Panel**, klik **Sinkronkan Pemotong**.

    ![Gambar 1](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image13.png)

5. Di panel **Sinkronkan Pemotong** (di sebelah kiri panel **Visualisasi**), di kolom kedua (yang menunjukkan sinkronisasi), centang kotak untuk **Ringkasan** dan Halaman **Performa Saya**.

    ![Gambar 93](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image14.png)

6. Pada halaman **Ringkasan**, pilih pemotong **Wilayah**.

7. Sinkronkan pemotong dengan halaman **Ringkasan** dan **Keuntungan**.

    ![Gambar 94](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image15.png)

8. Uji sinkronisasi pemotong dengan memilih opsi filter yang berbeda, lalu verifikasi bahwa pemotong yang disinkronkan memfilter berdasarkan pilihan yang sama.

9. Untuk menutup halaman **Sinkronisasi Pemotong**, klik **X** yang terletak di kanan atas panel.

    ![Gambar 98](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image16.png)

## <a name="exercise-2-configure-drill-through"></a>**Latihan 2: Mengonfigurasi Penelusuran**

Dalam latihan ini Anda akan membuat halaman baru dan mengonfigurasinya sebagai halaman penelusuran. Setelah Anda menyelesaikan desain, halaman akan terlihat seperti berikut:

![Gambar halaman baru, terdiri dari visual kartu dan visual tabel.](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image17.png)

### <a name="task-1-create-a-drill-through-page"></a>**Tugas 1: Membuat halaman penelusuran**

Dalam tugas ini, Anda akan membuat halaman baru dan mengonfigurasinya sebagai halaman penelusuran.

1. Tambahkan halaman laporan baru bernama **Detail Produk**.

    ![Gambar 95](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image18.png)

2. Klik kanan tab halaman **Detail Produk**, lalu pilih **Sembunyikan Halaman**.

    ![Gambar 97](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image19.png)

    *Pengguna laporan tidak akan dapat membuka halaman penelusuran secara langsung. Pengguna harus mengaksesnya dari visual di halaman lain. Anda akan mempelajari cara menelusuri halaman dalam latihan terakhir lab ini.*

3. Di bawah panel **Visualisasi**, di bagian **Penelusuran**, tambahkan bidang **Produk \| Kategori** ke kotak **Tambahkan Bidang Penelusuran Di Sini**.

    *Lab menggunakan notasi steno untuk mereferensikan bidang. Ini akan terlihat seperti ini: **Produk \| Kategori**. Dalam contoh ini, **Produk** adalah nama tabel dan **Kategori** adalah nama bidang.*

    ![Gambar 96](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image20.png)

4. Untuk menguji halaman penelusuran, di kartu filter penelusuran, pilih **Sepeda**.

    ![Gambar 99](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image21.png)

5. Di kiri atas halaman laporan, perhatikan tombol panah.

    ![Gambar 100](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image22.png)

    *Tombol ditambahkan secara otomatis ketika bidang ditambahkan ke penelusuran sumber/area. Hal ini memungkinkan pengguna laporan untuk menavigasi kembali ke halaman tempat mereka melakukan penelusuran.*

6. Tambahkan visual **Kartu** ke halaman, lalu ubah ukuran dan posisinya sehingga berada di sebelah kanan tombol dan memenuhi sisa lebar halaman yang tersisa.

    ![Gambar 13](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image23.png)

    ![Gambar 101](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image24.png)

7. Seret bidang **Produk \| Kategori** ke dalam visual kartu.

8. Konfigurasikan opsi format untuk visual, lalu ubah properti **Label Kategori** ke **Nonaktif**.

    ![Gambar 103](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image25.png)

9. Atur properti **Warna Latar Belakang** ke warna abu-abu terang.

10. Tambahkan visual **Tabel** ke halaman, lalu ubah ukuran dan posisinya sehingga berada di bawah visual kartu dan memenuhi ruang yang tersisa di halaman.

    ![Gambar 14](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image26.png)

    ![Gambar 105](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image27.png)

11. Tambahkan bidang berikut ke visual:

    - Produk \| Subkategori

    - Produk \| Warna

    - Penjualan \| Kuantitas

    - Penjualan \| Penjualan

    - Penjualan \| Margin Keuntungan

12. Konfigurasikan opsi format untuk visual, dan di bagian **Nilai**, atur properti **Ukuran Teks** ke **20pt**.

    *Desain halaman penelusuran hampir selesai. Anda akan menyempurnakan halaman dengan pemformatan bersyarat di latihan berikutnya.*

## <a name="exercise-3-add-conditional-formatting"></a>**Latihan 3: Menambahkan Pemformatan Bersyarat**

Dalam latihan ini Anda akan menyempurnakan halaman penelusuran dengan pemformatan bersyarat. Setelah Anda menyelesaikan desain, halaman akan terlihat seperti berikut:

![Gambar halaman yang diperbarui, menampilkan nilai dan ikon dengan format warna.](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image28.png)

### <a name="task-1-add-conditional-formatting"></a>**Tugas 1: Menambahkan pemformatan bersyarat**

Dalam tugas ini, Anda akan menyempurnakan halaman penelusuran dengan pemformatan bersyarat.

1. Pilih visual tabel.

2. Di panel visualisasi, klik panah bawah pada nilai **Margin Keuntungan**, lalu pilih Ikon **Pemformatan Bersyarat \|** .

    ![Gambar 107](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image29.png)

3. Di jendela **Ikon – Margin Keuntungan**, dalam daftar dropdown **Tata Letak Ikon**, pilih **Sebelah Kanan Data**.

    ![Gambar 108](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image30.png)

4. Untuk menghapus aturan tengah, di sebelah kiri segitiga kuning, klik **X**.

    ![Gambar 109](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image31.png)

5. Konfigurasikan aturan pertama (berlian merah) sebagai berikut:

    - Di kontrol kedua, hapus nilainya

    - Di kontrol ketiga, pilih **Nomor**

    - Di kontrol kelima, masukkan **0**

    - Di kontrol keenam, pilih **Nomor**

6. Konfigurasikan aturan kedua (lingkaran hijau) sebagai berikut:

    - Di kontrol kedua, masukkan **0**

    - Di kontrol ketiga, pilih **Nomor**

    - Di kontrol kelima, hapus nilainya

    - Di kontrol keenam, pilih **Nomor**

    ![Gambar 110](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image32.png)

    *Aturannya dapat diartikan sebagai berikut: tampilkan berlian merah jika nilai margin keuntungan kurang dari 0; sebaliknya jika nilainya besar atau sama dengan nol, tampilkan lingkaran hijau.*

7. Klik **OK**.

    ![Gambar 111](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image33.png)

8. Dalam visual tabel, pastikan bahwa ikon yang benar ditampilkan.

    ![Gambar 112](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image34.png)

9. Konfigurasikan pemformatan bersyarat warna latar belakang untuk bidang **Warna**.

10. Di jendela **Warna Latar Belakang – Warna**, di daftar dropdown **Gaya Format**, pilih **Nilai Bidang**.

    

11. Di daftar dropdown **Di bidang apa kita harus mendasarkan ini?** , pilih **Produk \| Pemformatan \| Format Warna Latar Belakang**.

    ![Gambar 114](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image36.png)

12. Klik **OK**.

    ![Gambar 115](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image37.png)

13. Ulangi langkah sebelumnya untuk mengonfigurasi pemformatan bersyarat warna font untuk bidang **Warna**, menggunakan bidang **Produk \| Pemformatan \| Format Warna Font**

    *Anda mungkin ingat bahwa latar belakang dan warna font berasal dari file **ColorFormats.csv** di lab **Mempersiapkan Data di Power BI Desktop**, lalu terintegrasi dengan kueri **Produk** di lab **Memuat Data di Power BI Desktop**.*

## <a name="exercise-4-add-bookmarks-and-buttons"></a>**Latihan 4: Menambahkan Bookmark dan Tombol**

Dalam latihan ini, Anda akan menyempurnakan halaman **Performa Saya** dengan tombol, yang memungkinkan pengguna laporan memilih jenis visual yang akan ditampilkan. Setelah Anda menyelesaikan desain, halaman akan terlihat seperti berikut:

![Gambar halaman 3 yang diperbarui, menampilkan dua tombol dan sekarang hanya dua visual.](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image38.png)

### <a name="task-1-add-bookmarks"></a>**Tugas 1: Menambahkan bookmark**

Dalam tugas ini Anda akan menambahkan dua bookmark, satu untuk menampilkan setiap visual penjualan/target bulanan.

1. Buka halaman **Performa Saya**.

2. Pada tab pita **Lihat**, dari dalam grup **Tampilkan Panel**, klik **Bookmark**.

    ![Gambar 118](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image39.png)

3. Pada tab pita **Lihat**, dari dalam grup **Tampilkan Panel**, klik **Pilihan**.

    ![Gambar 119](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image40.png)

4. Di panel **Pilihan**, di samping salah satu item **Penjualan dan Target berdasarkan Bulan**, untuk menyembunyikan visual, klik ikon mata.

    ![Gambar 120](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image41.png)

5. Di panel **Bookmark**, klik **Tambahkan**.

    ![Gambar 121](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image42.png)

6. Untuk mengganti nama bookmark, klik dua kali bookmark.

7. Jika bagan yang terlihat adalah bagan batang, ganti nama bookmark menjadi **Bagan Batang AKTIF**, jika tidak, ganti nama bookmark menjadi **Bagan Kolom AKTIF**.

8. Untuk mengedit bookmark, di panel **Bookmark**, arahkan kursor ke bookmark, klik elipsis, lalu pilih **Data**.

    ![Gambar 16](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image43.png)

    *Menonaktifkan opsi **Data** berarti bookmark tidak akan menggunakan status filter saat ini. Hal tersebut penting karena jika tidak, bookmark akan mengunci secara permanen filter yang saat ini diterapkan oleh pemotong **Tahun**.*

9. Untuk memperbarui bookmark, klik lagi elipsis, lalu pilih **Perbarui**.

    ![Gambar 18](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image44.png)

    *Di langkah berikutnya, Anda akan membuat dan mengonfigurasi bookmark kedua untuk menampilkan visual kedua.*

10. Di panel **Pilihan**, alihkan visibilitas dua item **Penjualan dan Target berdasarkan Bulan**.

    *Dengan kata lain, buat visual yang terlihat menjadi tersembunyi, dan buat visual yang tersembunyi menjadi terlihat.*

    ![Gambar 122](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image45.png)

11. Buat bookmark kedua, dan beri nama yang sesuai (baik **Bagan Kolom AKTIF** atau **Bagan Batang AKTIF).**

    ![Gambar 123](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image46.png)

12. Konfigurasikan bookmark kedua untuk mengabaikan filter (opsi **Data** nonaktif), dan perbarui bookmark.

13. Di panel **Pilihan**, untuk membuat kedua visual terlihat, cukup tampilkan visual yang tersembunyi.

14. Ubah kembali ukuran dan posisi dari kedua visual sehingga memenuhi halaman di bawah visual multi-kartu, dan benar-benar tumpang tindih satu sama lain.

    *Tips: Untuk memilih visual yang dicakup, pilih di panel **Pilihan**.*

    ![Gambar 124](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image47.png)

15. Di panel **Bookmark**, pilih setiap bookmark, dan perhatikan bahwa hanya satu visual yang terlihat.

    *Tahap desain berikutnya adalah menambahkan dua tombol ke halaman, yang memungkinkan pengguna laporan memilih bookmark.*

### <a name="task-2-add-buttons"></a>**Tugas 2: Menambahkan tombol**

Dalam tugas ini Anda akan menambahkan dua tombol, dan menetapkan tindakan bookmark untuk masing-masing tombol.

1. Pada pita **Sisipkan**, dari dalam grup **Elemen**, klik **Tombol**, lalu pilih **Kosong**.

    ![Gambar 125](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image48.png)

2. Menempatkan tombol tepat di bawah pemotong **Tahun**.

3. Pilih tombol, lalu di panel **tombol Format**, klik **Umum** dan ubah properti **Judul** menjadi **Aktif**.

    ![Gambar 126](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image49.png)

4. Luaskan bagian **Judul**, lalu di kotak **Teks**, masukkan **Bagan Batang**.

5. Luaskan bagian **Latar Belakang**, lalu atur warna latar belakang menggunakan warna pelengkap.

6. Klik **Tombol** dan ubah properti **Tindakan** menjadi **Aktif**.

    ![Gambar 127](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image50.png)

7. Luaskan bagian **Tindakan**, lalu atur daftar dropdown **Jenis** ke **Bookmark**.

8. Dalam daftar dropdown **Bookmark**, pilih **Diagram Batang AKTIF**.

    ![Gambar 128](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image51.png)

9. Buat salinan tombol dengan menggunakan salin dan tempel, lalu konfigurasikan tombol baru sebagai berikut:

    *Tips: Perintah pintasan untuk salin dan tempel adalah **Ctrl+C** diikuti oleh **Ctrl+V**.*

    - Atur properti **Teks Tombol** ke **Bagan Kolom**

    - Di bagian **Tindakan**, atur daftar dropdown **Bookmark** ke **Bagan Kolom AKTIF**

    *Desain laporan Analisis Penjualan kini telah selesai.*

### <a name="task-3-publish-the-report"></a>**Tugas 3: Menerbitkan laporan**

Dalam tugas ini Anda akan menerbitkan laporan.

1. Pilih halaman **Gambaran Umum**.

2. Di pemotong **Tahun**, pilih **FY2020**.

3. Di pemotong **Wilayah**, **Pilih Semua**.

4. Simpan file Power BI Desktop.

    *File harus selalu disimpan sebelum diterbitkan ke layanan Power BI.*

5. Pada tab pita **Beranda**, dari dalam grup **Bagikan**, klik **Terbitkan**.

    ![Gambar 21](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image52.png)

6. Di jendela **Terbitkan ke Power** BI, perhatikan bahwa **Ruang Kerja Saya** dipilih.

7. Untuk menerbitkan laporan, klik **Pilih**.

    ![Gambar 20](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image53.png)

8. Jika diminta untuk mengganti himpunan data, klik **Ganti**.

9. Ketika publikasi telah berhasil, klik **Mengerti**.

    ![Gambar 19](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image54.png)

10. Dapatkan Power BI Desktop.

    *Anda akan mempelajari laporan di layanan Power BI pada latihan berikutnya.*

## <a name="exercise-5-explore-the-report"></a>**Latihan 5: Menjelajahi Laporan**

Dalam latihan ini Anda akan menjelajahi laporan di layanan Power BI.

### <a name="task-1-explore-the-report"></a>**Tugas 1: Menjelajahi laporan**

Dalam tugas ini Anda akan menjelajahi laporan di layanan Power BI.

1. Di jendela browser Microsoft Edge, di layanan Power BI, di panel **Navigasi**, pilih **Ruang Kerja Saya**, lalu klik laporan **Analisis Penjualan**.

2. Untuk menguji laporan penelusuran, di halaman **Ringkasan**, dalam visual **Jumlah berdasarkan Kategori**, klik kanan bilah **Pakaian**, lalu pilih **Telusuri \| Detail Produk**.

    ![Gambar 130](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image55.png)

3. Perhatikan bahwa halaman **Detail Produk** adalah untuk **Pakaian**.

4. Untuk kembali ke halaman sumber, di pojok kiri atas halaman, klik tombol panah.

5. Pilih halaman **Performa Saya**.

6. Klik setiap tombol, dan kemudian perhatikan bahwa visual yang berbeda ditampilkan.

### <a name="task-2-finish-up"></a>**Tugas 2: Selesaikan**

Dalam tugas ini Anda akan menyelesaikan lab.

1. Untuk kembali ke ruang kerja Anda, pada spanduk di halaman web jendela, klik **Ruang Kerja Saya**.

    ![Gambar 23](Linked_image_Files/08-design-report-in-power-bi-desktop-enhanced_image56.png)

2. Biarkan jendela browser Microsoft Edge terbuka.
