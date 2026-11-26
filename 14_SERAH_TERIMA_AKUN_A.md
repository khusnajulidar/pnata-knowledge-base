# 14 — Serah-terima Akun A (26 November 2026)

**Fungsi:** titik lanjut untuk chat baru pada akun yang sama (akun A: Hijaiyah, Activity Book Salat/Wudhu, audit aset). Pelengkap `11_SESSION_CHECKPOINT_AUDIT.md`. Perbarui atau gantikan berkas ini di akhir sesi berikutnya; jangan menimpa `10_SESSION_CHECKPOINT.md` (milik akun B).

## Baca dulu (urutan)
`README.md`, `00_MASTER_INDEX.md`, `05_AI_WORKING_RULES.md`, `03_DECISION_LOG.md`, `12_POLA_KERJA_DUA_AKUN.md`, `13_SUMBER_RUJUKAN.md`, `11_SESSION_CHECKPOINT_AUDIT.md`, lalu berkas ini. Ringkas pemahaman ke pengguna dan tanyakan langkah berikutnya (satu pertanyaan).

## Cara kerja (ringkas, rincian di 12)
- Perubahan lewat branch dan pull request; commit langsung ke `main` hanya bila pengguna menulis izinnya untuk perubahan tertentu.
- Tidak menghapus apa pun tanpa izin eksplisit. Tidak mengklaim "selesai/diuji" tanpa bukti. Tidak mengarang dalil, teks Arab, nomor hadis.
- Pengguna awam pemrograman: beri langkah satu per satu, bahasa Indonesia sederhana. Konektor GitHub harus diaktifkan di chat baru (menu alat); token milik pengguna, jangan diminta di chat.
- Pembuatan PR lewat alat menampilkan formulir yang harus disubmit pengguna; bila tidak tampil, pengguna membuat PR dari halaman *Branches* GitHub.

## Status pekerjaan per 26 Nov 2026

### Audio dzikir setelah wudhu (Belajar Wudhu sesuai Sunnah)
- Branch `wudhu/audio-dzikir-setelah-wudhu` di `pnata-digital-projects` (turunan `main` `c38016f`): halaman pemutar `activity-book-wudhu/audio/dzikir-setelah-wudhu/index.html` (commit `99db4e4`) dan `dzikir-setelah-wudhu.mp3` (211.955 byte, diunggah pengguna; 8,8 detik, 192 kbps). PR belum digabung.
- Belum: gabungkan branch ke `main`, aktifkan GitHub Pages (Settings, Pages, deploy dari branch `main`, folder root) di `pnata-digital-projects`, lalu uji alamat `https://khusnajulidar.github.io/pnata-digital-projects/activity-book-wudhu/audio/dzikir-setelah-wudhu/` (belum diuji) di HP.
- PDF dengan ikon: dibuat di sesi sebelumnya (file tidak tersimpan di GitHub). Cara membuat ulang dari PDF asli (12 halaman gambar, 791,25 x 1118,25 pt, MediaBox terbalik `[0 1118.25 791.25 0]` yang harus dinormalkan ke `[0 0 W H]` pada halaman 9 sebelum menempel ikon dan tautan): ikon bulat teal `#13A89E` bergaris putih di pojok kanan atas kotak Arab halaman 9; pusat x = 0,9136 x lebar, y dari atas = 0,2382 x tinggi, radius = 0,03636 x lebar; area tautan 1,3 x radius; tautan URI ke alamat di atas. Penempatan ikon disetujui pengguna.
- Catatan: putar otomatis dapat diblokir peramban HP; anak mungkin perlu mengetuk tombol besar. Tautan di PDF membuka peramban (meninggalkan aplikasi PDF sebentar). Bacaan audio perlu diperiksa pengguna/pemeriksa berilmu; rujukan "HR. Muslim no. 234b" di halaman 9 berstatus NEEDS VERIFICATION.

### Hijaiyah (pnata-digital-projects)
- Temuan Tahap 9-12: `index_finalisasi_visual_tahap12.html` di branch Tahap 12 identik dengan `main`; `tahap9/10/11.html` hanya ada di branch masing-masing (versi antara), `main` punya tahap13-15. Branch jangan dihapus dulu.
- Langkah 2 berjalan: PR `fix/misi4-tahap16-controls-cards` ke `main` (formulir ditampilkan, belum dipastikan dibuat). Penggabungan akan menghapus dari `main` paket Misi 3 (folder, zip, varian `index_finalisasi_visual_tahap*.html`) dan zip `Tahap1_Revisi_UI` (tetap ada di riwayat). Periksa status mergeable; `main` dan `fix` bercabang jauh (363/110 commit sebelum PR #1). Gabungkan hanya atas perintah pengguna.
- Langkah 3: hosting alternatif Netlify (kredit habis), mis. GitHub Pages bila memenuhi syarat (periksa ketentuan terbaru). Langkah 4: uji di HP (suara, sentuhan, layar). README branch `fix` masih menyebut folder `audio/original` yang sudah tidak ada.

### Lain-lain
- `13_SUMBER_RUJUKAN.md` sudah ada di `main`. Daftar situs yang diizinkan masih kosong (diisi pengguna). Indeks (`00_MASTER_INDEX.md`) belum memuat berkas 13 dan 14.
- `new-folder`: rapikan bertahap atas persetujuan per butir (jangan hapus PNG bernomor di `Aset-PNata/` sebelum dibandingkan visual; hash berbeda dari halaman Wudhu).
- Petualangan Mufrodat Bahasa Arab (Canva): menunggu tautan untuk ditinjau.
- Pemeriksaan akhir materi agama oleh orang berilmu sudah ada dalam program pengguna.
- Token GitHub berizin tulis pernah dibuat; kembalikan ke baca-saja atau cabut setelah pekerjaan menulis selesai. Branch sementara (`bersih/...`, `kolaborasi/...`, `indeks/...`, `checkpoint/...`, `rujukan/...`) boleh dihapus pengguna kapan saja.

## Prompt pembuka yang disarankan untuk chat baru
"Bismillah. Lanjutkan pekerjaan P'Nata. Baca di GitHub `pnata-knowledge-base` (README, 05, 03, 12, 13, 11, dan 14_SERAH_TERIMA_AKUN_A.md; bila berkas 14 belum di main, baca di branch `handoff/akun-a-20261126`). Ringkas pemahamanmu, lalu tanyakan satu langkah berikutnya. Jangan mengubah repositori tanpa izinku."
