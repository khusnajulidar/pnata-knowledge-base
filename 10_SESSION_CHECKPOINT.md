# 10 — Session Checkpoint

**Diperbarui:** 26 November 2026 (WIB)
**Fungsi:** titik lanjut untuk sesi Claude berikutnya, termasuk di akun Claude yang berbeda. Perbarui file ini setiap selesai satu tahap kerja; jangan menumpuk banyak versi.

## Cara melanjutkan (untuk Claude di sesi baru)
1. Baca `README.md`, `00_MASTER_INDEX.md`, `05_AI_WORKING_RULES.md`, `08_CLAUDE_PROJECT_SETUP.md`, lalu file ini.
2. Ringkas pemahaman ke pengguna, lalu tanya langkah mana yang dipilih di bagian "Langkah berikutnya".
3. Jangan mengubah repositori sumber kecuali pengguna meminta perubahan spesifik.
4. Bahasa kerja pengguna: Indonesia.
5. Akses GitHub: di chat web, tautan GitHub tidak dapat dibuka (akses otomatis diblokir). Bila alat GitHub (MCP) tersedia di sesi, muat dengan pencarian alat, lalu baca/tulis repositori `khusnajulidar/*` **hanya pada branch terpisah, tidak pernah ke `main`, tanpa menghapus file**. Alat tulis tidak punya perintah "ganti teks": seluruh isi berkas harus dikirim ulang. Verifikasi hasilnya dengan membandingkan hash blob Git (`sha1("blob <ukuran>\0" + isi)`) berkas lokal dengan SHA yang dikembalikan GitHub. Membuka diff commit dapat meminta persetujuan pengguna dan bisa gagal ("No approval received"). Tanpa alat GitHub: minta pengguna mengunggah/menempel file, atau pakai GitHub di project knowledge (hanya baca); hasil kerja diserahkan sebagai file.

## Sudah dilakukan (sesi 24–26 Nov 2026)
- Audit baca-saja lima repositori `khusnajulidar/*` (semua publik); selaras dengan `04` dan `06`.
- Pilihan (c) (merapikan struktur repo, termasuk mengganti nama `.png.png`) **ditinggalkan sementara** atas permintaan pengguna.
- Pengguna memilih langkah (a): membaca lebih dalam **Petualangan Cinta Rasul**. Bahan: dokumen konsep & progres v1.1, 03/04/05, `tts-pilot-02.html`, bank TTS Wilayah 1 v1.0.
- **Audit TTS Pilot 02:** persilangan huruf kedua puzzle konsisten (0 konflik, 0 di luar grid, 0 kotak bersebelahan tak disengaja). 16 temuan (lihat bawah).
- **Semua perubahan kode dan bank dikerjakan di branch `claude` pada `pnata-digital-projects` (branch buatan pengguna). Belum ada PR dan belum digabung ke `main`.**
  - Commit `59979f1`: koreksi ejaan K2 di `petualangan-cinta-rasul/materi/wilayah-1-jejak-rasulullah-bank-tts-v1.0.md` (BANUHASYIM → BANIHASYIM, dua kemunculan). Ukuran berkas tetap 10.063 byte. **Diff belum diperiksa** (pembukaan diff gagal "No approval received"); pengguna diminta memeriksa halaman commit.
  - Commit `71528204`: `petualangan-cinta-rasul/prototipe/tts-pilot-02.html` (21.897 byte). Hash blob GitHub `6a9020f7…` **identik** dengan berkas yang diuji.
