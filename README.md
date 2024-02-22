# wajik-anime-api

Streaming dan download Anime subtitle Indonesia

# Sumber:

MOHON IZIN ABANG SUMBER, sumber bisa bertambah, bisa dm rekomendasi situs yang bagus

- https://otakudesu.cloud

domain sering berubah 2 jangan lupa pantau terus

# Installasi

- Jalankan perintah di terminal

```sh
# clone repo
git clone https://github.com/wajik45/wajik-anime-api.git

# masuk folder
cd wajik-anime-api

# install dependensi
npm install

# jalankan server
npm start
```

- Server akan berjalan di http://localhost:3001

# Routes

| Endpoint  | Params | Description                                                 |
| --------- | ------ | ----------------------------------------------------------- |
| /{source} |        | Deskripsi rute ada di response jangan lupa pake JSON viewer |

### Contoh request

```js
(async () => {
  const response = await fetch("http://localhost:3001/otakudesu/ongoing");
  const result = await response.json();

  console.log(result);
})();
```

### Contoh response

```json
{
  "statusCode": 200,
  "message": "Ok",
  "data": [
    {
      "judul": "Dr. Stone Season 3 Part 2",
      "slug": "drstn-s3-p2-sub-indo",
      "poster": "https://otakudesu.cloud/wp-content/uploads/2024/01/Dr.-Stone-Season-3-Part-2-Sub-Indo.jpg",
      "episodeTerbaru": "11",
      "hariRilis": "Jum'at",
      "tanggalRilisTerbaru": "05 Jan",
      "otakudesuUrl": "https://otakudesu.cloud/anime/drstn-s3-p2-sub-indo/"
    }
  ],
  "pagination": {
    "prevPage": false,
    "currentPage": 1,
    "nextPage": 2,
    "totalPages": 4
  },
  "error": false
}
```
