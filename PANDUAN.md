# Stok Dinar — Panduan

Aplikasi pencatat stok emas (Dinar KR, MR Gold, emas gram). Jalan **tanpa internet**, data tersimpan di masing-masing perangkat.

## Isi folder
| File | Fungsi |
|---|---|
| `index.html` | Aplikasinya (semua ada di file ini) |
| `sw.js`, `manifest.webmanifest`, `icon*.png/svg` | Agar bisa di-install di HP & jalan offline |

## Cara memasang

### Komputer (cara paling cepat)
Klik dua kali `index.html` → terbuka di Chrome/Edge/Safari. Langsung bisa dipakai tanpa internet.
> Selalu buka dengan browser yang sama, karena data tersimpan di browser itu.

### HP (Android / iPhone)
HP perlu membuka aplikasi **sekali** lewat alamat web (https). Setelah itu bisa offline selamanya.
1. Unggah isi folder ini ke hosting gratis, misalnya **Netlify Drop** (app.netlify.com/drop — tinggal seret folder) atau GitHub Pages.
2. Buka alamatnya di HP:
   - **Android (Chrome):** menu ⋮ → *Tambahkan ke layar utama / Install aplikasi*.
   - **iPhone (Safari):** tombol Bagikan → *Tambah ke Layar Utama*.
3. Selesai. Ikon "Stok Dinar" muncul di HP, bisa dibuka tanpa internet.

> Hosting hanya menyimpan **file aplikasi**, bukan data emas Anda. Data tetap hanya ada di perangkat.

## Pemakaian harian
- **Emas Masuk / Keluar:** pilih ukuran (ketuk kotaknya), atur jumlah, Simpan. "Simpan & tambah lagi" untuk mencatat beberapa jenis sekaligus.
- **Harga Hari Ini:** form otomatis terisi harga terakhir — ubah yang berubah saja, lalu Simpan.
  Bisa juga **📋 Tempel teks harga**: salin daftar harga dari WhatsApp/dinarkr.com, tempel, harga terisi sendiri.
- **Beranda:** total emas dalam **gram** atau **Dinar** (1 Dinar = 4,25 g), nilai rupiah (buyback & harga beli).
- **Laporan:** pilih periode, lihat grafik nilai & harga, tekan **Ekspor Excel**.

Harga emas lain (Emas 1 gram, timbang, dll) dihitung **per gram**. Dinar & MR Gold dihitung **per keping**.
Jika harga ukuran dinar tertentu belum diisi, nilainya diperkirakan dari harga 1 Dinar (ditandai "perkiraan").

## Menyatukan data antar HP & komputer
1. Di perangkat A: **Pengaturan → Kirim backup / Simpan file backup**.
2. Kirim filenya (WhatsApp, email, flashdisk) ke perangkat B.
3. Di perangkat B: **Pengaturan → Buka file backup… → Gabungkan**.
4. Agar semua perangkat sama, lakukan juga sebaliknya (B → A).

"Gabungkan" aman diulang: transaksi yang sama tidak akan dobel, dan perubahan/hapusan terbaru yang dipakai.

## Keamanan
- **PIN** (Pengaturan): aplikasi terkunci saat dibuka & setelah ditinggal 2 menit. PIN berlaku per perangkat.
- Lupa PIN = data di perangkat itu tidak bisa dibuka → pulihkan dari file backup. **Rajin backup** (aplikasi mengingatkan tiap 7 hari).
- Jangan "hapus data situs/riwayat browser" untuk aplikasi ini — data ikut terhapus.

## Memperbarui aplikasi
Jika `index.html` diubah, naikkan juga versi di baris `const CACHE = 'stokdinar-v…'` pada `sw.js`, lalu unggah ulang. HP akan memakai versi baru setelah aplikasi dibuka 2 kali saat online.
