# 11 — Checkpoint Audit: Hijaiyah, Salat, dan Aset

**Diperbarui:** 25 November 2026
**Fungsi:** titik lanjut untuk sesi audit lintas-repositori (Hijaiyah, Activity Book Salat, aset). Pelengkap `10_SESSION_CHECKPOINT.md`, yang khusus untuk pengerjaan Cinta Rasul oleh sesi Claude lain. Jangan saling menimpa; perbarui file masing-masing.

## Cara kerja sesi ini
- Sumber bukti: API GitHub (baca) dan halaman web publik. Bukan QA browser dan belum ada penilaian visual gambar.
- Perubahan ke repositori hanya lewat branch terpisah dan pull request, atas perintah eksplisit pengguna. Tidak ada commit langsung ke `main`.
- Catatan: butir 5 di `10_SESSION_CHECKPOINT.md` (Claude web tidak dapat menulis ke GitHub) tidak berlaku untuk sesi yang memakai konektor GitHub dengan token terbatas.
- Hierarki sumber mengikuti `05_AI_WORKING_RULES.md`: keputusan terbaru pengguna mengalahkan catatan lama.

## Keputusan dan klarifikasi pengguna (25 Nov 2026)
- ACTIVE: standar gambar makhluk bernyawa **satu untuk semua proyek**: secara asal tidak menggambar manusia/hewan secara utuh; bila karakter dibutuhkan (mis. contoh gerakan salat), gambarkan tanpa wajah dan/atau potong di leher agar kepala dan badan tidak tampak satu kesatuan.
- ACTIVE: watermark P'Nata pada layar game Hijaiyah **disengaja**. Gambar final Activity Book Salat **tanpa** watermark; pengguna menambahkannya manual setelah final (percobaan awal hasil watermark generator tidak sesuai).
- ACTIVE: daftar ulama bonus Cinta Rasul cukup **tujuh** nama.
- Status Salat terbaru dipegang catatan sesi di luar GitHub: H1–4 selesai, H5 direvisi manual, H6 ada draf, H7 direncanakan. Gambar versi terbaru **belum** ada di GitHub; knowledge base (dibuat dari ringkasan lama) perlu direvisi untuk bagian Salat.
- Adab Makan: situs Netlify sudah ada; deploy tertunda karena batas penggunaan. Catatan "hosting rencana Netlify" di `02_PROJECT_HISTORY.md` perlu diperbarui.
- Hijaiyah: rekaman audio baru 29 huruf sudah lengkap di branch `fix/misi4-tahap16-controls-cards` dan sudah didengarkan pengguna. Paket audio lama dihapus dari `main` (lihat bawah).
- Rencana audio Salat: ikon play di PDF dengan tautan per bacaan (GitHub Pages); aktivitas digital tanpa gunting-tempel. Belum ada di repositori.
- `new-folder` adalah repositori saluran transfer berkas (agar dapat dibaca GPT saat batas unggahan tercapai); bukan repositori produk.
- Petualangan Mufrodat Bahasa Arab: game pertama pengguna, sederhana, sudah dipublikasikan lewat Canva. Berkas rujukan: `new-folder/Aset-PNata/Petualangan Mufrodat Bahasa Arab (1).png`. Belum ditinjau isinya.

## Tindakan yang sudah dilakukan di repositori
- `pnata-digital-projects`: PR #1 "Hapus paket audio lama Audio_Seimbang_FINAL" digabung ke `main`, commit gabungan `c38016f` (commit isi: `b3cbcfd` folder, `09ee1b3` zip). Dihapus: folder `petualangan-huruf-hijaiyah/PNata_Petualangan_Hijaiyah_Audio_Seimbang_FINAL/` dan zip-nya. Paket Misi 3, Tahap1_Revisi_UI, README, logo/ikon tidak disentuh. Branch sementara `bersih/hapus-paket-audio-lama` masih ada.
- `pnata-knowledge-base`: file ini ditambahkan lewat branch `checkpoint/audit-20261125`.

## Temuan audit

### pnata-digital-projects
- Fakta: tujuh branch (`main`, `feature/tahap9-misi4-jembatan-urutan`, `feature/tahap10-misi4-controls-audio`, `feature/tahap11-misi4-final-mockup-controls`, `feature/tahap12-misi4-mockup-visual`, `fix/misi4-tahap16-controls-cards`, `test/github-integration-check-20261112`). Ujung `fix/...` = `913849a` (17 Nov); sebelum PR #1, `main` memuat 363 commit yang tidak ada di `fix` dan `fix` memuat 110 yang tidak ada di `main`.
- Fakta: `test/github-integration-check-20261112` sudah terjangkau dari `main`. Lima branch lain belum digabung.
- Fakta (branch `fix`, 14–17 Nov): Misi 5 "Istana Juara" (tujuh mockup di `petualangan-huruf-hijaiyah/assets/mockup/misi-5-istana-juara/`, integrasi mulai `886b005`), peta misi berurutan (`2ae5a6f`), watermark di setiap layar game (`36ffab0`), `index.html` kanonik di `petualangan-huruf-hijaiyah/index.html` (berasal dari `index_finalisasi_visual_tahap15.html`), aset merek dipindah ke `assets/brand/` dan `docs/brand/`, folder `original` audio dihapus, audio baru di `assets/audio/nama/01-29.mp3`.
- Fakta: README branch `fix` menyatakan `index.html` sebagai berkas utama, tetapi gambar strukturnya masih menyebut `audio/original/` yang sudah tidak ada (perlu dirapikan).
- Perlu verifikasi: ke-29 berkas `assets/audio/nama/` berukuran persis sama (40.801 byte) dengan hash berbeda; pengguna sudah mendengarkan dan menyatakan rekaman lengkap, jadi dianggap wajar (durasi/bitrate seragam).
- Belum terjawab: apakah Tahap 9–12 tercakup di `fix`. Dari 110 commit khusus `fix`, tidak ada judul Tahap 9–12. Cara cek: bandingkan `fix/misi4-tahap16-controls-cards...feature/tahap12-misi4-mockup-visual` di GitHub.
- Risiko: menggabungkan `fix` ke `main` membawa Misi 5, `index.html` kanonik, audio baru, dan memindahkan aset merek. Belum diputuskan.

