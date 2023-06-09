# _Super Cashier System_
## Background Project
Andi merupakan pemilik supermarket besar di salah satu kota di Indonesia. Andi memiliki rencana perbaikan proses bisnis yaitu membuat sistem kasir _self-service_ yang dapat memberikan kemudahan kepada para customer termasuk dalam melakukan transaksi jarak jauh. Dengan adanya sistem kasir ini, diharapkan customer dapat dengan mudah menambahkan produk dalam daftar belanja, melakukan perubahan dan aktivitas transaksi lainnya melalui sistem kasir yang telah dibuat.

## Objective & Requirements
### Objective
Membuat sistem kasir berbasis _self-service_  pada supermarket Andi untuk mempermudah Customer dalam melakukan proses transaksi belanja secara mandiri melalui aplikasi yang telah disediakan.
### Requirements
Fitur-fitur yang terdapat pada sistem kasir _self-service_ diantaranya:
1. Membuat ID transaksi Customer.
2. Melakukan input nama produk, jumlah produk, dan harga produk.
3. Melakukan update apabila terjadi kesalahan saat memasukkan input data.
4. Melakukan pembatalan/reset transaksi belanja 
5. Melakukan pengecekan terhadap daftar belanja.
6. Melakukan pembayaran atas transaksi belanja.

## Flowchart
![alt text](https://github.com/destaaa/Pacmann-Project-Phyton/blob/main/Saved%20Pictures/flowchart.png?raw=true)
### Penjelasan Kode Program
* `Transaction` : Class untuk menyimpan seluruh method untuk menjalankan proses transaksi.
* `add_item()` : Method dari class Transaction untuk melakukan penambahan nama item, jumlah dan harga ke dalam daftar belanja.
* `update_item_name()` : Method dari class Transaction untuk melakukan update/perubahan pada nama item yang telah dimasukkan ke dalam daftar belanja.
* `update_item_qty()` : Method dari class Transaction untuk melakukan update/perubahan pada jumlah item yang telah dimasukkan ke dalam daftar belanja.
* `update_item_price()` : Method dari class Transaction untuk melakukan update/perubahan pada harga item yang telah dimasukkan ke dalam daftar belanja.
* `delete_item()` : Method dari class Transaksi untuk menghapus salah satu item beserta jumlah dan harganya.
* `reset_transaction()` : Method dari class Transaction untuk mereset/mengosongkan daftar belanja.
* `check_order()` : Method dari class Transaction untuk menampilkan daftar belanja.
* `total_payment()` : Method dari class Transaction untuk menampilkan total pembelian daftar belanja.
### Penjelasan Alur Program
1. Customer masuk ke sistem dan memasukkan nama untuk mendapat ID transaksi
2. Customer memilih menu "1. Tambah Produk" untuk memasukkan nama-nama produk beserta jumlah dan harganya ke dalam daftar belanja.
3. Apabila Customer salah memasukkan data, Customer dapat:
   - memilih menu "2. Perbarui produk" untuk mengganti nama produk.
   - memilih menu "3. Perbarui jumlah produk" untuk mengganti jumlah produk.
   - memilih menu "4. Perbarui harga produk" untuk mengganti jumlah produk.
4. Apabila Customer merasa kurang yakin dengan produk-produk yang dibelanjakan, maka Customer dapat memilih "5. Hapus produk dari daftar".
5. Customer ingin mengosongkan daftar belanja dan memasukkan produk kembali, maka Customer dapat memilih "7. Reset daftar belanja".
6. Customer dapat melihat daftar belanja dengan memilih menu "6. Cek daftar belanja ".
7. Untuk melakukan pembayaran, Customer dapat memilih menu "8. Pembayaran"

## Test Case
### Test Case 1
Customer ingin menambahkan 2 item baru menggunakan method `add_item()`. Item yang ditambahkan adalah sebagai berikut:
* Nama item: Ayam goreng, Qty: 2, Harga: 20000
* Nama item: Pasta gigi, Qty: 3, Harga: 15000

![alt text](https://github.com/destaaa/Pacmann-Project-Phyton/blob/main/Saved%20Pictures/Add1.png?raw=true)
![alt text](https://github.com/destaaa/Pacmann-Project-Phyton/blob/main/Saved%20Pictures/Add2.png?raw=true)

Daftar belanja setelah ditambahkan:

![alt text](https://github.com/destaaa/Pacmann-Project-Phyton/blob/main/Saved%20Pictures/list1.png?raw=true)

### Test Case 2
Ternyata Customer salah membeli salah satu item dari belanjaan yang sudah ditambahkan, maka Customer dapat menggunakan method `delete_item()` untuk menghapus item yang dipilih. Item yang ingin dihapus adalah Pasta gigi.

![alt text](https://github.com/destaaa/Pacmann-Project-Phyton/blob/main/Saved%20Pictures/delete.png?raw=true)

Daftar belanja setelah item dihapus:

![alt text](https://github.com/destaaa/Pacmann-Project-Phyton/blob/main/Saved%20Pictures/list2.png?raw=true)

### Test Case 3
Ternyata setelah dipikir-pikir, Customer salah memasukkan item yang ingin dibelanjakan. Daripada menghapusnya satu-satu, maka Customer cukup menggunakan method `reset_transaction()` untuk menghapus semua item yang sudah ditambahkan.
Daftar belanja setelah diperbarui:

![alt text](https://github.com/destaaa/Pacmann-Project-Phyton/blob/main/Saved%20Pictures/reset.png?raw=true)

### Test Case 4
setelah Customer selesai berbelanja, maka sistem akan menghitung total belanja yang harus dibayarkan menggunakan method `total_payment()`. Sebelum mengeluarkan output total akan menampilkan daftar belanja.
Daftar belanja ketika melakukan pembayaran:

![alt text](https://github.com/destaaa/Pacmann-Project-Phyton/blob/main/Saved%20Pictures/list3.png?raw=true)

## Conclusion
Project python yang diprogram kali ini merupakan sekumpulan kode yang dibuat untuk mengelola proses transaksi pembelian barang dalam sebuah supermarket. Dalam project ini menggunakan class Transaction dengan beberapa methods di dalamnya :`add_item()`, `update_item_name()`, `update_item_qty()`, `update_item_price()`, `delete_item()`, `reset_transaction()`, `check_order()`, dan `total_payment()`. Method-method tersebut digunakan untuk mengelola data transaksi yang masuk seperti menambah produk, mengubah data produk, meihat daftar belanja, mereset daftar belanja dan melakukan pembayaran serta menghitung diskon yang didapat.

## Future Work
1.  Pengembangan program dengan fungsi yang kompleks seperti adanya pemberitahuan stok tersedia yang ada di swalayan.
2. perbaikan lain mengenai apabila customer(user) menemukan kendala di kemudian hari.
