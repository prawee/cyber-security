# How to configure docker-compose

## Create new file
```bash
nano docker-compose.yml | touch docker-compose.yml | vim docker-compose.yml
```

```bash
version: '3'

services:
  app:
    image: prawee/strapi
    container_name: 67-ced-strapi
    environment:
      - DATABASE_CLIENT=postgres
      - ...
      - ...
```

## Running
```bash
docker-compose up
docker-compose down
```