- Isi commit `71528204`:
  - Layar **pilih profil** Adik/Kakak lebih dulu; tiap profil hanya memuat soalnya sendiri (Adik 5: MUHAMMAD, AMINAH, YATIM, MAKKAH, ABDULLAH; Kakak 8). Pemilih "PILIH PUZZLE" dihapus; label konteks mengikuti profil ("WILAYAH 1 · ADIK/KAKAK"); tombol KEMBALI di dalam permainan kembali ke layar profil.
  - **Keyboard fisik:** huruf (jadi kapital), Backspace (hapus), Enter (periksa), tombol panah (pindah kotak); Ctrl/Cmd/Alt tidak mengetik; Enter pada daftar petunjuk tidak dicegat.
  - Tombol ⌫ menghapus huruf terakhir yang diketik (mundur bila kotak aktif kosong); huruf bantuan 💡 yang terkunci tidak terhapus.
  - Panel PENJELASAN (penjelasan, jenis sumber, rujukan dari bank TTS W1 v1.0) **hanya setelah jawaban benar**; panel tetap tampil saat pindah otomatis ke petunjuk berikutnya dan disembunyikan bila jawaban berikutnya salah.
  - Perbaikan ponsel: halaman tidak lagi melebar melebihi layar (`minmax(0,1fr)` + `min-width:0`); papan bergeser otomatis mengikuti kotak aktif.
- **Pengujian:** skrip logika dengan DOM tiruan (kedua profil diselesaikan penuh dengan keyboard fisik) dan Playwright/Chromium pada lebar 360, 375, 414, 768, 1100 px: tanpa galat JS, lebar dokumen = lebar layar. **Belum diuji di perangkat ponsel sungguhan.** Skrip uji tidak disimpan di repo.
- Nama berkas `tts-pilot-02.html` dipertahankan walau isinya kini berbasis profil (tidak ada file dihapus/diganti nama).

## Temuan audit TTS Pilot 02 (observasi, NEEDS REVIEW — bukan keputusan)
Status: ✔ selesai (di branch `claude`) · ◐ sebagian · ○ belum · — diputuskan/dicatat tanpa tindakan
1. ✔ ⌫ tidak menghapus huruf yang baru diketik.
2. ✔ Penjelasan/sumber setelah jawaban benar. Nomor hadis/ayat disalin dari bank (mis. Bukhari 3898/3902, Muslim 2276); **belum diverifikasi independen**.
3. ✔ Label "WILAYAH 1 · ADIK" tertulis tetap → kini mengikuti profil; alur pilih profil dibuat atas arahan pengguna (Pilot 02 memang belum final dibuat GPT).
4. ○ Latar dan ikon dimuat dari `raw.githubusercontent.com`; konsep menargetkan offline.
5. ✔ Lebar grid di ponsel: ternyata halaman melebar (505 px Kakak / 445 px Adik pada layar 375 px; keyboard dan daftar petunjuk terpotong) — sudah ada pada file asli, kini diperbaiki. Papan masih digeser di dalam wadahnya pada layar sempit; kotak min. 27 px.
6. ◐ Keyboard fisik ✔. Belum ada localStorage dan bintang.
7. — Petunjuk 3 (BANIHASYIM) memuat kata "Quraisy" (= jawaban petunjuk 6). Pengguna: tidak jadi masalah; tidak diubah. Redaksi bank K2 tidak memuat kata itu.
8. — Petunjuk 3 dan 6 menguji hadis yang sama (Muslim 2276); bank memang memuat K1 dan K2 dari hadis itu. Pengguna: tidak jadi masalah.
9. — Empat dari delapan petunjuk Kakak berpusat pada wahyu pertama: desain bank terkunci (K3–K6).
10. ○ Hanya sebagian petunjuk menyebut rujukan di teks petunjuk (kini dilengkapi panel penjelasan).
11. ○ Daftar ulama bonus berisi 7 nama, bukan 8; paket Kakak butuh 8 pasangan. Status "masih hidup" perlu dicek ulang menjelang rilis.
12. ○ Inkonsistensi dokumen konsep: daftar tautan Berburu Kata muncul dua kali dengan label versi berbeda; teks `\n` mentah; kalimat "bank soal utama belum final" di bagian atas ketinggalan.
13. ○ Prototipe memakai latar dari `desain/eksplorasi-background` dan tulisan "P'NATA DIGITAL LEARNING" yang belum tercatat di Decision Log/§12; latar belum diperiksa tidak memuat figur manusia.
14. ○ Misi khusus Berburu Kata W2 Adik (± 11 nama Ummahatul Mukminin) vs kuota reguler 6 target belum diputuskan.
15. ✔ Bank TTS W1: kunci K2 "BANUHASYIM" → BANIHASYIM (commit `59979f1`; menunggu pemeriksaan diff dan penggabungan).
16. ○ KEMBALI dari permainan ke layar profil mereset progres (belum ada penyimpanan); profil Adik masih dapat berpindah ke Kakak lewat layar profil. Penguncian profil menunggu sistem penyimpanan progres.
- Catatan kecil: nomor petunjuk pada grid Kakak tidak berurutan dari kiri-atas (3, 1, 7, 2, …).

