# LOYALTY ILHAM

**ACADEMIC WORKSPACE** — Edit. Refine. Format. Finish.

Aplikasi web untuk menyunting dan merapikan dokumen akademik. Versi ini tidak memakai API AI atau API key. Semua pemrosesan teks berjalan di browser dengan aturan bahasa dan kamus.

## Fitur yang sudah ada
- Landing page, dasbor, dan navigasi
- Editor dokumen (bold, italic, underline, heading, perataan, urungkan/ulangi, hitung kata, simpan otomatis)
- Unggah file TXT
- Pengaturan font, ukuran, spasi, dan margin dengan pratinjau di editor
- Text Refinery: deteksi frasa klise, kalimat panjang, kata berulang, spasi ganda; terima/tolak revisi; pulihkan teks asli
- Dokumen Saya: cari, buka, ganti nama, gandakan, hapus (disimpan di localStorage browser)
- Tema terang/gelap dan nama universitas
- Unggah logo universitas (PNG/JPG), atur lebar dan posisi
- Struktur akademik pada DOCX (bisa dimatikan di panel Editor): cover tanpa nomor, halaman romawi mulai ii sampai Daftar Isi, angka 1 dimulai dari heading "BAB I", daftar isi otomatis dari heading
- Ekspor DOCX (heading asli, margin, font, spasi, nomor halaman, logo), PDF (lewat dialog cetak browser: pilih Simpan sebagai PDF), dan PPTX (slide dari heading dan paragraf)

## Cara memakai struktur akademik
1. Tulis tiap bab dengan tombol **Judul** (misalnya "BAB I PENDAHULUAN") dan subbab dengan **Subjudul**.
2. Isi sebelum BAB I (misalnya Kata Pengantar) masuk ke bagian halaman romawi.
3. Ekspor DOCX, buka di Word, lalu klik **Ya** saat Word meminta memperbarui field agar daftar isi dan nomor halamannya terisi. Bisa diperbarui lagi lewat klik kanan pada daftar isi > Update Field.
4. Jika heading "BAB I" tidak ditemukan, seluruh isi dihitung sebagai halaman 1 dan seterusnya.
5. Penomoran romawi dan daftar isi belum ada pada ekspor PDF (cetak browser). Untuk PDF akademik, simpan PDF dari Word setelah daftar isi diperbarui.

## Belum tersedia
- Unggah DOCX dan ekstraksi pedoman PDF
- Editor slide (ubah urutan, tambah/hapus slide) sebelum ekspor PPTX
- Template kampus dan kamus parafrase yang lengkap

## Menjalankan
Tidak perlu instalasi. Buka `index.html` di browser, atau jalankan server lokal:

```
python3 -m http.server 8000
```

Lalu buka http://localhost:8000.

## Deploy ke GitHub Pages
Letakkan folder ini di repository, lalu aktifkan Pages di Settings > Pages. Jika repository sudah punya `index.html` lain, taruh file ini di subfolder (misalnya `loyalty-ilham/`) agar tidak menimpa aplikasi yang ada.

## Catatan
- Data dokumen tersimpan hanya di browser pengguna.
- Tidak ada environment variable yang diperlukan.
- Ekspor DOCX dan PPTX memuat library docx dan PptxGenJS dari CDN jsDelivr, jadi butuh internet.
- Logo hanya tampil di hasil ekspor (bagian atas halaman pertama), bukan di pratinjau editor.
- Font dimuat dari Google Fonts; tanpa internet, tampilan memakai font cadangan sistem.

Pesan commit yang disarankan: `feat: build loyalty ilham academic workspace MVP`
