# Modul 5: Background & Border CSS

**🎯 Tujuan Pembelajaran**
Setelah pertemuan ini, peserta mampu:

- Mengatur warna dan gambar latar belakang
- Mengontrol ukuran dan posisi background image
- Membuat sudut elemen membulat dengan border-radius
- Menerapkan background & border pada **banner website**

## 1️⃣ Background Color (`background-color`)

Digunakan untuk memberi warna latar belakang elemen.

```css
body {
  background-color: #f4f6f8;
}
```

📌 Gunakan warna dengan kontras yang nyaman.

## 2️⃣ Background Image (`background-image`)

Digunakan untuk menampilkan gambar sebagai latar.

```css
.banner {
  background-image: url("banner.jpg");
}
```

📌 Pastikan path gambar benar.

## 3️⃣ Background Size (`background-size`)

Mengatur ukuran background image.

```css
background-size: cover;
```

Nilai umum:

- `cover` → menutupi area
- `contain` → seluruh gambar terlihat
- ukuran manual: `100% 100%`
- 📌 `cover` paling sering digunakan untuk banner.

## 4️⃣ Background Position (`background-position`)

Mengatur posisi gambar latar.

```css
background-position: center;
```

Nilai umum:

- `center`
- `top`
- `bottom`
- `left`
- `right`

## 5️⃣ Border Radius (`border-radius`)

Digunakan untuk membuat sudut elemen menjadi membulat.

```css
.card {
  border-radius: 12px;
}
```

📌 Semakin besar nilai, semakin bulat sudutnya.

## 🧪 Praktik: Banner Website Sederhana

**🎯 Tujuan Praktik**
Membuat banner website dengan background image dan teks di atasnya.

### 1️⃣ Struktur File

- banner
  - index.html
  - style.css
  - banner.jpg

### 2️⃣ Kode HTML (`index.html`)

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <title>Banner Website</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="banner">
      <h1>Belajar CSS</h1>
      <p>Membuat tampilan website lebih menarik</p>
    </div>
  </body>
</html>
```

### 3️⃣ Kode CSS (`style.css`)

```css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
}

.banner {
  height: 300px;
  background-image: url("banner.jpg");
  background-size: cover;
  background-position: center;
  border-radius: 16px;
  margin: 40px;
  padding: 40px;
  color: white;
}

.banner h1 {
  font-size: 36px;
}

.banner p {
  font-size: 18px;
}
```
