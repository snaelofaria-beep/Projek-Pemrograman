# Mendeskripsikan Dunia

AI Tutor Teks Deskripsi berbasis kode Mutiara.

## Jalankan
1. Ekstrak seluruh ZIP; jangan hanya menjalankan app.py terpisah.
2. Buka terminal di folder Mendeskripsikan_Dunia.
3. Jalankan `python -m pip install -r requirements.txt`.
4. Salin `.streamlit/secrets.toml.example` menjadi `.streamlit/secrets.toml`; isi kunci API dan kode guru. Alternatif: variabel lingkungan dengan nama yang sama. Jangan bagikan kunci API kepada siswa.
5. Jalankan `python -m streamlit run app.py`.
6. Daftar akun siswa dengan ID unik dan kata sandi minimal delapan karakter. Akun guru membutuhkan kode guru yang dikonfigurasi pengelola. Pilih Masuk setelah pendaftaran.

## Fitur
Materi lengkap, tujuan, capaian, contoh, memahami isi, unsur bahasa, dua versi struktur, kaidah kebahasaan, latihan uraian, kuis 40 soal, evaluasi/refleksi, umpan balik AI, chat, referensi, favorit, catatan, absensi, progress, dashboard guru serta ekspor CSV. Semua materi dibundel; tidak membutuhkan upload ulang. Kunci evaluasi tidak masuk pencarian/chat siswa.

Batas 100 permintaan per akun berlaku sepanjang penggunaan; percakapan dan umpan balik memakai kuota sama. Login ulang atau menghapus tampilan chat tidak mereset kuota. Permintaan API gagal dikembalikan kuotanya. Kuis, materi, dan refleksi tetap dapat digunakan setelah kuota habis.

Tanpa API, chat mengambil kutipan materi lokal dan menandainya dengan jelas; ini bukan percakapan generatif. Dengan API, tutor menerima konteks percakapan serta materi relevan dan dapat memberikan contoh serta umpan balik. API memiliki biaya tersendiri. Koneksi/model API belum diuji langsung.

Data akun disimpan di SQLite; catatan, nilai lengkap, refleksi dan riwayat tersimpan di data_app. Pertahankan folder ini dan gunakan penyimpanan server persisten agar data tidak hilang ketika hosting dimulai ulang. Dashboard guru mencakup seluruh siswa pada instalasi tersebut. Aplikasi cocok untuk prototipe kelas; belum mencakup pengelompokan kelas, pemulihan kata sandi, atau pengelolaan pengguna massal.

Materi dan sitasi dipertahankan dari berkas pengguna dan belum divalidasi bibliografis. Capaian dalam berkas pengguna ditampilkan sebagai materi yang diberikan, bukan klaim verifikasi regulasi terbaru. Panduan memahami isi adalah tambahan kegiatan dari bahan terlampir. Umpan balik AI bersifat formatif; guru menetapkan nilai resmi.

## Pembaruan interaktif
- Panduan siswa/guru di aplikasi.
- Studio Ide: inspirasi acak, peta ide, brainstorming mandiri/AI.
- Bengkel Menulis: kerangka, draf, checklist, saran AI, revisi dan alasan perubahan.
- Tantangan Pancaindra: 5 contoh buatan dengan umpan balik langsung.
- Portofolio: simpan dan unduh karya, bandingkan draf/revisi.
- Guru dapat membaca aktivitas/portofolio dan absensi serta mengekspor rekap.
- Absensi menggunakan waktu Asia/Jakarta.

Jika memperbarui instalasi lama, cadangkan data_app terlebih dahulu, lalu pertahankan folder itu ketika mengganti kode dan materi. Pertahankan pula secrets.toml milik pengelola.
