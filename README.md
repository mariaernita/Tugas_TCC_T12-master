# Docker Compose Dengan PHP

## Langkah pertama adalah menginstall docker terlebih dahulu jika belum ada dockernya
```Langkah-langkahnya bisa searching di google. Jika sudah berhasil kemudian lakukan langkah berikutnya..```

## Buat Dockerfile
```
FROM php:7.0-apache
COPY src/ /var/www/html/
EXPOSE 80
```

## Langkah berikutnya membuat docker-compose.yml
```
version: '2'
services:
  web:
    build: .
    ports:
     - "8000:80"
```

## Buat file php
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Tugas TCC</title>
</head>
<body>
<?php
  echo "Nama    : Adi Primanto";
  echo "<br>";
  echo "NIM     : 155410139";
  echo "<br>";
  echo "Jurusan : Teknik Informatika"
 ?>
</body>
</html>
```

## Lalu lakukan build dengan menggunakan perintah
```
docker-compose up 
atau
docker-compose build kemudian jalankan perintah docker-compose up
```

## Lakukan pengujian dengan membuka pada browser dan ketik "localhost:8000/"
```Maka browser akan menampilkan hasil berupa```
```
Nama : Adi Primanto
NIM : 155410139
Jurusan : Teknik Informatika
```

## Langkah terakhir adalah mengupload tugas docker compose ini ke GitHub
```Jika sudah berhasil di upload maka share link tugas ini ke email yang sudah diberikan :)```
