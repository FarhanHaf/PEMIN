# Basic Routing dan Migration

1. menambahkan endpoint dengan method GET pada aplikasi kita, kita dapat mengunjungi file web.php pada folder routes. Kemudian tambahkan baris ini pada akhir file\
   ![GET](https://github.com/FarhanHaf/PEMIN/assets/103462399/a4731102-af58-49a0-a1b4-f911b03e4bfc)

2. Setelah itu coba jalankan aplikasi dengan command 'php -S localhost:8000 -t public'\
   ![STARTHOST GET](https://github.com/FarhanHaf/PEMIN/assets/103462399/91df2290-4fb2-4f0b-a00c-5deabf1ea23d)

3. menambahkan methode POST, PUT, PATCH, DELETE, dan OPTIONS pada file web.php
   ![OTHER METODE](https://github.com/FarhanHaf/PEMIN/assets/103462399/00597ca8-6bc7-4b16-8dff-4a0e2e8a7d55)

4. Akses url yang baru saja ditambahkan pada aplikasi dengan methodnya menggunakan postman
   ![postman post](https://github.com/FarhanHaf/PEMIN/assets/103462399/f74db295-72db-4b4d-bb35-fc1c6b1d5117)\
   ![postman put](https://github.com/FarhanHaf/PEMIN/assets/103462399/647330dd-423f-4047-be70-c44ddfcf1246)\
   ![postman delete](https://github.com/FarhanHaf/PEMIN/assets/103462399/35db89a5-55d7-43c3-a977-2c5966cad5b6)\
   ![postman patch](https://github.com/FarhanHaf/PEMIN/assets/103462399/a93175ea-cc97-4828-abbc-81f7b01d3336)\
   ![postman options](https://github.com/FarhanHaf/PEMIN/assets/103462399/ded192a9-1c26-4dd2-a208-8ca18db3e00f)\

# Migrasi Database
1. Membuat database pada phpmyadmin dengan nama 'lumenapi'
   ![Create Database](https://github.com/FarhanHaf/PEMIN/assets/103462399/075aa96c-35ae-4ab2-a90f-b084584fcdba)

2. Mengubah konfigurasi database pada file .env sesuai database
   ![env database](https://github.com/FarhanHaf/PEMIN/assets/103462399/69f7d5ac-7c40-4f8a-b387-18f60bb05b03)

3. Menghidupkan beberapa library bawaan dari lumen dengan membuka file app.php pada folder bootstrap\
   ![library on](https://github.com/FarhanHaf/PEMIN/assets/103462399/a3db9120-b941-413d-94a0-2894a24b23e7)

4. jalankan command berikut untuk membuat file migration\
   'php artisan make:migration create_users_table' membuat migrasi untuk tabel users\
   'php artisan make:migration create_products_table' membuat migrasi untuk tabel products\
   ![buat file migration](https://github.com/FarhanHaf/PEMIN/assets/103462399/15f42ac0-747b-4a16-b899-d34e4d516df6)

5. Ubah fungsi up pada file migrasi 'create_users_table' dan 'create_products_table'\
   USER\
   ![func up user](https://github.com/FarhanHaf/PEMIN/assets/103462399/c40ab129-16ec-4a99-9128-70f21c198547)

   PRODUCTS\
   ![func up product](https://github.com/FarhanHaf/PEMIN/assets/103462399/af51d5e1-1457-457b-be84-ff62c94c9a77)
 
6. Migrasi ke database dengan command 'php artisan migrate'
   ![artisan migrate](https://github.com/FarhanHaf/PEMIN/assets/103462399/8058c8f3-fb02-46b2-b90f-7b03182e369a)

   






