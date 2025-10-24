
---

## 1. Apa Itu Sass?

**Sass** (singkatan dari **S**yntactically **A**wesome **S**tyle **Sheets**) adalah sebuah **Pre-prosesor CSS**.

* **Pre-prosesor** artinya Sass adalah "bahasa" yang akan diolah atau "dimasak" terlebih dahulu sebelum menjadi CSS.
* **Cara Kerjanya:** Anda menulis kode dalam format Sass (biasanya ekstensi **`.scss`**), lalu menggunakan alat khusus (disebut **Kompiler/Processor**) untuk mengubahnya menjadi file **CSS murni** (`.css`). Hanya file CSS murni inilah yang dapat dibaca dan diterapkan oleh *browser*.

## 2. Bedanya Sass dengan CSS Biasa

Perbedaan utamanya adalah Sass memiliki **fitur-fitur tambahan** yang tidak dimiliki oleh CSS, membuat penulisan *styling* lebih efisien, terstruktur, dan bersih.

| Fitur Utama | CSS Biasa | Sass (SCSS) |
| :--- | :--- | :--- |
| **Variabel** | ❌ Tidak ada (harus mengetik nilai berulang) | ✅ Ada, ditandai dengan `$` (misal: `$warna-utama: blue;`) |
| **Nesting** | ❌ Tidak bisa menulis selector bersarang | ✅ Bisa menulis selector bersarang, meniru struktur HTML |
| **Mixins** | ❌ Tidak ada | ✅ Ada, seperti *function* untuk menyimpan blok kode yang bisa dipanggil berulang |
| **Fungsi Logika** | ❌ Tidak ada | ✅ Ada, seperti *if/else* atau *loop* (perulangan) |

## 3. Analogi Paling Sederhana Sass

Anggaplah CSS itu seperti: **Membuat kue dari nol tanpa cetakan dan resep.**

* Setiap kali ingin membuat kue baru dengan warna yang sama, Anda harus mengukur dan mencampur semua bahannya dari awal lagi.
* Jika warna kue utama diubah, Anda harus mencari dan mengganti warna di semua resep kue Anda satu per satu.

Sedangkan **Sass** itu seperti: **Menggunakan *Mixer*, *Cetakan Khusus*, dan *Buku Resep* yang canggih.**

* Anda bisa menyimpan warna atau ukuran favorit Anda sebagai **Variabel** (bahan baku di *stock*).
* Anda bisa menggunakan **Mixins** (cetakan khusus) untuk membuat blok kode *styling* yang kompleks dan memanggilnya hanya dengan satu baris.
* Semua "resep" (file SCSS) akan digabungkan dan diolah otomatis menjadi satu hasil akhir (file CSS murni) yang disajikan ke *browser*.

Intinya: Sass membantu Anda **menulis kode lebih cepat, lebih rapi, dan lebih mudah diubah**.

---

## Perbandingan Kelebihan dan Kekurangan

### 4. Kelebihan Sass

1.  **Menghemat Waktu dengan Variabel:** Anda dapat menyimpan nilai (misalnya kode warna, *font size*, dll.) di satu tempat, sehingga jika perlu diubah, cukup ubah satu kali.
2.  **Kode Lebih Rapi (Nesting):** Memungkinkan Anda menulis selector CSS bersarang (seperti di HTML), membuat struktur kode lebih mudah dibaca dan dikelola.
3.  **Dapat Digunakan Kembali (Mixins/Extend):** Anda dapat membuat blok kode *styling* yang kompleks dan memanggilnya di mana saja tanpa perlu mengetik ulang propertinya.
4.  **Organisasi File Baik (Partial):** Memungkinkan Anda membagi *styling* proyek besar ke dalam file-file kecil (`_header.scss`, `_footer.scss`, dll.) yang terpisah dan terorganisir.

### 5. Kekurangan Sass

1.  **Perlu Proses Kompilasi:** Tidak bisa langsung dipakai oleh *browser*. Anda harus menginstal dan menjalankan *pre-processor* (kompiler) untuk mengubahnya menjadi file CSS. Ini menambah satu langkah dalam alur kerja.
2.  **Kompleksitas di Awal:** Untuk pemula, mempelajari fitur-fitur tambahan seperti *mixins*, *functions*, dan *control flow* bisa sedikit membingungkan pada awalnya.
3.  **Potensi CSS *Bloat*:** Jika *nesting* atau *extend* digunakan secara berlebihan dan tidak hati-hati, hasil kompilasi CSS-nya bisa menjadi sangat besar (banyak kode berulang) dan kurang efisien.

### 6. Kelebihan CSS Biasa

1.  **Universal:** Merupakan bahasa dasar *styling* web yang sudah dipahami oleh semua *browser*.
2.  **Tidak Perlu Kompilasi:** Anda bisa langsung menggunakannya di HTML tanpa memerlukan alat pihak ketiga (kompiler) atau proses tambahan.
3.  **Sederhana:** Untuk proyek yang sangat kecil dan sederhana, CSS murni lebih cepat untuk diimplementasikan tanpa *overhead* (proses ekstra) Sass.

### 7. Kekurangan CSS Biasa

1.  **Pengulangan Kode (Repetitif):** Tidak ada variabel, sehingga Anda harus mengetik ulang nilai (seperti kode warna) di banyak tempat.
2.  **Skalabilitas Buruk:** Sulit diatur untuk proyek besar. File CSS bisa menjadi sangat panjang, sulit dicari, dan rentan terhadap kesalahan (*bug*) karena kode berulang.
3.  **Kurang Logis:** Tidak memiliki fitur logika seperti *if/else* atau *loop* yang ada pada bahasa pemrograman.

---

## 8. Apakah Sass Framework atau Library?

Sass **BUKAN** *Framework* atau *Library*.

Sass adalah **CSS Pre-processor** (Pra-prosesor CSS).

* **Framework** (contoh: Bootstrap) menyediakan kode CSS yang sudah jadi dan siap pakai.
* **Library** (contoh: jQuery) menyediakan fungsi yang Anda panggil di kode Anda.
* **Pre-processor** (Sass) menyediakan **bahasa/sintaks** yang lebih canggih untuk **menulis** CSS. Setelah Anda menulisnya, bahasa tersebut akan diubah menjadi CSS murni yang digunakan oleh *browser*.
