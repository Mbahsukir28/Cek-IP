
```
bash
#!/bin/bash

echo "Masukkan URL website:"
read url

ip=$(dig +short $url | head -n 1)

if [ -n "$ip" ]; then
  echo "IP website $url adalah: $ip"
else
  echo "Gagal mendapatkan IP website $url"
fi
```
Simpan script ini dengan nama `cek_ip.sh` dan jalankan dengan perintah:
```
bash
bash cek_ip.sh
```
Masukkan URL website yang ingin Anda cek, dan script akan menampilkan IP website tersebut.

Pastikan Anda telah menginstal `dnsutils` di Termux dengan perintah:
```
bash
pkg install dnsutils
```
Atau, Anda bisa menggunakan perintah `dig` langsung di Termux untuk mengecek IP website:
```
bash
dig +short example.com
```
Ganti `example.com` dengan URL website yang ingin Anda cek.