## Belum diverifikasi
- Total 486 commit dan isi branch non-main di repositori lain (termasuk branch fitur Hijaiyah Misi 4).
- Tampilan dan sentuhan pada perangkat ponsel nyata untuk TTS (diuji hanya di Chromium desktop dengan lebar ponsel).
- Dalil, lafaz Arab, dan terjemahan di semua materi; nomor hadis pada bank dan data HTML.
- Diff commit `59979f1` (hanya dua baris berubah).
- Ekspor percakapan dari empat akun ChatGPT belum diterima.

## Keputusan terbaru
- Alur permainan: pemain memilih profil Adik/Kakak lebih dulu, lalu masuk ke versi profilnya; **profil Adik tidak membuka soal Kakak dan sebaliknya** (keputusan pengguna 25 Nov). Dibuat dua versi tampilan/soal terpisah.
- Panel PENJELASAN hanya setelah jawaban benar.
- Butir 7 dan 8: tidak jadi masalah; petunjuk tidak diubah.
- Koreksi ejaan K2 → BANIHASYIM disetujui dan dikerjakan.
- Pilihan (c) ditinggalkan sementara; fokus Cinta Rasul.
- Pembuatan papan TTS dan Berburu Kata dari Canva ke Claude: **belum diputuskan.** Secara teknis bisa (papan HTML/CSS, susunan dihitung dan divalidasi skrip); ilustrasi bermutu mockup tetap dari Canva/alat gambar pengguna.
- Lainnya: keputusan di `03_DECISION_LOG.md` dan `05_AI_WORKING_RULES.md` tetap berlaku.

## Tindakan untuk pengguna (belum dilakukan)
- Periksa halaman commit `59979f1` (bank) dan `71528204` (HTML) di branch `claude`, lalu buka pull request ke `main` bila setuju.
- Uji TTS di ponsel sungguhan (profil Adik dan Kakak).
- Tambahkan catatan §12 dokumen konsep Cinta Rasul. Usulan teks:
  > **25 November 2026:** TTS Pilot 02 diubah menjadi alur dua profil: pemain memilih Adik (5 petunjuk) atau Kakak (8 petunjuk) lebih dulu dan tiap profil hanya memuat soalnya sendiri. Ditambahkan input keyboard fisik, perbaikan tombol hapus, panel penjelasan setelah jawaban benar (penjelasan, jenis sumber, rujukan dari Bank TTS Wilayah 1 v1.0; rujukan disalin dari bank dan belum diverifikasi ulang), serta perbaikan tampilan ponsel. Ejaan kunci K2 di bank dikoreksi menjadi BANIHASYIM. Pengujian: skrip dan Chromium (lebar 360–1100 px); belum uji perangkat ponsel.

## Langkah berikutnya (usulan, belum dipilih pengguna)
- (a) Papan TTS dan Berburu Kata dibuat langsung di Claude. Butuh: bank TTS W2–3, bank Berburu Kata W1–3, serta keputusan arah kata (mendatar/menurun/diagonal per profil) dan ukuran kisi.
- (b) Penyimpanan progres (localStorage), bintang, dan penguncian profil (butir 6 dan 16).
- (c) Aset latar/ikon tertanam atau lokal untuk mode offline (butir 4).
- (d) Lengkapi daftar ulama bonus menjadi 8 nama dan verifikasi status (butir 11).
- (e) Rapikan inkonsistensi dokumen konsep (butir 12).

## Pertanyaan untuk pengguna
- Jika papan TTS dan Berburu Kata dikerjakan di Claude: file bank mana yang akan diunggah lebih dulu?
