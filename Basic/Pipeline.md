## Pipeline

- Perintah yang dikirim dari client ke server redis menggunakan Request/Response protocol
- Artinya tiap request yang dikirim ke server redis, maka redis akan membalasnya secara langsung
- Kadang ada kebutuhan kita mengirim data ke redis dalam jumlah besar, misal ketika ada kasus memindahkan data dari database mysql ke redis
- Jika kita mengirim satu per satu datanya, maka akan butuh waktu lama untuk selesai
- Redis mendukung operasi bulk via pipeline, dimana kita bisa mengirim beberapa perintah sekaligus dalam satu request
- Namun perlu diketahui, server redis tidak akan membalas tiap perintah yang dikirim via pipeline

```bash
# Input file to redis
redis-cli -h host -p port -n database --pipe < input_file

# Example
redis-cli -h localhost -p 6379 -n 1 --pipe < input_file.txt
```