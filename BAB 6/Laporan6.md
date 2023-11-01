# Model, Controller dan Request-Response Handler
### Model
1. Memastikan adanya table users pada aplikasi.
![tableuser](https://github.com/FarhanHaf/PEMIN/assets/103462399/b0989d22-7c74-4519-b6f1-a8fe69068076)

2. Mengganti isi dari file `User.php` pada path `app/Models`dengan menggunakan sintkas dibawah ini.
![userphp](https://github.com/FarhanHaf/PEMIN/assets/103462399/73503b66-3098-4646-be24-a567c544d1ae)


### Controller
1. Membuat salinan dari file `ExampleController.php` pada folder `app/Http/Controllers` dengan nama `HomeController.php` serta membuat function index dengan sintaks dibawah ini.
![homecontrollerphp](https://github.com/FarhanHaf/PEMIN/assets/103462399/ca64e72a-b9cb-4254-9c9d-7190df9c719f)

2. Mengubah route pada file `routes/web/php` seperti dibawwah ini.
![ubah route](https://github.com/FarhanHaf/PEMIN/assets/103462399/7b0df79f-6fb0-46ec-9762-d7b7ca36ad53)


3. Menjalakan aplikasi dengan memasukkan `localhost:8000` pada browser sehingga muncul tampilan seperti dibawah ini.
![jalankan aplikasi](https://github.com/FarhanHaf/PEMIN/assets/103462399/f088a04b-b15b-4849-8085-bc958e26c0d3)

### Request Handler
1. Melakukan import library request pada file `HomeController.php`.
![importlibrary controller](https://github.com/FarhanHaf/PEMIN/assets/103462399/1b1e0613-4b1d-4c26-abcf-6f278f148777)

2. Merubaha `function index()` menjadi seperti dibawah ini.
![ubah index](https://github.com/FarhanHaf/PEMIN/assets/103462399/ee588b4a-3655-43fd-9b3d-c545656fca7a)

3. Menjalankan kembali aplikasi tersebut.\
![jalankan aplikasi2](https://github.com/FarhanHaf/PEMIN/assets/103462399/c5bc97bc-484d-47f1-bf26-e9f7f5900989)

### Response Handler
1. Melakukan import library response pada file `HomeController.php`.
![importlibrary controller2](https://github.com/FarhanHaf/PEMIN/assets/103462399/2ea9cad4-83f8-4b6c-b930-745af7da0654)

2. Membuat `function hello()`.
![addfunction hello()](https://github.com/FarhanHaf/PEMIN/assets/103462399/034dc8c6-dc93-49fd-ba37-35b7838442e1)

3. Menambahkan route `/hello` pada file `routes/web.php`.
![addroute hello](https://github.com/FarhanHaf/PEMIN/assets/103462399/c92761ca-1d4a-4e0c-b664-ac73f30e3e5f)

4. Menjalankan aplikasi pada route /hello.
![jalankan aplikasi hello](https://github.com/FarhanHaf/PEMIN/assets/103462399/70f37183-abde-4724-9141-d93a0640ba3d)

### Penerapan
1. Melakukan import model User dengan menambahkan sintaks berikut pada file `HomeController.php`.
![importlibrary controller3](https://github.com/FarhanHaf/PEMIN/assets/103462399/fb3bf0dd-4957-40af-a6ef-4c8e2b25be2c)

2. Menambahkan `function defaultUser()`, `function createUseer()`, dan `function getUsers()`.
![addtigafungsi](https://github.com/FarhanHaf/PEMIN/assets/103462399/2f110dde-741c-4fd5-83df-4a6f22ceb2d6)

3. Menambahkan route untuk setiap function yang telah dibuat sebelumnya.
![addtiga route](https://github.com/FarhanHaf/PEMIN/assets/103462399/22081b05-0692-49f7-b3e9-853fd1ad2644)

4. Menjalankan aplikasi pada route `/users/default` menggunakan Postman.
![postman default](https://github.com/FarhanHaf/PEMIN/assets/103462399/fd61eea7-9112-43b4-9a25-945bec55db09)

5. Menjalankan kembali aplikasi melalui Postman pada route `/users/new` dengan mengisi field body seperti dibawah ini.
![create new users](https://github.com/FarhanHaf/PEMIN/assets/103462399/f094d6a4-93f4-4842-ad4a-e8bb386a5f9e)

6. Menjalankan aplikasi pada route `/users/all`.
![get user a;;](https://github.com/FarhanHaf/PEMIN/assets/103462399/7e98d752-f0ec-4a1e-aaf9-421557fa56bb)
