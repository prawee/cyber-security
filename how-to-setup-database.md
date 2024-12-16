# How to setup database with `Postgres` via `Docker`

## CLI
```bash
docker run --name my_db -p 54321:5432 -e POSTGRES_PASSWORD=i8A64_oS -e POSTGRES_USER=prawee -e POSTGRES_DB=prawee postgres
```
## UI
### Name
  Container Name = my_db
### Ports
  - 54321:5432
### Environment Variable
  - POSTGRES_PASSWORD
  - POSTGRES_USER
  - POSTGRES_DB