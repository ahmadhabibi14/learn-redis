## Increment and Decrement

- Operasi Increment & Decrement sekilas sangat mudah dilakukan, hanya tinggal mengupdate data yang di redis dengan data baru (data lama ditambah 1)
- Namun jika operasi dilakukan secara paralel dan dalam waktu yang sangat cepat, hal ini bisa memungkinkan race condition
- Untungnya redis memiliki operasi untuk melakukan increment dan decrement


```bash
# Must be number
SET counter 1

INCR counter
DECR counter

INCRBY counter 5
DECRBY counter 4
```