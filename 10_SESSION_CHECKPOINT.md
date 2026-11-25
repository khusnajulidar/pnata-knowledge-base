# 10 — Session Checkpoint

**Diperbarui:** 24 November 2026, malam (WIB)
**Fungsi:** titik lanjut untuk sesi Claude berikutnya, termasuk di akun Claude yang berbeda. Perbarui file ini setiap selesai satu tahap kerja; jangan menumpuk banyak versi.

## Cara melanjutkan (untuk Claude di sesi baru)
1. Baca `README.md`, `00_MASTER_INDEX.md`, `05_AI_WORKING_RULES.md`, `08_CLAUDE_PROJECT_SETUP.md`, lalu file ini.
2. Ringkas pemahaman ke pengguna, lalu tanya langkah mana yang dipilih di bagian "Langkah berikutnya".
3. Jangan mengubah repositori sumber kecuali pengguna meminta perubahan spesifik.
4. Bahasa kerja pengguna: Indonesia.
5. Claude di chat web tidak dapat membaca GitHub lewat tautan (akses otomatis diblokir) dan tidak dapat menulis ke GitHub. Minta pengguna mengunggah/menempel file, atau gunakan GitHub di project knowledge (hanya baca). Hasil kerja diserahkan sebagai file untuk ditempatkan pengguna, kecuali pengguna memakai Claude Code (lihat "Alur kerja").

## Sudah dilakukan (sesi 24 Nov 2026)
- Audit baca-saja lima repositori `khusnajulidar/*` (semua publik); selaras dengan `04` dan `06`. Posisi `pnata-knowledge-base`: branch `main`, commit `900da3f`.
- Pilihan (c) (merapikan struktur repo, termasuk mengganti nama `.png.png`) **ditinggalkan sementara** atas permintaan pengguna.
- Pengguna memilih langkah (a): membaca lebih dalam **Petualangan Cinta Rasul**. Bahan: dokumen konsep & progres v1.1, 03/04/05, `tts-pilot-02.html`, dan bank TTS Wilayah 1 v1.0.
- **Audit TTS Pilot 02** (baca kode + skrip; bukan QA browser): persilangan huruf kedua puzzle konsisten (0 konflik, 0 di luar grid, 0 kotak bersebelahan tak disengaja). 14 temuan (lihat bawah).
- **Butir 1 selesai:** tombol ⌫ menghapus huruf terakhir yang diketik (mundur bila kotak aktif kosong); huruf bantuan 💡 yang terkunci tidak terhapus.
- **Butir 2 selesai:** panel PENJELASAN (penjelasan, jenis sumber, rujukan) tampil **hanya setelah jawaban benar** (keputusan pengguna). Panel tetap tampil saat permainan pindah otomatis ke petunjuk berikutnya (mekanik pindah-otomatis tidak diubah) dan disembunyikan bila jawaban berikutnya salah. Isi 13 butir (5 Adik + 8 Kakak) diambil dari bank TTS Wilayah 1 v1.0. Seluruh jawaban di prototipe sama dengan bank. Uji: skrip asli dengan DOM tiruan, kedelapan petunjuk Pilot 02 diselesaikan seperti pemain.
- Berkas hasil: `tts-pilot-02.html` (memuat butir 1 + 2; menggantikan versi sebelumnya). File asli yang diunggah pengguna tidak diubah.
- **Belum ditempatkan pengguna ke repo:** berkas `tts-pilot-02.html` terbaru belum disalin ke `prototipe/tts-pilot-02.html`, `10_SESSION_CHECKPOINT.md` ini belum menggantikan versi lama, dan catatan §12 belum ditambah.

## Temuan audit TTS Pilot 02 (observasi, NEEDS REVIEW — bukan keputusan)
Status: ✔ selesai · ○ belum · — diputuskan/dicatat tanpa tindakan
1. ✔ ⌫ tidak menghapus huruf yang baru diketik.
2. ✔ Penjelasan/sumber setelah jawaban benar. Catatan: nomor hadis/ayat pada data HTML disalin dari bank (mis. Bukhari 3898/3902, Muslim 2276); **belum diverifikasi independen** terhadap sumbernya.
3. ○ Label "WILAYAH 1 · ADIK" tertulis tetap; Pilot 02 (8 petunjuk) = profil Kakak, Pilot 01 (5 petunjuk) = Adik.
4. ○ Latar dan ikon dimuat dari `raw.githubusercontent.com`; konsep menargetkan offline.
5. ○ Di ponsel 375 px grid Pilot 02 ± 417 px vs ruang ± 280 px (hitungan CSS; belum diuji perangkat).
6. ○ Belum ada input keyboard fisik, localStorage, dan bintang.
7. — Petunjuk 3 (BANIHASYIM) di HTML memuat kata "Quraisy" (= jawaban petunjuk 6). Pengguna: tidak jadi masalah. Tidak diubah. Catatan baru: redaksi bank K2 ("…kabilah Bani …") tidak memuat kata itu; teks HTML adalah versi berbeda.
8. — Petunjuk 3 dan 6 menguji hadis yang sama (Muslim 2276); bank memang memuat K1 dan K2 dari hadis itu. Pengguna: tidak jadi masalah.
9. — Empat dari delapan petunjuk Kakak berpusat pada wahyu pertama (HIRA, JIBRIL, KHADIJAH, ALALAQ): ini desain bank terkunci (K3–K6), bukan kekeliruan prototipe.
10. ○ Hanya sebagian petunjuk menyebut rujukan di teks petunjuk (kini dilengkapi panel penjelasan).
11. ○ Daftar ulama bonus berisi 7 nama, bukan 8; paket Kakak butuh 8 pasangan. Status "masih hidup" perlu dicek ulang menjelang rilis.
12. ○ Inkonsistensi dokumen konsep: daftar tautan Berburu Kata muncul dua kali dengan label versi berbeda; teks `\n` mentah; kalimat "bank soal utama belum final" di bagian atas ketinggalan.
13. ○ Prototipe memakai latar dari `desain/eksplorasi-background`, pemilih puzzle, dan tulisan "P'NATA DIGITAL LEARNING" yang belum tercatat di Decision Log/§12; latar belum diperiksa tidak memuat figur manusia.
14. ○ Misi khusus Berburu Kata W2 Adik (± 11 nama Ummahatul Mukminin) vs kuota reguler 6 target belum diputuskan.
15. ○ (baru) Bank TTS W1: judul kunci K2 tertulis "BANUHASYIM" (bagian "Kunci dan penjelasan" dan tabel D) sedangkan tabel C dan HTML memakai **BANIHASYIM**. Aturan bank mewajibkan ejaan kunci konsisten; koreksi bank menjadi BANIHASYIM (menunggu persetujuan pengguna).
- Catatan kecil: nomor petunjuk pada grid Pilot 02 tidak berurutan dari kiri-atas (3, 1, 7, 2, …).

