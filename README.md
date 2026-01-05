# 📘 Modul 6: Layout dengan Flexbox

**🎯 Tujuan Pembelajaran**
Setelah pertemuan ini, peserta mampu:

- Memahami konsep dasar Flexbox
- Menggunakan Flexbox untuk mengatur layout
- Mengatur perataan dan arah elemen
- Membangun **navbar** dan **layout 2 kolom**

## 1️⃣ Apa Itu Flexbox?

**Flexbox (Flexible Box Layout)** adalah sistem layout CSS untuk:

- Menyusun elemen secara fleksibel
- Membuat layout responsif
- Mengatur posisi elemen secara horizontal & vertikal

📌 Cocok untuk **navbar**, **card**, dan **layout kolom**.

## 2️⃣ Mengaktifkan Flexbox (`display: flex`)

Untuk menggunakan Flexbox, container harus di-set:

```css
.container {
  display: flex;
}
```

📌 Semua child element menjadi **flex items**.

## 3️⃣ Arah Elemen (`flex-direction`)

Menentukan arah susunan elemen.

```css
flex-direction: row;
```

Nilai umum:

- `row` (default) → horizontal
- `column` → vertikal
- `row-reverse`
- `column-reverse`

## 4️⃣ Perataan Horizontal (`justify-content`)

Mengatur posisi elemen di `arah utama`.

```css
justify-content: space-between;
```

Nilai umum:

- `flex-start`
- `center`
- `flex-end`
- `space-between`
- `space-around`
- `space-evenly`

## 5️⃣ Perataan Vertikal (`align-items`)

Mengatur posisi elemen di **arah silang (cross-axis)**.

```css
align-items: center;
```

Nilai umum:

- `flex-start`
- `center`
- `flex-end`
- `stretch`

## 6️⃣ Jarak Antar Elemen (`gap`)

Digunakan untuk memberi jarak antar flex item.

```css
gap: 20px;
```

📌 Lebih rapi daripada `margin`.

## 🧪 Praktik 1: Navbar dengan Flexbox

**🎯 Tujuan**
Membuat navbar horizontal modern.

### HTML

```html
<nav class="navbar">
  <h2 class="logo">MyWebsite</h2>
  <ul class="menu">
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
  </ul>
</nav>
```

### CSS

```css
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #222;
  padding: 15px 30px;
  color: white;
}

.menu {
  display: flex;
  list-style: none;
  gap: 20px;
}
```

## 🧪 Praktik 2: Layout 2 Kolom

**🎯 Tujuan**
Membuat layout konten dan sidebar.

### HTML

```html
<div class="container">
  <div class="content">Konten Utama</div>
  <div class="sidebar">Sidebar</div>
</div>
```

### CSS

```css
.container {
  display: flex;
  gap: 20px;
  padding: 20px;
}

.content {
  flex: 3;
  background-color: #f4f4f4;
  padding: 20px;
}

.sidebar {
  flex: 1;
  background-color: #ddd;
  padding: 20px;
}
```

📌 Properti `flex` mengatur proporsi kolom.
