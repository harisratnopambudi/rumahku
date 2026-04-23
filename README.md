# 🏠 KPR Tracker — Rumahku

> Dashboard pribadi untuk memantau dan menyemangati perjalanan cicilan KPR.  
> Satu halaman, tanpa scroll, tanpa framework — murni HTML + CSS + JS.

![Preview](https://img.shields.io/badge/status-aktif-brightgreen) ![HTML](https://img.shields.io/badge/HTML-5-orange) ![CSS](https://img.shields.io/badge/CSS-3-blue) ![JS](https://img.shields.io/badge/JavaScript-Vanilla-yellow) ![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

## ✨ Fitur

- **Layout 16:9 penuh** — semua informasi terlihat dalam satu layar tanpa scroll di desktop
- **Tipografi besar & tegas** — menggunakan Bebas Neue untuk angka-angka utama yang mendominasi layar
- **Real-time countdown** — hitung mundur otomatis menuju tanggal jatuh tempo (tgl 8 tiap bulan)
- **Progress bar animasi** — visualisasi persentase cicilan yang sudah terlunasi
- **Estimasi lunas otomatis** — dihitung dari tanggal hari ini + sisa cicilan
- **Responsive** — tampil optimal di desktop (16:9) maupun mobile
- **Zero dependencies** — tidak butuh Node.js, npm, atau framework apapun
- **Dark theme** — nyaman di mata, cocok dibuka kapan saja

---

## 📸 Preview

```
┌─────────────────────────────────────────────────────────────┐
│  RUMAHKU          KPR SSA/SSB · 5%    23 April 2026  ● Aktif│
├──────────────┬──────────────┬──────────────────────────────┤
│              │   57,27%     │  Rp 1.226.000                │
│  RP          │              │  Angsuran / bulan             │
│  52.217.297  ├──────────────┤  Pokok      Rp 960.444       │
│              │   84         │  Bunga      Rp 265.556       │
│  Terlunasi   │  / 132 cicilan│  Total      Rp 1.226.000    │
│  57,27% ████─┤  48 bln sisa ├──────────────────────────────┤
│              │              │  15                          │
├──────────────┴──────────────┤  hari menuju tgl 8           │
│  84 BULAN KONSISTEN · LEBIH │  8 Mei 2026                  │
│  DARI SEPARUH JALAN · ...   │  RUMAH BEBAS HUTANG          │
└─────────────────────────────┴──────────────────────────────┘
```

---

## 🚀 Cara Pakai

### 1. Clone atau Download

```bash
git clone https://github.com/username/kpr-tracker.git
cd kpr-tracker
```

Atau langsung download file `kpr-tracker.html` dan buka di browser.

### 2. Buka di Browser

```bash
# Tidak perlu server — cukup buka langsung
open kpr-tracker.html

# Atau drag & drop file ke browser
```

### 3. Sesuaikan Data KPR Kamu

Buka `kpr-tracker.html` dengan text editor, cari bagian HTML dan ubah sesuai data KPR-mu:

```html
<!-- Ubah angka saldo tersisa -->
<div class="saldo-angka">52.217.297</div>

<!-- Ubah teks caption -->
<div class="saldo-caption">
  Dari plafon awal Rp 122.200.000<br>
  Terlunasi Rp 69.982.703
</div>

<!-- Ubah cicilan berjalan -->
<div class="cicilan-besar">84</div>
<div class="cicilan-of">/ 132 CICILAN</div>

<!-- Ubah rincian angsuran -->
<div class="angsuran-total">Rp 1.226.000</div>
```

Juga sesuaikan bagian JavaScript untuk countdown yang akurat:

```javascript
// Ganti angka sesuai sisa cicilan kamu
const lunas = new Date(today.getFullYear(), today.getMonth() + 48, 1);

// Ganti tanggal jatuh tempo jika bukan tgl 8
let nextDue = new Date(today.getFullYear(), today.getMonth(), 8);
if (today.getDate() >= 8) nextDue = new Date(..., today.getMonth() + 1, 8);
```

Dan progress bar di HTML:

```html
<!-- Sesuaikan persentase lunas -->
<div class="bar-fill" style="width:57.27%"></div>
```

---

## 📁 Struktur File

```
kpr-tracker/
└── kpr-tracker.html    # Semua kode dalam satu file (HTML + CSS + JS)
```

---

## 🎨 Desain

| Elemen | Font | Keterangan |
|--------|------|------------|
| Angka utama | Bebas Neue | Display, tegas, besar |
| Body text | Outfit | Bersih, modern, mudah dibaca |
| Label & kode | JetBrains Mono | Monospace untuk data teknis |

**Palet warna:**

| Nama | Hex | Digunakan untuk |
|------|-----|-----------------|
| Background | `#0C0F0A` | Latar utama (hampir hitam) |
| Surface | `#141810` | Panel & header |
| Green | `#A8E063` | Aksen utama, progress, countdown |
| Orange | `#F5A623` | Total angsuran |
| Red | `#E05252` | Peringatan jatuh tempo |
| White | `#F4F7F0` | Teks utama |

---

## ⚙️ Kustomisasi Lanjutan

### Ubah Tanggal Jatuh Tempo

```javascript
// Ubah angka 8 menjadi tanggal jatuh tempo KPR kamu
let nextDue = new Date(today.getFullYear(), today.getMonth(), 8);
if (today.getDate() >= 8) nextDue = new Date(today.getFullYear(), today.getMonth() + 1, 8);
```

### Ubah Warna Aksen

```css
:root {
  --green: #A8E063;   /* Ganti warna aksen utama */
  --orange: #F5A623;  /* Ganti warna angsuran */
}
```

### Ubah Ticker Motivasi

```html
<span class="ticker-inner">
  PESAN MOTIVASIMU SENDIRI DI SINI · SEMANGAT! ·
</span>
```

---

## 📱 Kompatibilitas

| Platform | Status |
|----------|--------|
| Chrome (desktop) | ✅ Optimal |
| Firefox (desktop) | ✅ Optimal |
| Safari (desktop) | ✅ Optimal |
| Chrome (mobile) | ✅ Responsive |
| Safari (iOS) | ✅ Responsive |

---

## 💡 Tips

- **Bookmark** halaman ini di browser supaya mudah dibuka kapan saja
- **Pasang sebagai homepage** browser untuk pengingat otomatis setiap hari
- Buka di **fullscreen mode** (`F11`) untuk tampilan 16:9 yang maksimal
- Di HP, putar ke **landscape** untuk tampilan lebih lega

---

## 📄 Lisensi

MIT License — bebas digunakan, dimodifikasi, dan dibagikan.

---

<p align="center">
  Dibuat dengan ❤️ sebagai pengingat bahwa setiap cicilan adalah langkah nyata menuju <strong>rumah bebas hutang</strong>.
</p>
