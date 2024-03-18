## Lists

- Terdapat banyak sekali perintah-perintah yang bisa kita gunakan untuk struktur data List
- Kita bisa lihat semua perintahnya di halaman dokumentasi :
https://redis.io/commands/?group=list 


```bash
LPUSH barca "Messi"
LPUSH barca "Busquets"
LPUSHX barca "Iniesta"

RPUSH barca "Pique"
RPUSHX barca "Neymar"

LRANGE barca 0 2
LLEN barca

LPOP barca 2
RPOP barca 5
```