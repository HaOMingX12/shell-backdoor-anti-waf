Shell Backdoor Anti WAF

Deskripsi:
Shell Backdoor Anti WAF ini adalah sebuah skrip PHP yang dirancang untuk memberikan akses tak sah ke server melalui mekanisme login yang sangat sederhana. Skrip ini juga memiliki kemampuan untuk mengeksekusi kode PHP yang diambil dari URL eksternal. Meskipun ini adalah contoh teknis dari metode yang digunakan dalam eksploitasi keamanan, penggunaannya pada sistem produksi sangat tidak disarankan karena potensi risikonya yang tinggi.

Fitur
Autentikasi Pengguna: Skrip menggunakan cookie sederhana untuk mengidentifikasi pengguna yang telah login. Hanya pengguna yang memiliki cookie dengan nilai tertentu yang dapat mengakses fungsionalitas utama dari backdoor ini.


Eksekusi Kode Dinamis: Setelah login, skrip dapat mengambil dan mengeksekusi kode PHP dari URL eksternal. Ini memungkinkan penyerang untuk menjalankan kode yang mungkin disimpan di server lain.


Metode Pengambilan Konten: Skrip menggunakan beberapa metode untuk mendapatkan konten dari URL, termasuk curl, file_get_contents, dan fopen.


Cara Kerja

Autentikasi:


Skrip memeriksa apakah cookie user_id ada dan nilainya cocok dengan 'chou'.

Jika tidak, skrip menampilkan formulir login.

Login:asukau


Jika password yang dimasukkan benar, cookie akan diatur dan akses diberikan.

Eksekusi Kode:

Jika pengguna sudah login, skrip akan mendownload dan mengeksekusi kode PHP dari URL yang ditentukan menggunakan fungsi geturlsinfo.
Fungsi ini mencoba beberapa metode untuk mendapatkan konten dari URL jika salah satu metode tidak tersedia.
