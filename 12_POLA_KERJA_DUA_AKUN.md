# 12 — Pola Kerja Dua Akun Claude

**Disepakati pengguna:** 25 November 2026
**Fungsi:** aturan kerja agar dua sesi/akun Claude dapat bekerja di GitHub yang sama tanpa saling menimpa. Berlaku bersama `05_AI_WORKING_RULES.md`; bila ada konflik, keputusan eksplisit pengguna yang terbaru menang.

## Pembagian lahan (usulan awal, ubah hanya atas arahan pengguna)
- Akun B: Petualangan Cinta Rasul (`pnata-digital-projects/petualangan-cinta-rasul/`).
- Akun A: Petualangan Huruf Hijaiyah, Activity Book Salat, dan audit aset.
- Adab Makan: belum ditugaskan; tanyakan pengguna sebelum menyentuhnya.
- Jangan mengubah folder proyek yang dipegang akun lain.

## Branch
- Satu branch per proyek per akun. Awalan yang disarankan: `cinta-rasul/...`, `hijaiyah/...`, `salat/...`, `bersih/...`, `kolaborasi/...`.
- Dua akun tidak menulis ke branch yang sama.
- Tidak ada commit langsung ke `main`. Semua perubahan lewat branch dan pull request; pengguna memutuskan penggabungan (atau menyetujui penggabungan secara eksplisit).
- Tidak ada penghapusan tanpa izin pengguna; penghapusan pun lewat branch dan PR dengan daftar yang jelas.

## Berkas bersama
Contoh: `README.md` akar, `00_MASTER_INDEX.md`, `03_DECISION_LOG.md`, `04_PROGRESS_STATUS.md`, `07_OPEN_QUESTIONS.md`, `09_GIT_HISTORY_AND_BRANCHES.md`, `index.html` di akar proyek, aset bersama.
- Ubah hanya atas izin pengguna, satu akun pada satu waktu.
- Baca versi terbaru dan catat SHA sebelum mengubah; jangan menimpa perubahan akun lain.

## Serah-terima
- Setiap akun memelihara checkpoint sendiri: `10_SESSION_CHECKPOINT.md` (Cinta Rasul) dan `11_SESSION_CHECKPOINT_AUDIT.md` (Hijaiyah, Salat, aset). Perbarui di akhir tiap tahap; jangan menumpuk banyak versi dan jangan menimpa checkpoint akun lain.
- Catat provenance: repo, path, branch, commit, tanggal.
- Jangan mengklaim "selesai" atau "sudah diuji" tanpa bukti (lihat `05_AI_WORKING_RULES.md`).
- Sesi baru membaca: `README.md`, `00_MASTER_INDEX.md`, `05_AI_WORKING_RULES.md`, `03_DECISION_LOG.md`, checkpoint miliknya, lalu checkpoint akun lain; meringkas pemahaman ke pengguna dan menanyakan langkah berikutnya.

## Keputusan inti yang berlaku lintas akun (ringkas)
- Standar gambar makhluk bernyawa satu untuk semua proyek: pada dasarnya tidak digambar utuh; bila perlu, tanpa wajah dan/atau dipotong di leher.
- Watermark P'Nata disengaja di layar game Hijaiyah; gambar final Activity Book Salat tanpa watermark (ditambah manual oleh pengguna).
- Daftar ulama bonus Cinta Rasul: tujuh nama.
- Mockup adalah template visual berkualitas; jangan mengarang dalil, teks Arab, atau nomor hadis.

## Akses GitHub
- Tiap akun memakai kredensial sendiri dengan izin sesempit mungkin dan masa berlaku pendek; token dicabut atau dikembalikan ke baca-saja setelah pekerjaan menulis selesai.
- Token dan kredensial tidak pernah ditempel ke chat atau disimpan di repositori.
- Alternatif bila konektor tidak tersedia: unggah manual lewat branch, atau Claude Code.
