## Dynamic Route & Middleware

## Langkah Percobaan

1. Dynamic route adalah route yang dapat berubah-ubah, contohnya pada saat kita membuka suatu halaman web, kadang kita melihat '/users/1' atau '/users/2' , hal ini yang dinamakan dynamic routes. Untuk menambahkan dynamic routes pada aplikasi lumen kita, kita dapat menggunakan
syntax berikut,
![dynamic routes](https://github.com/FarhanHaf/PEMIN/assets/103462399/d2435bc2-bab5-4aa6-8a6c-cc7b249f7853)
![users1](https://github.com/FarhanHaf/PEMIN/assets/103462399/71644f1d-abc2-42c9-95db-a71edae852ef)
![user1](https://github.com/FarhanHaf/PEMIN/assets/103462399/73162d91-be00-409c-b98d-002cc1e46e9e)


Saat menambahkan parameter pada routes, kita tidak terbatas pada 1 variable saja, namun kita dapat menambahkan sebanyak yang diperlukan seperti kode berikut,
![post comment12](https://github.com/FarhanHaf/PEMIN/assets/103462399/774c3589-fa8f-4836-ab34-e12a817dd4aa)

Pada dynamic routes kita juga bisa menambahkan optional routes, yang mana optional routes tidak mengharuskan kita untuk memberi variable pada endpoint kita, namun saat kita memanggil endpoint, dapat menggunakan parameter variable ataupun tidak, seperti pada kode dibawah ini,
![optional routes](https://github.com/FarhanHaf/PEMIN/assets/103462399/eb9e98eb-d4e9-48cb-8d6e-176832e0027a)




2. Aliases Route
Aliases Route digunakan untuk memberi nama pada route yang telah kita buat, hal ini dapat membantu kita, saat kita ingin memanggil route tersebut pada aplikasi kita. Berikut syntax untuk menambahkan aliases route
![aliases route](https://github.com/FarhanHaf/PEMIN/assets/103462399/e075b5c5-a077-4546-aa8e-6959679361e3)

![aliases login](https://github.com/FarhanHaf/PEMIN/assets/103462399/7e0cc890-1ed4-4bf7-9484-e4d90c3b497a)


3. Group Route
  Pada lumen, kita juga dapat memberikan grouping pada routes kita agar lebih mudah pada saat penulisan route pada web.php kita. Kita dapat melakukan grouping dengan
menggunakan syntax berikut,
![group route](https://github.com/FarhanHaf/PEMIN/assets/103462399/0b0d498b-c168-446d-96ea-e4869715268c)
![group route test](https://github.com/FarhanHaf/PEMIN/assets/103462399/90b26053-7f55-401f-b7c2-a77321ce4438)


5. Middleware
   Middleware adalah penengah antara komunikasi aplikasi dan client. Middleware biasanya digunakan untuk membatasi siapa yang dapat berinteraksi dengan aplikasi kita dan semacamnya, kita dapat menambahkan middleware dengan menambahkan file pada folder 'app/Http/Middleware' . Pada folder tersebut terdapat file ExampleMiddleware , kita dapat men-copy file tersebut untuk membuat middleware baru. Pada praktikum kali ini akan dibuat middleware Age dengan isi,
  ![Agemiddleware php](https://github.com/FarhanHaf/PEMIN/assets/103462399/64263a4b-6266-4081-8fa8-0b8ccb87a1e6)

Kemudian, setelah menambahkan filter pada 'AgeMiddleware' , kita harus mendaftarkan 'AgeMiddleware' pada aplikasi kita, pada file 'bootstrap/app.php' seperti berikut ini,

![filter bootstrap](https://github.com/FarhanHaf/PEMIN/assets/103462399/065a9b36-7e98-410b-8dd7-3575fb81f98e)
Pada baris 65 terdapat comment mengenai proses mendaftarkan suatu middleware dalam aplikasi kita. Untuk menambahkan middleware pada aplikasi kita, kita dapat men- uncomment baris 75 hingga 77, kemudian menambahkan age middleware ke dalamnya. Namun, karena kita hanya ingin menambahkan middleware pada route tertentu, kita akan menghapus comment pada baris 79 hingga 81, kemudian menambahkan middleware age di dalamnya. Lalu, kita dapat menambahkan middleware pada routes kita dengan menambahkan opsi middleware pada salah satu route, contohnya,

![route age](https://github.com/FarhanHaf/PEMIN/assets/103462399/b9ceb1fc-9961-446a-9a01-929d02530cce)


hasil percobaan dibawah umur, 
![dibawah umur](https://github.com/FarhanHaf/PEMIN/assets/103462399/3d83d079-4b3f-4099-bc3a-7658da30e53b)

hasil percobaan diatas 17 tahun, 
![dewasa](https://github.com/FarhanHaf/PEMIN/assets/103462399/dfe24629-61ab-423d-b9bf-0b01283695c4)

