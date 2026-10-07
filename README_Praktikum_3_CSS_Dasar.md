# Praktikum 3 - CSS Dasar

## Identitas
- Nama: **[Isi Nama]**
- NIM: **[Isi NIM]**
- Kelas: **[Isi Kelas]**
- Mata Kuliah: **Pemrograman Web**

## Tujuan Praktikum
Praktikum ini bertujuan untuk memahami konsep dasar CSS, aturan penulisan CSS, penggunaan selector, serta penerapan CSS pada dokumen HTML. CSS digunakan untuk mengatur tampilan halaman web agar lebih terstruktur dan menarik.

---

# Langkah-Langkah Praktikum

## 1. Membuat Dokumen HTML

Pertama, membuat file baru dengan nama:

```text
lab3_css_dasar.html
```

Kemudian membuat struktur dasar HTML dan menambahkan bagian `header`, `nav`, `div` dengan ID `intro`, heading, paragraf, dan link.

Contoh kode:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
</head>
<body>

<header>
    <h1>CSS Internal dan <i>Inline CSS</i></h1>
</header>

<nav>
    <a href="lab3_css_dasar.html">CSS Dasar</a>
    <a href="lab3_css_eksternal.html">CSS Eksternal</a>
    <a href="lab1_tag_dasar.html">HTML Dasar</a>
</nav>

<div id="intro">
    <h1>Hello World</h1>
    <p>
        Kami sedang belajar HTML dan CSS dasar, pada mata kuliah
        <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>.
    </p>

    <a class="button btn-primary" href="#intro">
        Informasi selengkapnya.
    </a>
</div>

</body>
</html>
```

### Hasil
Dokumen HTML berhasil dibuat dan dapat dibuka melalui browser.

![Screenshot langkah 1](screenshots/01-html-dasar.png)

---

## 2. Menambahkan CSS Internal

CSS internal ditambahkan pada bagian `<head>` menggunakan tag `<style>`.

Kode CSS:

```html
<style>
    body {
        font-family: 'Open Sans', sans-serif;
    }

    header {
        min-height: 80px;
        border-bottom: 1px solid #77CCEF;
    }

    h1 {
        font-size: 24px;
        color: #0F189F;
        text-align: center;
        padding: 20px 10px;
    }

    h1 i {
        color: #6d6a6b;
    }
</style>
```

### Penjelasan
CSS internal digunakan untuk mengatur tampilan HTML dari dalam file HTML yang sama. Pada praktikum ini, CSS digunakan untuk mengatur jenis font, ukuran heading, warna, posisi teks, padding, dan garis bawah header.

### Hasil

![Screenshot langkah 2](screenshots/02-css-internal.png)

---

## 3. Menambahkan Inline CSS

Selanjutnya ditambahkan CSS secara langsung pada elemen HTML menggunakan atribut `style`.

Contoh:

```html
<p style="text-align: center; color: #ccd8e4;">
    Kami sedang belajar HTML dan CSS dasar.
</p>
```

### Penjelasan
Inline CSS ditulis langsung pada tag HTML dan hanya memengaruhi elemen tempat CSS tersebut ditulis.

### Hasil

![Screenshot langkah 3](screenshots/03-inline-css.png)

---

## 4. Membuat CSS Eksternal

Selanjutnya dibuat file baru dengan nama:

```text
style_eksternal.css
```

CSS eksternal ditulis terpisah dari file HTML.

Contoh:

```css
nav {
    background: #20A759;
    color: #fff;
    padding: 10px;
}

nav a {
    color: #fff;
    text-decoration: none;
    padding: 10px 20px;
}

nav .active,
nav a:hover {
    background: #0B6B3A;
}
```

Kemudian file CSS dihubungkan dengan HTML menggunakan:

```html
<link rel="stylesheet" href="style_eksternal.css" type="text/css">
```

### Penjelasan
CSS eksternal membuat aturan CSS berada pada file terpisah sehingga dapat digunakan untuk mengatur halaman HTML dengan lebih terstruktur.

### Hasil

![Screenshot langkah 4](screenshots/04-css-eksternal.png)

---

## 5. Menambahkan CSS Selector ID dan Class

Selanjutnya ditambahkan selector ID dan Class pada file `style_eksternal.css`.

### ID Selector

```css
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}

#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}
```

### Class Selector

```css
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
}

.btn-primary {
    background: #E42A42;
}
```

### Penjelasan
Selector ID menggunakan tanda `#` dan digunakan untuk memilih elemen berdasarkan ID. Selector Class menggunakan tanda `.` dan digunakan untuk memilih elemen berdasarkan class.

Pada HTML terdapat:

```html
<div id="intro">
```

dan:

```html
<a class="button btn-primary" href="#intro">
    Informasi selengkapnya.
</a>
```

### Hasil

![Screenshot langkah 5](screenshots/05-selector-id-class.png)

---

# Pertanyaan dan Tugas

## 1. Eksperimen Mengubah dan Menambah Properti CSS

Eksperimen dilakukan dengan mengubah dan menambahkan beberapa properti CSS. Contohnya:

