# Jadwal Khatib & Imam Sholat Jum'at Masjid An-Nuur Kotagede

Situs statis menampilkan jadwal khatib &amp; imam sholat Jum'at
sepanjang tahun 2026, disusun per bulan berdasarkan pasaran (Wage,
Legi, Pon, Kliwon, Pahing).

## Struktur folder

```
jadwal-khatib/
├── index.html
├── css/style.css
└── assets/logo.svg
```

## Cara mengubah data

Buka `index.html`, cari blok bulan yang ingin diubah — ditandai dengan
`<div class="month-card">`. Setiap baris jadwal berbentuk:

```html
<tr>
  <td class="no">1</td>
  <td class="tgl">2</td>
  <td><span class="pasaran wage">Wage</span></td>
  <td class="khotib">Maryono, MT</td>
</tr>
```

- Ganti angka, tanggal, dan nama khotib sesuai kebutuhan.
- Untuk kolom "Pasaran", class yang tersedia: `wage`, `legi`, `pon`,
  `kliwon`, `pahing` — warnanya otomatis menyesuaikan.

## Cara upload ke GitHub & tayangkan lewat GitHub Pages

1. Buat repository baru di GitHub (public).
2. Upload seluruh isi folder ini lewat "Add file → Upload files", atau lewat git:
   ```bash
   git init
   git add .
   git commit -m "Jadwal khatib dan imam Jumat"
   git branch -M main
   git remote add origin https://github.com/USERNAME/NAMA-REPO.git
   git push -u origin main
   ```
3. Tambahkan file kosong bernama `.nojekyll` di root repo (mencegah error build).
4. Buka **Settings → Pages**, pilih branch `main` dan folder `/ (root)`, lalu **Save**.
5. Situs akan tayang di `https://USERNAME.github.io/NAMA-REPO/`.
