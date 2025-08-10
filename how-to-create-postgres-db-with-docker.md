# How to create postgres with docker file

## 1.Create repository
- create on github account

## 2. Clone repository to your machine
```bash
git clone {url-of-repo}
```

## 3.Create `README.md` file
```
nano README.md | open with IDE on your machine
```
```bash
# Python Prisma

Prawee Wongsa
```

## 4.Define `env`
### 4.1 create `env.simple` file
```bash
nano env.simple | open with IDE on your machine
```
```bash
# Database
DATABASE_PORT=modified
DATABASE_NAME=modified
DATABASE_PASSWORD=modified
DATABASE_USER=modified
```
### 4.2 update `README.md` file
```bash
nano README.md | open with IDE on your machine
```
```bash
...
## Using it
### Windows
copy env.simple .env
### Mac / Linux
cp env.simple .env
```

## 5. Ignore `env`
```bash
nano .gitignore | open with IDE on your machine
```
```bash
.env
```

## 6.Create `db.yml`
### 6.1 create db.yml
```bash
nano db.yml
```
```bash
services:
  db:
    image: postgres:latest
    container_name: my_db_prisma
    environment:
      POSTGRES_USER: ${DATABASE_USER}
      POSTGRES_PASSWORD: ${DATABASE_PASSWORD}
      POSTGRES_DB: ${DATABASE_NAME}
    ports:
      - "${DATABASE_PORT}:5432"
```
### 6.2 update readme file
```bash
nano README.md
```
```bash
docker compose -f db.yml up -d
```

## 7.Backup branch
```bash
git checkout -b "1-create-postgres-db"
git push -u origin 1-create-postgres-db
git checkout develop
```
