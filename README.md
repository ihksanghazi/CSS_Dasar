# 📘 Modul 4: Box Model CSS

**🎯 Tujuan Pembelajaran**
Setelah pertemuan ini, peserta mampu:

- Memahami konsep **CSS Box Model**
- Mengatur ukuran dan ruang elemen
- Menggunakan margin, padding, dan border dengan tepat
- Menerapkan `box-sizing: border-box`
- Membuat layout **card sederhana**

## 1️⃣ Apa Itu Box Model?

Setiap elemen HTML dianggap sebagai **kotak (box)** yang terdiri dari:

```bash
+----------------------+
|      margin          |
|  +---------------+  |
|  |   border      |  |
|  | +-----------+ |  |
|  | | padding   | |  |
|  | | content   | |  |
|  | +-----------+ |  |
|  +---------------+  |
+----------------------+

```

📌 Urutan: **Content → Padding → Border → Margin**

## 2️⃣ Width & Height

Digunakan untuk mengatur **ukuran konten** elemen.

```css
.card {
  width: 300px;
  height: auto;
}
```

📌 `height: auto` menyesuaikan isi.

## 3️⃣ Padding

Ruang **di dalam elemen**, antara konten dan border.

```css
.card {
  padding: 20px;
}
```

📌 Bisa spesifik:

```css
.card {
  padding: 10px 20px;
}
```

## 4️⃣ Border

Garis pembatas elemen.

```css
.card {
  border: 1px solid #ccc;
}
```

📌 Format: `border: width style color`

## 5️⃣ Margin

Ruang **di luar elemen**, untuk jarak antar elemen.

```css
.card {
  margin: 20px auto;
}
```

📌 `auto` membuat elemen berada di tengah (horizontal).

## 6️⃣ Box-Sizing

Mengatur cara browser menghitung ukuran elemen.
**Default:**

```css
box-sizing: content-box;
```

**Best Practice:**

```css
* {
  box-sizing: border-box;
}
```

📌 Dengan `border-box`, **padding dan border tidak menambah ukuran elemen**.

## 🧪 Praktik: Layout Kartu (Card) Sederhana

**🎯 Tujuan Praktik**
Membuat komponen **card** seperti pada website modern.

### 1️⃣ Struktur File

- card-layout
  - index.html
  - style.css

### 2️⃣ Kode HTML (`index.html`)

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <title>Card Layout</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="card">
      <h2>Judul Card</h2>
      <p>Ini adalah contoh card sederhana menggunakan konsep box model CSS.</p>
      <a href="#">Baca Selengkapnya</a>
    </div>
  </body>
</html>
```

### 3️⃣ Kode CSS (`style.css`)

```css
* {
  box-sizing: border-box;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  background-color: #f5f5f5;
}

.card {
  width: 300px;
  background-color: #ffffff;
  border: 1px solid #ddd;
  padding: 20px;
  margin: 40px auto;
  border-radius: 8px;
}

.card h2 {
  margin-top: 0;
}

.card a {
  text-decoration: none;
  color: #007bff;
}
```
