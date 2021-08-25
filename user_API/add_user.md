Add User Type API

Fitur ini digunakan untuk menambahkan data akun baru dari seorang user. URI Pattern:

POST/register
Request Requirements: Setiap data user yang akan ditambahkan, harus sesuai dengan format yang telah ditentukan yaitu username dan email yang ditambahkan harus bersifat unik (belum pernah digunakan sebelumnya) dan password 1 dan password_confrim harus sama.

Media type:
application/json
Content:

    {
        "username": "guru",
        "email" : "guru@gmail.com'
        "password" : "123"
        "password_confirm" : "123"
        "role" : "TUTOR"
    }

Response: Response yang diberikan dalam bentuk format JSON dengan ketentuan :

Jika data yang dimasukkan valid maka akan mengembalikan pesan 200 Ok, dengan informasi berupa: id, password, last_login, dan lainnya Berikut ini adalah contoh response yang diberikan ketika data yang dimasukkan valid.
HTTP 200 OK
Allow: OPTIONS, POST
Content-Type: application/json
Vary: Accept

{
id: 1,
username: 'guru',
email: 'guru@gmail.com',
password: '$2b$10$yTQR6ZSD95C/uRrrWNa0De5Ezo55Vd8S7FNRhBuQj3a.EO4L7Ut5e',
role: 'TUTOR',
createdAt: 2021-08-10T05:06:53.641Z,
updatedAt: 2021-08-10T05:06:53.641Z
}
