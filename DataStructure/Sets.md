## Sets

- Sets adalah struktur data mirip seperti Lists, namun yang membedakan adalah, pada Sets, isi data harus unik
- Jika kita memasukkan data yang sebelumnya sudah ada, maka otomatis data tersebut tidak akan diterima
- Data di Sets itu tidak berurutan sesuai waktu kita memasukkan data ke Sets, jadi kita tidak bisa menjamin urutan data di dalam Sets, hal ini dikarenakan data Sets akan
- Terdapat banyak sekali perintah-perintah yang bisa kita gunakan untuk struktur data Sets
- Kita bisa lihat semua perintahnya di halaman dokumentasi : https://redis.io/commands/?group=set

```bash
SADD race "Habi" "Dian" "Doni"
SADD race "Habi" "Dian" "Doni" "Ruby" # return 1 bc 3 other data is exist in db

TYPE race

SISMEMBER race "Habi"
SREM race "Doni"

SCARD race
SMEMBERS race
```

### Membandingkan Set

- Karena Sets adalah struktur data yang berisi nilai-nilai yang unik, jadi terdapat operasi yang bisa kita gunakan untuk membandingkan antar Sets
- SDIFF digunakan untuk melihat perbedaan (different) dari Sets pertama dengan Sets lainnya
- SINTER digunakan untuk melihat kesamaan (intersect) dari beberapa Sets
- SUNION digunakan untuk melihat gabungan unik (union) dari beberapa Sets

```bash
SADD hacker "Gilang" "Dimas" "Gian" "Wahyu" "Habi"

SDIFF race hacker
SINTER race hacker
SUNION race hacker
```