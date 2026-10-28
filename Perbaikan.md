# Perbaikan 19Store

Dokumentasi pelacakan perbaikan bug dan kendala teknis pada aset visual 19Store.

## [PRIORITY: HIGH]
- Location: `css/style.css` dan integrasi aset gambar `assets/images/`
- Severity: High
- Status: Solved
- Root Cause: 
  1. File gambar yang disiapkan memiliki format penamaan berbeda (mengandung spasi, huruf kapital, ekstensi `.webp`) sementara markup awal berekspektasi ekstensi `.jpg` dan slug spesifik.
  2. Implementasi awal menggunakan CSS variable `--img` pada pseudo-element `.fig::after`. Karena `.fig` menggunakan `display: grid` dengan `place-items: center`, pseudo-element absolute tanpa dimensi eksplisit mengalami collapse (width 0, height 0).
  3. Elemen placeholder `.dev` tidak disembunyikan saat gambar dimuat, sehingga siluet abu-abu tetap terlihat di latar belakang.
- Solution:
  1. Melakukan normalisasi dan pemetaan menyeluruh untuk seluruh 18 produk ke slug terstandarisasi (`<slug>.webp` dan `<slug>.jpg`) dengan mempertahankan file asli.
  2. Memperbarui seluruh halaman web (`index.html`, `store.html`, halaman kategori, dan 18 halaman detail `p-*.html`) untuk menggunakan elemen semantik `<img>` dengan kelas `.product-img` dan atribut `alt` yang aksesibel.
  3. Memperbarui `css/style.css` dengan aturan `.product-img` yang mencakup `mix-blend-mode: multiply` pada latar terang, penataan kartu showcase pada latar gelap (`.dark`), padding proporsional pada kartu produk, serta efek mikro-interaksi hover (`transform: scale(1.04)`).
- Target Deadline: Selesai (17 Oktober 2026).
