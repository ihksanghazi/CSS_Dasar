# 📘 Modul 8: Position & Z-Index

**🎯 Tujuan Pembelajaran**
Setelah pertemuan ini, peserta mampu:

- Memahami cara kerja sistem posisi di CSS
- Menggunakan `relative`, `absolute`, `fixed`, dan `sticky` dengan benar
- Mengontrol tumpukan elemen menggunakan `z-index`
- Menerapkan positioning pada kasus nyata website

## 1️⃣ Konsep Dasar Positioning

Secara default, semua elemen HTML memiliki:

```css
position: static;
```

Artinya:

- Elemen mengikuti alur normal dokumen
- Tidak bisa dipindahkan dengan `top`, `left`, `dll`

## 2️⃣ `position: relative`

Digunakan untuk:

- Menggeser elemen **tanpa keluar dari alur**
- Menjadi **parent** bagi elemen absolute

```css
.card {
  position: relative;
}
```

📌 Biasanya **tidak terlihat efeknya**, tapi sangat penting.

## 3️⃣ `position: absolute`

Digunakan untuk:

- Memposisikan elemen secara bebas
- Menempel pada **parent terdekat yang** `relative`

```css
.badge {
  position: absolute;
  top: 10px;
  right: 10px;
}
```

📌 Jika tidak ada parent `relative` → menempel ke `body` ❌

## 🧪 Praktik Utama: Relative & Absolute

**🎯 Studi Kasus**

Membuat **Card Produk** dengan **Badge di pojok kanan atas**

### HTML

```html
<div class="card">
  <span class="badge">NEW</span>
  <h2>Produk A</h2>
  <p>Contoh penggunaan relative dan absolute.</p>
</div>
```

### CSS

```css
.card {
  position: relative;
  width: 300px;
  padding: 20px;
  background: white;
  border-radius: 8px;
}

.badge {
  position: absolute;
  top: 12px;
  right: 12px;
  background: crimson;
  color: white;
  padding: 4px 10px;
  border-radius: 12px;
  font-size: 12px;
}
```

## 4️⃣ `position: fixed`

Digunakan untuk:

- Elemen yang **selalu terlihat di layar**
- Tidak bergerak saat scroll

```css
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
}
```

📌 Cocok untuk navbar & floating button.

## 5️⃣ `position: sticky`

Gabungan:

- `relative` (awal)
- `fixed` (saat scroll)

```css
.header {
  position: sticky;
  top: 0;
}
```

## 🧪 Praktik Tambahan: Header Sticky

### HTML

```html
<header class="header">Header Sticky</header>

<main class="content">
  <p>Scroll ke bawah...</p>
</main>
```

### CSS

```css
.header {
  position: sticky;
  top: 0;
  background: #333;
  color: white;
  padding: 16px;
}
.content {
  height: 1500px;
}
```

## 6️⃣ Z-Index (Lapisan Elemen)

Digunakan untuk mengatur **urutan depan-belakang** elemen.

```css
.popup {
  position: fixed;
  z-index: 10;
}
```

📌 Syarat:

- Elemen harus punya `position`
- Nilai besar → lebih depan

## 🧪 Praktik Tambahan: Popup Sederhana

### HTML

```html
<div class="popup">Ini popup</div>
```

### CSS

```css
.popup {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: white;
  padding: 20px;
  z-index: 10;
}
```
