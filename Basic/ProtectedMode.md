## Protected Mode

- Secara default, ketika kita menyalakan redis server, redis server akan mendengarkan request dari semua network interface. Ini sangat berbahaya, karena bisa jadi redis terekspos secara public
- Namun, redis punya second layer untuk pengecekan koneksi, yaitu mode protected, secara default mode protectednya aktif, artinya walaupun redis bisa diakses dari manapun, tapi redis hanya mau menerima request dari 127.0.0.1 (localhost)

```bash
# redis.conf
# bind 127.0.0.1 -::1
bind 192.168.162.21

redis-cli -h 192.168.162.21 -p 6379
```