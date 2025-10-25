Cara penulisan selector di SCSS (Sass) pada dasarnya **sama dengan CSS standar**, tetapi diperkaya dengan fitur **Nesting** dan penggunaan simbol **Ampersand ($\&$)** yang membuatnya lebih terstruktur dan efisien.

-----

## 1\. Selektor Dasar (Sama dengan CSS)

Anda tetap menggunakan semua jenis selektor yang ada di CSS, seperti:

| Tipe Selektor | Sintaks SCSS/CSS | Keterangan |
| :--- | :--- | :--- |
| **Element** | `h1 { ... }` | Menargetkan semua elemen `<h1>`. |
| **Class** | `.header { ... }` | Menargetkan elemen dengan atribut `class="header"`. |
| **ID** | `\#main { ... }` | Menargetkan elemen dengan atribut `id="main"`. |
| **Attribute** | `input[type="text"] { ... }` | Menargetkan elemen berdasarkan atributnya. |

## 2\. Nesting (Sarang)

Ini adalah fitur utama yang membedakan penulisan selektor di SCSS. Anda menempatkan selektor anak (child) di dalam blok kurung kurawal $(\{\})$ selektor induk (parent).

### Contoh Nesting

```scss
/* SCSS */
.nav { // Selektor Induk
  list-style: none;

  ul { // Selektor Anak (akan menjadi .nav ul)
    padding: 0;
    
    li { // Selektor Cucu (akan menjadi .nav ul li)
      display: inline-block;
      
      a { // Selektor Buyut (akan menjadi .nav ul li a)
        text-decoration: none;
        color: black;
      }
    }
  }
}
```

**Hasil Compile ke CSS:**

```css
.nav {
  list-style: none;
}

.nav ul {
  padding: 0;
}

.nav ul li {
  display: inline-block;
}

.nav ul li a {
  text-decoration: none;
  color: black;
}
```

-----

## 3\. Penggunaan Ampersand ($\&$)

Simbol $\&$ mewakili **selektor induk** saat ini. Ini sangat penting untuk menargetkan:

### A. Pseudo-class/Pseudo-element

Digunakan untuk menargetkan status atau bagian dari elemen induk tanpa membuat selektor yang panjang.

```scss
.button {
  background-color: blue;
  
  // Menjadi: .button:hover
  &:hover { 
    background-color: darkblue;
  }
  
  // Menjadi: .button::before
  &::before {
    content: "🚀";
  }
}
```

### B. Selektor Turunan yang Berdekatan (Modifier Class)

Berguna untuk membuat kelas modifikasi yang terkait erat dengan kelas induk (sering digunakan dalam metodologi seperti BEM - Block Element Modifier).

```scss
.card {
  border: 1px solid gray;
  padding: 15px;

  // Menjadi: .card--large
  &--large {
    font-size: 1.5em;
  }

  // Menjadi: .card__title
  &__title {
    margin-top: 0;
  }
}
```

### C. Kombinator

Anda dapat menggunakan $\&$ dengan kombinator seperti `+` (adjacent sibling), `~` (general sibling), atau `>` (child selector).

```scss
.item {
  margin-bottom: 10px;

  // Menjadi: .item + .item (menargetkan .item yang didahului oleh .item)
  & + & { 
    border-top: 1px solid #ccc;
  }

  // Menjadi: .item > span (menargetkan elemen <span> anak langsung)
  & > span {
    font-weight: bold;
  }
}
```

Dengan fitur-fitur ini, penulisan selektor di SCSS menjadi jauh lebih rapi, terstruktur, dan mudah dikelola dibandingkan dengan CSS biasa.