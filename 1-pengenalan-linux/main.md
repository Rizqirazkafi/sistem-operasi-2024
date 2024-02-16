# Linux

## Praktikum 1.1

### Instalasi Ubuntu
**Persiapan:**
1. Device dengan spesifikasi minimum 4 Core CPU, 8GB RAM, 50GB Free-space, 8GB USB.
1. Mahasiswa menginstall salah satu Virtual-Machine Manager ([VirtualBox](https://www.virtualbox.org/wiki/Downloads), [VMware](https://www.vmware.com/products/workstation-player.html), [virt-manager](https://virt-manager.org/))
1. Mahasiswa mendownload ISO salah satu distribusi GNU/Linux (Disarankan [Ubuntu](https://ubuntu.com/desktop)).

**Membuat bootable device**
1. Download [Ventoy](https://www.ventoy.net/en/download.html) untuk membuat bootable device.
1. Extract archive dengan [WinRAR](https://www.rarlab.com/download.htm), [Peazip](https://peazip.github.io/index.html), atau [GNU tar](https://savannah.gnu.org/git/?group=tar).
1. Jalankan executable ventoy-GUI.
1. Ubah flashdisk menjadi ventoy device
1. Copy ISO kedalam flashdisk

**Instalasi**
1. Tancapkan flashdisk ke port USB sebelum menyalakan PC
1. Tekan/spam/tahan tombol BIOS
1. Ubah boot order ke USB device
1. Simpan dan keluar

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

Untuk peta dari Linux Kernel bisa diakses [Linux Kernel Map](https://makelinux.github.io/kernel/map/)


## User Space Distribusi GNU/Linux



## Todo
[  ] Melengkapi definisi dan penjelasan terkait sistem operasi GNU/Linux\
[  ] Membuat modul praktikum untuk mahasiswa

