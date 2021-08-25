# Delete Child API

Fitur ini digunakan untuk menghapus student dari user dengan role tutor.
**URI Pattern**:

```
localhost:3000/deletestudent
```

**Request Requirements**:

- student hanya dapat dihapus oleh user yang telah login dan memiliki role tutor. Setelah student dihapus maka user tidak dapat menggunakan data yang berhubungan dengan student tersebut.
  Berikut adalah contoh sebuah request yang valid :

```
var settings = {
  "url": "localhost:3000/deletestudent",
  "method": "DELETE",
  "timeout": 0,
};

$.ajax(settings).done(function (response) {
  console.log(response);
});

```

**Response**:
_Response_ yang diberikan dalam bentuk format JSON dengan ketentuan :

- Jika request yang diberikan adalah valid, maka akan mengembalikan pesan 200, dengan informasi berupa status 200 dan message "Student deleted" yang dapat diartikan bahwa student berhasil di hapus.
- Berikut ini adalah contoh response yang diberikan ketika data yang dimasukkan valid.

```
{
    "status": 200,
    "message": "student deleted",
    "data": 1
}

```
