## Persistance

- Media penyimpanan utama redis adalah di memory
- Namun kita bisa menyimpan data di memory redis tersebut di disk jika kita mau
- Namun perlu diingat proses penyimpanan data ke disk redis tidak realtime, dia dilakukan secara scheduler dengan konfigurasi tertentu
- Jadi jangan jadikan redis sebagai media penyimpanan persistence, gunakan redis sebagai database untuk membantu database persistence lainnya

```bash
# redis.conf
save 3600 10 300 100 60 500

# Synchronous
SAVE

# Asynchronous
BGSAVE
```