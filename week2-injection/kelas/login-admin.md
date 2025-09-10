# Login Admin

Log in with the admin's user account.

## Reference

- https://github.com/payloadbox/sql-injection-payload-list
- https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SQL%20Injection

## Steps

1. diminta untuk login sebagai user `admin` yang dimana kita akan mencoba cari data dari admin di website tersebut. Pada website ini ada tampilan product atau catalog yang berisi review" dari user.

<img src="./img/admincatalog.png">

kita temukan data email dari user `admin` pada page catalog. Email `admin@juice-sh.op` akan kita coba masukkan payload.

2. Berdasarkan referensi ada banyak opsi payload yang digunakan. Saya menggunakan `admin@juice-sh.op' OR 1=1--` lalu passwordnya bebas.

<img src="./img/adminpayload.png">.

3. Hasilnya adalah kita dapat masuk sebagai user `admin` disini.

<img src="./img/adminloggedin.png">
