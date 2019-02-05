# 10515106_uas_ecom

Aplikasi Pendataan Siswa di SMK Sinar Parahyangan
Hasil dari project ini yaitu aplikasi pendataan Siswa di SMK Parahyangan dengan menggunakan framework Laravel ver 5.7. Aplikasi ini dibuat sebagai tugas besar UAS untuk mata kuliah E-Commerce Lanjut

# Penginstallan Laravel
Project ini menggunakan framework laravel, untuk menginstall laravel di perangkat anda yaitu dengan cara copy saja satu folder fresh install laravel dari orang lain ke perangkat kamu. Kemudian akses Laravel kalian seperti contoh yang saya yaitu http://localhost/10515106_UAS_ECOM/public

# Integrasi Laravel dengan Template AdminLTE 2.3.11
Laravel yang telah di install kemudian di integrasikan dengan template admin LTE 2.3.11. Langkah awal yaitu persiapkan template AdminLTE 2.3.11 yang bisa didapatkan dari alamat https://codeload.github.com/almasaeed2010/AdminLTE/zip/v2.3.11. Selanjutnya buat folder assets di folder public laravel. Copy folder dist, bootstrap dan plugin dari template AdminLTE ke folder tersebut. Kemudian buat folder baru dengan nama templates pada folder resources/views di laravel kamu. Kemudian didalam folder templates, buat 2 file dengan nama header.blade.php dan footer.blade.php Kemudian buat folder baru dengan nama kelas pada folder resources/views di laravel kamu. Didalam folder kelas, buat file dengan nama index.blade.php Kemudian buka folder AdminLTE-2.3.11 kamu, kemudian cari file blank.html di folder pages/examples Selanjutnya buka file tersebut dengan editor kesayanganmu. Lakukan langkah-langkah berikut:

Copy Line 1 s.d 391, paste di file templates/header.blade.php
Copy line 392 s.d 432, paste di file index.blade.php
Copy line 433 s.d 654, paste di file templates/footer.blade.php Pada file templates/header.blade.php baris 21, tambahkan: @stack digunakan untuk menyimpan potongan script dari hasil @push Masih pada file templates/header.blade.php baris terakhir, tambahkan 2 baris sintaks berikut:
@yield digunakan untuk menyimpan potongan script dari hasil @section
@include digunakan untuk menyisipkan file lain Buka file kelas/index.blade.php, tambahkan pada baris pertama kodingan ini : @extends('templates/header') @section('content')' Dan pada baris terakhir tambahkan : @endsection Pada file templates/header.blade.php dan templates/footer.blade.php lakukan Find and Replace untuk mengganti semua link asset ke folder asset yang sudah kita copy kan tadi. Find : ../.. | Replace : {{asset('assets')}} Buka Command Prompt (dengan cara tekan Shift + Klik Kanan di sembarang tempat, pilih Open windows command windows here) di folder belajarLaravel, buat Controller baru menggunakan artisan dengan syntax berikut: php artisan make:controller Kelas Controller Buka file app/Http/Controllers/KelasController.php, tambahkan sintaks berikut ke dalam kodingan class KelasController : public function index() { return view('kelas/index'); } Selanjutnya buka file routes/web.php, tambahkan kodingan routes yang sudah ada menjadi : Route::get('/', 'KelasController@index); Akses web kalian dengan alamat url sesuai dengan yang sudah di install di awal maka Template AdminLTE 2.3.11 telah terintegrasi ke Laravel anda.

# CRUD
Pada pembahasan selanjutnya akan dijelaskan bagaimana membaca data dari database menggunakan Laravel dan Eloquent. Eloquent sendiri merupakan fitur dari Laravel yang memungkinkan kita memanggil data dari database dalam bentuk Entity Object, tanpa syntax MySQL sama sekali. Untuk membuat database MySQL nya pun akan digunakan fitur migration dari Laravel. Fitur ini bermanfaat sekali apabila kalian sudah membangun project laravel dalam suatu tim. Migration ini membantu web artisan dalam mendefinisikan table (DDL) dalam bentuk sintaks pemrograman PHP. Tutorial Make Simple CRUD sendiri dapat di akses di link berikut : https://drive.google.com/file/d/1AmexPu9OEQEz1cHfvVOHHIx3-47ml-Jm/view

Di link tersebut sudah dijelaskan dengan sangat detail tentang Membuat CRUD yang simpel mulai dari Read Data, Create Data, Updating Data, dan Delete Data.

 # Minimum Sistem Perangkat Yang Dibutuhkan
CPU     :	AMD FX4300 or Intel Core i3 2130	
RAM     :	512 MB RAM	
GPU     :	Intel HD Graphics 3000	
OS      :	32bit versions of Windows® 7
Store   :	500 mB available space	
Network :	Broadband Internet connection
