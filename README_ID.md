# HILLCRYPT PWA — Panduan Deploy

Paket ini membuat **pintu masuk PWA bermerek HILLCRYPT**. Mesin aplikasi, algoritma, dan seluruh fitur tetap berjalan pada aplikasi Streamlit yang sudah ada:
https://hillcrypt-mamay.streamlit.app

## Deploy gratis melalui GitHub Pages

1. Ekstrak ZIP ini di komputer.
2. Buka GitHub dan buat repository baru bernama `HILLCRYPT-PWA`.
3. Atur repository menjadi **Public**.
4. Upload seluruh ISI folder `HILLCRYPT_PWA` ke root repository (pastikan `index.html`, `manifest.webmanifest`, dan `sw.js` berada langsung di root).
5. Klik **Settings** pada repository.
6. Buka **Pages** di menu kiri.
7. Pada **Build and deployment**, pilih **Deploy from a branch**.
8. Pilih branch `main`, folder `/(root)`, lalu klik **Save**.
9. Tunggu proses publikasi selesai. URL biasanya berbentuk:
   `https://USERNAME.github.io/HILLCRYPT-PWA/`
   Ganti `USERNAME` dengan nama akun GitHub pemilik repository.
10. Buka URL tersebut melalui Chrome Android. Dari menu titik tiga pilih **Install app** atau **Add to Home screen**. Pada iPhone, buka melalui Safari → Share → Add to Home Screen.

## Catatan penting

- PWA ini adalah pembungkus/launcher bermerek HILLCRYPT, bukan aplikasi Android APK native.
- Konten HILLCRYPT tetap dimuat dari Streamlit Cloud; koneksi internet diperlukan.
- Jangan menghapus atau mengubah repository Streamlit `HILLCRYPT` yang sudah berjalan.
- Jangan mengaktifkan cache untuk konten iframe Streamlit. Service worker dalam paket ini hanya menyimpan shell PWA dan ikon.
- GitHub Pages harus selesai menerbitkan situs HTTPS sebelum instalasi PWA tersedia.
- Nama/ikon khusus dikendalikan oleh `manifest.webmanifest`; dukungan tampilan instalasi dapat berbeda antar-browser dan OS.
