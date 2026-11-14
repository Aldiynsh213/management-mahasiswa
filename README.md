# Manajemen Data Mahasiswa

Aplikasi web untuk mengelola data mahasiswa (sarjana dan magister) sekaligus mendemonstrasikan algoritma pencarian dan pengurutan beserta analisis kompleksitasnya.

## Fitur
- CRUD data mahasiswa (NIM, nama, email, jenjang)
- Pencarian: linear dan binary search
- Pengurutan: beberapa algoritma sort dengan perbandingan
- Analisis kompleksitas waktu dan ruang per algoritma
- Dashboard statistik

## Teknologi
| Bagian | Stack |
|---|---|
| Frontend | React, TypeScript, Vite, Tailwind CSS, shadcn/ui |
| Backend | Python, Flask, Flask-CORS |
| Data | File JSON (`backend/data/mahasiswa.json`) |

## Struktur
```
backend/    API Flask (routes, models, algorithms, utils, data)
frontend/   Aplikasi React (src/pages, src/components, src/hooks, src/api)
```

## Menjalankan
Backend (port 5000):
```bash
cd backend
pip install -r requirements.txt
python app.py
```
Frontend (port 3000):
```bash
cd frontend
npm install
npm run dev
```
Frontend memanggil API di `http://localhost:5000/api`.

## Endpoint utama
| Prefix | Fungsi |
|---|---|
| `/api/mahasiswa` | CRUD dan `/stats` |
| `/api/search` | pencarian |
| `/api/sort` | pengurutan |
| `/api/analysis` | analisis kompleksitas |
| `/health` | status server |

## Catatan produksi
- Set `SECRET_KEY` lewat environment variable. Nilai bawaan hanya untuk pengembangan.
- `CORS_ORIGINS` bawaan `*`. Batasi ke domain frontend saat deploy.
- Penyimpanan JSON cocok untuk demo, bukan untuk banyak pengguna bersamaan.

## Lisensi
MIT
