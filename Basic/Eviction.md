## Eviction

- Redis mendukung fitur eviction (menghapus data lama, dan menerima data baru)
- Namun untuk mengaktifkan fitur ini, kita perlu memberi tahu redis, maximum memory yang boleh digunakan, dan bagaimana strategi untuk melakukan eviction nya
- https://redis.io/docs/reference/eviction/ 

```bash
# redis.conf
maxmemory 100mb

maxmemory-policy noeviction
```