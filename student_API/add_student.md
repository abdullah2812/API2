# Add Student API

Fitur ini digunakan untuk menambahkan data student dari user dengan role tutor.
**URI Pattern**:

```
localhost:3000/addstudent
```

**Request Requirements**:

- Setiap data anak yang akan ditambahkan, harus sesuai dengan format yang telah ditentukan yaitu name, age, kelas, birthday, dan deskripsi. data userId diambil dari user dengan role orangtua yang sedang login pada saat itu.
  Berikut adalah contoh sebuah request yang valid :

```
var settings = {
  "url": "localhost:3000/addstudent",
  "method": "POST",
  "timeout": 0,
  "data": {
    "name": "Lotus",
    "age": "12",
    "kelas": "2 SMP",
    "deskripsi": "Suka ibadah",
    "userId": "1"
  }
};

$.ajax(settings).done(function (response) {
  console.log(response);
});

```

**Response**:
_Response_ yang diberikan dalam bentuk format JSON dengan ketentuan :

- Jika data yang dimasukkan valid maka akan mengembalikan pesan 200, dengan informasi berupa: id, name, age, kelas, dan lainnya.
- Berikut ini adalah contoh response yang diberikan ketika data yang dimasukkan valid.

```
{
    "status": 200,
    "message": {
        "id": 7,
        "name": "Lotus",
        "age": 12,
        "kelas": "2 SMP",
        "birthday": "2021-08-01T00:00:00.000Z",
        "deskripsi": "Suka ibadah",
        "userId": 1,
        "updatedAt": "2021-08-10T09:07:58.271Z",
        "createdAt": "2021-08-10T09:07:58.271Z"
    }
}

```
