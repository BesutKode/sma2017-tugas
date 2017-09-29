# Tugas 2

Temukan dan perbaiki bug teknis yang terdapat pada pesan-pesan terjemahan yang terdapat pada repo-repo GitHub atau GitLab atau Bitbucket.

## Tujuan

Tugas ini bertujuan untuk membantu peserta mendapatkan pemahaman tingkat lanjut mengenai markup teks dan format-format berkas terjemahan, serta alat-alat pengecek kualitas bersumber terbuka yang tersedia untuk format berkas tersebut.

JANGAN menerjemahkan pesan-pesan, karena hal tersebut bukan tujuan dari tugas ini.

## Peringatan

Selama fase eliminasi berlangsung, para peserta tidak diperkenankan untuk berinteraksi dengan repo yang telah dipilih oleh peserta lain untuk tugas ini sampai peserta tersebut telah berhasil menyelesaikan tugasnya.

## Temukan 10 bug dalam proyek terjemahan

Bug yang terdapat pada pesan-pesan terjemahan termasuk masalah-masalah

- Semantik, seperti struktur tata bahasa yang hilang, contoh: tidak adanya titik pada akhir kalimat, dan lain sebagainya.

- Error sintaks, seperti pada variasi bahasa dari bahasa sumber yang tidak semestinya di terjemahkan namun sudah terlanjur di terjemahkan.

Telah ada alat-alat bersumber terbuka untuk menemukan dan bahkan memperbaiki masalah-masalah ini secara otomatis.
Contoh alat bersumber terbuka untuk hal ini adalah [`translate-toolkit`](https://en.wikipedia.org/wiki/Translate_Toolkit),
yang mana telah disertakan pada distribusi Linux pada umumnya.

Lihat "[Existing tools](https://github.com/BesutKode/uni-task-1/wiki/Existing-tools)" (perangkat yang telah tersedia)
tersebut berisi alat-alat yang mungkin berguna.

Wajib bagi Anda untuk mencari bug-bug terjemahan pada proyek-proyek yang menggunakan layanan Weblate.
Weblate mengizinkan siapapun untuk memberikan kontribusi terjemahan yang kemudian akan di-lazy-commit-kan pada reponya.

Apabila proyek weblate disambungkan pada sebuah repo GitHub, perubahan-perubahan yang dibuat pada layanan weblate akan
muncul pada profil GitHub kontributor yang membuat perubahan tersebut di weblate, HANYA apabila alamat surel (e-mail)
yang digunakan oleh kontributor di GitHub dan di weblate sama.

Beberapa layanan weblate memungkinkan otentikasi (pembuktian) menggunakan akun GitHub, apabila Anda menggunakan
alamat surel (e-mail) yang sama antara weblate dan GitHub.

Pada wiki ada halaman "[Weblate](https://github.com/BesutKode/uni-task-1/wiki/Weblate)" yang berisi informasi
mengenai layanan-layanan weblate.
Dua layanan weblate terbesar yang di dalamnya terdapat beragam proyek yang tersambung dengan repo GitHub adalah:

- https://hosted.weblate.org/
- https://l10n.opensuse.org/

## Daftarkan proyek Anda

Hanya satu peserta yang diperkenankan untuk bekerja pada satu repo GitHub pada satu waktu.
Hal ini diberlakukan untuk menghindari berbagai perubahan yang mungkin bentrok.

Jika orang lain telah mendaftarkan repositori tersebut, maka Anda harus tidak memilihnya, atau Anda akan dieliminasi.

1. Perbaiki bug-bug terjemahan yang ada pada repositori tersebut
2. Berikan _Star_ pada repo

Apabila Anda tidak menemukan dan memperbaiki 10 pesan bermasalah dalam
repositori terdaftar pertama Anda, Anda dapat memilih repositori lain
di halaman wiki Anda, dan mengulanginya hingga Anda berhasil memperbaiki 10 pesan.

#### Contoh

[Contoh tugas](https://wikimedia-id.github.io/besutkode/university-sample-task-1-en.html)
ini memiliki latar belakang tentang proyek penerjemahan phpMyAdmin.

Peserta yang menyelesaikan contoh tugas ini dapat dilihat di
[`id.po`](https://github.com/phpmyadmin/localized_docs/commits/master/po/id.po).

Contoh-contoh perbaikan-perbaikan kecil juga dapat dilihat di sana, seperti:

- https://github.com/phpmyadmin/localized_docs/commit/9cc7914fe0ddc8caa90ca5da32150442de2561e4#diff-ef37f181f82218fc93bce3f96e620e4d
- https://github.com/phpmyadmin/localized_docs/commit/877c28f9f859a4806b1556764be697d0aab0501c#diff-ef37f181f82218fc93bce3f96e620e4d
