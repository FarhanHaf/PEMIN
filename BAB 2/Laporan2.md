#CRUD MongoDB

1. Lakukan koneksi ke MongoDB menggunakan connection string
![Connect](https://github.com/FarhanHaf/PEMIN/assets/103462399/a438e075-afa8-4a9d-9fd3-f62386262fa4)

2. Buat database dengan melakukan klik “Create Database”
![create database](https://github.com/FarhanHaf/PEMIN/assets/103462399/9c4bd3dc-b806-4509-a0c8-a230fe16d581)


3. Lakukan insert buku pertama dengan melakukan klik “Add Data”, pilih “Insert Document”, isi dengan data yang diinginkan dan klik “Insert”
   ![insert doc](https://github.com/FarhanHaf/PEMIN/assets/103462399/aceb6fb2-f817-4bdf-af8c-aa48a92e7e3a)


4. Lakukan insert buku kedua dengan cara yang sama.
![insert doc 2](https://github.com/FarhanHaf/PEMIN/assets/103462399/efa30535-dde4-4647-ac85-173bc49b85fc)

5. Lakukan pencarian buku dengan author “Osamu Dazai” dengan mengisi filter yang diinginkan dan klik “Find”
  ![find book](https://github.com/FarhanHaf/PEMIN/assets/103462399/2e59b1ae-a4dc-435d-a17c-bc2d87a78f16)

6. Lakukan perubahan summary pada buku “No Longer Human” menjadi “Buku yang
bagus (<NAMA>,<NIM>) dengan melakukan klik “Edit Document” (berlambang
pensil), mengisi nilai summary yang baru, dan melakukan klik “Update”
![upadate book](https://github.com/FarhanHaf/PEMIN/assets/103462399/5c631a1b-7228-40d3-b4b7-fe7398f38973)

7. Lakukan penghapusan pada buku “I Am a Cat” dengan melakukan klik “Remove
Document” (berlambang tong sampah) dan melakukan klik “Delete”
![delete book](https://github.com/FarhanHaf/PEMIN/assets/103462399/a1f66b72-dd0b-4d90-9f01-7dfda595d516)


## Menggunakan Mongo DB Shell

1. Lakukan koneksi ke MongoDB Server dengan menjalankan command mongosh bagi
yang menggunakan terminal build in OS sehingga tampilan terminal kalian akan
menjadi seperti berikut
![connect mongosh](https://github.com/FarhanHaf/PEMIN/assets/103462399/86c4b3d4-e802-4972-ab7f-428fb833cf45)

2. Mencoba melihat list database yang ada di server dengan menjalankan command
`show dbs`
![show dbs](https://github.com/FarhanHaf/PEMIN/assets/103462399/852eb76e-d750-4870-9873-dadabfbdbc8e)

Untuk berpindah ke database “bookstore” gunakan command `use bookstore` , kalian
dapat memastikan telah berpindah ke database yang benar dengan melihat tulisan
sebelum tanda “>”
![use](https://github.com/FarhanHaf/PEMIN/assets/103462399/3972bead-7461-45bf-99f9-2920dcc917eb)

Cobalah untuk melihat collection yang ada pada database tersebut dengan
menggunakan command `show collections`
![show coll](https://github.com/FarhanHaf/PEMIN/assets/103462399/a48ea9ef-c988-4b94-89bc-3a563867cf66)

3. Lakukan insert buku “Overlord I” dengan menggunakan command
`db.books.insertOne(<data kalian>)` , setelah insert buku berhasil maka MongoDB akan
mengembalikan pesan sebagai berikut.

![Cuplikan layar 2023-09-18 222814](https://github.com/dimassputro28/Praktikum-PEMIN/assets/145313055/c3f47078-9367-4666-8034-beef296dca72)


4. Lakukan insert buku “The Setting Sun” dan “Hujan” dengan insert many dengan
menggunakan command `db.books.insertMany(<data kalian>)` , dan akan mengembalikan pesan sebagai berikut.
![insertone](https://github.com/FarhanHaf/PEMIN/assets/103462399/10e0d703-a79d-431a-9988-3f003ae700f4)

5. Lakukan pencarian buku dengan menggunakan command `db.books.find()` untuk
melakukan pencarian semua buku.
![find()](https://github.com/FarhanHaf/PEMIN/assets/103462399/affe888d-16e4-4554-b2c7-878fa6330441)

6. Tampilkan seluruh buku dengan author “Osamu Dazai” dengan mengisi argument
pada find() dengan menggunakan command `db.books.find({<filter yang ingin
diisi>})`
![search osamu](https://github.com/FarhanHaf/PEMIN/assets/103462399/00d3251e-a054-44fd-b6e5-b0c1bdc6b3cf)

7. Lakukan perubahan summary pada buku “Hujan” menjadi “Buku yang bagus
(<NAMA>,<NIM>) dengan mengunakan `command db.books.updateOne({<filter>},
{$set: {<data yang akan di update>}})` sehingga output yang dihasilkan oleh MongoDB
akan menjadi seperti berikut
![updateOne](https://github.com/FarhanHaf/PEMIN/assets/103462399/e4ccb8b7-45f5-4484-b76c-6f61778ba582)

8. Lakukan perubahan publisher menjadi “Yen Press” pada semua buku “Osamu
Dazai” dengan menggunakan command `db.books.updateMany({<filter>}, {$set: {<data
yang akan di update>}})`
![updateMany](https://github.com/FarhanHaf/PEMIN/assets/103462399/0e75d560-af3b-4c9a-be21-3e6cccd9edfb)

9. Lakukan penghapusan pada buku “Overlord I” dengan menggunakan command
`db.books.deleteOne({<argument>})`
![deleteOne](https://github.com/FarhanHaf/PEMIN/assets/103462399/8b41055b-5a07-4ffe-b089-68eae24c53f4)

10.Lakukan penghapusan pada semua buku “Osamu Dazai dengan menggunakan
command `db.books.deleteMany({<argument>})` 
![delete many](https://github.com/FarhanHaf/PEMIN/assets/103462399/f98f6768-295a-4090-9e7e-d3d6ba6d49bc)
