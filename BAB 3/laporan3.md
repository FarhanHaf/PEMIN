# Integrasi MongoDB dan Express

1. memeriksa NodeJS sudah terinstall
   ![node js](https://github.com/FarhanHaf/PEMIN/assets/103462399/0dcea7e5-3fa9-4b76-ba2e-be153b223583)

# Inisiasi project Express dan pemasangan package
1. Lakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam folder tersebut lalu buka melalui text editor masing-masing
   dan Lakukan npm init untuk mengenerate file package.json dengan menggunakan command `npm init -y`
   ![npm init](https://github.com/FarhanHaf/PEMIN/assets/103462399/a77684f2-abf3-4953-b754-9a9c79423aa1)

2. Lakukan instalasi express, mongoose, dan dotenv dengan menggunakan command `npm i express mongoose dotenv`
   ![npm dotenv](https://github.com/FarhanHaf/PEMIN/assets/103462399/b48a353c-ddba-4f9e-b833-5bcf70857368)

# Koneksi Express ke MongoDB

1. membuat file index.js pada root folder dan memasukkan kode
   ![index js](https://github.com/FarhanHaf/PEMIN/assets/103462399/d1af7ef1-2ff5-48e9-917d-e49d2dfd8050)

2. Lakukan pembuatan file .env dan masukkan port
![env](https://github.com/FarhanHaf/PEMIN/assets/103462399/2e6ef18b-3fa0-44fe-8b1f-de18cda7a47c)

    Setelah itu ubahlah kode pada listening port menjadi berikut
   ![tambah index](https://github.com/FarhanHaf/PEMIN/assets/103462399/bee0d747-7f3e-4e3a-beb1-870d4488cb86)

3. Copy connection string yang terdapat pada compas atau atlas dan paste kan pada .env seperti berikut
   ![mongo_uri](https://github.com/FarhanHaf/PEMIN/assets/103462399/25828ee3-8f48-435b-9297-392220d9c021)

4. Menjalankan Aplikasi
   ![start port 5000](https://github.com/FarhanHaf/PEMIN/assets/103462399/7e1489f2-108f-453a-b5f9-3deee92e33f6)

# Pembuatan Routing
1. Lakukan pembuatan direktori routes di tingkat yang sama dengan index.js
   
2. Buat file book.route.js di dalamnya
   
3. Tambahkan syntax berikut untuk fungsi getAllBooks, getOneBook, createBook, updateBook, dan deleteBook\
   ![addFuncBookRoute](https://github.com/FarhanHaf/PEMIN/assets/103462399/cdd83f02-8a16-46b4-9734-b6699b69d91e)

5. Melakukan import book.route.js pada file index.js dan tambahkan baris kode berikut
   ![import book index](https://github.com/FarhanHaf/PEMIN/assets/103462399/31bfc063-49fe-41e1-8737-44d1933f486c)

6. Uji endpoint dengan Postman
   ![uji postman](https://github.com/FarhanHaf/PEMIN/assets/103462399/7e7776b0-c32e-4b39-8d81-cd2238bc8d7e)

# Pembuatan Controller
1. Lakukan pembuatan direktori controllers di tingkat yang sama dengan index.js
2. Buatlah file book.controller.js di dalamnya
3. Salin baris kode dari routes untuk fungsi getAllBooks, getOneBook, createBook, updateBook, dan deleteBook\
   ![ChangeFuncBookControl](https://github.com/FarhanHaf/PEMIN/assets/103462399/3a77c3de-f61c-417c-8550-a58d4a9525dc)

5. Lakukan import book.controller.js pada file book.route.js dan ubah pada fungsi agar dapat memanggil fungsi dari book.controller.js
   ![ChangeFuncBookRouet](https://github.com/FarhanHaf/PEMIN/assets/103462399/70833573-7870-4f3a-a84a-59fd5096c244)

6. Lakukan pengujian kembali, pastikan response tetap sama
   ![addbookPost2](https://github.com/FarhanHaf/PEMIN/assets/103462399/a9a7f689-7ecd-41cb-95fd-2d01614124f3)

# Pembuatan Model
1. Lakukan pembuatan direktori models di tingkat yang sama dengan index.js
2. Buatlah file book.model.js di dalamnya
3. Tambahkan kode pada book.model.js
   ![BookModels](https://github.com/FarhanHaf/PEMIN/assets/103462399/a1c7748f-b582-4661-afc7-73dd2602bf67)

# Operasi CRUD
1. Hapus semua data pada collection books
![hapusdata](https://github.com/FarhanHaf/PEMIN/assets/103462399/760c85f1-ad59-4c09-af57-c66b5ccf81ee)

2. Lakukan import book.model.js pada file book.controller.js dan ubah fungsi createBook
   ![importbookmodels change func](https://github.com/FarhanHaf/PEMIN/assets/103462399/2d1db51e-5e53-457f-b7a3-a64f05916ca9)

3. Membuat dua buah buku dengan Postman
   ![addbookPost](https://github.com/FarhanHaf/PEMIN/assets/103462399/ec20c719-047d-45a7-b4c4-d3af8838c783)
   ![addbookPost2](https://github.com/FarhanHaf/PEMIN/assets/103462399/0eb06be7-dd17-4393-8196-9a7064aefe9c)

4. Lakukan perubahan pada fungsi getAllBooks, getOnebook
   ![ChangeFuncgetAll and One Book](https://github.com/FarhanHaf/PEMIN/assets/103462399/a92a8de4-b84e-4f91-a2db-7a71b3303a22)

5. Menampilkan semua buku dengan Postman
   ![TampilSemuaBuku](https://github.com/FarhanHaf/PEMIN/assets/103462399/de0562a5-7091-48ae-9337-a1218982661e)

6. Menampilkan buku dilan 1990
   ![TampilSatuBuku](https://github.com/FarhanHaf/PEMIN/assets/103462399/12ce8558-aafa-44b8-b3af-cd521b32eb0a)

7. Melakukan perubahan pada fungsi updateBook
   ![ChangeUpdateBook](https://github.com/FarhanHaf/PEMIN/assets/103462399/5469aeb0-3e65-4ef4-854b-95ad6c236c61)

9. Mengubah judul buku Dilan 1991 menjadi “<NAMA PANGGILAN> 1991” dengan Postman
   ![UbahJudulBuku](https://github.com/FarhanHaf/PEMIN/assets/103462399/6b9e3cb1-9856-4ecd-8d56-295a2bab0bd0)
 
11. Lakukan perubahan pada fungsi deleteBook
    ![ChangeDeleteBook](https://github.com/FarhanHaf/PEMIN/assets/103462399/5025c287-28f1-4930-8114-0f8eb24e2783)

13. Hapus buku Dilan 1990 dengan Postman
    ![DeleteSatuBuku](https://github.com/FarhanHaf/PEMIN/assets/103462399/4bbe349f-47b0-4ad1-a055-f112790fffc2)








