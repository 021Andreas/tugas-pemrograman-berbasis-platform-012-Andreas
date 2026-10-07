# Tugas Mandiri 4 — Pengujian API dengan Postman dan curl

## A. Menggunakan Postman

### GET

```text
GET https://httpbin.org/get
```

Request GET digunakan untuk meminta data dari HTTPBin.

### POST

```text
POST https://httpbin.org/post
```

JSON yang dikirim:

```json
{
  "nama": "Umar",
  "kelas": "Informatika"
}
```

Response POST mengembalikan data JSON yang dikirim pada bagian `json`.

## B. Menggunakan curl

### curl `-i`

Perintah:

```powershell
curl.exe -i https://httpbin.org/get
```

Opsi `-i` menampilkan HTTP response headers beserta response body.

Pengujian status 404:

```powershell
curl.exe -i https://httpbin.org/status/404
```

### curl `-s`

Perintah:

```powershell
curl.exe -s https://httpbin.org/get
```

## C. Perbandingan `curl -s` dan `curl -i`

`curl -s` menggunakan mode silent sehingga output tambahan dari curl tidak ditampilkan dan response body dapat terlihat lebih bersih. `curl -i` menampilkan response headers beserta response body. Opsi `-s` berguna ketika hanya membutuhkan hasil response tanpa informasi tambahan dari curl. Opsi `-i` berguna ketika ingin melihat status code dan header HTTP yang diberikan server.
