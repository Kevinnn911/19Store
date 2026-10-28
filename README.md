# 19Store

Website e-commerce statis (HTML5 + CSS3 saja, tanpa JavaScript) untuk etalase produk Apple. Antarmuka Bahasa Indonesia.

## Cara membuka
Buka `index.html` di browser. Tidak perlu server, build tool, atau instalasi.

## Struktur
- `index.html`, `store.html`, `iphone.html`, `mac.html`, `ipad.html`, `watch.html`, `airpods.html`, `accessories.html`
- `product.html` (iPhone 17 Pro) dan `p-<produk>.html` (detail produk lain)
- `bag.html` (demo shopping bag)
- `css/style.css` (stylesheet bersama, 14 bagian)
- `assets/images/` (kosong; letakkan foto berlisensi di sini)

## Batasan (jujur)
- Gambar produk adalah ilustrasi placeholder CSS. Ganti dengan foto yang berlisensi atau seizin pemilik merek.
- Harga adalah contoh ilustrasi, bukan harga resmi.
- Pencarian, keranjang, pilihan varian, dan checkout tidak berfungsi (memerlukan JavaScript/backend) dan diberi label demo.
- Info pengiriman, garansi, pengembalian, kontak, privasi, dan syarat masih placeholder.
- 19Store tidak mengklaim sebagai situs resmi Apple atau Apple Authorized Reseller.

## Menambahkan foto produk
Simpan foto berlisensi (atau foto sendiri) di `assets/images/` dengan nama sesuai slug produk, mis. `iphone-17-pro.jpg`, `macbook-air.jpg`, `airpods-pro-3.jpg`. Foto otomatis tampil menggantikan placeholder; tanpa file, placeholder tetap muncul. Jangan hotlink atau menyalin aset dari apple.com tanpa izin tertulis.
Daftar nama file: nama halaman `p-<slug>.html` tanpa `p-` dan `.html` (iPhone 17 Pro memakai `iphone-17-pro`).

## Catatan penggunaan gambar
Proyek ini untuk tugas sekolah non-komersial. Jika memakai gambar dari apple.com atau Apple Newsroom, unduh dan simpan lokal di `assets/images/` (jangan hotlink), dan cantumkan sumbernya (sudah ada di footer). Jangan dipakai untuk keperluan komersial tanpa izin.
