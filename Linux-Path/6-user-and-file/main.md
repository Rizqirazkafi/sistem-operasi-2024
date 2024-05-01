# User and File Management

Pada satu sistem operasi bisa memiliki beberapa user/pengguna yang berbeda.
Masing-masing user bisa memiliki file dan aplikasi sendiri. Setiap user juga
dapat memilih file dan/atau aplikasi manakah yang boleh diakses oleh user lain,
baik itu akses read-only maupun full access.

## User Level
Ada beberapa jenis akun user berdasarkan penggunaan dan access level.

- Root User: Akses penuh ke sistem yang dapat mengubah setiap unsur dari sistem.
- Standard User: Akses pengguna terbatas, tidak mampu melakukan aksi yang 
mempengaruhi inti dari pengaturan sistem atau akun pengguna lain.
- Sudo User: Pengguna strandard yang telah diberikan izin untuk menjalankan
perintah tertentu sebagai root user
- System Account: Akun pengguna untuk aplikasi atau layanan otomasi yang butuh
menjalankan pekerjaan spesifik di sistem
- Guest User: Akun sementara dengan akses terbatas dan terkontrol
- User Groups: Izin di berikan ke sekumpulan pengguna yang di organisasikan ke
group logical.

### List User

```bash
cat /etc/passwd
```

### User Existance

Kita bisa membuat user baru dengan perintah dibawah ini:

```bash
sudo useradd newuser
# atau
sudo adduser newuser
# Untuk penambahan informasi user lebih detail

# Untuk menghapus user, gunakan
sudo userdel -r newuser
# ini akan menghapus user beserta home directory
```

### Modify Default user

`usermod` di Linux digunakan untuk memodifikasi atribut dari user yang ada.
* -d - Mengubah directory home dari pengguna
* -s - Mengubah default shell pengguna
* -e - Menetapkan tanggal kadaluarsa akun
* -c - Menambah komentar ke entry pengguna
* -u - Mengubah UID (User ID)
* -aG - Menambah group untuk pengguna yang ada

Di contoh berikut, flag `-d` digunakan untuk mengubah lokasi dari home
directory pengguna.

```bash
sudo usermod -d /var/newuser newuser
```

### Change user
`su` singkatan dari Switch User digunakan untuk berpindah ke user lain.
Apabila tidak didefinisikan, maka akan pindah ke user root.
```bash
su newuser
```

<!-- ### Group Permission -->
<!-- Memodifikasi group akan berefek pada semua user yang berada pada group tersebut. -->
<!---->
<!-- __Create Group__ -->
<!---->
<!-- ```bash -->
<!-- sudo groupadd test_group -->
<!-- # check group -->
<!-- getent group -->
<!-- ``` -->
