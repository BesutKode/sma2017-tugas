# Tugas 3: Membuat paket R untuk openSUSE dengan Open Build Service

## Latar belakang

Bahasa pemrograman R mempunyai sistem pemaketan bernama CRAN yang bisa ditemukan
di https://cran.r-project.org/ .

Salah satu contoh paket adalah knitr
https://cran.r-project.org/web/packages/knitr .

Anda harus memperhatikan *dependencies* (kebutuhan) untuk setiap paket R
yang dideskripsikan CRAN. Pada saat membuat file `.spec`, semua *dependencies*
paket harus sudah dibangun.

Sudah ada banyak paket-paket R di openSUSE, seperti
https://software.opensuse.org/package/R-knitr .

Proyek pemaketan R utama untuk openSUSE berada di
https://build.opensuse.org/project/show/devel:languages:R .

Sebelumnya, mereka membangun RPM secara otomatis, tetapi telah dihentikan
3 tahun yang lalu, jadi semua paket-paket RPM disini tidak berguna:
https://build.opensuse.org/project/show/devel:languages:R:CRAN-packages .

Tidak ada tata cara untuk mempaketkan paket R
https://en.opensuse.org/openSUSE:Packaging_guidelines#R .

Pakailah paket-paket yang sudah ada sebagai contoh bagaimana membangun paket R.

## Objektif

Paketkah 2 paket R yang belum ada paketnya untuk openSUSE di
https://software.opensuse.org/ .

## Memilih dua paket R

Pilihlah sebuah 2 paket R yang Anda ingin memaketkan.

- ~~crayon~~
- ~~stringdist~~
- ~~tufte~~
- ~~withr~~
- ~~rex~~
- xml2
- ~~DT~~
- sourcetools
- Cairo
- FastRWeb
- webshot
- issueReporter
- WikidataR
- pageviews
- WikipediR
- wikilake
- covr
- crul
- urltools
- WikidataQueryServiceR
- wikitaxa
- hellno
- cranlogs
- wikipediatrend
- WikiSocio
- TiddlyWikiR
- lubridate
- spData
- rgdal
- spdep
- sf
- osmdata
- osmplotr
- raster
- tmap
- tmaptools
- sphet
- splm
- spgwr
- McSpatial
- dggridR
- choroplethr
- mapview

And latest version of

- sp
- maptools

## Membuat proyek baru di Open Build Service

Di halaman utama Open Build Service, masuklah ke halaman "Home project" Anda,
dan tekan "New project".

Ikutilah panduan penamaan dan panduan deskripsi saat menuliskan nama dan deskripsi
paket.

## Menyalakan build untuk openSUSE Tumbleweed dan openSUSE Leap 42.3

Pada halaman home project Anda, masuklah ke halaman Repositories
tambahkan repositori untuk openSUSE Tumbleweed dan openSUSE Leap 42.3

## Memeriksa build

Di halaman proyek Anda, terdapat status pembangunan paket di sebelah kanan.

Log pembangunan bisa dilihat dengan menekan status pembangunan sesuai distro
target.

Jika masih terdapat kegagalan, Mohon untuk memeriksa dan diagnosa masalah yang
terjadi.

Bagian `%check` di file spec, buatlah program R sederhana yang mengimpor paket
baru yang telah dibuat untuk memeriksa apakah paket tersebut dapat di-*load*
dengan baik

Jika bisa, jalankan tes apapun yang disediakan oleh paket tersebut.

## Dokumentasi

Setelah kamu membangun dan mencoba paket R, buatlah draf untuk memperbagus
halaman https://en.opensuse.org/openSUSE:Packaging_R,
dan publikasikan draf kamu setelah sebuah mentor telah memerika draf kamu.

## Referensi

1. https://en.opensuse.org/openSUSE:Build_Service_Tutorial
2. https://en.opensuse.org/openSUSE:Build_Service_Tips_and_Tricks
3. https://en.opensuse.org/openSUSE:Package_naming_guidelines
4. https://en.opensuse.org/openSUSE:Package_description_guidelines
5. https://en.opensuse.org/openSUSE:Package_dependencies
6. https://en.opensuse.org/openSUSE:Packaging_checks
7. https://en.opensuse.org/openSUSE:Packaging_guidelines
