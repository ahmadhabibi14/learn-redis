## String

```bash
SET nama "Ahmad"
GET nama
EXISTS nama
APPEND nama " Rizky"
GET nama
DEL nama

SETRANGE nama 6 "Rizky Nusantara Habibi"
GETRANGE nama 4 25

MSET budi "100" joko "100" rully "300"
MGET budi joko rully nama test
```