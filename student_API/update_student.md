# Update Child API

Fitur ini digunakan untuk mengupdate data student dari user dengan role tutor.
**URI Pattern**:

```
localhost:3000/updatestudent
```

**Request Requirements**:

- student hanya dapat diedit oleh user yang telah login dan memiliki role tutor. Request untuk update berisikan payload yang terdiri atas data name,age, kelas, birthday, dan deskripsi dari child yang akan di update.
  Berikut adalah contoh sebuah request yang valid :

```
var settings = {
  "url": "localhost:3000/updatestudent",
  "method": "PATCH",
  "timeout": 0,
  "data": {
    "name": "Lotus",
    "age": "12",
    "kelas": "2 SMP",
    "deskripsi": "Mencari Kebenaran"
  }
};

$.ajax(settings).done(function (response) {
  console.log(response);
});

```

**Response**:
_Response_ yang diberikan dalam bentuk format JSON dengan ketentuan :

- Jika user yang login memiliki role tutor, maka akan mengembalikan pesan 200, dengan informasi berupa status 200 dan message 1 yang dapat diartikan bahwa data dari child berhasil di update.
- Berikut ini adalah contoh response yang diberikan ketika data yang dimasukkan valid.

```
{
    "status": 200,
    "message": [
        1
    ]
}

```
