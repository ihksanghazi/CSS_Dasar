# 📘 Modul 9: Responsive Web Design

**🎯 Tujuan Pembelajaran**
Setelah pertemuan ini, peserta mampu:

- Memahami konsep Responsive Web Design (RWD)
- Menggunakan **media query** dengan benar
- Membuat layout yang menyesuaikan ukuran layar
- Menerapkan **mobile-first approach**
- Membangun layout yang nyaman di **mobile & desktop**

## 1️⃣ Apa Itu Responsive Web Design?

**Responsive Web Design** adalah teknik agar website:

- Tampil rapi di **mobile**, **tablet**, **dan desktop**
- Menyesuaikan ukuran layar secara otomatis
- Tidak perlu membuat website terpisah

📌 Ini adalah **standar wajib** di dunia kerja.

## 2️⃣ Media Query

Media query digunakan untuk menerapkan CSS **berdasarkan kondisi layar**.
**Sintaks Dasar:**

```css
@media (max-width: 768px) {
  /* CSS untuk layar kecil */
}
```

Artinya:

- CSS di dalamnya aktif jika layar **≤ 768px**
- Biasanya untuk **tablet & mobile**

## 3️⃣ Breakpoint Umum

| Device  | Ukuran   |
| ------- | -------- |
| Mobile  | ≤ 576px  |
| Tablet  | ≤ 768px  |
| Laptop  | ≤ 1024px |
| Desktop | > 1024px |

## 4️⃣ Responsive Layout

Responsive layout berarti:

- Kolom bisa berubah jumlah
- Menu bisa berpindah posisi
- Ukuran font & padding menyesuaikan

📌 Umumnya dikombinasikan dengan:

- Flexbox
- CSS Grid

## 5️⃣ Mobile-First Concept ⭐

**Mobile-first** berarti:

1. Desain untuk **mobile terlebih dahulu**
2. Tambahkan fitur untuk layar lebih besar

**Contoh:**

```css
/* Mobile (default) */
.container {
  display: flex;
  flex-direction: column;
}

/* Desktop */
@media (min-width: 768px) {
  .container {
    flex-direction: row;
  }
}
```

📌 Ini adalah **best practice industri**.

## 🧪 Praktik: Layout Responsif Mobile & Desktop

**🎯 Studi Kasus**
Layout dengan:

- Sidebar
- Konten utama

### HTML

```html
<div class="layout">
  <div class="sidebar">Sidebar</div>
  <div class="content">Konten Utama</div>
</div>
```

### CSS

```css
body {
  font-family: Arial, Helvetica, sans-serif;
  margin: 0;
}

.layout {
  display: flex;
  flex-direction: column;
}

/* Sidebar & konten */
.sidebar {
  background: #2c3e50;
  color: white;
  padding: 16px;
}

.content {
  padding: 16px;
}

/* Desktop layout */
@media (min-width: 768px) {
  .layout {
    flex-direction: row;
    min-height: 100vh;
  }

  .sidebar {
    width: 250px;
  }

  .content {
    flex: 1;
  }
}
```
