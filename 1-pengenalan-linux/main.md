# Linux

## Definisi dan Sejarah
[Linux](https://en.wikipedia.org/wiki/Linux_kernel/) awalnya adalah kernel yang ditulis oleh [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds).
Kernel ini pada awalnya ditulis oleh Linus untuk pribadi yang terinspirasi dari UNIX. Linus memulai dengan task switcher dalam bahasa intel 80386 assembly dan sebuah driver terminal pada 25 Agustus 1991.\
Sesuai dengan bahasa yang digunakan, Linux berjalan pada processor intel 386(486) AT clones.
Tidak perlu waktu lama, Linux diadaptasi oleh GNU operating system sebagai penggantu kernel mereka sendiri (GNU Hurd) yang tidak rampung.\
Linux sebagai kernel memiliki arsitektur monolitik dengan desain yang modular. Monolitik kernel adalah arsitektur sistem dimana semua sistem operasi bekerja di kernel space.
![Jenis Kernel](https://upload.wikimedia.org/wikipedia/commons/d/d0/OS-structure2.svg)
Linux juga di desain dengan sifat modular, dimana kita bisa memasukkan dan melepas loadable kernel modules. Ini memungkinkan kernel mendukung banyak fitur yang hanya tersedia pada kernel sistem operasi tidak terbuka.

## Penggambaran Peran Linux Kernel
Linux kernel berperan sebagai media komunikasi antara user space dengan hardware. Segala aktivitas yang kita lakukan didepan layar akan dilempar ke kernel menggunakan system call sebagai request yang kemudian diteruskan ke hardware dimana permintaan kita diproses.
![Penggambaran Linux](https://upload.wikimedia.org/wikipedia/commons/3/3a/Linux_kernel_ubiquity.svg)

Untuk peta dari Linux Kernel bisa diakses [Linux Kernel Map](https://makelinux.github.io/kernel/map/)\

## Linux Boot Process

### BIOS/UEFI POST Test
POST (Power On Self Test). Pada tahap ini, setelah tombol **power** ditekan, sistem akan menjalankan serangkaian tes untuk memastikan semua hardware berjalan dengan baik. Proses ini meliputi tes CPU, RAM, Disk (HDD/SSD), GPU, dsb. Sebagian vendor motherboard juga melakukan pengecekan terhadap kehadiran mouse dan/atau keyboard untuk POST test.\
Untuk motherboard yang menggunakan BIOS (Basic Input Output System) akan mencari disk yang memiliki file bootable pada bagian awal sektor untuk memulai sistem operasi.\
Pada sistem UEFI (Unified Extensible Firmware Interface), firmware akan mencari partisi EFI yang menggunakan filesystem FAT-32. Dalam partisi tersebut, firmware akan mencari file sistem operasi dengan format .efi yang mengarah pada kernel sistem operasi tersebut dan menyerahkan proses kepada kernel.

### GRUB2/Systemd Boot
Pada sistem operasi modern, BIOS/UEFI tidak akan memuat kernel sistem operasi secara mandiri. Tugas ini kini diserahkan sepenuhnya ke bootloader pihak ketiga yang memiliki kompatibilitas dengan BIOS/UEFI.\
**GRand Unified Bootloader 2** yang sekarang menjadi bootloader utama untuk mayoritas distribusi GNU/Linux. GRUB2 adalah program yang membuat komputer cukup pintar untuk mencari kernel sistem operasi dan memasukkannya kedalam memori.\
Pada BIOS, GRUB2 akan di install pada Master Boot Record (MBR) pada sektor 512-byte awal disamping tabel partisi pada HDD/SSD.
GRUB2 mendukung sistem baik dengan Legacy BIOS maupun UEFI.\
**Systemd boot**

## GNU/Linux

## Praktikum 1.1

## Todo
[  ] Melengkapi Linux Boot Process dengan gambar dan penjelasan\
[  ] Melengkapi definisi dan penjelasan terkait sistem operasi GNU/Linux\
[  ] Membuat modul praktikum untuk mahasiswa

