# Tugas Mandiri 5 — Membandingkan SQL Mentah dan ORM

## Operasi yang Dipilih

Operasi yang dipilih adalah mengambil satu data tanaman berdasarkan ID dari tabel `plants`.

Contoh ID yang digunakan adalah `1`.

## A. SQL Mentah

```sql
SELECT *
FROM plants
WHERE id = ?;
```

Contoh menggunakan Node.js dan `mysql2`:

```typescript
const [rows] = await connection.execute(
  "SELECT * FROM plants WHERE id = ?",
  [1]
);
```

Pada pendekatan ini programmer menulis query SQL secara langsung.

## B. ORM

Contoh menggunakan Drizzle ORM:

```typescript
const plant = await db
  .select()
  .from(plants)
  .where(eq(plants.id, 1));
```

ORM menyediakan abstraksi untuk mengakses database melalui API library ORM.

## Perbandingan

### Apa perbedaan SQL mentah dan ORM?

SQL mentah memungkinkan programmer menulis perintah SQL secara langsung. ORM menyediakan abstraksi sehingga programmer dapat mengakses database menggunakan API ORM.

### Apa kelebihan SQL mentah?

SQL mentah memberikan kontrol yang besar terhadap query yang dijalankan dan memungkinkan programmer menentukan query secara detail.

### Apa kelebihan ORM?

ORM membuat kode akses database lebih terstruktur dan dapat mempermudah pengembangan serta pemeliharaan kode.

### Apa risiko SQL injection?

SQL injection adalah serangan ketika input pengguna dimasukkan ke query SQL secara tidak aman sehingga dapat mengubah maksud query dan berpotensi membaca, mengubah, atau menghapus data.

### Mengapa penggunaan parameter query dapat mengurangi risiko SQL injection?

Parameter query memisahkan nilai input dari struktur SQL sehingga nilai tersebut diperlakukan sebagai data, bukan sebagai bagian dari perintah SQL.

Contoh:

```typescript
await connection.execute(
  "SELECT * FROM plants WHERE id = ?",
  [1]
);
```

### Bagaimana ORM membantu programmer dalam mengakses database?

ORM menyediakan API untuk operasi database seperti select, insert, update, dan delete sehingga programmer tidak harus menulis seluruh query SQL secara manual.
