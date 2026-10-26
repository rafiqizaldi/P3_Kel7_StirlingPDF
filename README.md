# Aplikasi Web "Stirling-PDF"

**Proyek Komunikasi Data dan Jaringan Komputer (KDJK)**
**Kelompok 7, Paralel 3**

| Nama | NIM |
| :-- | :-- |
| Yoel Christopel Napitupulu | M0403241110 |
| Valentino Pierre Rufinus Purimahua | M0403241114 |
| Rafiqi Zaldi Riyatno | M0403241116 |
| Gilang Muhamad Widiagung | M0403241117 |

Situs yang berjalan: [https://pdf.gimiaw.web.id/](https://pdf.gimiaw.web.id/)

## Sekilas Tentang

Deskripsi singkat tentang aplikasi tsb.


## Instalasi

- Prasyarat, apa saja yang harus diinstal sebelumnya.
- Langkah instalasi dalam CLI.


## Konfigurasi (opsional)

Setting server tambahan yang diperlukan untuk meningkatkan fungsi dan kinerja aplikasi, misalnya:
- batas upload file
- batas memori
- dll

Plugin untuk fungsi tambahan
- login dengan Google/Facebook
- editor Markdown
- dll


##  Maintenance (opsional)

Setting tambahan untuk maintenance secara periodik, misalnya:
- buat backup database tiap pekan
- hapus direktori sampah tiap hari
- dll


## Otomatisasi (opsional)

Skrip shell untuk otomatisasi instalasi, konfigurasi, dan maintenance.


# Pembahasan
 
## Kelebihan
 
- **Gratis dan semua tool PDF dapat dipakai.** Menurut dokumentasi resmi, paket Free sudah mencakup seluruh tool PDF dan REST API. Paket berbayar hanya menambah fitur untuk skala organisasi, seperti SAML SSO, audit log, dan database eksternal.
- **Data tetap di server sendiri.** Dokumen tidak diunggah ke layanan pihak ketiga, sehingga cocok untuk dokumen yang sensitif.
- **Tidak ada kuota tugas harian; batas ukuran mengikuti konfigurasi server.** Berbeda dengan layanan online gratis seperti iLovePDF.
- **Fitur lengkap.** Ada 50+ operasi PDF, antara lain *merge*, *split*, kompresi, konversi dari/ke format Office, OCR, tanda tangan, dan *redact*.
- **Pemasangan relatif mudah.** Cukup satu *container* Docker tanpa database eksternal, dan komunitasnya besar (sekitar 89 ribu *stars* di GitHub) sehingga panduan mudah ditemukan.
- **Bisa dipakai offline** di jaringan lokal.
## Kekurangan
 
- **Harus dikelola sendiri.** Pemasangan, pembaruan, *backup*, dan keamanan server menjadi tanggung jawab kita.
- **Cukup berat untuk server kecil.** Aplikasinya berbasis Java sehingga membutuhkan sekitar 1-2 GB RAM atau lebih, dan varian *fat* (dengan LibreOffice dan OCR) disarankan minimal 2 GB.
- **Ada batas 5 akun pada paket Free.** Batas ini berlaku bila menggunakan mode multi-user.
- **Keamanan perlu diatur.** Pada beberapa panduan, instalasi awal berjalan tanpa login dan memakai kredensial bawaan, sehingga perlu diamankan sebelum dibuka ke internet.
- **Hanya untuk PDF.** Kebutuhan gambar, video, atau audio memerlukan aplikasi lain.
 
## Perbandingan dengan Aplikasi Sejenis
 
| Aspek | Stirling-PDF | SnapOtter | iLovePDF |
|---|---|---|---|
| **Jenis layanan** | *Self-hosted* | *Self-hosted* | Layanan web (online) |
| **Cakupan** | Khusus PDF | Gambar, video, audio, PDF, dan file umum | Khusus PDF |
| **Privasi data** | File diproses di server sendiri | File diproses di server sendiri | File diunggah ke server iLovePDF dan dihapus otomatis setelah beberapa jam |
| **Biaya** | Gratis; biaya hanya server. Ada paket berbayar untuk tim besar | Gratis (AGPLv3); biaya hanya server | Gratis dengan batasan; *Premium* berbayar |
| **Batasan** | Tanpa login, tidak ada batas pengguna; 5 akun jika login bawaan diaktifkan | Tergantung server | Dibatasi jumlah tugas dan ukuran file di paket gratis |
| **Kebutuhan server** | Sekitar 1-2 GB RAM | Minimal 1 GB RAM dan 5 GB disk | Tidak perlu server |
| **Komunitas** | Sangat besar (± 89 ribu *stars*) | Masih kecil (± 2,2 ribu *stars*), proyek baru | Layanan komersial mapan |
| **Kemudahan** | Perlu setup awal | Perlu setup awal | Paling mudah, langsung buka browser |
 
## Kesimpulan
 
- **Stirling-PDF cocok jika** kita ingin mengolah PDF tanpa batas dengan data tetap di server sendiri dan ada server yang bisa dikelola. **Tetapi jika** tidak ada server atau tidak ingin repot merawatnya, iLovePDF lebih praktis dengan konsekuensi file diunggah ke pihak ketiga dan ada batasan pemakaian.
- **Stirling-PDF lebih baik daripada SnapOtter jika** fokusnya hanya PDF dan kita ingin aplikasi yang matang dengan komunitas besar. **Tetapi jika** kita butuh satu platform untuk banyak jenis file (gambar, video, audio), SnapOtter lebih sesuai.

## Referensi
 
1. https://github.com/Stirling-Tools/Stirling-PDF
2. https://docs.stirlingpdf.com/Server/Licensing/Plans-and-Licences/
3. https://docs.stirlingpdf.com/Modes%20and%20Licensing
4. https://railway.com/deploy/stirling
5. https://hub.docker.com/r/snapotter/snapotter
6. https://dinao.com/conteneur/snapotter
7. https://www.opentechhub.io/snapotter/
8. https://www.switchlabs.dev/compare/pdf-to-word-vs-ilovepdf
9. https://us.fitgap.com/products/ilovepdf
10. https://dev.to/vikasprogrammer/self-hosting-stirling-pdf-in-2026-i-ditched-adobe-and-smallpdf-1pd9
