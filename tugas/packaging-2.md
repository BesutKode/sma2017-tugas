# Tugas 2: Membuat paket untuk dataset nltk untuk openSUSE dengan Open Build Service

## Latar belakang

Open Build Service adalah sebuah program yang memudahkan pekerjaan pemelihara
paket untuk berbagai distribusi GNU/Linux. Open Build Service memberikan sebuah
alat untuk membangun dan publikasi sebuah paket dengan cepat dan otomatis.

## Objektif

Di dalam tugas ini Anda akan membuat paket untuk sebuah dataset nltk yang Anda
telah pilih untuk openSUSE dengan Open Build Service.

## Memilih dataset yang mau dipaketkan

Silahkan pilih dataset apa yang mau dipaketkan, Kumpulan dataset nltk bisa
dilihat [disini](https://github.com/nltk/nltk_data/tree/gh-pages/packages).

Di dalam folder itu ada folder-folder yang bernama kategori dataset tersebut,
di dalamnya terdapat file zip yang berisi dataset-nya dan file xml sebagai
*meta-data*.

Pastikan ukuran dataset tersebut kecil bagi Anda yang mempunyai akses Internet
berkuota atau terbatas. Jika Anda mempunyai akses Internet tidak terbatas,
mohon mengerjakan yang lebih besar.

Cek apakah dataset tersebut telah di ambil dengan melihat
[disini][nltk_data], jika sudah di ambil, mohon mencari yang lain.

## Membuat proyek baru di Open Build Service

Di halaman utama Open Build Service, masuklah ke halaman "Home project" Anda,
dan tekan "Sub projects", dan tekan "ntlk_data", dan tekan "Create package".

Silahkan namakan dengan format `nltk-data-<nama data>`

## Upload data files

Download dataset.

Tekan "Add file" dan upload.

## Menulis file spec

File spec adalah file yang berisi spesifikasi paket dan cara membangun
proyek tersebut.

Anda bisa melihat referensi di bawah untuk cara menulis file spec, jika
masih bingung Anda bisa melihat paket-paket lain dan melihat bagaimana
file spec mereka menulis file spec-nya.

Yang dibutuhkan adalah:
* `BuildRequires` berisi `python3-nltk` dan `unzip`
* `Recommends` berisi `python3-nltk` dan `python-nltk`
* `BuildArch` diset `noarch`
* Fase `%check` memperiksa apakah dataset telah terpasang dengan baik
  dengan mencoba load dataset tersebut ke NLTK.

Sebagai contoh, bisa melihat paket `nltk-data-punkt` yang Anda telah
branch ke dalam subproject `nltk_data`.

## Memeriksa build

Di halaman subproyek `nltk_data` Anda, terdapat status pembangunan paket di
sebelah kanan.

Log pembangunan bisa dilihat dengan menekan status pembangunan sesuai distro
target.

Jika masih terdapat kegagalan, Mohon untuk memeriksa dan diagnosa masalah yang
terjadi.

## Submit

Jika *build*-nya sukses, silahkan submit paket ke
[home:jayvdb:nltk_data][nltk_data].

## Referensi

1. https://en.opensuse.org/openSUSE:Build_Service_Tutorial
2. https://en.opensuse.org/openSUSE:Build_Service_Tips_and_Tricks
3. https://en.opensuse.org/openSUSE:Package_naming_guidelines
4. https://en.opensuse.org/openSUSE:Package_description_guidelines
5. https://en.opensuse.org/openSUSE:Package_dependencies
6. https://en.opensuse.org/openSUSE:Packaging_checks

[nltk_data]: https://build.opensuse.org/project/show/home:jayvdb:nltk_data