## Belum diverifikasi
- Total 486 commit dan isi branch non-main (termasuk branch fitur Hijaiyah Misi 4).
- Tampilan di browser/perangkat nyata untuk TTS Pilot 02 versi terbaru (butir 1–2 hanya diuji dengan skrip).
- Dalil, lafaz Arab, dan terjemahan di semua materi; nomor hadis pada bank dan data HTML.
- Ekspor percakapan dari empat akun ChatGPT belum diterima.

## Keputusan terbaru (sesi ini)
- Butir 7 dan 8: pengguna menyatakan tidak jadi masalah; petunjuk tidak diubah.
- Panel PENJELASAN hanya setelah jawaban benar.
- Pilihan (c) ditinggalkan sementara; fokus Cinta Rasul.
- Pengguna sedang mempertimbangkan memindahkan pembuatan papan TTS dan Berburu Kata dari Canva ke Claude (kode permainan oleh Claude, bukan GPT). **Belum diputuskan.** Jawaban Claude: secara teknis bisa (papan dibuat sebagai HTML/CSS, susunan dihitung dan divalidasi dengan skrip); ilustrasi bermutu mockup (latar, ornamen, 3D) tetap berasal dari Canva/alat gambar pengguna.
- Lainnya: keputusan di `03_DECISION_LOG.md` dan `05_AI_WORKING_RULES.md` tetap berlaku.

## Alur kerja agar Claude dapat merevisi repo (informasi dari dokumentasi Anthropic, 24 Nov 2026; periksa ulang bila lama)
- **Project knowledge + GitHub (hanya baca):** di Projects, tombol "+" → GitHub → pilih repositori dan file/folder tertentu; hanya nama dan isi file pada satu branch yang disinkronkan (tanpa riwayat commit/PR); muat dalam jendela konteks; pakai "Sync" setelah ada perubahan. Pilih berkas teks/kode (md, html), jangan gambar/audio/ZIP.
- **Claude Code di web (`claude.ai/code`) atau aplikasi desktop:** memilih repositori GitHub, bekerja pada branch baru, lalu mendorong branch dan membuat pull request untuk ditinjau. Membutuhkan GitHub App Claude terpasang di repositori dan akun dengan hak push; ketersediaan per paket langganan perlu dicek.
- **Manual:** buat branch di GitHub → Add file → Upload files → commit → pull request.
- Semua jalur mengikuti aturan pengguna: branch terpisah, tidak ada file dihapus.

## Tindakan untuk pengguna (belum dilakukan)
- Salin `tts-pilot-02.html` terbaru ke `prototipe/tts-pilot-02.html` dan `10_SESSION_CHECKPOINT.md` ini ke root (sebaiknya lewat branch terpisah).
- Tambahkan catatan §12. Usulan teks:
  > **24 November 2026:** Tombol hapus (⌫) pada TTS Pilot 02 diperbaiki agar menghapus huruf terakhir yang diketik. Ditambahkan panel penjelasan yang tampil setelah jawaban benar, berisi penjelasan, jenis sumber, dan rujukan dari Bank TTS Wilayah 1 v1.0 untuk 13 butir (Pilot 01 dan 02). Rujukan disalin dari bank dan belum diverifikasi ulang. Pengujian baru berupa skrip, belum uji browser/ponsel.
- Putuskan koreksi ejaan K2 di bank (butir 15).

## Langkah berikutnya (usulan, belum dipilih pengguna)
- (a) Papan TTS dan Berburu Kata dibuat langsung di Claude. Butuh: bank TTS W2–3, bank Berburu Kata W1–3, dan keputusan arah kata (mendatar/menurun/diagonal per profil) serta ukuran kisi.
- (b) Butir 3: label profil Adik/Kakak mengikuti puzzle yang dipilih.
- (c) Butir 4–5: aset tertanam/lokal dan uji lebar grid di ponsel.
- (d) Butir 11: lengkapi daftar ulama bonus menjadi 8 nama dan verifikasi status.
- (e) Rapikan inkonsistensi dokumen konsep (butir 12) dan ejaan K2 (butir 15).

## Pertanyaan untuk pengguna
- Jika papan TTS dan Berburu Kata dikerjakan di Claude: file bank mana yang akan diunggah lebih dulu?
