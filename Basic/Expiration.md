## Expiration

- Secara default saat kita menyimpan data ke redis, redis akan menyimpannya secara permanen sampai kita menghapusnya
- Kadang kita mendapatkan kasus ingin menghapus data di redis secara otomatis dalam waktu tertentu
- Misal kita menyimpan data cache di redis selama 10 menit, setelah 10 menit kita akan query ulang ke database untuk mendapatkan data terbaru
- Hal ini bisa dilakukan di redis, redis memiliki fitur expiration secara otomatis pada data yang kita simpan di redis

```bash
SET habi "Haabibich"
EXPIRE habi 5
TTL habi

SETEX habi 10 "Habi XD"
```