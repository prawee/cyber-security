# How to mapping volume of data

```bash
nano docker-compose.yml
```

```bash
services:
   ...
   db:
      ...
      volumes:
         - ./database/data:/var/lib/postgres/data
```
