View User

Fitur ini digunakan untuk melihat daftar dari keseluruhan data akun dari semua user yang ada pada database. URI Pattern:

GET/user
Request Requirements: Untuk dapat meilhat daftar dari seluruh data akun user yang ada pada aplikasi, maka pengguna yang berhak melakukannya adalah hanya oleh Admin saja. Hal ini dilakukan untuk menjaga keamanan data dari setiap user. Berikut adalah contoh sebuah request yang valid :

GET http://localhost/user

Response: Response yang diberikan dalam bentuk format JSON dengan ketentuan :

Jika credential tidak valid, maka akan dikembalikan pesan kesalahan (403)Foribidden. Sebaliknya (200), ketika credential valid serta yang masuk adalah Admin, maka akan dikembalikan daftar data akun setiap user. Berikut ini adalah contoh response yang diberikan ketika credential yang diberikan valid.
HTTP 200 OK
Allow: GET, OPTIONS
Content-Type: application/json
Vary: Accept

[
{
id: 1,
username: 'guru',
email: 'guru@gmail.com',
password: '$2b$10$yTQR6ZSD95C/uRrrWNa0De5Ezo55Vd8S7FNRhBuQj3a.EO4L7Ut5e',
fullname: null,
jeniskelamin: null,
provinsi: null,
gaji: null,
deskripsi: null,
phonenumber: null,
address: null,
role: 'TUTOR',
createdAt: 2021-08-10T05:06:53.641Z,
updatedAt: 2021-08-10T05:06:53.641Z
},
{
id: 2,
username: 'ortu',
email: 'ortu@gmail.com',
password: '$2b$10$65hf3igJ.AnB2NNTtc4kO.RQR7nCVWoRW5gd9pHR9yB5d.60pDwQO',
fullname: null,
jeniskelamin: null,
provinsi: null,
gaji: null,
deskripsi: null,
phonenumber: null,
address: null,
role: 'ORANGTUA',
createdAt: 2021-08-10T09:46:11.112Z,
updatedAt: 2021-08-10T09:46:11.112Z
}
]
