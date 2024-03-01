## Flush

- Kadang kita butuh mengosongkan seluruh data di redis, misal ketika terjadi kesalahan kode sehingga menyebabkan data di redis salah
- Menghapus data di redis satu-satu menggunakan operasi delete bukanlah hal yang bijak
- Redis memiliki fitur untuk menghapus seluruh data di database redis, yaitu operasi flush

```bash
# Remove all key from a database
FLUSHDB

FLUSHDB ASYNC
FLUSHDB SYNC

# Remove all key from all databases
FLUSHALL
```