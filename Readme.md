<h1><img width="200px" alt="Sass" src="https://rawgit.com/sass/sass-site/main/source/assets/img/logos/logo.svg" /></h1>

[![@SassCSS on Twitter](https://img.shields.io/twitter/follow/SassCSS?label=%40SassCSS&style=social)](https://twitter.com/SassCSS)
&nbsp;&nbsp;
[![stackoverflow](https://img.shields.io/stackexchange/stackoverflow/t/sass?label=Sass%20questions&logo=stackoverflow&style=social)](https://stackoverflow.com/questions/tagged/sass)
&nbsp;&nbsp;
[![Gitter](https://img.shields.io/gitter/room/sass/sass?label=chat&logo=gitter&style=social)](https://gitter.im/sass/sass?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

**Sass membuat CSS menyenangkan kembali**. Sass adalah ekstensi CSS yang menambahkan aturan bersarang,
variabel, mixin, pewarisan selektor, dan banyak lagi. Sass diterjemahkan ke dalam
CSS standar yang diformat dengan baik menggunakan alat baris perintah atau plugin untuk
sistem pengembangan Anda.

```scss
$font-stack: Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;

  color: $primary-color;
}

@mixin border-radius($radius) {
  -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
      -ms-border-radius: $radius;
          border-radius: $radius;
}

nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { @include border-radius(10px); }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

## Install Sass
Anda dapat menginstal Sass di Windows, Mac, atau Linux dengan mengunduh paket untuk
sistem operasi Anda [dari GitHub] dan [menambahkannya ke `PATH`][PATH] Anda. Itu saja—tidak ada dependensi eksternal dan tidak ada lagi yang perlu Anda instal.
[from GitHub]: https://github.com/sass/dart-sass/releases
[PATH]: https://katiek2.github.io/path-doc/
Jika Anda menggunakan Node.js, Anda juga dapat menginstal Sass menggunakan [npm] dengan menjalankan

[npm]: https://www.npmjs.com/

```
npm install -g sass
```

**Namun, perlu diketahui** bahwa ini akan menginstal implementasi JavaScript murni
dari Sass, yang berjalan agak lebih lambat daripada opsi lain yang tercantum
di sini. Namun, antarmukanya sama, jadi akan mudah untuk mengganti implementasi lain
nanti jika Anda membutuhkan kecepatan lebih!

Lihat [situs web Sass](https://sass-lang.com/install) untuk cara lain menginstal
Sass.

Setelah Sass terinstal, Anda dapat menjalankan file `sass` untuk mengompilasi
file `.sass` dan `.scss` menjadi file `.css`. Misalnya:

```
sass source/stylesheets/index.scss build/stylesheets/index.css
```

## Pelajari Sass

Kunjungi [situs web Sass](https://sass-lang.com/guide) untuk panduan tentang cara
mempelajari Sass!

## Lisensi

Jika Anda ingin mengkloning proyek ini, pastikan lisensi dan izin telah diberikan oleh pembuatnya. Silakan hubungi davin.gm.etc@gmail.com Proyek ini berada di bawah naungan (Etc.). Semua hak dan kebijakan privasi akan ditindaklanjuti oleh perusahaan.