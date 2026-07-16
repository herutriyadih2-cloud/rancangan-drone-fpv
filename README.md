# Rancangan Desain 3D Drone Lengkap

Rancangan teknis sebuah **quadcopter FPV freestyle 5 inci** (True-X, 220 mm, sistem 6S) —
lengkap dengan model 3D interaktif, daftar belanja, kode firmware, dan anggaran.

**Situs:** https://herutriyadih2-cloud.github.io/rancangan-drone-fpv/

---

## Isi

| Bagian | Isi |
|---|---|
| **Model 3D** | Viewer interaktif — putar 360°, zoom, mode urai (exploded), propeller berputar, sorot per komponen. Ditulis dari nol dengan canvas 2D, tanpa library. |
| **01 · Daftar belanja** | Tiap komponen dengan rekomendasi produk bermerek, alternatif hemat & premium, dan harga estimasi. |
| **02 · Arsitektur sistem** | Tiga jalur — daya, kontrol, video — dan bagaimana semuanya terhubung. |
| **03 · Perhitungan** | Thrust-to-weight, arus puncak, durasi terbang, RPM. Angka yang menentukan drone ini terbang atau tidak. |
| **04 · Bedah kode 3D** | Renderer 3D dijelaskan baris demi baris: geometri, rotasi, proyeksi perspektif, painter's algorithm, Lambert shading. |
| **05 · Sistem kendali terbang** | Kode C: filter gyro, PID, mixer Quad-X, DShot600, parsing CRSF, arming & failsafe, main loop 8 kHz. |
| **06 · Simulator PID** | Kode PID di atas benar-benar berjalan di browser, mengendalikan model fisika sumbu roll. Geser slider, lihat apa yang rusak. |
| **07 · Konfigurasi Betaflight** | Dump CLI siap tempel, dengan penjelasan baris-baris pentingnya. |
| **08 · Urutan perakitan** | Delapan langkah, dari frame kering sampai hover test. |

## Spesifikasi ringkas

| | |
|---|---|
| Konfigurasi | True-X quad, wheelbase 220 mm |
| Motor | 2207 · 1900 KV × 4 |
| Propeller | 5×4.3×3 tri-blade |
| Baterai | LiPo 6S 1300 mAh 100C |
| Massa terbang (AUW) | 685 g |
| Thrust-to-weight | 7,0 : 1 |
| Durasi terbang | 4–6 menit (freestyle) |
| Biaya drone | ± Rp 5,3 juta |
| Biaya total (+ radio, goggles, alat) | ± Rp 12,3 juta |

## Masukan yang dicari

Rancangan ini **belum dibangun** — masih tahap desain, dan sedang dimintakan pendapat.
Masukan yang paling berguna:

- **Pemilihan komponen** — apakah kombinasi motor/prop/baterai ini masuk akal untuk 2026?
- **Harga** — angka rupiah di dokumen adalah estimasi, belum diverifikasi ke marketplace.
- **Tren terkini** — sistem digital (DJI O4, Walksnail, HDZero) vs analog; apakah analog masih layak untuk build pertama?
- **Frame** — apakah ada frame 5" yang lebih tahan crash dengan harga sekelas?

## Catatan teknis

Situs ini adalah **satu file HTML statis** (`index.html`, ±146 KB). Tanpa build step,
tanpa dependency, tanpa framework. Bisa dibuka langsung dari folder tanpa internet.
Berjalan di semua browser modern (desktop & mobile); tidak mendukung Internet Explorer.

Untuk mengubah isinya: edit `index.html`, lalu `git commit` dan `git push` —
GitHub Pages akan otomatis memperbarui situs dalam ±1 menit.
