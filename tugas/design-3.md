# Tugas 3: Memperbaiki aset-aset permainan milik MovingBlocks

## Latar Belakang

Organisasi [MovingBlocks](https://github.com/MovingBlocks) mengembangkan sebuah
permainan yang bernama [Terasology](https://github.com/MovingBlocks/Terasology).
Terasology adalah permainan yang bersumber terbuka dan aset-asetnya dapat
ditemukan di [GitHub](https://github.com/Terasology).

## Objektif

Di dalam tugas ini Anda akan memperbaiki tekstur-tekstur yang tidak mengikuti
gaya atau aturan yang berlaku.

Selain itu, anda akan diharuskan untuk mengambil screenshot barang yang sudah
anda perbaiki di dalam game Terasology.

## Menjalankan Terasology dari kode sumber.

Apabila Anda ingin mencoba menjalankan Terasology untuk melihat permainannya
secara langsung, Anda dapat membangun Terasology dari kode sumbernya dengan
mengikuti [panduan](https://github.com/MovingBlocks/Terasology/wiki/Preparing-an-Engine-Workspace).

## Mencari tekstur yang tidak layak

Temukan aset berupa tekstur yang ada di salah satu repositori Terasology yang
belum memenuhi tiga kriteria berikut:

- Persegi (sebaiknya berukuran 32x32 atau 64x64 piksel)
- Berlatar belakang transparan
- Terlihat bagus di dalam permainan (subjektif, gunakan kemampuan desain Anda dalam menilai)

Sebagai contoh, lihat repositori [Cooking](https://github.com/Terasology/Cooking)
dan buka folder `assets/textures`. Di dalamnya terdapat beberapa berkas tekstur
yang tidak memenuhi satu atau lebih kriteria di atas, seperti berkas `Tongs.png`,
`Whisk.png`, dan `starfruit.png`.

## Memperbaiki tekstur

Setelah anda mendapatkan repositori modul yang memiliki tesktur yang tidak layak,
anda harus mendownload modul teresebut ke dalam folder game anda.

Cara melakukan hal tersebut dapat anda dengan mengikuti
[panduan](https://github.com/MovingBlocks/Terasology/wiki/Developing-Modules)
ini. (Tepatnya pada bagian *Fetch an existing module*)

Perbaikilah tekstur yang sudah Anda temukan hingga sesuai kriteria. Anda dapat
mengedit tekstur yang sudah ada, atau Anda dapat membuat sendiri tekstur yang baru.
Pastikan Anda membuat tekstur yang orisinal. Apabila Anda menggunakan sumber
eksternal, pastikan lisensinya memperbolehkan Anda untuk melakukannya.

## Mendapatkan screenshot barang anda

Setelah anda sudah memperbaiki tesktur yang ada, jalankan permainan Terasology
dan buatlah dunia baru melalui menu singleplayer (Jangan lupa untuk menyalakan modul cooking melalui tombol "Modules..").

Dapatkan item yang sudah anda buat melalui console (Tekan F1) dan ketik perintah

    give <nama item>

Lalu setelah mendapatkan barang tersebut, pegang barang tersebut di tangan dan
tekan tombol F12 untuk melalukan screenshot. Screenshot anda lalu akan tersimpan
di folder *screenshots* di folder game anda.
