Update user account Type API

Fitur ini digunakan untuk mengedit data dari sebuah akun tertentu yang ada pada database. URI Pattern:

PACTH/user/:id
Request Requirements: Akun hanya dapat diedit oleh user yang telah terautentikasi untuk menjaga keamanan aplikasi dari modifikasi data dari pengguna yang tidak berkepentingan, maka pengguna yang terautentikasi harus dipastikan mengubah data dari akun nya sendiri. Setiap request akan berisikan payload yang terdiri atas data dari akun yang akan di update. Berikut adalah contoh sebuah request yang valid :

HTTP 200 OK
Allow: PATCH, GET, OPTIONS
Content-Type: application/json
Vary: Accept

{
"id": 1,
"username": 'guru',
"email": 'guru@gmail.com',
"password": '$2b$10$yTQR6ZSD95C/uRrrWNa0De5Ezo55Vd8S7FNRhBuQj3a.EO4L7Ut5e',
"fullname": null,
"jeniskelamin": null,
"provinsi": null,
"gaji": null,
"deskripsi": null,
"phonenumber": null,
"address": null,
"role": 'TUTOR',
"createdAt": 2021-08-10T05:06:53.641Z,
"updatedAt": 2021-08-10T05:06:53.641Z
}

Media type:
application/json
Content:

    {
    "fullname": "guru_hebat",
    "jeniskelamin": "Laki - laki",
    "provinsi": "jawa barat",
    "gaji": 2.000.000,
    "deskripsi": "Sangat berprestasi dalam segala bidang",
    "phonenumber": 0822134124,
    "address": "Jln. Aja yuk jadian nanti, no.2 kec. Ghosting"
    }

Response: Response yang diberikan dalam bentuk format JSON dengan ketentuan :

Jika credential tidak valid, maka akan dikembalikan pesan kesalahan (403). Sebaliknya (200), ketika credential valid dan akan dikembalikan data yang telah diupdate. Berikut ini adalah contoh response yang diberikan ketika credential yang diberikan valid.
HTTP 200 OK
Allow: PATCH, GET, OPTIONS
Content-Type: application/json
Vary: Accept

{
"id": 1,
"username": 'guru',
"email": 'guru@gmail.com',
"password": '$2b$10$yTQR6ZSD95C/uRrrWNa0De5Ezo55Vd8S7FNRhBuQj3a.EO4L7Ut5e',
"fullname": "guru_hebat",
"jeniskelamin": "Laki - laki",
"provinsi": "jawa barat",
"gaji": 2.000.000,
"deskripsi": "Sangat berprestasi dalam segala bidang",
"pho"address": "Jln. Aja yuk jadian nanti, no.2 kec. Ghosting",
"role": 'TUTOR',
"createdAt": 2021-08-10T05:06:53.641Z,
"updatedAt": 2021-08-10T05:06:53.641Z
}
