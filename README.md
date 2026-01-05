# 📘 Modul 2: Selector CSS

**🎯 Tujuan Pembelajaran**
Setelah pertemuan ini, peserta mampu:

- Memahami fungsi selector dalam CSS
- Menggunakan berbagai jenis selector dengan tepat
- Menerapkan selector CSS untuk styling halaman biodata

## 1️⃣ Apa Itu Selector CSS?

**Selector CSS** adalah cara untuk **memilih elemen HTML** yang ingin diberi gaya (style).

📌 Selector menentukan **elemen mana** yang akan dipengaruhi oleh aturan CSS.

## 2️⃣ Element Selector

Digunakan untuk memilih **elemen HTML berdasarkan nama tag**.

```css
p {
  color: black;
  font-size: 16px;
}
```

📌 Selector ini akan mempengaruhi **semua** `<p>` di halaman.

## 3️⃣ Class Selector

Digunakan untuk memilih elemen berdasarkan **atribut class**.
**HTML:**

```html
<p class="title">Biodata Saya</p>
```

**CSS**

```css
.title {
  color: blue;
  font-weight: bold;
}
```

📌 Class bisa digunakan **lebih dari satu kali**.

## 4️⃣ ID Selector

Digunakan untuk memilih elemen dengan **id unik**.
**HTML:**

```html
<h1 id="header">Profil</h1>
```

**CSS:**

```css
#header {
  background-color: lightgray;
  padding: 10px;
}
```

📌 ID hanya boleh digunakan **satu kali dalam satu halaman**.

## 5️⃣ Group Selector

Digunakan untuk memberi style yang sama ke **beberapa selector sekaligus**.

**Contoh:**

```css
h1,
h2,
p {
  font-family: Arial;
}
```

📌 Menghemat kode dan meningkatkan konsistensi desain.

## 6️⃣ Universal Selector

Digunakan untuk memilih **semua elemen HTML**.
**Contoh:**

```css
* {
  margin: 0;
  padding: 0;
}
```

📌 Umumnya digunakan untuk **reset CSS**.

## 🧪 Praktik: Styling Halaman Biodata

**🎯 Tujuan Praktik**
Menggunakan berbagai selector CSS untuk mempercantik halaman biodata.

### 1️⃣ Struktur File

- biodata
  - index.html
  - style.css

### 2️⃣ Kode HTML (`index.html`)

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <title>Biodata</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1 id="header">Biodata Mahasiswa</h1>

    <p class="title">Informasi Pribadi</p>

    <ul>
      <li>Nama: Andi</li>
      <li>Umur: 22 Tahun</li>
      <li>Hobi: Coding</li>
    </ul>

    <p>Terima kasih telah mengunjungi halaman biodata.</p>
  </body>
</html>
```

### 3️⃣ Kode CSS (`style.css`)

```css
/* Universal Selector */
* {
  font-family: Arial, sans-serif;
}

/* ID Selector */
#header {
  background-color: #f2f2f2;
  padding: 15px;
  text-align: center;
}

/* Class Selector */
.title {
  color: darkblue;
  font-size: 18px;
}

/* Element Selector */
p {
  color: #333;
}

/* Group Selector */
li,
p {
  line-height: 1.6;
}
```
