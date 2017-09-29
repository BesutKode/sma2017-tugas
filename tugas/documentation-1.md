# Tugas 1: Lagi males, tidak baca

## Latar Belakang

Proyek tldr-pages bertujuan untuk mensimplifikasi "man pages". Man pages
adalah manual yang dipakai di sistem berbasis UNIX, biasanya untuk
membacanya mengunakan perintah `man`.

## Objektif

Di dalam tugas ini, Anda akan menulis dokumentasi yang simple untuk sebuah
perintah.

## Fork repositori

Pada repositori yang Anda telah pilih, tekanlah tombol fork.

Anda akan dialihkan ke salinan repositori yang sama dengan URL seperti `https://github.com/username_kamu/tldr`.

## Aktivasi Travis CI

Masuk ke https://travis-ci.org mengunakan akun GitHub Anda.

Untuk mengaktivasi Travis CI pada _fork_ kamu, masuk ke "Your profile", dan

1. Tekan "Sync account"
2. _Scroll_ ke bawah, carilah fork kamu, dan tekan pada tombol "X" abu-abu
   untuk menjadikan check biru.

## Menulis dokumentasi

Tulislah sebuah dokumentasi untuk perintah yang Anda tahu, pastikan belum
ada dokumentasi untuk perintah yang Anda mau dokumentasikan.

Halaman dokumentasi berada di dalam folder `pages` dan di kategori tertentu.

Kategorinya adalah:
  * `common`, perintah yang umum di sebuah sistem POSIX (standar UNIX).
  * `linux`, perintah yang hanya ada di sebuah sistem Linux atau distribusi
    Linux.
  * `osx`, perintah yang hanya ada di sebuah sistem macOS.
  * `sunos`, perintah yang hanya ada di sebuah sistem SunOS/Solaris.

## Menjalankan Travis CI

Setiap ada _commit_ di _fork_ kamu, Travis CI akan mencoba untuk menjalankan
tugas-tugas sesuai file `.travis.yml`.

Tunggu sampai prosesnya sudah selesai. Jika proses build sudah selesai dan
sukses, Anda telah menyelesaikan tugas ini. Jika masih belum, mohon
memperbaikinya dengan membaca *Build log* Travis.

## Referensi

1. https://github.com/tldr-pages/tldr
