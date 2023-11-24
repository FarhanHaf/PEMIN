# JSON Web Token (JWT)

## Penyesuaian Database
1. Merubah kolom token pada file migrasi `AddColumnTokenUsers`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/2a3711da-4f77-4edc-aa03-02056053cb87)

2. Menjalankan pereintah `php artisan migrate:fresh` untuk memperbarui data yang lama.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/37ded066-3052-4612-a690-fbdcaf6a5928)

3. Menjalankan endpoint `/auth/register` menggunakan postman seperti dibawah ini.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/964599b6-071c-4085-b949-db461a6e157e)

## JWT Manual
1. Menambahkan 3 fungsi pada file `AuthController.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/4309815b-8076-464b-a83e-28430f590173)

2. Merubah fungsi login.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/9ac7df7a-85e4-47be-880a-4af673dc93e7)

3. Menambahkan 4 fungsi pada file `Middleware/Authorization.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/52300041-4d74-495f-a9b7-da1aa1455c80)

4. Melakukan perubahan pada fungsi `handle` pada file `Authorization.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/ae88a451-60c3-4e0b-a971-813b8b35140e)

5. Menjalankan endpoint `/auth/login` menggunakan postman serta menyalin token yang didapat setelah menjalankan endpoint tersebut.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/b1d4e678-688b-420c-9ed5-be262ea57f14)

6. Menjalankan endpoint `/home` serta memasukkan token yang telah didapat dari langkah sebelumnya.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/669a30f4-045e-40a6-9d41-8e29c97e827d)

## JWT Library
1. Melakukan akses terhadap website `https://djecrety.ir/` dan generate jwt key secara online.\
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/872860d1-ebac-42de-8137-9ee02934b51e)
Setelah mendapatkan key yang sudah di generate lakukan perubahan pada file `.env` dengan membuat variabel baru dengan nama `JWT_SECRET` dan isi value nya dengan jwt key yang sudah di generate pada langkah sebelumnya.\
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/6e562e10-db2e-4ea2-ac84-46eb5011112f)

2. Melakukan instalasi package jwt firebase dengan menjalankan perintah `composer require firebase/php-jwt`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/bac57e17-3f2c-4d8e-8337-56c173b52b22)

3. Menambahkan fungsi dibawah ini pada file `AuthController.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/fc025318-5887-4ef2-a336-a0f1c56a9489)

4. Merubah fungsi `login` pada file `AuthController.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/844d8057-2cc9-4093-8fcf-35eceb084596)

5. Membuat `JwtMiddleware.php` dan isi file tersebut dengan sintaks dibawah ini.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/9b967dea-73ee-4454-9b6d-a40519704dce)

6. Menambahkan middleware yang dibuat pada langkah sebelumnya pada `bootstrap/app.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/d85c5319-e5dd-4fa7-aeb8-6ffb66a4fdf6)

7. Menambahkan route baru pada `web.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/152fca75-c1cd-4902-99f4-74a90fad93bb)

8. Menjalankan endpoint `/auth/login` dengan menggunakan postman dan menyalin token yang didapat setalah menjalankan endpoint tersebut.

9. Menjalankan endpoint `/home` serta memasukkan token yang didapat dari langkah sebelumnya.
