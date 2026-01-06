# 📘 Modul 10: Mini Project CSS

**🎯 Tujuan Pembelajaran**

Setelah menyelesaikan mini project ini, peserta mampu:

- Menggabungkan seluruh materi CSS yang telah dipelajari
- Membangun tampilan website modern dan responsif
- Menggunakan **Flexbox & CSS Grid** secara tepat
- Menyusun struktur CSS yang rapi dan mudah dikembangkan
- (Bonus) Menambahkan animasi sederhana untuk meningkatkan UX

## 🗂️ Pilihan Mini Project

Peserta memilih **satu** dari berikut:

### 🔹 [1. Landing Page](https://ihksanghazi.github.io/ExampleLandingPage/)

Cocok untuk:

- Produk
- Event
- Startup

Fitur minimal:

- Hero section
- Call-to-action (CTA)
- Section informasi

### 🔹 [2. Website Portfolio](https://ihksanghazi.github.io/ExampleWebsitePortfolio/)

Cocok untuk:

- Mahasiswa
- Fresh graduate
- Developer pemula

Fitur minimal:

- Profil singkat
- Daftar project (grid)
- Kontak

### 🔹 [3. Company Profile Sederhana](https://ihksanghazi.github.io/ExampleCompanyProfile/)

Cocok untuk:

- Sekolah
- UKM
- Organisasi

Fitur minimal:

- Tentang perusahaan
- Layanan
- Kontak

## 📌 Kriteria Wajib Project

### ✅ 1. Menggunakan Flexbox & Grid

- Flexbox → navbar, alignment
- Grid → galeri, section, layout utama

### ✅ 2. Responsive

- Mobile-first
- Minimal 1 media query (768px)
- Tampilan nyaman di mobile & desktop

### ✅ 3. Struktur CSS Rapi

- Selector jelas
- CSS terpisah (style.css)

## 🗃️ Struktur Folder (Disarankan)

- mini-project-css/
  - index.html
  - style.css
  - assets/
    - images/

## 🧩 Contoh Struktur HTML (Ringkas)

```html
<header class="navbar">
  <h1>MyWebsite</h1>
</header>

<section class="hero">
  <h2>Welcome</h2>
  <p>Website modern dengan CSS</p>
</section>

<section class="projects">
  <div class="card">Project 1</div>
  <div class="card">Project 2</div>
  <div class="card">Project 3</div>
</section>
```

## 🎨 Contoh CSS (Gabungan Materi)

```css
/* RESET */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

/* NAVBAR */
.navbar {
  display: flex;
  justify-content: space-between;
  padding: 16px 32px;
  background: #222;
  color: white;
}

/* HERO */
.hero {
  padding: 60px 20px;
  text-align: center;
}

/* GRID */
.projects {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  padding: 40px;
}

/* CARD */
.card {
  background: #f4f4f4;
  padding: 20px;
  border-radius: 8px;
  transition: transform 0.3s;
}

.card:hover {
  transform: translateY(-8px);
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .projects {
    grid-template-columns: 1fr;
  }
}
```
