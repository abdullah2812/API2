# Get Child API

Fitur ini digunakan untuk menampilkan daftar student dari user dengan role tutor.
**URI Pattern**:

```
localhost:3000/tutor-dashboard
```

**Request Requirements**:

- Daftar data anak yang ditampilkan, hanya menampilkan daftar anak dari user dengan role tutor yang telah login pada saat itu.
  Berikut adalah contoh sebuah request yang valid :

```
var settings = {
  "url": "localhost:3000/tutor-dashboard",
  "method": "GET",
  "timeout": 0,
};

$.ajax(settings).done(function (response) {
  console.log(response);
});

```

**Response**:
_Response_ yang diberikan dalam bentuk format JSON dengan ketentuan :

- Jika user yang login memiliki role tutor, maka akan mengembalikan pesan 200, dengan informasi berupa daftar anak dari user dengan role orangtua.
- Berikut ini adalah contoh response yang diberikan ketika data yang dimasukkan valid.

```
{
    "status": 200,
    "message": [
        {
            "name": "Lotus",
            "age": 12,
            "kelas": "2 SMP",
            "deskripsi": "Suka ibadah",
            "userId": 1
        },
        {
            "name": "Wawan",
            "age": 11,
            "kelas": "1 SMP",
            "deskripsi": "Yesaya 5:22",
            "userId": 1
        },
        {
            "name": "Adi",
            "age": 12,
            "kelas": "1 SMP",
            "deskripsi": "Anaknya suka insecure",
            "userId": 1
        }
    ]
}

```
