# Portal KKDN NTT 2026

Portal kunjungan kerja dalam negeri Provinsi Nusa Tenggara Timur, 16–20 November 2026. Isinya: insight gempa Flores M7,7, pointer diskusi per sasaran, peta lokasi kunjungan, rencana kegiatan, profil tiap sasaran, dan laporan lengkap gempa.

## Isi folder

| File | Isi |
|---|---|
| `index.html` | Halaman pembuka; langsung mengalihkan ke portal |
| `Main.dc.html` | Portal utama |
| `Sasaran-01-…` s.d. `Sasaran-09-….dc.html` | Profil tiap sasaran (8 halaman; sekolah belum ada profil) |
| `Laporan-Gempa-Flores.dc.html` | Laporan lengkap 88 hari setelah gempa |
| `support.js` | Runtime halaman `.dc.html` (wajib ada di folder yang sama) |
| `vendor/leaflet.js`, `vendor/leaflet.css` | Pustaka peta (Leaflet 1.9.4) |
| `.nojekyll` | Mencegah GitHub Pages memproses folder dengan Jekyll |

## Cara deploy ke GitHub Pages

1. Buat repository baru di GitHub, misalnya `kkdn-ntt` (Public).
2. Unggah **seluruh isi folder ini** ke root repository (Add file → Upload files, tarik semua file dan folder `vendor`), lalu Commit.
   Atau lewat terminal:
   ```bash
   cd kkdn-ntt
   git init
   git add .
   git commit -m "Portal KKDN NTT 2026"
   git branch -M main
   git remote add origin https://github.com/<akun>/kkdn-ntt.git
   git push -u origin main
   ```
3. Buka Settings → Pages → Build and deployment → Source: **Deploy from a branch**, Branch: **main**, folder **/ (root)** → Save.
4. Tunggu 1–2 menit. Portal tayang di `https://<akun>.github.io/kkdn-ntt/`.

## Catatan

- Halaman memuat React dan Babel dari unpkg.com serta font dari Google Fonts, dan peta dasar dari server OpenStreetMap, jadi pembaca perlu koneksi internet.
- Hitung mundur dan penanda hari dihitung dari tanggal perangkat pembaca (zona WITA), sehingga otomatis berganti tiap hari dan menjadi "Selesai" setelah 20 Nov 2026 pukul 13.55 WITA.
- Untuk memperbarui isi, ubah di kanvas Claude Design lalu ekspor ulang, atau sunting file `.dc.html` langsung lalu commit.
