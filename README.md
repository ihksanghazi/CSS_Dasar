# 📘 Modul 1: Pengenalan CSS

**🎯 Tujuan Pembelajaran**
Setelah pertemuan ini, peserta mampu:

- Menjelaskan peran CSS dalam pengembangan web
- Memahami cara kerja CSS bersama HTML
- Menjelaskan perbedaan Inline, Internal, dan External CSS
- Menulis struktur dasar CSS
- Mengubah tampilan teks HTML menggunakan CSS

## 1️⃣ Apa Itu CSS?

**CSS (Cascading Style Sheets)** adalah bahasa yang digunakan untuk:

- Mengatur **tampilan visual** halaman web
- Mengontrol warna, font, ukuran, dan layout
- Memisahkan **struktur (HTML)** dan **desain (CSS)**

📌 Tanpa CSS, website hanya berisi teks polos.

## 2️⃣ Fungsi CSS dalam Web

CSS berfungsi untuk:

- Membuat tampilan website lebih menarik
- Menjaga konsistensi desain
- Memudahkan maintenance kode
- Membuat website responsif

📌 CSS bekerja di sisi client (browser).

## 3️⃣ Cara Kerja CSS (HTML + CSS)

Browser membaca:

1. Struktur HTML
2. Aturan CSS
3. Menggabungkan keduanya menjadi tampilan visual

📌 CSS menargetkan elemen HTML menggunakan selector.

## 4️⃣ Cara Menggunakan CSS

### 🔹 1. Inline CSS

Ditulis langsung pada tag HTML.

```html
<p style="color: red;">Teks Merah</p>
```

✅ Cepat & mudah
❌ Tidak efisien untuk proyek besar

### 🔹 2. Internal CSS

Ditulis di dalam tag `<style>` pada `<head>`.

```html
<style>
  p {
    color: blue;
  }
</style>
```

📌 Cocok untuk satu halaman.

### 🔹 3. External CSS (Best Practice)

CSS ditulis di file terpisah `.css`.

```html
<link rel="stylesheet" href="style.css" />
```

```css
p {
  color: green;
}
```

📌 Digunakan di proyek profesional.

## 5️⃣ Struktur Dasar CSS

Struktur umum CSS:

```css
selector {
  property: value;
}
```

**Contoh:**

```css
p {
  color: red;
  font-size: 16px;
}
```

📌 Penjelasan:

- **Selector** → elemen HTML yang dipilih
- **Property** → jenis styling
- **Value** → nilai styling

## 🧪 Praktik: Mengubah Warna & Font Teks HTML

**🎯 Tujuan Praktik**
Menerapkan CSS dasar untuk mengubah tampilan teks.
**Instruksi:**

1. Buat file `index.html`
2. Tambahkan Internal CSS
3. Ubah warna dan font teks

**Contoh Hasil Praktik:**

```html
<!DOCTYPE html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <title>Pengenalan CSS</title>

    <style>
      h1 {
        color: darkblue;
        font-family: Arial;
      }

      p {
        color: gray;
        font-size: 18px;
      }
    </style>
  </head>
  <body>
    <h1>Belajar CSS</h1>
    <p>CSS membuat tampilan website lebih menarik.</p>
  </body>
</html>
```
