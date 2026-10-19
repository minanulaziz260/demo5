# Undangan Digital Pernikahan - Habib & Adiba (Spesial 01)

Website undangan pernikahan digital interaktif dan responsif, hasil kloning dan rekonstruksi (Reverse Engineering) lengkap dari:
**`https://inv.punakawandigital.id/spesial-01/`**

---

## 🌟 Fitur & Keunggulan

1. **100% Offline & Standalone Ready**:
   - Seluruh aset (CSS, JavaScript, Google Fonts, Bisdev custom fonts, Icon FontAwesome, Gambar resolusi tinggi, dan Audio background) disimpan secara lokal di folder `assets/`.
   - Tidak ada dependensi eksternal yang memblokir rendering halaman.
2. **Sampul Interaktif & Tirai Pembuka**:
   - Animasi tirai cover slide-up saat tombol **"Buka Undangan"** diklik.
   - Efek musik langsung berputar otomatis (autoplay) saat dibuka.
3. **Pemutar Musik Latar (Background Music Player)**:
   - Floating disc button di pojok kanan bawah yang berputar saat musik diputar.
   - Kontrol Play / Pause, pause otomatis saat tab diminimize/pindah halaman, dan resume otomatis saat kembali.
   - Lagu: *Tiara Andini & Arsy Widianto - Lagu Pernikahan Kita*.
4. **Personalisasi Nama Tamu Dinamis via URL**:
   - Mendukung parameter URL `?to=Nama+Tamu` (contoh: `index.html?to=Bapak+Joko+&+Ibu`).
   - Secara otomatis memperbarui teks nama tamu di sampul undangan dan kolom nama formulir RSVP.
5. **Amplop Digital & Copy Nomor Rekening**:
   - Tombol **"Klik Disini"** untuk membuka detail rekening bank dan alamat pengiriman kado.
   - Tombol **"Copy"** rekening dengan fitur salin clipboard otomatis dan indikator pesan *"Disalin!"*.
6. **Buku Tamu / Ucapan & Doa (RSVP) Offline Support**:
   - Komentar bawaan telah tersemat langsung di halaman.
   - Pengunjung dapat mengisi nama, konfirmasi kehadiran (*Hadir* / *Tidak Hadir*), dan doa restu.
   - Ucapan baru langsung muncul seketika di daftar ucapan dan disimpan di `localStorage` peramban.
7. **Galeri Foto & Love Story Timeline**:
   - Tampilan foto grid/slider mempelai yang estetik.
   - Cerita perjalanan cinta (timeline) dengan ikon cincin dan hati.
8. **Hitung Mundur (Countdown Timer)**:
   - Countdown otomatis menuju hari bahagia pernikahan.
9. **Desain Mobile-First & Responsif**:
   - Tampilan rapi dan optimal untuk smartphone (Android & iPhone) maupun layar laptop/desktop.

---

## 📁 Struktur File & Folder

```
undangan_spesial_01/
├── index.html                 # Halaman utama undangan web
├── README.md                  # Dokumentasi panduan penggunaan & kustomisasi
└── assets/
    ├── audio/                 # File musik latar (MP3)
    ├── css/                   # Seluruh stylesheet (Elementor, Bisdev, Hello theme, Animations)
    ├── fonts/                 # Webfont lokal (.woff2, .woff, .ttf, .eot)
    ├── images/                # Foto mempelai, background watercolor, floral frame, ikon bank
    └── js/                    # Script interaktif (jQuery, Elementor Frontend, Reveal, RSVP, Music)
```

---

## 🚀 Cara Menjalankan

### Cara 1: Buka Langsung di Browser
Cukup klik dua kali (double-click) file `index.html` menggunakan browser apa pun (Google Chrome, Microsoft Edge, Safari, Firefox).

### Cara 2: Menjalankan via Local Web Server (Disarankan untuk pengujian penuh)
Buka terminal pada folder ini, lalu jalankan:
```bash
# Menggunakan Python
python3 -m http.server 8080

# Atau menggunakan Node.js
npx serve .
```
Lalu buka di browser: `http://localhost:8080/index.html?to=Nama+Tamu`

---

## ✏️ Panduan Kustomisasi

### 1. Mengubah Nama Tamu pada Tautan
Cukup tambahkan query string `?to=` di akhir URL:
- `https://domain-anda.com/?to=Bapak+Ahmad+Keluarga`
- `https://domain-anda.com/?to=Sahabat+Tercinta`

### 2. Mengubah Nama Pengantin & Tanggal Acara
Buka file `index.html` dengan text editor (VS Code, Notepad, dll.):
- Cari kata **"Habib"** dan **"Adiba"**, ganti dengan nama pasangan yang diinginkan.
- Cari tanggal **"Senin, 28 Desember 2026"**, ganti dengan tanggal acara pernikahan baru.

### 3. Mengubah Rekening Bank & Alamat Kado
- Cari teks `12345678` di `index.html`, ganti dengan nomor rekening Anda.
- Ganti teks nama bank (*BCA / Mandiri / BRI*) dan nama pemilik rekening.
- Ganti alamat kirim kado pada bagian `idb-kirim-hadiah`.

### 4. Mengganti Lagu Musik Latar
Simpan file MP3 baru Anda di folder `assets/audio/`, lalu pada `index.html` sesuaikan nama file pada tag `<audio>` atau ubah nama file MP3 baru Anda menjadi sama dengan yang ada di folder audio.

---

## 🌐 Panduan Upload / Hosting

Website ini murni berformat **HTML, CSS, dan JS statis**, sehingga dapat dihosting gratis di:
- **GitHub Pages**
- **Vercel**
- **Netlify**
- **Cloudflare Pages**
- Atau hosting cPanel biasa (upload semua isi folder ini ke `public_html`).
