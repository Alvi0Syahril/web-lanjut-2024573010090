# Laporan Modul 1: Perkenalan Laravel
**Mata Kuliah:** Workshop Web Lanjut   
**Nama:** Alvi Syahril 
**NIM:** 2024573010090
**Kelas:** TI-2C

---

## Abstrak 
Tuliskan ringkasan singkat tentang isi laporan ini dan tujuan Anda membuat laporan.
Laporan ini membahas Laravel dikenal dengan pendekatan arsitektur MVC (Model-View-Controller), sistem routing yang fleksibel, ORM (Object Relational Mapping) bernama Eloquent, serta berbagai fitur modern lain seperti middleware, migration, dan authentication yang membuat proses pengembangan aplikasi web lebih terstruktur dan efisien.Tujuan dari laporan ini adalah untuk memperkenalkan konsep dasar Laravel, komponen utamanya, struktur folder proyek, serta kelebihan dan tantangan dalam penggunaannya.
---

## 1. Pendahuluan
- Tuliskan teori perkenalan tentang laravel
Laravel dirancang untuk menyelesaikan permasalahan umum yang sering muncul dalam pengembangan web, seperti pengelolaan rute, interaksi dengan database, autentikasi pengguna, serta pengelolaan tampilan.
Meskipun pada dasarnya Laravel adalah framework back-end, Anda bisa menggunakannya untuk pengembangan full-stack dalam PHP, membuat sistem front-end React atau Vue, dan sebagai API back-end.

- Apa itu Laravel?
Laravel adalah framework berbasis PHP yang menggunakan konsep MVC (Model-View-Controller). MVC ini membantu memisahkan antara logika bisnis (Model), tampilan (View).

- Arsitektur MVC → memisahkan antara Model (data), View (tampilan), dan Controller (logika bisnis).
Routing Fleksibel → mendukung berbagai metode HTTP (GET, POST, PUT, DELETE).
Eloquent ORM → interaksi database dengan pendekatan OOP.
Blade Template Engine → membuat tampilan web dinamis dengan sintaks yang sederhana.
Artisan CLI → command line untuk otomatisasi (buat controller, migration, dll).
Migration & Seeder → sistem version control untuk database.
Keamanan bawaan → seperti proteksi CSRF, enkripsi password.

- Untuk jenis aplikasi apa Laravel cocok?
Aplikasi berskala menengah (e-commerce, sistem reservasi, manajemen inventori.).
Aplikasi bersekala kompleks(ERP, LMS, sistem informasi akademik.)
---

## 2. Komponen Utama Laravel (ringkas)
Tuliskan penjelasan singkat (1–3 kalimat) untuk tiap komponen berikut:
- Blade (templating)
Blade adalah engine template bawaan yang ada didalam Laravel yang digunakan untuk membuat tampilan dengan sintaks. 
- Eloquent (ORM)
Eloquent adalah Object Relational Mapper (ORM) Dengan ini proses  interaksi dengan database menggunakan model berbasis PHP, tanpa harus menulis query SQL secara manual.
- Routing
Routing di Laravel mengatur bagaimana aplikasi merespon sebuah request (URL) dari user. dan menentukan URL tertentu harus diarahkan ke fungsi atau controller
- Controllers
Controller berfungsi sebagai penghubung antara Model dan View. Dan dimana logika aplikasi akan ditempatkan, sehingga lebih terorganisir.
- Migrations & Seeders
Penggunaan Migration untuk mengatur struktur database secara version control. Seeder digunakan untuk mengisi data ke dalam tabel, seperti data dummy atau data default.
- Artisan CLI
Artisan CLI adalah command line interface bawaan Laravel yang berfungsi sebagai penyedida perintah dan untuk mempercepat pengembangan, seperti membuat migration, controller,model,
- Testing (PHPUnit)
laravel menyediakan vitur testing dengan PHPUnit untuk memastikan fitur atau fungsi dalam aplikasi berjalan sesuai yang di  inginkan. ini bertujuan untuk mencegah bug pada aplikasi saat proses pengembangan lebih lanjut.

---

## 3. Berikan penjelasan untuk setiap folder dan files yang ada didalam struktur sebuah project laravel.

Berikut ini adalah Folder-Folder yang ada di laravel

1.**App**
Folder app berisi Di dalamnya terdapat komponen utama seperti Models, Controllers, dan Middleware.

2.**Bootstrap**
folder bootstrap Folder ini mengandung file yang digunakan untuk proses inisialisasi aplikasi, termasuk app.php yang bertugas memuat seluruh komponen inti Laravel.

3.**Config**
Folder config memiliki peran krusial dalam pengaturan aplikasi. Semua konfigurasi utama, seperti database, mail, session, cache, dan layanan pihak ketiga, disimpan di sini dalam bentuk file PHP.

