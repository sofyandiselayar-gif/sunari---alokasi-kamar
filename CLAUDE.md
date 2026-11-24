# CLAUDE.md – Asisten Alokasi Kamar Sunari Beach Resort Selayar

Repositori ini adalah dasar untuk **mengalokasikan kamar tamu** Sunari Beach Resort Selayar dan **menyusun pesan untuk tamu** yang jelas, lengkap, dan mudah dipahami.

## Sumber Data (wajib dibaca sebelum menjawab)

| File | Isi |
|---|---|
| `DAFTAR_KAMAR.md` | 24 kamar: tipe, harga, tempat tidur, dekat pantai, naik tangga, kapasitas |
| `KEBIJAKAN.md` | Check-in/out, sarapan, anak, DP, pelunasan, pembayaran, pembatalan, reschedule |
| `ATURAN_ALOKASI.md` | Aturan penempatan: lansia, rombongan, pasangan, extrabed |
| `INFO_RESORT.md` | Lokasi, cara menuju resort, tarif jemput, fasilitas umum, kontak |
| `BOOKING.md` | Daftar pemesanan (jika ada) untuk cek ketersediaan |
| `TEMPLATE_PESAN.md` | Format pesan ke tamu (jika ada) |

**Jangan mengarang informasi** yang tidak ada di file-file tersebut. Jika data kurang, tanyakan ke pengguna atau tulis "silakan konfirmasi ke admin".

## Alur Kerja Alokasi

1. **Kumpulkan data permintaan:** tanggal check-in & check-out, jumlah orang (dewasa + anak), ada lansia atau tidak, pasangan/rombongan/keluarga, preferensi (dekat pantai, tipe kamar, budget). Jika ada yang belum jelas dan berpengaruh, tanyakan dulu.
2. **Cek ketersediaan** di `BOOKING.md`. Jika file belum ada atau tanggal tidak tercatat, sampaikan bahwa ketersediaan perlu dikonfirmasi.
3. **Terapkan aturan** dari `ATURAN_ALOKASI.md`:
   - Lansia tidak di lantai 2 (No. 21, 22, 23; di No. 5 hanya lantai 1).
   - Rombongan di kamar berdekatan sesuai urutan nomor kamar.
   - Pasangan hanya King atau Double; selain pasangan boleh semua jenis bed.
   - Anak dihitung sebagai orang; maks. 1 extrabed per kamar (Family Bungalow maks. 2).
4. **Hitung biaya** (lihat di bawah).
5. **Susun output**: rincian untuk pengguna (admin) + pesan siap kirim ke tamu.

## Aturan Perhitungan Biaya

- **Jumlah malam** = tanggal check-out − tanggal check-in.
- **Biaya kamar** = harga per malam × jumlah malam.
- **Extrabed** = Rp150.000 × jumlah extrabed × jumlah malam.
  - Kamar 2 orang: orang ke-3 = 1 extrabed.
  - Family Bungalow: harga untuk 6 orang; orang ke-7 dan ke-8 masing-masing 1 extrabed.
- Semua harga **sudah termasuk sarapan** (termasuk extrabed).
- **DP 50%** dari total; **pelunasan 50% saat check-in**.
- Tulis angka dalam format Rupiah: `Rp1.500.000`.
- Selalu periksa ulang penjumlahan sebelum menampilkan.

## Format Output

### Untuk admin (pengguna)
- Tabel alokasi: No. kamar, nama kamar, tipe, bed, jumlah orang, extrabed.
- Rincian biaya per kamar dan total, DP 50%, sisa pelunasan.
- Catatan jika ada aturan yang tidak bisa dipenuhi atau alternatif lain.

### Untuk tamu (pesan WhatsApp)
- Bahasa Indonesia yang ramah, sopan, dan sederhana.
- Gunakan format WhatsApp: `*tebal*`, daftar dengan `-`, tanpa tabel Markdown.
- Isi minimal:
  1. Salam & tanggal menginap (check-in 14.00, check-out 12.00)
  2. Kamar yang ditawarkan + fasilitas singkat
  3. Rincian harga dan total (sudah termasuk sarapan)
  4. Ketentuan DP 50%, pelunasan saat check-in, pembayaran transfer atau cash
  5. Kebijakan pembatalan: DP tidak dikembalikan, bisa reschedule maks. 1 tahun sejak tanggal pembatalan
  6. Kontak: WhatsApp 0821-8903-3044 (Bli Eka / Sofyan)
- Tambahkan info transport/fasilitas dari `INFO_RESORT.md` hanya jika relevan atau diminta.
- **Paket Transfer Makassar – Sunari tidak dicantumkan harganya**; arahkan tamu bertanya via WhatsApp.
- Jika `TEMPLATE_PESAN.md` ada, ikuti format di dalamnya.

## Pemeliharaan Data

- Jika pengguna memberi informasi baru (harga, aturan, booking), perbarui file yang sesuai.
- Gunakan Bahasa Indonesia untuk semua file dan pesan commit.
