---
lab:
  title: Terapkan Keamanan Tingkat Baris
  module: Module 12 - Row-Level Security
ms.openlocfilehash: f47cc7c54428589aaa9d6b37afd9ee4d11c5884e
ms.sourcegitcommit: 9ea1e7e21b9b3c718030c94b1693d153a2010ec7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/29/2022
ms.locfileid: "146650108"
---
# <a name="enforce-row-level-security"></a>**Menerapkan Keamanan Tingkat Baris**

**Perkiraan waktu untuk menyelesaikan lab adalah 45 menit**

Di lab ini, Anda akan menerapkan keamanan tingkat baris untuk memastikan bahwa staf penjualan hanya dapat menganalisis data penjualan untuk wilayah yang ditetapkan untuk mereka.

Di lab ini Anda mempelajari cara:


- Menerapkan keamanan tingkat baris

### <a name="lab-story"></a>**Cerita lab**

Lab ini adalah salah satu dari sekian banyak lab yang dirancang sebagai cerita lengkap, mulai dari persiapan data hingga publikasi sebagai laporan dan dasbor. Anda dapat menyelesaikan lab dalam urutan apa pun. Namun, jika Anda ingin mengerjakan beberapa lab sekaligus, sebaiknya Anda mengerjakannya dengan urutan berikut:

1. Mempersiapkan Data di Power BI Desktop

2. Muat Data di Power BI Desktop

3. Data Model di Power BI Desktop

5. Membuat Perhitungan DAX di Power BI Desktop, Bagian 1

6. Membuat Perhitungan DAX di Power BI Desktop, Bagian 2

7. Merancang Laporan di Power BI Desktop, Bagian 1

8. Merancang Laporan di Power BI Desktop, Bagian 2

9. Buat Dasbor Power BI

10. Menganalisis Data di Power BI Desktop

11. **Menerapkan Keamanan Tingkat Baris**

## <a name="exercise-1-enforce-row-level-security"></a>**Latihan 1: Menerapkan keamanan tingkat baris**

Dalam latihan ini, Anda akan menerapkan keamanan tingkat baris untuk memastikan staf penjualan hanya dapat melihat penjualan yang dilakukan di wilayah yang ditetapkan untuk mereka.

### <a name="task-1-get-started"></a>**Tugas 1: Mulai**

Dalam tugas ini Anda akan menyiapkan lingkungan untuk lab.

*Penting: Jika Anda melanjutkan dari lab sebelumnya (dan Anda berhasil menyelesaikan lab tersebut), jangan selesaikan tugas ini; sebagai gantinya, lanjutkan dari tugas berikutnya.*

1. Untuk membuka Power BI Desktop, pada taskbar, klik pintasan Microsoft Power BI Desktop.

    ![Gambar 8](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image1.png)

1. Untuk menutup jendela memulai, di kiri atas jendela, klik **X**.

    ![Gambar 7](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image2.png)

1. Untuk membuka file Power BI Desktop pertama, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Buka Laporan**.

    ![Gambar 6](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image3.png)

1. Klik **Jelajahi Laporan**.

    ![Gambar 5](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image4.png)

1. Di jendela **Buka**, navigasikan ke folder **D:\PL300\Labs\10-row-level-security\Starter**.

1. Pilih file **Analisis Penjualan**.

1. Klik **Buka**.

    ![Gambar 4](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image5.png)

1. Tutup semua jendela informasi yang mungkin terbuka.

1. Untuk membuat salinan file, klik tab pita **File** untuk membuka tampilan backstage.

1. Pilih **Simpan**.

    ![Gambar 3](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image6.png)

1. Jika diminta untuk menerapkan perubahan, klik **Terapkan**.

    ![Gambar 15](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image7.png)

1. Di jendela **Simpan Sebagai**, navigasikan ke folder **D:\PL300\MySolution**.

1. Klik **Simpan**.

    ![Gambar 2](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image8.png)

### <a name="task-2-enforce-row-level-security"></a>**Tugas 2: Menerapkan keamanan tingkat baris**

