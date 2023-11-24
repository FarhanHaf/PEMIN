## Pembuatan Tabel
1. Memastikan sudah ada database dengan nama `lumenpost`.
![1](https://github.com/FarhanHaf/PEMIN/assets/103462399/5154f7be-2af5-4b89-96c2-314a168cab08)

2. Mengubah konfigurasi database pada file `.env`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/2710bd6f-881d-4e6e-8d8a-7e414c9de12c)

3. Menghidupkan library dengan melakukan uncomment sintak pada file `app.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/d2548e31-bf08-45ff-80bf-fc324376e6e1)

4. Menjalankan perintah dibawah pada command line untuk membuat file migration.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/dff4e7b9-6569-4c07-8024-4b39fa4ae795)

5. Merubah fungsi `up()` pada file `migrasi create_posts_table`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/9f958716-a5d7-4811-85c0-49ad6d4374ce)

6. Merubah fungsi `up()` pada file `create_comments_table`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/60fb11c8-8cc4-461e-acd4-8728f4c1cffd)

8. Merubah fungsi `up()` pada file `create_tags_table`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/a7e95670-2045-46d8-be43-ccb6dd20a0ef)

9. Merubah fungsi `up()` pada file `create_post_tag_table`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/34376685-1628-432a-b6c0-48c5a1d1cec0)

10. Menjalankan command `php artisan migrate`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/5e1b69c6-3d74-475f-8e34-f6af5524e76d)

## Pembuatan Model
1. Membuat file dengan nama `Post.php` dan isi dengan sintak berikut.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/9870e4cd-3244-4cfb-8ca7-142fb56622a0)

2. Membuat file dengan nama `Comment.php` dan isi dengan sintak berikut.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/1603c7f2-b2f0-4dd2-8c84-17d08fe8a6ed)

3. Membuat file dengan nama `Tag.php` dan isi dengan sintak berikut.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/3e5d5373-1909-45d6-94fc-a4b8155846c9)

## Relasi One-to-Many
1. Menambahkan fungsi `comments()` pada file `Post.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/2f0bbce7-0281-4376-9702-b3b24107505d)

2. Menambahkan fungsi `post()` dan atribut postId pada `$fillable` pada file `Comment.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/f74d7956-1065-42a1-915d-779a94b31cd2)

3. Membuat file dengan nama `PostController.php` dan isi dengan sintak berikut.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/f971f35c-f612-4ba4-afa3-14eebdc754b5)

4. Membuat file dengan nama `CommentController.php` dan isi dengan sintak berikut.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/071744aa-166c-4d12-ac60-766a76a5d8d3)

5. Menambahkan sintak dibawah pada `routes/web.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/64b04dc0-4369-4923-bf24-cbfbfb86a006)

6. Membuat satu post menggunakan postman.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/f89c1556-468e-4514-b36d-3eaf155ff28f)

7. Membuat satu comment menggunakan postman.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/40abace0-d3f6-463e-96c4-227f0a8dcd37)

8. Menampilkan post menggunakan postman.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/af4a9479-4dab-4cc6-b866-99a2a48d4205)

## Relasi Many-to-Many
1. Menambahkan fungsi `tags()` pada file `Post.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/b89fe175-8c20-457f-b4be-7119c7a0b268)

2. Menambahkan fungsi `posts()` pada file `Tag.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/f5c82899-43c0-419d-9f15-c47e005f4ee3)

3. Membuat file dengan nama `TagController.php` dan isi dengan sintak berikut.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/dbc2e1fb-e4b4-4c4c-87ee-5408597fd08e)

4. menambahkan fungsi `addTag` dan response `tags` pada `PostController.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/ac329d27-db4e-4496-a131-4cb90948781d)

5. Menambahkan sintak dibawah pada `routes/web.php`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/8639c229-488a-41da-936e-8b55cf56919c)

6. Membuat satu tag menggunakan postman.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/d77d5166-bd23-49a4-bb54-18bac51a7352)

7. Menambahkan tag `jadul` pada post `disana engkau berdua`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/2cf6e271-2a41-499f-9085-3ee66253a5c9)

8. Menampilkan post `disana engkau berdua` menggunakan Postman.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/b3c2ea5f-740a-4274-9fdc-69a2fdaa508b)

9. Membuat postingan `tanpamu apa artinya` menggunakan postman.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/30b8579c-8b5b-4ca9-bd43-2f37b71cb3c6)

10. Menambahkan tag `jadul` pada postingan `tanpamu apa aritnya`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/07c6b712-616c-49e1-b433-378fa84bd1e9)

11. Membuat tag `lagu` menggunakan postman.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/c64f75fa-36fe-4717-b4ae-8a094ee07303)

12. Menambahkan tag `lagu` pada postingan `tanpamu apa artinya`.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/877728d9-bed4-41f0-b2cf-ba943ab6c911)

13. Menampilkan post pertama.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/59afc6a1-339e-4156-b74e-9556f55210ae)

14. Menampilkan post kedua.
![image](https://github.com/FarhanHaf/PEMIN/assets/103462399/f5a7fc29-a975-4baa-922c-26ff2a7e7f3e)
