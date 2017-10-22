# Tugas 3: Selamat datang di era kontainer!

## Latar belakang

Salah satu masalah yang sering terjadi di era informasi adalah menjalankan
sebuah program (biasanya sebuah aplikasi web) di sebuah server. Banyak
programmer dan pengembang proyek meremehkan untuk memikirkan bagaimana
proyek mereka jalan di sebuah server produksi yang harus jalan 24/7.
Dulunya mereka hanya membiarkan masalah tersebut kepada operator server,
tetapi makin lama para pengembang mulai mengalami masalah yang sama.
Bagaimana seorang pengembang bisa menjamin proyek mereka jalan di komputer
dia sendiri dan komputer pengembang lainnya. Bisa saja, kamu memakai
distribusi Linux Ubuntu dan temanmu memakai Fedora atau openSUSE atau
mungkin Windows. Belum juga, makin berkembangnya teknologi, makin besarnya
kumpulan program yang dibutuhkan untuk proyeknya agar bisa dijalankan, bisa dari sebuah
database, web server, sampai message broker.

Dulunya solusinya adalah menggunakan sebuah Virtual machine tetapi
masalahnya adalah teman pengembang kamu bekerja di sebuah laptop yang biasanya
tidak kuat untuk menjalankan virtual machine sama sekali. Belum juga Virtual
machine itu besar sekali ukurannya untuk dikirim, bisa saja sampai 25 GB atau
bahkan lebih. Belum juga dengan virtual machine kita terpaksa harus mengalokasi
resource komputer dan resource yang dialokasi tidak bisa dibagi antar VM dan
host.

Karena itu, kontainer dibuat untuk memecahkan masalah-masalah yang tersebut.
Cara kerja kontainer adalah menggunakan fitur "change root" yang ada di operasi
sistem berbasis UNIX (seperti Linux, macOS, BSD, dll) dan mengisolasinya dengan
menggunakan fitur Linux seperti process namespace, cgroups, dll.

## Objektif

Membuat image Docker untuk sebuah proyek aplikasi web dengan bantuan continuous
integration Docker cloud dan contoh setup dengan Docker compose.

## Memilih sebuah proyek

### Memilih sebuah repositori GitHub

Carilah repositori di GitHub yang mempunyai kriteria berikut:

1. Mempunyai bintang 50 atau lebih.
2. Tidak mempunyai sebuah image Docker resmi.
3. Sebuah proyek aplikasi web.

Fitur pencarian lanjut di GitHub bisa dipakai untuk membantu mencari proyek yang
mempunyai kriteria di atas.

Untuk memfilter repositori yang tidak memenuhi kriteria, gunakanlah
`stars:>50`.

Istilah pencarian opsional `forks:>100` bisa dipakai untuk mencari repositori
yang bisa memenuhi kriteria proyek.

Di sebelah kanan halaman pencarian adalah pemilihan bahasa pemrograman yang
dipakai, Anda bisa menggunakan itu untuk mencari proyek yang menggunakan bahasa
pemrograman yang Anda minati.

Istilah pencarian opsional `size:5000...10000` bisa dipakai untuk mencari
repositori yang berukuran 5-10 MB. Jika Anda mempunyai internet yang lambat
atau berkuota, istilah pencarian ini bisa dipakai.

Untuk mengecek apakah proyek tersebut mempunyai image Docker resmi, lihatlah
apakah ada file yang bernama `Dockerfile`. Biasanya file ini berada di akar
repositori.

Ada beberapa cara untuk mencari proyek aplikasi web, Anda bisa menggunakan
topik GitHub yaitu dengan menambahkan istilah pencarian `topic:<topic>`
seperti `topic:server`, `topic:web`, `topic:self-hosted` dll tetapi tidak
semuanya adalah sebuah aplikasi web, sebagian besar yang mungkin muncul adalah
library untuk membangun aplikasi web seperti Django, Express, Flask, Rails, dll.
Sehingga masih membutuhkan pengecekan manual.

Cara lain untuk mencari aplikasi web adalah mencari "awesome lists". Awesome
lists adalah sebuah repositori yang membuat daftar proyek-proyek yang menurut
orang banyak keren. Biasanya daftar ini memilik tema seperti [proyek-proyek
keren dari Indonesia][awesome-indonesia repo], [proyek-proyek keren yang
menggunakan docker][awesome-docker repo], [proyek-proyek keren untuk sebuah teks
editor][awesome-emacs repo], dll.


