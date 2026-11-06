# Muslimate Website & Static Web Pages for GitHub Pages

Direktori ini berisi seluruh file web statis untuk **Muslimate** (`https://muslimate.app`), yang siap langsung di-*push* ke repository baru untuk di-hosting di **GitHub Pages**.

## Struktur File

```
web_pages/
├── CNAME                         # Domain kustom: muslimate.app
├── index.html                    # Halaman Beranda (Landing Page + Download Google Play)
├── style.css                     # Desain responsif, tipografi Plus Jakarta Sans, palet Muslimate
├── privasi/
│   └── index.html                # Kebijakan Privasi (Sesuai syarat Google Play Data Safety)
├── privasi.html                  # Fallback redirect ke /privasi/
├── bantuan/
│   └── index.html                # Pusat Bantuan & FAQ (Panduan notifikasi adzan, kompas kiblat, dll.)
├── bantuan.html                  # Fallback redirect ke /bantuan/
├── syarat-ketentuan/
│   └── index.html                # Syarat & Ketentuan Layanan (Disclaimer akurasi hisab, kompas, hak cipta)
└── syarat-ketentuan.html         # Fallback redirect ke /syarat-ketentuan/
```

## Cara Deploy ke GitHub Pages

1. **Buat Repository Baru di GitHub**:
   - Buat repo baru (misalnya `muslimate-web` atau `muslimate.github.io`).

2. **Copy / Inisialisasi Git di folder `web_pages`**:
   ```bash
   cd web_pages
   git init
   git add .
   git commit -m "feat: initial commit muslimate static web pages"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo-name>.git
   git push -u origin main
   ```

3. **Aktifkan GitHub Pages**:
   - Masuk ke repo di GitHub > **Settings** > **Pages**.
   - Pada bagian **Build and deployment > Source**, pilih **Deploy from a branch**.
   - Pilih Branch: `main` dan Folder: `/ (root)`, lalu klik **Save**.

4. **Konfigurasi Custom Domain (muslimate.app)**:
   - File `CNAME` sudah otomatis tersedia dengan isi `muslimate.app`.
   - Di DNS provider domain Anda (misal Cloudflare, Niagahoster, Namecheap, dll.), arahkan DNS record:
     - **A Record**:
       - `185.199.108.153`
       - `185.199.109.153`
       - `185.199.110.153`
       - `185.199.111.153`
     - Atau **CNAME Record** untuk subdomain: `<username>.github.io`.
   - Centang **Enforce HTTPS** di GitHub Pages Settings.
