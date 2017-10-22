# Tugas 3: Kunci yang terlupakan

## Latar belakang

LibreOffice adalah salah satu proyek dengan komunitas translator yang luas. Salah
satu kesalahan yang sering terjadi adalah konflik tombol pintasan. Yang dimaksud
dengan tombol pintasan adalah shortcut yang biasa untuk menekan komponen GUI
dengan keyboard. Salah satu contoh konflik tombol pintasan adalah seperti
[pranala ini][conflict example].

## Objektif

Pada tugas ini, Anda mencari sebuah 5 konflik tombol pintasan dan mengubahnya.

## Clone repositori translation

Repositori translation LibreOffice itu besar (~2 GB), bagi yang mempunyai
internet terbatas mohon cari wifi publik yang cepat (seperti wifi.id).

Silahkan clone repositori translation dengan melakukan:

```bash
$ git clone git://anongit.freedesktop.org/libreoffice/translations
```

## Membuka file `po`

File `po` adalah file-file yang dipakai untuk melakukan lokalisasi dengan
library GNU gettext. Ada banyak sekali editor spesial untuk file po ini tetapi
file po sangat mudah untuk dimodifikasi dengan teks editor apapun.

File-file `po`-nya sudah dimasukan di dalam repositori ini, silahkan memakai
`git` dan melakukan clone dan kerja secara lokal.

## Mencari konflik tombol pintasan

Sayangnya tidak ada cara mudah untuk mencari konflik tombol pintasan. Saya
rekomendasikan download LibreOffice dan cari disitu. Tombol pintasan tidak
hanya ada di menu bar, komponen seperti tombol di dialog box juga memakai
tombol pintasan.

Silahkan melihat referensi-referensi di bawah untuk mengetahui cara untuk
mencarinya dan tentang tombol pintasan.

Untuk setiap menu atau dialog yang Anda temui konfliknya, Anda perlu membuat
cuplikan layar (screenshot) objek tersebut, yang jelas menunjukkan huruf mana
saja yang mengalami konflik.

Salah satu cara mudah untuk mencari access key itu dengan mengunakan `grep`.

## Submit

Silakan submit dengan membuat patch. Ini bisa dilakukan dengan
mengunakan `format-patch`. Jangan sertakan file .mo yang merupakan hasil
kompilasi ke dalam patch Anda. Sertakan cuplikan layar yang telah Anda buat
sebelumnya.

Secara dasarnya untuk memakai format patch adalah sebagai berikut:

```
$ git format-patch <commit SHA sebelum perubahan Anda>
```

[conflict example]: https://www.facebook.com/atriwidada/posts/10155669214064594:38

After a mentor has checked your work, create an account on https://translations.documentfoundation.org/
with your global username and make the corrections to the appropriate messages
in the `master` projects only.

## References

1. https://i14i.andika.info/index.php?title=Halaman_Utama
2. https://i14i.andika.info/index.php?title=GNOME/Uji_Hasil_Terjemahan#Pemeriksaan_Konflik_Pintasan
3. https://www.slideshare.net/atriwidada/translating-gnome
