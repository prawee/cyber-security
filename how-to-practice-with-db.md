# Practice with DB

## Create project
```bash
mkdir cybersec-admin && cd cybersec-admin
pwd
```

## Install package of ORM and db
```bash
npm install prisma | yarn add prisma # orm
npm install sqlite3 | yarn add sqlite3 # db
```
## Initialize prisma and sqlite
```bash
npx prisma
npx prisma init --datasource-provider sqlite
```
## Create model
```bash
cd prisma
nano schema.prisma
```
```bash
...
model User {
  id Int @id @default(autoincrement())
  username String
  password String
}
```
```bash
npx prisma format
```
