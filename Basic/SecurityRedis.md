## Security

### Authentication

- Authentication adalah proses verifikasi identitas untuk memastikan bahwa yang mengakses adalah identitas yang benar
- Redis memiliki fitur authentication, dan kita bisa menambahkannya di file konfigurasi di server redis
- Namun perlu diingat, proses authentication di redis itu sangat cepat, jadi pastikan gunakan password sepanjang mungkin agar tidak mudah untuk di brute force 

### Authorization

- Authorization adalah prose memberi hak akses terhadap identitas yang telah berhasil melewati proses authentication
- Redis mendukung hal ini, jadi kita bisa membatasi hak akses apa saja yang bisa dilakukan oleh identitas yang kita buat
- https://redis.io/docs/management/security/acl/ 

<br />
<br />

```bash
# On redis.conf
user default on +@connection
user habi on +@all ~* >habi12345678
```

```bash
redis-cli -h 192.168.162.21 -p 6379

# AUTH <user> <password>
AUTH habi habi12345678
```