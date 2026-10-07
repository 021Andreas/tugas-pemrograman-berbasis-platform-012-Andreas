# Tugas Mandiri 3 — Memahami Request dan Response

## Pengujian `/get`

**Request:**
```text
GET https://httpbin.org/get?nama=Umar&kelas=TI
```

HTTPBin menampilkan kembali informasi request yang diterima server. Query parameter dapat dilihat pada bagian `args`.

Contoh:
```json
{
  "args": {
    "nama": "Umar",
    "kelas": "TI"
  }
}
```

## Pengujian `/headers`

**Request:**
```text
GET https://httpbin.org/headers
```

Endpoint `/headers` digunakan untuk melihat HTTP header yang diterima server.

## Jawaban Pertanyaan

### Apa yang dimaksud request?

Request adalah permintaan yang dikirim client kepada server untuk meminta data atau melakukan operasi tertentu.

### Apa yang dimaksud response?

Response adalah jawaban yang diberikan server setelah menerima dan memproses request.

### Apa fungsi query parameter?

Query parameter digunakan untuk mengirim informasi tambahan melalui URL, misalnya untuk filter, pencarian, atau parameter tertentu.

### Apa fungsi HTTP header?

HTTP header membawa informasi tambahan mengenai request atau response, seperti jenis konten dan informasi client.

### Apa perbedaan data pada URL dengan data pada request body?

Data pada URL, seperti query parameter, terlihat pada alamat request. Request body berisi data yang dikirim sebagai isi request dan dapat digunakan untuk mengirim data terstruktur seperti JSON.
