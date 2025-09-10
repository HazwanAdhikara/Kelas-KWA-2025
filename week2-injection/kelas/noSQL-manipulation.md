# NoSQL Manipulation

Update multiple product reviews at the same time.

## Reference

- https://github.com/payloadbox/sql-injection-payload-list
- https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SQL%20Injection

## Steps

1. Saya tahu bahwa endpoint `/rest/products/reviews` dipakai untuk memperbarui ulasan produk. Jadi, saya pun intercept request edit review `(PATCH)` menggunakan Burp Suite.

2. Saya menyadari bahwa field `id` ternyata bisa dimanipulasi. Karena database yang digunakan adalah MongoDB, maka ia menerima operator seperti `$ne (not equal)`. Artinya, saya bisa memanfaatkan NoSQL Injection untuk menargetkan banyak entri sekaligus.