### pnata-activity-book (main; 32 commit, semuanya 13 Nov 2026)
- Fakta: folder halaman hanya H1–H4, masing-masing satu PNG sekitar 2 MB (`page-01-cover.png`, `page-02-waktu-salat.png`, `page-03-persiapan-salat.png`, `page-04-gerakan-salat-revisi.png`), diunggah 13 Nov 09:37–09:38 UTC (`e077416`, `2d3181e`, `4fc6083`, `85042c2`). Tidak ada H5–H10.
- Fakta: lingkup Salat saja (`a560613`, Wudhu dikeluarkan).
- Konflik dokumen: README tujuan dan `02_PROJECT_HISTORY.md` menyebut empat gambar belum dimigrasikan; faktanya sudah ada (versi 13 Nov). README `page-04` masih menyuruh mengunggah berkas padahal berkas sudah ada.
- Konflik standar: `PROJECT_GUIDE.md` dan `CHANGELOG.md` (13 Nov) menulis karakter manusia tanpa mata dan alis diperbolehkan; standar pengguna lebih ketat (lihat Keputusan). Teks repositori belum diselaraskan.
- Belum diverifikasi: apakah gambar tersimpan bebas watermark (commit `5e05d45`, `cadfef3`, `4625055` hanya mencatat permintaan).

### pnata-belajar-salat (sumber/arsip)
- Fakta: `pages/page-01..04` berisi gambar berekstensi ganda `.png.png` (ukuran H1 dan H4 sama dengan salinan tujuan); `page-05..10` kosong; `exports/final/` hanya README; `assets/illustrations/` hanya `.gitkeep` dan README.

### new-folder
- Fakta: `Belajar Wudhu sesuai Sunnah.pdf` adalah **folder** berisi 12 PNG (bukan berkas PDF). Sesuai keputusan, tidak dimigrasikan ke Activity Book.
- Fakta: `Aset-PNata/1.png, 2.png, 3.png, 6.png, 10.png` berukuran sama dengan halaman Wudhu bernomor sama tetapi hash berbeda: **bukan salinan identik**; jangan dihapus sebelum dibandingkan secara visual.
- Fakta: ada folder bernama sangat panjang dari teks teka-teki Cinta Rasul ("Down 1. Nama Rasulullah ..."), berisi 4 PNG kecil; tampak kesalahan penamaan.
- Fakta: `P-Nata_Visual_Identity_Guide_v1.0.md` (14.278 byte) dan `PNata_Ikon_HQ_4x.png` dirujuk knowledge base; jangan dipindah atau dihapus tanpa memperbarui rujukan.
- Belum diketahui isi: `image.png`, `image1.jpg` s.d. `image6.jpg`.
- Rencana: rapikan secara bertahap (ganti nama folder panjang dan folder `.pdf`; bandingkan PNG bernomor) hanya dengan persetujuan per butir.

## Dokumen knowledge base yang perlu direvisi (belum diubah)
- `04_PROGRESS_STATUS.md`: status Salat (H1–4 selesai, H5–H7), Adab Makan (deploy tertunda batas), Hijaiyah (Misi 5, `index.html` kanonik di `fix`).
- `09_GIT_HISTORY_AND_BRANCHES.md`: tambahkan Misi 5, PR #1, dan hasil perbandingan `main`/`fix`.
- `02_PROJECT_HISTORY.md`: Netlify, migrasi gambar Salat, Misi 5.
- `03_DECISION_LOG.md`: standar gambar tunggal, watermark per produk, tujuh ulama.
- `07_OPEN_QUESTIONS.md`: coret butir yang sudah terjawab (jumlah ulama, Netlify, status PDF Wudhu, branch Hijaiyah sebagian).

## Belum diverifikasi
- `adab-makan/` dan `petualangan-cinta-rasul/` di `main` (isi file dan commit) pada sesi audit ini; lihat `10_SESSION_CHECKPOINT.md` untuk Cinta Rasul.
- Tahap 9–12 vs `fix`; QA browser Hijaiyah (responsif, audio, perangkat nyata); dalil, lafaz, dan terjemahan semua materi; status final bank 126 butir.
- Tinjauan Mufrodat Bahasa Arab (tautan Canva belum diterima).

## Langkah berikutnya (usulan)
1. Baca `adab-makan/` dan `petualangan-cinta-rasul/` di `main`, lalu susun laporan akhir (merek, sejarah, status, keputusan, konflik, prioritas).
2. Cek Tahap 9–12 vs `fix`.
3. Usulan teks revisi dokumen 02/03/04/07/09 untuk ditinjau pengguna.
4. Rapikan `new-folder` per butir dengan persetujuan.
5. Tinjau Mufrodat setelah tautan diterima.

## Pembagian kerja dua akun Claude (disepakati sebagai usulan)
- Satu branch per proyek per akun, awalan `hijaiyah/`, `cinta-rasul/`, dst.; tidak ada dua akun menulis ke branch yang sama; perubahan ke `main` lewat PR.
- Berkas bersama (README akar, indeks knowledge base) diubah bergantian.
- Setiap akun menutup sesi dengan memperbarui checkpoint masing-masing.