## _Fork_ repositori

Silahkan meminta mentor untuk melakukan _fork_ repositori yang kamu ingin pakai
ke organisasi Besut Kode. Ini diperlukan supaya mentor dapat memantau progres
di Docker cloud.

## Menulis `Dockerfile`

Sebuah `Dockerfile` adalah file teks yang berisi instruksi untuk membangun
sebuah image Docker. Dokumentasi Docker mempunyai referensi untuk menulis
sebuah file Docker dan praktik bagus untuk menulisnya. Mohon untuk membacanya.

Berusahalah untuk membuat image Docker sekecil mungkin dengan melakukan
pembersihan setelah melakukan sebuah perintah.

Biasanya sebuah `Dockerfile` menggunakan sebuah image sistem operasi Linux
sebagai "base"-nya atau image yang dibuat untuk menjalankan program yang
ditulis dengan bahasa pemrograman tertentu.

## Ikut organisasi Docker cloud

Mintalah kepada mentor untuk invitasi organisasi Docker cloud Besut Kode.

Alasan untuk melakukan ini adalah supaya mentor dapat melihat progres di Docker
cloud.

## Aktivasi Docker cloud

Docker mempunyai layanan Docker Cloud yang dapat dipakai untuk mengotomatisasikan
proses build dan publikasi.

Pertama yang Anda harus lakukan adalah membuat repositori baru, link kode
sumber dari GitHub ke repositori Docker cloud, dan membuat otomatisasi build di
repositori GitHub tersebut. Untuk cara melakukan hal-hal tersebut, bisa
dibaca pada referensi di bawah.

Pastikan Anda membuatnya di organisasi Docker cloud Besut Kode, bukan atas user
Anda.

Jika sukses, Anda seharusnya dapat melihat hasil build di tab "builds" di
repositori Docker Cloud Anda dan simbol cek di sebelah commit terbaru di halaman
"commits" di repositori GitHub Anda.

Jika gagal, Anda bisa melihat log dari build tersebut.

## Membuat hooks di Docker cloud

Fungsi-fungsi di Docker cloud bisa di *override* atau menambah dengan membuat
hook scripts.

Dalam tugas ini, kami ingin menjamin kualitas `Dockerfile` sebelum membangun
image-nya, untuk itu kita akan mengunakan Hadolint yaitu sebuah *linter* untuk
Dockerfile.

Buatlah file `hooks/pre_test` berisi ini:

```bash
#!/bin/bash

set -e -x

docker run --rm -i lukasmartinelli/hadolint < Dockerfile
```

Jangan lupa untuk menambahkan executable bit ke file tersebut
(`chmod +x hooks/pre_test`) !

## Menulis `docker-compose.yml`

Docker compose adalah sebuah alat yang digunakan untuk meng-orkestrasi beberapa kontainer
untuk menjalankan sebuah program. Seperti sebuah aplikasi web membutuhkan sebuah
database untuk menyimpan data atau web server tambahan untuk menyediakan
file-file statis.

Dokumentasi Docker mempunyai panduan yang lengkap untuk menulis `docker-compose.yml`
dan panduan untuk menggunakan alat ini.

## Referensi

1. https://docs.docker.com/docker-cloud/builds/repos/
2. https://docs.docker.com/docker-cloud/builds/link-source/#link-to-a-github-user-account
3. https://docs.docker.com/docker-cloud/builds/automated-build/
4. https://docs.docker.com/docker-cloud/builds/advanced/#custom-build-phase-hooks
5. https://docs.docker.com/engine/reference/builder/
6. https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/
7. https://docs.docker.com/get-started/
8. https://docs.docker.com/compose/overview/
9. https://docs.docker.com/compose/compose-file/
10. https://docs.docker.com/compose/gettingstarted/
11. https://www.youtube.com/watch?v=Q5POuMHxW-0
12. https://www.youtube.com/watch?v=pts6F00GFuU
13. https://www.youtube.com/watch?v=bV5vbNK3Uhw&list=PLkA60AVN3hh_6cAz8TUGtkYbJSL2bdZ4h

[awesome-indonesia repo]: https://github.com/GitIndonesia/awesome-indonesia-repo
[awesome-docker repo]: https://github.com/veggiemonk/awesome-docker
[awesome-emacs repo]: https://github.com/emacs-tw/awesome-emacs
