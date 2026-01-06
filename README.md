# 📘 Pertemuan 7: CSS Grid

**🎯 Tujuan Pembelajaran**
Setelah pertemuan ini, peserta mampu:

- Memahami konsep **CSS Grid Layout**
- Membuat layout kompleks dan responsif
- Mengatur baris dan kolom dengan Grid
- Menerapkan Grid untuk **galeri** dan **dashboard**

## 1️⃣ Apa Itu CSS Grid?

CSS Grid adalah sistem layout CSS untuk:

- Membuat layout **dua dimensi** (baris & kolom)
- Mengatur elemen dengan presisi tinggi
- Membangun layout kompleks seperti dashboard

📌 **Flexbox = 1 dimensi**, **Grid = 2 dimensi**

## 2️⃣ Mengaktifkan Grid (`display: grid`)

Untuk menggunakan CSS Grid:

```css
.container {
  display: grid;
}
```

📌 Semua elemen di dalamnya otomatis menjadi `grid item`.

## 3️⃣ Mengatur Kolom (`grid-template-columns`)

Menentukan jumlah dan ukuran kolom.

```css
grid-template-columns: 200px 1fr;
```

Artinya:

- Kolom kiri: tetap 200px
- Kolom kanan: sisa layar

Contoh lain:

```css
grid-template-columns: repeat(3, 1fr);
```

## 4️⃣ Mengatur Baris (`grid-template-rows`)

Menentukan tinggi baris.

```css
grid-template-rows: 60px 1fr 50px;
```

Artinya:

- Baris Atas: 60px
- Baris Tengah: fleksibel
- Baris Bawah: 50px

## 5️⃣ Jarak Antar Grid (`gap`)

Mengatur jarak antar baris & kolom.

```css
gap: 20px;
```

📌 Lebih rapi daripada margin manual.

## 6️⃣ ❗ Masalah Umum CSS Grid (WAJIB PAHAM)

Jika hanya menulis:

```css
display: grid;
grid-template-columns: 200px 1fr;
grid-template-rows: 60px 1fr 50px;
```

➡️ **Browser akan menempatkan elemen otomatis berdasarkan urutan HTML,**
➡️ Hasil layout sering **tidak sesuai desain**.

✅ SOLUSI INDUSTRI: grid-template-areas

## 7️⃣ Grid Template Areas (Kunci Layout Rapi)

Digunakan untuk **mengatur posisi elemen secara eksplisit**.

```css
grid-template-areas:
  "sidebar header"
  "sidebar content"
  "sidebar footer";
```

📌 Ini adalah cara paling aman & readable untuk layout besar.

## 🧪 Praktik 1: Layout Galeri Foto

**🎯 Tujuan**
Membuat galeri gambar responsif.

### HTML

```html
<div class="gallery">
  <div class="item">Foto 1</div>
  <div class="item">Foto 2</div>
  <div class="item">Foto 3</div>
  <div class="item">Foto 4</div>
  <div class="item">Foto 5</div>
  <div class="item">Foto 6</div>
</div>
```

### CSS

```css
.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  padding: 20px;
}

.item {
  background-color: #ddd;
  height: 150px;
  display: flex;
  align-items: center;
  justify-content: center;
}
```

📌 Mudah diubah ke 2 atau 4 kolom.

## 🧪 Praktik 2: Layout Dashboard Sederhana

**🎯 Tujuan**
Membuat struktur dashboard dengan.

- Sidebar
- Header
- Konten
- Footer

### HTML

```html
<div class="dashboard">
  <div class="sidebar">Sidebar</div>
  <div class="header">Header</div>
  <div class="content">Konten</div>
  <div class="footer">Footer</div>
</div>
```

### CSS

```css
.dashboard {
  display: grid;
  grid-template-columns: 220px 1fr;
  grid-template-rows: 60px 1fr 50px;
  grid-template-areas:
    "sidebar header"
    "sidebar content"
    "sidebar footer";
  gap: 12px;
  height: 100vh;
}

.sidebar {
  grid-area: sidebar;
  background: #2c3e50;
  color: white;
  padding: 16px;
}

.header {
  grid-area: header;
  background: #ecf0f1;
  padding: 16px;
}

.content {
  grid-area: content;
  background: #ffffff;
  padding: 16px;
}

.footer {
  grid-area: footer;
  background: #ecf0f1;
  padding: 16px;
}
```

📌 Grid memudahkan layout kompleks tanpa nested div.
