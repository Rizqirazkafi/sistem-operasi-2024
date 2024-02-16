# Linux Boot Process

## BIOS/UEFI POST Test
POST (Power On Self Test). Pada tahap ini, setelah tombol **power** ditekan, sistem akan menjalankan serangkaian tes untuk memastikan semua hardware berjalan dengan baik. Proses ini meliputi tes CPU, RAM, Disk (HDD/SSD), GPU, dsb. Sebagian vendor motherboard juga melakukan pengecekan terhadap kehadiran mouse dan/atau keyboard untuk POST test.\
Untuk motherboard yang menggunakan BIOS (Basic Input Output System) akan mencari disk yang memiliki file bootable pada bagian awal sektor untuk memulai sistem operasi.\
Pada sistem UEFI (Unified Extensible Firmware Interface), firmware akan mencari partisi EFI yang menggunakan filesystem FAT-32. Dalam partisi tersebut, firmware akan mencari file sistem operasi dengan format .efi yang mengarah pada kernel sistem operasi tersebut dan menyerahkan proses kepada kernel.

## GRUB2/Systemd Boot
Pada sistem operasi modern, BIOS/UEFI tidak akan memuat kernel sistem operasi secara mandiri. Tugas ini kini diserahkan sepenuhnya ke bootloader pihak ketiga yang memiliki kompatibilitas dengan BIOS/UEFI.\
**GRand Unified Bootloader 2** yang sekarang menjadi bootloader utama untuk mayoritas distribusi GNU/Linux. GRUB2 adalah program yang membuat komputer cukup pintar untuk mencari kernel sistem operasi dan memasukkannya kedalam memori.\
Pada BIOS, GRUB2 akan di install pada Master Boot Record (MBR) pada sektor 512-byte awal disamping tabel partisi pada HDD/SSD.
GRUB2 mendukung sistem baik dengan Legacy BIOS maupun UEFI.\
**Systemd boot** adalah bootloader alternatif dari GRUB. systemd-boot dikhususkan untuk hardware dan sistem operasi berbasis UEFI. Cara kerjanya hampir sama dengan GRUB. Namun daripada menggunakan MBR, systemd-boot menggunakan GPT agar bisa digunakan.

