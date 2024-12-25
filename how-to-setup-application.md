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
or
```bash
docker run --name my_app -p 8080:1337 -e DATABASE_CLIENT=postgres -e DATABASE_NAME=? -e DATABASE_HOST=? -e DATABASE_PORT=? -e DATABASE_USERNAME=? -e DATABASE_PASSWORD=? prawee/strapi
```

## UI
### Name
  Container Name = my_app
### Ports
  - 8080:1337
### Environment Variable
  - DATABASE_CLIENT=postgres
  - DATABASE_NAME={ชื่อฐานข้อมูล}
  - DATABASE_HOST= `คำสั่งในการหาตาม os (windows) => ipconfig, (Linux/mac) => ifconfig *** ใน local ให้สังเกต 192.168.x.x`
  - DATABASE_PORT={port ที่ mapping ไว้ตอนสร้าง container}
  - DATABASE_USERNAME={ชื่อผู้ใช้งานฐานข้อมูล}
  - DATABASE_PASSWORD={รหัสผ่านของฐานข้อมูล}
