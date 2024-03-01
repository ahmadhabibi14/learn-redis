## Server Information

- Kadang kita butuh mendapatkan informasi dan statistik redis server
- Seperti jumlah memory yang sudah terpakai, konfigurasi dan lain-lain
- Redis memiliki fitur ini, sehingga kita sangat mudah untuk mendapat informasi server dan memonitor nya

```bash
INFO

CONFIG GET DATABASES
CONFIG GET *max-*-entries* maxmemory
CONFIG GET BIND
CONFIG GET SAVE
CONFIG GET PORT

CONFIG SET maxclients 1000

# The CONFIG REWRITE command in Redis is used to rewrite the configuration file (redis.conf) with the configuration currently used by the running server. This command is useful when you've made changes to the Redis configuration using the CONFIG SET command, and you want to persist those changes to the configuration file so that they survive a server restart.
CONFIG REWRITE
```