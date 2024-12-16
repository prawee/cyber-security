# How to setup `pgAdmin`

## CLI
```bash
docker run --name pg_admin -p 4433:443 -p 9090:80 -e PGADMIN_DEFAULT_EMAIL={your_email} -e PGADMIN_DEFAULT_PASSWORD={your_password}  dpage/pgadmin4
```
## UI
### Image
- dpage/pgadmin4
### Name
Container Name = pg_admin
### Ports
- 4433:443
- 9090:80
### Environment Variable
- PGADMIN_DEFAULT_EMAIL
- PGADMIN_DEFAULT_PASSWORD
