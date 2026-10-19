# Global Volcano Explorer

WebGIS interaktif untuk menjelajahi gunung api Holosen dunia (Smithsonian Institution, Global Volcanism Program, Volcanoes of the World 5.4.0, 1.214 catatan, diunduh 19 Okt 2026).

Situs statis: tanpa build, tanpa backend, tanpa API key.

## Menjalankan lokal
Buka `index.html` di browser, atau jalankan server sederhana:

    python3 -m http.server 8000

lalu buka http://localhost:8000

## Hosting di GitHub Pages
1. Push seluruh isi folder ini ke repositori (branch `main`).
2. Settings > Pages > Source: Deploy from a branch > `main` / `(root)` > Save.
3. Situs aktif di `https://<username>.github.io/<nama-repo>/`.

## Struktur
- `index.html` - aplikasi (HTML, CSS, JS)
- `data/gvp-data.js` - data GVP (1.214 baris, kolom sesuai berkas asli)
- `data/borders.js` - batas negara
- `assets/basemap.jpg` dan `basemap-sm.jpg` - basemap Natural Earth (Cross Blended Hypso with Relief, Water, Drains, and Ocean Bottom), Web Mercator, digelapkan; versi kecil untuk ponsel
- `vendor/` - Leaflet 1.9.4

## Catatan data
Daftar gunung api Holosen, bukan seluruh gunung api di dunia. Bukti aktivitas dan letusan terakhir adalah catatan historis, bukan status aktivitas saat ini. Warna marker seragam dan tidak menunjukkan tingkat bahaya.

## Sumber
- Smithsonian GVP: https://volcano.si.edu/
- Natural Earth (domain publik): https://www.naturalearthdata.com/
- Leaflet (BSD-2-Clause)
