![tambah index](https://github.com/FarhanHaf/PEMIN/assets/103462399/c5e6e412-193a-45be-aa87-1fa09dd2266f)#  Integrasi MongoDB dan Express

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
7. Lakukan pencarian buku dengan author “Osamu Dazai” dengan mengisi filter yang diinginkan dan klik “Find” find book

8. Lakukan perubahan summary pada buku “No Longer Human” menjadi “Buku yang bagus (,) dengan melakukan klik “Edit Document” (berlambang pensil), mengisi nilai summary yang baru, dan melakukan klik “Update” upadate book

9. Lakukan penghapusan pada buku “I Am a Cat” dengan melakukan klik “Remove Document” (berlambang tong sampah) dan melakukan klik “Delete” delete book
