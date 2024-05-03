## Hash

- Hash adalah struktur data berbentuk pair (key-value)
- Dengan menggunakan struktur data Hash ini, kita bisa menentukan key untuk value yang kita ingin gunakan
- Berbeda dengan Lists yang menggunakan index, pada Hash, kita bisa menggunakan key apapun yang kita mau
- Terdapat banyak sekali perintah-perintah yang bisa kita gunakan untuk struktur data Hash
- Kita bisa lihat semua perintahnya di halaman dokumentasi : https://redis.io/commands/?group=hash 

```bash
HSET "user:1" name "Ahmad Rizky Nusantara Habibi" age 20 address "Lombok, Indonesia" job "Software Engineer"
HGET "user:1" name
HKEYS "user:1"
HGETALL "user:1"

HINCRBY "user:1" age 10
```

### Increment & Decrement

- Redis memiliki perintah yang bisa digunakan untuk melakukan increment dan decrement pada value yang terdapat pada Hashes
- Kita bisa menggunakan perintah HINCRBY