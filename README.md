# Landing Page SMADORS

Halaman "link-in-bio" SMA Dr. Soetomo Surabaya untuk informasi SPMB: kontak WhatsApp, kanal resmi, dan lokasi sekolah.

Situs statis di folder `docs/` tanpa build step, dipakai oleh GitHub Pages dan Cloudflare (lihat `wrangler.jsonc`). Warna dan font mengikuti design token website utama SMADORS.

## Menjalankan secara lokal

```bash
npx http-server@14.1.1 docs -p 5173 -c-1
```

Lalu buka http://localhost:5173.

## Struktur

- `docs/index.html` — halaman, termasuk CSS
- `docs/assets/logo.png` — logo sekolah
- `docs/assets/gedung.jpg` — foto gedung untuk latar
- `docs/assets/map.png` — pratinjau peta statis dari OpenStreetMap (atribusi "© OpenStreetMap" wajib tetap tampil)
- `wrangler.jsonc` — konfigurasi Cloudflare Workers (static assets dari `docs/`)

## Design token

- Tipografi (rem): 10 / 12 / 14 / 16 / 28 px → `--text-xs` … `--text-xl`
- Jarak (rem, kelipatan 4px): 4 / 8 / 12 / 16 / 24 / 32 / 48 px → `--space-1` … `--space-12`
