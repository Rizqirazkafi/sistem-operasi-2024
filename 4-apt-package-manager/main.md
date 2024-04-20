# Package Manager

## Apa itu package/paket?
Source code dari sebuah perangkat lunak akan dikompilasi/dicompile kedalam bentuk
binary oleh pengembang. Baik source code maupun binary akan dikemas dalam format
tertentu oleh distribusi GNU/Linux untuk di distribusikan. Bentuk kemasan inilah 
yang disebut __Package/paket__.

Untuk format pendistribusiannya, bagi paket yang berisi source code biasanya
akan berformat .tar.gz, sedangkan untuk yang sudah berupa binary akan 
menggunakan format .deb untuk distribusi berbasis Debian dan Ubuntu.

## Apa itu repository?
Repository merupakan tempat untuk menyimpan paket yang bisa diakses secara remote.
Contoh repository untuk Ubuntu adalah:

- archive.ubuntu.com/ubuntu

## Apa itu mirror?
Mirror merupakan salinan dari repository utama. Mirror berguna apabila
repository utama terlalu jauh dari jangkauan internet pengguna. Dengan adanya
mirror, akan menambah kecepatan untuk mengunduh paket apabila lokasi mirror
berada dekat dengan pengguna. Contoh mirror ubuntu di Surabaya adalah:

- kartolo.sby.datautama.net.id/ubuntu
- buaya.klas.or.id/ubuntu

## Apa itu dependensi?
Contoh ketika anda tidak bisa menginstall software A sebelum menginstall .NET
Framework di Windows, maka .NET adalah dependensi untuk A. Hubungan ketergantungan
ini dinamakan dependensi(ketergantungan), dimana Paket A butuh paket B, paket B 
butuh paket C, dst, maka ini disebut dependensi.

## Apa itu Package Manager?
Package manager adalah perangkat lunak yang digunakan untuk menginstall dan
menghapus program dari sistem. Package Manager juga melakukan manajemen dependensi
untuk memastikan setiap program yang di install juga di install beserta dependensinya.

Beberapa contoh package manager yaitu APT untuk Ubuntu dan Debian based, pacman
untuk Arch base, portage untuk Gentoo, dan masih banyak lagi.
Dalam kasus Ubuntu dan Debian, APT bertugas mengunduh paket, sedangkan paket
yang diinstall dalam bentuk .deb.

## Praktikum
Dalam praktikum ini, akan digunakan APT sebagai package manager.

```bash
sudo apt update
sudo apt upgrade
sudo apt install fping
sudo apt remove fping
```
