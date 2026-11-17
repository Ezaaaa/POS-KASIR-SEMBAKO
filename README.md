# Sembako POS

Aplikasi kasir dan manajemen toko offline untuk **Toko Bukit Safa Market**.

## Instalasi

1. Jalankan file `Sembako-POS-Setup-1.0.0.exe` di folder ini. Nama file dapat berubah mengikuti versi rilis.
2. Ikuti petunjuk installer. Buat shortcut Desktop jika diinginkan.
3. Buka **Sembako POS** dari Desktop atau Start Menu.
4. Saat pertama dibuka, pilih **Buat akun pemilik**, lalu isi nama, nama pengguna, dan kata sandi minimal 4 karakter.
5. Setelah masuk, tambahkan barang dan sesuaikan identitas toko melalui menu **Pengaturan**.

Instalasi aplikasi tidak memerlukan Node.js atau npm.

## Persyaratan sistem

- Windows 10 atau lebih baru, 64-bit.
- Koneksi internet tidak diperlukan untuk transaksi harian.
- Windows 7 tidak didukung oleh versi Electron yang digunakan aplikasi ini.

## Pengaturan printer struk

1. Sambungkan printer dan pasang driver Windows-nya terlebih dahulu.
2. Pastikan nama printer tampil di daftar printer Windows.
3. Di Sembako POS, buka **Pengaturan → Printer struk**.
4. Pilih printer yang digunakan, pilih ukuran kertas **58 mm** atau **80 mm**, lalu tekan **Uji cetak**.
5. Jika cetakan terpotong, periksa kembali ukuran kertas di preferensi/driver printer Windows.

Struk dicetak otomatis setelah pembayaran berhasil.

## Memperbarui aplikasi dan data

- Jalankan installer versi terbaru untuk memperbarui aplikasi.
- Data tersimpan lokal untuk akun Windows yang sedang digunakan, terpisah dari file installer. Penginstalan di akun Windows lain dimulai dengan pendaftaran pemilik baru.
- Sebelum pembaruan besar atau pemindahan perangkat, buat salinan melalui **Pengaturan → Database & backup → Buat backup**.
- Untuk memulihkan salinan, gunakan **Pulihkan backup** pada menu yang sama.
- Menghapus aplikasi tidak otomatis menghapus database lokal. Jangan menghapus data aplikasi jika ingin menyimpan transaksi.

## Kredit

- Nama toko dan logo: **Toko Bukit Safa Market** (logo disediakan oleh pemilik toko).
- Aplikasi desktop: [Electron](https://www.electronjs.org/).
- Antarmuka: [React](https://react.dev/) dan [Vite](https://vite.dev/).
- Bahasa dan pemeriksaan tipe: [TypeScript](https://www.typescriptlang.org/).
- Grafik: [Recharts](https://recharts.org/).
- Ikon: [Lucide](https://lucide.dev/).
- Pembuatan installer Windows: [electron-builder](https://www.electron.build/).
- Database lokal: SQLite melalui modul `node:sqlite` yang disertakan bersama Electron/Node.js.

Nama, merek, dan lisensi masing-masing proyek pihak ketiga tetap menjadi milik pemegang haknya.

## Membuat installer dari source code

Bagian ini hanya untuk pengembang. Pasang Node.js versi 22 atau lebih baru, buka terminal pada folder proyek, lalu jalankan:

```powershell
npm install
npm run dist
```

Installer hasil build dibuat di folder `release`.
