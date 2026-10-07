# Tugas Mandiri 1 — Mengenal HTTP Method dan Endpoint

## Hasil Pengujian

| No | Method | Endpoint | Data yang Dikirim | Status | Hasil |
|---:|---|---|---|---:|---|
| 1 | GET | `/get` | Query parameter `nama=Andre`, `kelas=TI` | 200 | Server mengembalikan query parameter serta informasi request. |
| 2 | POST | `/post` | JSON `{"nama":"Andre","kelas":"TI"}` | 200 | Server mengembalikan data JSON yang dikirim pada response. |
| 3 | PUT | `/put` | JSON `{"nama":"Andre","status":"mahasiswa"}` | 200 | Server mengembalikan data JSON dan informasi request PUT. |
| 4 | PATCH | `/patch` | JSON `{"status":"aktif"}` | 200 | Server mengembalikan data JSON dan informasi request PATCH. |
| 5 | DELETE | `/delete` | Tidak ada body | 200 | Server mengembalikan informasi request DELETE. |

## 1. GET `/get`

**URL:** `https://httpbin.org/get?nama=Andre&kelas=TI`

**Tujuan:** Menguji request GET dengan query parameter.

**Data yang dikirim:**
```text
nama=Andre
kelas=TI
```

**Status:** `200 OK`

**Response:** HTTPBin mengembalikan query parameter pada bagian `args`, serta informasi seperti headers, origin, dan URL.

Contoh:
```json
{
  "args": {
    "kelas": "TI",
    "nama": "Andre"
  }
}
```

## 2. POST `/post`

**URL:** `https://httpbin.org/post`

**Tujuan:** Menguji pengiriman data JSON melalui request body.

**Data yang dikirim:**
```json
{
  "nama": "Andre",
  "kelas": "TI"
}
```

**Status:** `200 OK`

**Response:** Data JSON yang dikirim dikembalikan pada bagian `json`, bersama informasi request lainnya.

## 3. PUT `/put`

**URL:** `https://httpbin.org/put`

**Tujuan:** Menguji request PUT dengan JSON body.

**Data yang dikirim:**
```json
{
  "nama": "Andre",
  "status": "mahasiswa"
}
```

**Status:** `200 OK`

**Response:** HTTPBin mengembalikan data JSON yang dikirim dan informasi request PUT.

## 4. PATCH `/patch`

**URL:** `https://httpbin.org/patch`

**Tujuan:** Menguji request PATCH dengan JSON body.

**Data yang dikirim:**
```json
{
  "status": "aktif"
}
```

**Status:** `200 OK`

**Response:** HTTPBin mengembalikan data JSON yang dikirim dan informasi request PATCH.

## 5. DELETE `/delete`

**URL:** `https://httpbin.org/delete`

**Tujuan:** Menguji request DELETE.

**Data yang dikirim:** Tidak ada request body.

**Status:** `200 OK`

**Response:** HTTPBin mengembalikan informasi request DELETE seperti headers, origin, URL, dan data request.

## Kesimpulan

Kelima HTTP method berhasil diuji dan mendapatkan status `200 OK`. GET menggunakan query parameter, sedangkan POST, PUT, dan PATCH menggunakan request body JSON. DELETE diuji tanpa request body.
