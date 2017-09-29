# Tugas 2: Deployment semudah 1-2-3

## Latar belakang

Deployment adalah salah satu masalah yang sering terjadi di sebuah proyek,
sebelum ada alat-alat otomatisasi CI, deployment dilakukan secara manual oleh
tim operator tetapi karena semakin cepatnya perkembangan perangkat lunak,
otomatisasi sangat diperlukan untuk mempercepat pengiriman dari kode - tes -
produksi.

## Objektif

Di tugas ini, Anda akan mendeploy website tugas 1 dengan menggunakan fitur
*deployment*-nya Travis CI.

## Buat repositori baru

Buatlah repositori baru dengan nama yang mengikuti format `hugo-nama_organisasi`
(contoh: `hugo-wikimedia-id`).

Untuk membuka situs GitHub pages untuk repositori tersebut, bisa membukanya
lewat `https://username_kamu.github.io/hugo-nama_organisasi`.
(contoh: `https://yukiisbored.github.io/hugo-wikimedia-id`)

## Mengonversi website Jekyll ke Hugo

Hugo mempunyai fitur untuk mengimpor posts dari Jekyll ke Hugo, silakan
lihat referensi di bawah untuk dokuemntasi Hugo.

Jangan lupa untuk menambahkan `public` di `.gitignore` supaya folder `public`
tidak muncul di repositori Anda. Untuk informasi lebih lanjut  tentang
`.gitignore`, silakan baca referensi di bawah.

Jangan lupa untuk set tema, Untuk menambahkan tema kami rekomendasikan memakai
git submodule.

## Aktivasi Travis CI

Masuk ke https://travis-ci.org menggunakan akun GitHub Anda.

Untuk mengaktivasi Travis CI pada _fork_ Anda, masuk ke "Your profile", dan

1. Tekan "Sync account"
2. _Scroll_ ke bawah, carilah fork Anda, dan tekan pada tombol "X" abu-abu
   untuk menjadikan check biru.

## Menulis `.travis.yml`

Silakan tulis `.travis.yml` berdasarkan contoh dibawah ini.

```yaml
language: go

install:
  - mkdir ~/bin
  - curl https://github.com/gohugoio/hugo/releases/download/v0.26/hugo_0.26_Linux-64bit.tar.gz -O hugo.tgz
  - tar xfv hugo.tgz -C bin
  - rm hugo.tgz bin/*.md
  - export PATH=$HOME/bin:$PATH

script:
  - <masukan perintah untuk membangun website>

deploy:
  provider: pages
  skip_cleanup: true
  github_token: $GITHUB_TOKEN
  local_dir: <name folder website yang dibangun>
  target_branch: gh-pages
  on:
    branch: master
```

File tersebut butuh dimodifikasi supaya Travis dapat bekerja dan mendeploy
website tersebut dan butuh aksi lebih lanjut supaya Travis bisa mendeploy
situsnya. Silakan baca referensi untuk informasi lebih lanjut.

## Menjalankan Travis CI

Setiap ada _commit_ di _fork_ Anda, Travis CI akan mencoba untuk menjalankan
tugas-tugas sesuai file `.travis.yml`.

Tunggu sampai prosesnya sudah selesai. Jika proses build sudah selesai dan
website-nya muncul di repositori `gh-pages`, Anda telah menyelesaikan tugas
ini. Jika masih belum, mohon memperbaikinya dengan membaca *Build log*
Travis.

## Referensi

1. https://docs.travis-ci.com/user/getting-started
2. https://docs.travis-ci.com/user/deployment/pages/
3. https://gohugo.io/getting-started/
4. https://gohugo.io/getting-started/installing/
5. https://gohugo.io/getting-started/usage/
6. https://gohugo.io/commands/
7. https://gohugo.io/commands/hugo/
8. https://gohugo.io/hosting-and-deployment/deployment-with-wercker/
   (Menggunakan wercker, butuh modifikasi supaya bisa dipakai di Travis)
9. https://gohugo.io/commands/hugo_import_jekyll/
