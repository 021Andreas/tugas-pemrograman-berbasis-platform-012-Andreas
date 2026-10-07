# Tugas Mandiri 2 — Memahami HTTP Status Code

## Hasil Pengujian

| Status Code | Arti | Hasil Pengujian | Kapan Digunakan |
|---:|---|---|---|
| 200 | OK | Server berhasil memproses request. | Ketika request berhasil. |
| 201 | Created | Server berhasil membuat resource baru. | Setelah berhasil membuat resource/data baru. |
| 400 | Bad Request | Request dari client tidak valid. | Ketika terdapat kesalahan pada request client. |
| 401 | Unauthorized | Request membutuhkan autentikasi yang valid. | Ketika autentikasi belum diberikan atau tidak valid. |
| 403 | Forbidden | Server memahami request tetapi menolak akses. | Ketika client tidak memiliki izin mengakses resource. |
| 404 | Not Found | Resource atau endpoint tidak ditemukan. | Ketika resource atau URL yang diminta tidak tersedia. |
| 500 | Internal Server Error | Terjadi kesalahan internal pada server. | Ketika server mengalami error internal yang tidak terduga. |

## Endpoint yang Diuji

```text
GET https://httpbin.org/status/200
GET https://httpbin.org/status/201
GET https://httpbin.org/status/400
GET https://httpbin.org/status/401
GET https://httpbin.org/status/403
GET https://httpbin.org/status/404
GET https://httpbin.org/status/500
```

## Jawaban Pertanyaan

### Apa perbedaan 400 dan 404?

Status 400 menunjukkan bahwa request yang dikirim client tidak valid atau tidak dapat diproses. Status 404 menunjukkan bahwa resource atau endpoint yang diminta tidak ditemukan.

### Apa perbedaan 401 dan 403?

Status 401 menunjukkan bahwa request membutuhkan autentikasi yang valid. Status 403 menunjukkan bahwa server memahami request tetapi client tidak memiliki izin untuk mengakses resource.

### Mengapa 500 menunjukkan masalah pada sisi server?

Status 500 termasuk kelompok server error dan menunjukkan bahwa terjadi kesalahan internal ketika server memproses request.

### Apakah semua error HTTP berarti server mengalami kerusakan?

Tidak. Status 400, 401, 403, dan 404 dapat menunjukkan masalah pada request atau akses dari client. Status 500 menunjukkan kesalahan pada sisi server.