```css
h1 {
    font-size: 30px;
    color: blue;
    text-align: center;
    background-color: lightgray;
    padding: 10px;
}

p {
    color: black;
    font-size: 18px;
    line-height: 1.5;
    font-family: Arial, sans-serif;
}
```

Properti yang ditambahkan antara lain `font-size`, `color`, `text-align`, `background-color`, `padding`, `line-height`, dan `font-family`. Perubahan tersebut memengaruhi ukuran, warna, posisi, latar belakang, jarak, dan jenis tulisan pada halaman web.

### Screenshot Eksperimen

![Screenshot eksperimen CSS](screenshots/06-eksperimen-css.png)

---

## 2. Perbedaan `h1 {...}` dengan `#intro h1 {...}`

`h1 {...}` merupakan selector elemen yang berlaku untuk semua elemen `<h1>` pada halaman.

Contoh:

```css
h1 {
    color: blue;
}
```

Sedangkan:

```css
#intro h1 {
    color: red;
}
```

hanya berlaku untuk elemen `<h1>` yang berada di dalam elemen yang memiliki ID `intro`.

Contoh HTML:

```html
<div id="intro">
    <h1>Hello World</h1>
</div>

<h1>Judul Lain</h1>
```

Dengan CSS tersebut, `<h1>` di dalam `#intro` akan berwarna merah, sedangkan `<h1>` lainnya berwarna biru.

Jadi, `#intro h1` lebih spesifik karena memilih `<h1>` berdasarkan ID `intro`.

---

## 3. CSS Internal, Eksternal, dan Inline

Jika terdapat CSS internal, eksternal, dan inline yang mengatur elemen serta properti yang sama, maka **inline CSS memiliki prioritas lebih tinggi** daripada CSS internal atau eksternal apabila tingkat spesifikasinya sama.

Contoh CSS eksternal:

```css
p {
    color: blue;
}
```

CSS internal:

```html
<style>
    p {
        color: green;
    }
</style>
```

Inline CSS:

```html
<p style="color: red;">
    Halo Dunia
</p>
```

Hasil yang ditampilkan pada browser adalah **warna merah**, karena aturan inline diterapkan langsung pada elemen tersebut.

Secara sederhana:

```text
Inline CSS > Internal/External CSS
```

Untuk internal dan eksternal yang memiliki tingkat specificity sama, aturan yang ditulis paling akhir dapat menjadi aturan yang digunakan.

---

## 4. Perbedaan Prioritas ID dan Class

Misalnya terdapat elemen:

```html
<p id="paragraf-1" class="text paragraf">
    Ini adalah paragraf.
</p>
```

Kemudian terdapat CSS:

```css
.text {
    color: blue;
}

#paragraf-1 {
    color: red;
}
```

Hasilnya teks akan berwarna **merah**.

Hal tersebut terjadi karena selector ID memiliki specificity yang lebih tinggi daripada selector Class.

Urutan sederhananya:

```text
ID > Class > Element
```

Jadi pada elemen:

```html
<p id="paragraf-1" class="text paragraf">
```

selector:

```css
#paragraf-1
```

lebih kuat daripada:

```css
.text
```

atau:

```css
.paragraf
```

---

# Validasi CSS

Dokumen CSS dapat divalidasi menggunakan CSS Validator dari W3C untuk mengetahui apakah penulisan CSS sudah sesuai aturan.

![Screenshot validasi CSS](screenshots/07-validasi-css.png)

---

# Kesimpulan

Dari praktikum CSS Dasar ini dapat dipahami bahwa CSS digunakan untuk mengatur tampilan halaman web. CSS dapat ditulis menggunakan tiga cara, yaitu **internal, eksternal, dan inline**. Selain itu, CSS memiliki beberapa selector seperti **element selector, class selector, dan ID selector**.

Element selector berlaku pada elemen HTML tertentu, class selector menggunakan tanda `.`, sedangkan ID selector menggunakan tanda `#`. ID memiliki tingkat specificity yang lebih tinggi daripada class. Dengan CSS, tampilan halaman HTML dapat diatur mulai dari warna, ukuran tulisan, posisi, background, jarak, hingga tampilan navigasi.

---

# Struktur Repository

Contoh struktur repository:

```text
Lab3Web/
│
├── lab3_css_dasar.html
├── style_eksternal.css
├── README.md
└── screenshots/
    ├── 01-html-dasar.png
    ├── 02-css-internal.png
    ├── 03-inline-css.png
    ├── 04-css-eksternal.png
    ├── 05-selector-id-class.png
    ├── 06-eksperimen-css.png
    └── 07-validasi-css.png
```

---

# Commit dan Repository

Setelah semua latihan selesai dan screenshot dimasukkan, lakukan commit dan push ke repository GitHub.

Contoh perintah:

```bash
git add .
git commit -m "Menyelesaikan Praktikum 3 CSS Dasar"
git push -u origin main
```

Nama repository:

```text
Lab3Web
```

URL repository:

```text
[Masukkan URL repository GitHub di sini]
```

Setelah itu, URL repository dikirimkan melalui e-learning eCampus.
