# SuaraKu — AI Voice Changer (Prototipe)

Prototipe web berbasis Vue 3 + Vite untuk tugas Implementasi dan Pengujian Perangkat Lunak.

## Fitur yang sudah diimplementasikan

- Memilih 4 preset karakter: Natural, Radio, Deep, dan Bright.
- Meminta izin akses mikrofon melalui browser.
- Memproses input audio menggunakan Web Audio API (filter, gain, dan waveshaper).
- Mengatur intensitas efek audio.
- Menampilkan indikator level input dan durasi sesi.
- Mengaktifkan atau mematikan monitor audio.
- Merekam hasil audio yang telah melewati efek dan mengunduhnya sebagai `.webm`.
- Menghentikan sesi dan melepas stream mikrofon.
- Menampilkan pesan jika izin ditolak atau mikrofon tidak ditemukan.

## Batasan prototipe

Preset saat ini mengubah karakteristik/timbre audio menggunakan efek audio dasar. Ini **belum** merupakan konversi pitch berbasis AI, voice cloning, atau model multi-karakter AI. Kontrol intensitas mengatur kekuatan efek, bukan algoritme pitch-shifting. Fitur tersebut dapat dijadikan pengembangan berikutnya setelah MVP diuji.

## Persyaratan

- Node.js versi LTS yang masih didukung.
- Browser modern dengan dukungan `getUserMedia`, Web Audio API, dan MediaRecorder.
- Mikrofon. Gunakan headphone saat monitor audio aktif untuk mengurangi feedback.

## Cara menjalankan

```bash
npm install
npm run dev
```

Buka URL lokal yang ditampilkan Vite (biasanya `http://localhost:5173`).

Untuk membuat build produksi:

```bash
npm run build
npm run preview
```

Akses mikrofon umumnya memerlukan `localhost` atau HTTPS. Jika browser meminta izin mikrofon, pilih **Allow/Izinkan**.

## Rencana pengujian awal

| ID | Pengujian | Hasil yang diharapkan |
|---|---|---|
| TC-01 | Jalankan aplikasi | Halaman SuaraKu tampil tanpa error |
| TC-02 | Pilih preset karakter | Preset aktif berubah |
| TC-03 | Geser intensitas | Nilai persentase berubah dan efek diperbarui |
| TC-04 | Izinkan mikrofon | Status aktif dan indikator level bergerak ketika ada suara |
| TC-05 | Tolak izin mikrofon | Pesan kesalahan tampil |
| TC-06 | Mulai rekam lalu hentikan | Rekaman tersedia untuk diunduh |
| TC-07 | Simpan rekaman | File `.webm` terunduh |
| TC-08 | Akhiri sesi | Stream mikrofon dihentikan dan status kembali tidak aktif |

## Struktur

```text
suaraku-vue/
├── index.html
├── package.json
├── vite.config.js
└── src/
    ├── App.vue
    ├── main.js
    └── style.css
```

## Mengunggah ke GitHub

Ekstrak ZIP, buka terminal pada folder proyek, lalu jalankan:

```bash
git init
git add .
git commit -m "Implementasi prototipe awal SuaraKu"
git branch -M main
git remote add origin https://github.com/Reiyya10/Voice-changer.git
git push -u origin main
```

Jika folder lokal sudah terhubung ke repository yang benar, **jangan jalankan `git remote add origin` lagi**. Periksa dahulu dengan `git remote -v`. Jika repository lokal yang sudah ada digunakan, salin file proyek ini ke dalam folder repository tersebut, lalu lakukan `git add`, `git commit`, dan `git push`.
