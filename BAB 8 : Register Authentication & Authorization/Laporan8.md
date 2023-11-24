1. Pastikan terdapat tabel users yang dibuat menggunakan migration pada bab Basic Routing dan Migration.
   Berikut informasi kolom yang harus ada
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/5b7a8917-ca7e-441c-94bc-adaf213cf870)

2. Pastikan terdapat model User.php yang digunakan pada bab 󾠲 Model, Controller dan Request-Response Handler.
   Berikut baris kode yang harus ada
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/450958d5-ccb9-4e56-a9b6-c476ea0f1252)

3. Buatlah file AuthController.php dan isilah dengan baris kode berikut
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/9a48e366-8f77-4ead-a9c1-fdf31b9bf93e)

4. Menambahkan group route pada `routes/web.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/9690d6c9-e78f-499a-8b06-8783e8e3875a)

5. Jalankan aplikasi pada endpoint /auth/register dengan body berikut
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/bd861ef2-150e-45ef-b509-f7820dee3a99)

## Authentication
1. Buatlah fungsi login(Request $request) pada file AuthController.php
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/fe31ae16-1948-4120-a069-073cb681b2a9)

2. Menambahkan route pada file `web.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/1ec996dd-04b2-4711-b1e5-3ad2d4a298e0)

3. Menjalankan aplikasi pada endpoint `/auth/login` dengan ini body seperti dibawah ini menggunakan postman.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/ab202dfa-f404-4acd-beb1-31abc1e2eb84)

## Token
1. Menjalankan perintah dibawhah ini untuk membuat migrasi baru.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/0bb02487-cb7e-459a-b3f5-a4e997ef3560)

2. Menambahkan sintaks dibawah ini pada file migration yang dibuat pada langkah sebelumnya.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/a31dbe9c-d951-4d3b-919e-91329326b4fb)

3. Menambahkan atribut token di `$fillable` pada `User.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/5d1eed50-51d8-4a9e-9d3f-62b160692764)

4. Menambahkan baris berikut pada file `AuthController.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/a68f25a5-2bac-4a18-89b5-5cda368e8d4c)

5. Menjalankan perintah dibawah ini untuk menjalankan migrasi terbaru.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/04d49ec2-5482-4deb-b515-1a2f0084d441)

6. Menjalankan aplikasi pada endpoint `/auth/login` dengan ini body seperti dibawah ini menggunakan postman, dan salin token yang didapat ke notepad.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/a2b8cdea-f69f-4ca5-bc36-79f635edf2ca)

## Authorization
1. Membuat file `Authorization.php` pada folder `App/Http/Middleware` dan isi dengan sintaks dibawah ini.\
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/7ce84706-5f9a-44ef-aa69-0e444d5bd2bc)

2. Menambahkan middleware yang baru dibuat pada `bootstrap/app.php.`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/4d8b4283-d011-4d75-b978-c073a41f4ea9)

3. Membuat fungsi `home()` pada `HomeController.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/3d2543d3-507f-40f8-8382-ae94dea3b148)

4. Menambahkan route pada file `web.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/68d76c03-83c1-492b-a712-3439dc721c36)

5. Menjalankan alikasi pada endpoint `/home` dengan memasukkan nilai token yang telah didapat sebelumnya.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/3545a912-5cbd-4591-b8ea-32b35ed826f1)
