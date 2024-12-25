# How to setup database with `Postgres` via `Docker`

## CLI
```bash
docker run --name my_db -p 54321:5432 -e POSTGRES_PASSWORD={password} -e POSTGRES_USER={your_name} -e POSTGRES_DB={your_name} postgres
```
- {password} is password of database
- {your_name} is real name

## UI
### Name
  Container Name = my_db
### Ports
  - 54321:5432
### Environment Variable
  - POSTGRES_PASSWORD
  - POSTGRES_USER
  - POSTGRES_DB
