# Christmas Special

Order the Christmas special offer of 2014.

## Reference

- https://github.com/payloadbox/sql-injection-payload-list
- https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/SQL%20Injection

## Steps

1. Saya penasaran dengan fitur pencarian produk di aplikasi ini. Dari tampilan di browser, URL-nya muncul `#/search?q=....` Tapi setelah saya perhatikan, ternyata itu hanya bagian dari routing milik Angular di sisi klien. Artinya, URL tersebut tidak benar-benar mengirim permintaan ke server.

2. Saya coba analisis request yang benar-benar dikirim. Dari situ saya menemukan endpoint backend, `yaitu /rest/products/search?q=....` Endpoint inilah yang digunakan untuk mengambil data produk dari server. Nah, di titik ini saya menyadari kalau parameter q bisa jadi titik masuk.

3. Berikutnya, saya coba melakukan pencarian biasa dengan memasukkan kata kunci `carrot`. Hasilnya aman. Tapi ketika saya masukkan input yang aneh, query aplikasi jadi error. Dari sini saya mengkonfirmasi bahwa parameter pencarian memang rentan.

4. Saya mendapati ada produk dengan ID tertentu yang seharusnya tidak muncul—produk ini statusnya sudah dihapus atau disembunyikan. Tapi entah bagaimana, datanya masih bisa muncul kembali. Jadi bisa disimpulkan kalau ada data yang seharusnya tidak boleh diakses publik, tapi tetap bisa muncul lewat jalur ini.

5. jadi saya lanjut meninjau proses ketika aplikasi menambahkan produk ke keranjang belanja. Di sana, saya melihat bahwa sistem masih menerima ID produk tersebut. Akibatnya, produk yang seharusnya tersembunyi bisa tetap masuk ke alur pembelian.