Dalam tugas ini, Anda akan menerapkan keamanan tingkat baris untuk memastikan staf penjualan hanya dapat melihat penjualan yang dilakukan di wilayah yang ditetapkan untuk mereka.

1. Beralih ke tampilan Data.

    ![Gambar 5701](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image20.png)

2. Di panel **Bidang**, pilih tabel **Penjual (Performa)** .

3. Tinjau data, perhatikan bahwa Michael Blythe (EmployeeKey 281) memiliki nilai UPN: **michael-blythe@adventureworks.com**

    *Ingatlah bahwa Michael Blythe ditugaskan ke tiga wilayah penjualan: Timur Laut AS, US Tengah, dan Tenggara AS.*

4. Beralih ke tampilan Laporan.

5. Pada tab pita **Pemodelan**, dari dalam grup **Keamanan**, klik **Kelola Peran**.

    ![Gambar 5700](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image21.png)

6. Di jendela **Kelola Peran**, klik **Buat**.

    ![Gambar 5702](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image22.png)

7. Di dalam kotak, ganti teks yang dipilih dengan nama peran: **Penjual**, lalu tekan **Enter**.

    ![Gambar 5703](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image23.png)

8. Untuk menetapkan filter, untuk tabel **Penjual (Performa)** , klik karakter elipsis (…), lalu pilih **Tambahkan Filter \| [UPN]** .

    ![Gambar 5704](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image24.png)

9. Di kotak **Ekspresi DAX Filter Tabel**, ubah ekspresi dengan mengganti **“Value”** dengan **USERPRINCIPALNAME()** .

    ![Gambar 11](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image25.png)

    *USERPRINCIPALNAME() adalah fungsi Data Analysis Expressions (DAX) yang mengembalikan nama pengguna yang diautentikasi. Artinya tabel **Penjual (Performa)** akan memfilter berdasarkan Nama Prinsipal Pengguna (UPN) dari pengguna yang mengkueri model.*

10. Klik **Simpan**.

    ![Gambar 5706](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image26.png)

11. Untuk menguji peran keamanan, pada tab pita **Pemodelan**, dari dalam grup **Keamanan**, klik **Lihat Sebagai**.

    ![Gambar 5708](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image27.png)

12. Di jendela **Lihat sebagai Peran**, centang item **Pengguna Lain**, lalu di kotak yang sesuai, masukkan: **michael-blythe@adventureworks.com**

13. Periksa peran **Penjual**.

    ![Gambar 5709](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image28.png)

    *Konfigurasi ini menghasilkan penggunaan peran **Penjual** dan meniru pengguna dengan nama Michael Blythe Anda.*

14. Klik **OK**.

    ![Gambar 5710](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image29.png)

15. Perhatikan spanduk kuning di atas halaman laporan, yang menjelaskan konteks keamanan pengujian.

    ![Gambar 13](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image30.png)

16. Dalam visual tabel, perhatikan bahwa hanya penjual **Michael Blythe** yang terdaftar.

    ![Gambar 5713](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image31.png)

17. Untuk menghentikan pengujian, di sisi kanan spanduk kuning, klik **Berhenti Menampilkan**.

    ![Gambar 5712](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image32.png)

    *Saat file Power BI Desktop diterbitkan ke layanan Power BI, Anda harus menyelesaikan tugas pasca penerbitan untuk memetakan prinsip keamanan ke peran **Penjual**. Anda tidak akan melakukannya di lab ini.*

18. Untuk menghapus peran, pada tab pita **Pemodelan**, dari dalam grup **Keamanan**, klik **Kelola Peran**.

    ![Gambar 16](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image33.png)

19. Di jendela **Kelola Peran**, klik **Hapus**.

    ![Gambar 17](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image34.png)

20. Saat diminta untuk mengonfirmasi penghapusan, klik **Ya, Hapus**.

21. Klik **Simpan**.

    ![Gambar 18](Linked_image_Files/04-configure-data-model-in-power-bi-desktop-advanced_image35.png)

### <a name="task-3-finish-up"></a>**Tugas 3: Selesaikan**

Dalam tugas ini Anda akan menyelesaikan lab.

1. Simpan file Power BI Desktop.