4.**Database**
Folder database digunakan untuk mengelola hal-hal yang berhubungan dengan basis data. Di dalamnya terdapat migration, seeder, dan factory.

5.**public**
Folder public berfungsi sebagai gerbang utama aplikasi. Semua file yang dapat diakses secara langsung oleh pengguna, seperti index.php, aset gambar, CSS, dan JavaScript, ditempatkan di sini. File index.php

6.**Resources**
Folder resources adalah tempat penyimpanan sumber daya aplikasi, meliputi file view berbasis Blade, file bahasa untuk internasionalisasi, serta aset front-end seperti CSS dan JavaScript sebelum dikompilasi. beberapa file routing akan tersedia seperti: web.php, api.php, console.php, dan channels.php.

7.**Storage**
Folder storage adalah yang digunakan untuk menyimpan file sementara, log aplikasi, cache, serta file yang diunggah pengguna. Laravel membagi folder ini menjadi beberapa sub-direktori, seperti logs, app, dan framework.

8.**Tests**
Folder tests adalah tempat untuk mendukung praktik Test-Driven Development (TDD). Pengembang dapat menuliskan unit test maupun feature test guna memastikan bahwa aplikasi berjalan sesuai harapan dan bebas dari bug. Folder ini sangat bermanfaat untuk menjaga kualitas kode,

9.**Vendor**
adalah tempat semua dependensi aplikasi yang dikelola melalui Composer. Semua library pihak ketiga, termasuk inti Laravel itu sendiri, ditempatkan di sini.

Berikut adalah file-file yang tersedia secara default:

10.**Editorconfig**
ile ini digunakan untuk menjaga konsistensi gaya penulisan kode di antara tim pengembang. Misalnya, pengaturan indentasi (spasi atau tab), ukuran indentasi, encoding file (UTF-8), hingga penempatan akhir baris.

11.**.env dan .env.example**
Teile .env berfungsi untuk menyimpan variabel lingkungan (environment variables) yang bersifat sensitif atau dapat berbeda antara server lokal dan server produksi. Misalnya konfigurasi database (DB_HOST, DB_DATABASE), konfigurasi mail server (MAIL_HOST, MAIL_PORT), hingga APP_KEY.

12.**.gitignore dan .gitattributes**
.gitignore: Berisi daftar file atau folder yang tidak perlu dimasukkan ke dalam version control (Git). Misalnya folder vendor/, node_modules/, atau file .env

.gitattributes: Digunakan untuk mendefinisikan perilaku file tertentu dalam Git, seperti bagaimana file teks diperlakukan (line endings), bahasa file untuk syntax highlighting, atau aturan khusus saat merge.

13.**artisan**
adalah command-line interface (CLI) bawaan Laravel. Dengan Artisan, pengembang dapat menjalankan berbagai perintah, seperti membuat model, controller, migrasi database, menjalankan server lokal, hingga membersihkan cache aplikasi.

14.**composer.json dan composer.lock**
Fcomposer.json: Berisi daftar dependency PHP yang digunakan oleh proyek, termasuk versi minimal yang dibutuhkan.

composer.lock: Menyimpan versi pasti dari semua dependency yang diinstal.

15.**package.json**
File ini mirip dengan composer.json, tetapi khusus untuk dependency berbasis JavaScript (Node.js). Di dalamnya terdapat daftar library frontend (misalnya Vue, React, atau Bootstrap) dan alat build (seperti Laravel Mix atau Webpack).

16.**phpunit.xml**
File ini digunakan untuk mengatur konfigurasi testing di Laravel dengan PHPUnit.

17.**readme.md**
File dokumentasi dasar dalam format Markdown. Biasanya berisi penjelasan singkat mengenai proyek, cara instalasi, cara menjalankan, serta catatan penting lainnya.

18.**server.php**
File ini berfungsi sebagai entry point ketika aplikasi dijalankan menggunakan server built-in PHP.
public/index.php
server.php
php artisan serve


19.**webpack.mix.js**
File ini adalah konfigurasi untuk Laravel Mix, sebuah wrapper di atas Webpack yang menyederhanakan proses kompilasi aset frontend (CSS, JavaScript, gambar)

---

## 4. Diagram MVC dan Cara kerjanya

![Berikut adalah Gambar dari diagram MVC Dan Cara kerjanya](gambar/MVC.web)

---

## 6. Kelebihan & Kekurangan (refleksi singkat)
- Sintaks elegan dan mudah dipahami.
- Dokumentasi lengkap.
-Dukungan keamanan bawaan.

- Performa lebih berat dibanding micro-framework (Lumen, Slim).
-Learning curve tinggi untuk pemula.

---

## 7. Referensi
TUTORIAL LARAVELhttps://laracasts.com
https://chatgpt.com/

---
