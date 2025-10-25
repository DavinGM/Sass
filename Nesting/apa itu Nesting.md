Nesting dalam SCSS (`Sassy CSS`) atau Sass (`Syntactically Awesome Style Sheets`) adalah fitur yang memungkinkan Anda menempatkan (menyimpan) selektor CSS di dalam selektor lain. Ini mencerminkan struktur hierarki (parent-child) dari elemen HTML Anda dan membantu menjaga kode stylesheet tetap terorganisir, lebih mudah dibaca, dan dikelola.

Secara Garis tradisonal Css 
```css
/* CSS Tradisional */
nav {
  background-color: #333;
}

nav ul {
  list-style: none;
}

nav ul li a {
  color: white;
}
```

dengan Nesting di Scss/Sass Kode di atas bisa kita tulis cukup sederhana menjadi :
```scss
/* SCSS dengan Nesting */
nav {
  background-color: #333;

  ul { // Selector 'ul' di-nesting di dalam 'nav'
    list-style: none;

    li { // Selector 'li' di-nesting di dalam 'ul'
      
      a { // Selector 'a' di-nesting di dalam 'li'
        color: white;
      }
    }
  }
}
```


**Keuntungan Utama Nesting**

Keterbacaan yang Lebih Baik: Struktur CSS/SCSS Anda terlihat mirip dengan struktur HTML Anda, memudahkan Anda melacak aturan mana yang berlaku untuk elemen mana.

Mengurangi Pengulangan: Anda tidak perlu mengulang selektor induk (misalnya, `nav`) berulang kali.

Kemudahan Pemeliharaan: Ketika Anda mengubah nama kelas atau ID, Anda hanya perlu melakukannya di satu tempat (selektor induk), dan semua selektor anak (nested) akan diperbarui secara implisit.

**Simbol Ampersand (`&`)**

Fitur penting dalam nesting adalah simbol ampersand (`&`). Simbol ini mewakili selektor induk yang sedang Anda kerjakan. Ini sering digunakan untuk:

**Pseudo-class/element**: Menambahkan pseudo-class seperti :`hover`, `:focus`, atau pseudo-element seperti `::before` langsung ke selektor induk.

**Selektor Turunan** (Modified Classes): Membuat kelas yang terkait erat dengan selektor induk (misalnya, mengikuti metodologi BEM).

Contoh penggunaan `&`:
```scss
.button {
  padding: 10px 20px;
  border: 1px solid blue;
  
  // Menggunakan & untuk pseudo-class :hover
  &:hover { 
    background-color: lightblue; // Menjadi: .button:hover
  }
  
  // Menggunakan & untuk kelas modifier
  &--disabled { 
    opacity: 0.5; // Menjadi: .button--disabled
  }
}
```
Ketika Di compile Ke Css, Kode Scss tadi akan menjadi
```css
.button {
  padding: 10px 20px;
  border: 1px solid blue;
}

.button:hover {
  background-color: lightblue;
}

.button--disabled {
  opacity: 0.5;
}
```

Catatan Penting tapi **Jangan Berlebihan!**
Meskipun nesting sangat berguna, **terlalu banyak nesting** (misalnya, lebih dari 3 atau 4 tingkat kedalaman) dapat:

Menghasilkan CSS yang Sangat Spesifik (Specific): Ini membuat sulit untuk menimpa (override) gaya di tempat lain.

Membuat Kode Sulit Dibaca: Jika terlalu dalam, manfaat keterbacaan justru hilang.

Praktik terbaik menganjurkan nesting hanya seperlunya untuk menjaga kode tetap rapi dan flat (datar) sebisa mungkin