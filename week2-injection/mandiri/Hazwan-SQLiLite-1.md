# SQLiLite (picoCTF)

<img src="./img/1-soal.png">

## Reference

- https://github.com/payloadbox/sql-injection-payload-list
- https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SQL%20Injection

## Steps

1. Launch instance terlebih dahulu, ketika dibuka muncul login page. Saya mencoba inject dengan beberapa payload. Disini saya menggunakan `' OR 1=1 --` dengan password bebas.

<img src="./img/1-payload.png">

<img src="./img/1-loggedin.png">

2. Setelah itu, tinggal inspect di source code dan flagnya ada di tag hidden.

<img src="./img/1-flag.png">
