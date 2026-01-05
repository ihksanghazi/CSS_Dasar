# 📘 Modul 3: Warna, Font, dan Text Styling

**🎯 Tujuan Pembelajaran**
Setelah pertemuan ini, peserta mampu:

- Mengatur warna teks menggunakan CSS
- Mengubah jenis, ukuran, dan ketebalan font
- Mengatur perataan dan dekorasi teks
- Menerapkan text styling untuk halaman artikel

## 1️⃣ Mengatur Warna Teks (`color`)

Properti `color` digunakan untuk mengatur warna teks.
**Contoh:**

```css
p {
  color: darkslategray;
}
```

**Jenis Penulisan Warna:**

- Nama warna: `red`, `blue`
- Hex: `#333333`
- RGB: `rgb(0, 0, 0)`

📌 **Best practice**: Gunakan kode **hex** agar konsisten.

## 2️⃣ Mengatur Jenis Font (`font-family`)

Menentukan jenis huruf yang digunakan.
**Contoh:**

```css
body {
  font-family: Arial, Helvetica, sans-serif;
}
```

📌 Browser akan menggunakan font cadangan jika font utama tidak tersedia.

## 3️⃣ Mengatur Ukuran Font (`font-size`)

Digunakan untuk menentukan ukuran teks.
**Contoh:**

```css
p {
  font-size: 16px;
}
```

📌 Satuan umum:

- `px` → ukuran tetap
- `em`, `rem` → responsif (direkomendasikan)

## 4️⃣ Ketebalan Teks (`font-weight`)

Mengatur tebal-tipis teks.
**Contoh:**

```css
h1 {
  font-weight: bold;
}
```

Atau numerik:

```css
font-weight: 400; /* normal */
font-weight: 700; /* bold */
```

## 5️⃣ Perataan Teks (`text-align`)

Mengatur posisi teks secara horizontal.
**Contoh:**

```css
h1 {
  text-align: center;
}
```

Nilai umum:

- `left`
- `center`
- `right`
- `justify`

## 6️⃣ Dekorasi Teks (`text-decoration`)

Mengatur garis pada teks.
**Contoh:**

```css
a {
  text-decoration: none;
}
```

Nilai:

- `none`
- `underline`
- `line-through`
- `overline`

📌 Umumnya digunakan pada **link**.

## 🧪 Praktik: Mempercantik Halaman Artikel

**🎯 Tujuan Praktik**
Menerapkan styling teks untuk membuat artikel lebih nyaman dibaca.

### 1️⃣ Struktur File

- artikel
  - index.html
  - style.css

### 2️⃣ Kode HTML (`index.html`)

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <title>Artikel CSS</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <h1 class="judul">Belajar CSS Dasar</h1>

    <p class="penulis">Ditulis oleh Andi | 2026</p>

    <p>
      CSS membantu developer mengatur tampilan website agar terlihat menarik dan
      profesional.
    </p>

    <p>
      Dengan CSS, kita dapat mengatur warna, font, dan tata letak halaman secara
      terpisah dari HTML.
    </p>
  </body>
</html>
```

### 3️⃣ Kode CSS (`style.css`)

```css
body {
  font-family: Arial, Helvetica, sans-serif;
  color: #333;
}

.judul {
  text-align: center;
  font-size: 32px;
  font-weight: 700;
}

.penulis {
  text-align: center;
  font-size: 14px;
  color: gray;
  text-decoration: underline;
}

p {
  font-size: 16px;
  line-height: 1.8;
  text-align: justify;
}
```
