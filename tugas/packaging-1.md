# Tugas 1: Mencari dataset NLTK

## Latar belakang

Dataset NLTK tidak mempunyai paket di distribusi manapun, alangkah baiknya
jika kita memaketkanya supaya orang bisa memasang NLTK dengan mudah.

## Objektif

Di dalam tugas ini Anda akan memilih dataset NLTK yang akan dipakai untuk
Tugas kedua.

## Membuat subproject untuk nltk

Buatlah subproject bernama `nltk_data` di dalam Home project Anda. Ini bisa
dilakukan dengan membuka halaman "Home project", masuk ke tab Subprojects, dan
namakan subproject tersebut `nltk_data`.

## Mempersiapkan subproject `nltk_data`

Untuk mempersiapkan subproject supaya bisa dipakai untuk mempaket `nltk_data`,
kita harus "branch" paket [nltk-data-punkt][nltk-data-punkt],
[python-nltk][python-nltk], [python3-nltk][python3-nltk], dan
[python-rpm-macros][python-rpm-macros].

Untuk melakukan branch ke subproject Anda, bukalah subproject `nltk_data` Anda
dan tekan "Branch existing packages" dan isilah formnya.

Untuk "Name of original project", masukan nama project paket tersebut.
Untuk "Name of package in original project", masukan nama paket tersebut.
Untuk "New package name", bisa dibiarkan kosong.

Jika benar, paketnya akan muncul dalam subproject `nltk_data` Anda.

## Menyalakan build untuk openSUSE Tumbleweed dan openSUSE Leap 42.3

Pada halaman subproject `nltk_data` Anda, masuklah ke halaman Repositories
tambahkan repositori untuk openSUSE Tumbleweed dan openSUSE Leap 42.3

[nltk-data-punkt]: https://build.opensuse.org/package/show/home:jayvdb:nltk_data/nltk-data-punkt
[python-nltk]: https://build.opensuse.org/package/show/devel:languages:python/python-nltk
[python3-nltk]: https://build.opensuse.org/package/show/devel:languages:python3/python3-nltk
[python-rpm-macros]: https://build.opensuse.org/package/show/devel:languages:python/python-rpm-macros
