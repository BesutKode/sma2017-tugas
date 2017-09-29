# Tugas 1: Otomatisasikan proyek!

## Latar belakang

Komputer adalah alat yang sangat berguna untuk melakukan hal-hal yang
berulang-ulang, sehingga mengotomatisasikan hal-hal dasar seperti "Apakah proyek
saya masih dapat build dengan sukses setelah perubahan ini?" bisa diotomatisasikan dan
tidak perlu dilakukan secara manual. Karena inilah peralat-alatan otomatisasi
seperti _Continuous integration_ sangat populer di dunia pekerjaan modern dan
organisasi-organisasi perangkat lunak bebas. Kalau komputer bisa ditugaskan,
mengapa harus manusia yang melakukannya?

## Objektif

Di dalam tugas ini Anda akan mempersiapkan sistem _Continuous integration_ dengan
Travis CI untuk sebuah repositori GitHub pages.

## Mencari situs GitHub pages yang menggunakan Jekyll

Carilah repositori GitHub pages sebuah organisasi yang merupakan blog.

Untuk memeriksa apakah situs itu dimiliki oleh sebuah organisasi,
masuklah ke repositorinya dan cek apakah pemilik repo tersebut adalah
sebuah organisasi bukan user biasa.

Contoh:
* Untuk https://fossasia.github.io repositorinya berada di
  https://github.com/fossasia/fossasia.github.io
* https://github.com/coala adalah sebuah organisasi sedangkan
  https://github.com/yukiisbored adalah sebuah user biasa.

Untuk memastikan itu adalah sebuah blog, bisa mengecek apakah ada
folder bernama `_posts`. Jika ada, itu adalah sebuah blog dan bisa
dipakai untuk tugas ini.

Anda bisa mencoba menggunakan query
`site:github.io inurl:2016 inurl:10 "Powered by Jekyll" -theme` di Google
untuk mencari situs blog Jekyll. Silakan modifikasi query tersebut untuk
mendapatkan hasil yang lebih baik.

Domain GitHub pages yang tidak menggunakan domain custom selalu mempunyai
struktur `username.github.io`, Anda bisa mendapatkan repositori GitHub-nya
dengan membuka `github.com/username/username.github.io`.

Silakan cek apakah ada file bernama `Gemfile`, jika ada, proyek tersebut
tidak bisa dipakai untuk tugas ini.

## _Fork_ repositori

Pada repositori yang Anda telah pilih, tekanlah tombol _fork_.

Anda akan dialihkan ke salinan repositori yang sama dengan URL seperti
`https://github.com/username_kamu/nama_repositori_yang_kamu_pilih`.

## Set sumber cabang GitHub pages

Terkadang sumber GitHub pages berada di branch "master" atau "gh-pages", Anda bisa
memperiksa di mana sumber cabangnya tersebut.

Silakan buka [dokumen ini][gh-pages branch] untuk melihat bagaimana cara set
sumber cabangnya.

## Aktivasi Travis CI

Masuk ke https://travis-ci.org menggunakan akun GitHub Anda.

Untuk mengaktivasi Travis CI pada _fork_ Anda, masuk ke "Your profile", dan

1. Tekan "Sync account"
2. _Scroll_ ke bawah, carilah fork Anda, dan tekan pada tombol "X" abu-abu
   untuk menjadikan check biru.

## Menulis Gemfile

Sebuah Gemfile adalah file yang berisi kebutuhan sebuah proyek supaya bisa
jalan atau kebutuhan untuk pengembangan proyek tersebut.

Karena mayoritas dari repositori GitHub pages yang menggunakan Jekyll hanya
membutuhkan `jekyll`, Anda cukup menuliskan Gemfile seperti di bawah ini:

```ruby
source 'https://rubygems.org'

gem 'jekyll'
```

Jika website Anda butuh gem-gem lain seperti tema, silakan cari tahu tentang
nama "gem"-nya.

## Menulis `.travis.yml`

Silakan tulis file `.travis.yml` berdasarkan contoh di bawah ini.

```yaml
language: ruby

install:
  - bundle install

script:
  - jekyll build
```

## Menjalankan Travis CI

Setiap ada _commit_ di _fork_ Anda, Travis CI akan mencoba untuk menjalankan
tugas-tugas sesuai file `.travis.yml`.

Tunggu sampai prosesnya sudah selesai. Jika proses build sudah selesai dan
sukses, Anda telah menyelesaikan tugas ini. Jika masih belum, mohon
memperbaikinya dengan membaca *Build log* Travis.

## Membuka situsnya

Jika sukses, situsnya bisa dilihat di
`https://username_kamu.github.io/nama_repositori_yang_kamu_pilih` contoh

## Referensi

1. https://docs.travis-ci.com/user/getting-started
2. https://docs.travis-ci.com/user/languages/ruby/
3. https://jekyllrb.com/docs/usage/
4. https://bundler.io/v1.15/gemfile.html
5. https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/#default-source-settings-for-repositories-without-the-username-naming-scheme

[gh-pages branch]: https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/#default-source-settings-for-repositories-without-the-username-naming-scheme
