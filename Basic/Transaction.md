## Transaction

- Seperti pada database relational, redis juga mendukung transaction
- Proses transaction adalah proses dimana kita mengirimkan beberapa perintah, dan perintah tersebut akan dianggap sukses jika semua perintah sukses, jika gagal maka semua perintah harus dibatalkan

```bash
# Start transaction
MULTI

# Do operations
SET apple "Apple"
SET samsung "Samsung"
SET xiaomi "Xiaomi"
SET nokia "Nokia"
SET oppo "Oppo"

# Execute operations
EXEC

# Discard or Rollback operations
DISCARD
```