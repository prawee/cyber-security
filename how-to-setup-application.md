# How to setup application with `Strapi4` via `Docker`

## CLI
```bash
docker run
 --name my_app \
 -p 8080:1337 \
 -e DATABASE_CLIENT=postgres  \
 -e DATABASE_NAME=? \
 -e DATABASE_HOST=? \
 -e DATABASE_PORT=? \
 -e DATABASE_USERNAME=? \
 -e DATABASE_PASSWORD=? \
 prawee/strapi
```
## UI
### Name
  Container Name = my_app
### Ports
  - 8080:1337
### Environment Variable
  -DATABASE_CLIENT=postgres
  -DATABASE_NAME=?
  -DATABASE_HOST= `(windows) => ipconfig, (Linux/mac) => ifconfig` *** 192.168.x.x
  `
  -DATABASE_PORT=?
  -DATABASE_USERNAME=?
  -DATABASE_PASSWORD=?
