## Client Connection

- Redis menyimpan semua informasi client di server
- Hal ini memudahkan kita untuk melihat daftar client, dan juga mengecek jika ada anomali, seperti terlalu banyak koneksi client ke redis

```bash
# List clients
CLIENT LIST

# ID of current client
CLIENT ID

# Kill client
CLIENT KILL 127.0.0.1:35252
```