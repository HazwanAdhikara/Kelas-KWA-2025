# Login Jim

Log in with the jim's user account.

## Reference

- https://github.com/payloadbox/sql-injection-payload-list
- https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SQL%20Injection

## Steps

1. diminta untuk login sebagai user `jim` yang dimana kita akan mencoba cari data dari jim di website tersebut. Pada website ini ada tampilan product atau catalog yang berisi review" dari user.

<img src="./img/jimcatalog.png">

kita temukan data email dari user `jim` pada page catalog. Email `jim@juice-sh.op` akan kita coba masukkan payload.

2. Berdasarkan referensi ada banyak opsi payload yang digunakan. Saya menggunakan `jim@juice-sh.op'--` lalu passwordnya bebas.

<img src="./img/jimpayload.png">.

3. Hasilnya adalah kita dapat masuk sebagai user `jim` disini.

<img src="./img/jimloggedin.png">
