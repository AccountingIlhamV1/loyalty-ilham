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

## Belum tersedia
- Ekspor DOCX, PDF, dan PPTX
- Unggah DOCX, logo universitas, ekstraksi pedoman PDF
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
- Font dimuat dari Google Fonts; tanpa internet, tampilan memakai font cadangan sistem.

Pesan commit yang disarankan: `feat: build loyalty ilham academic workspace MVP`
