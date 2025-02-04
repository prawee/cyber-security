# How to create store data

## On render website
1. Name with `cybersec-{your-class}-store-{your-name}` Exp. `cybersec-ced-store-prawee`
2. Project with `ced`
3. Database
  - dbname  `{your-name}` Exp. `prawee`
  - user `{your-name}` Exp. `prawee`
4. Region with `Singapore`
5. PostgreSQL Version `16`
6. Instance Type `Free`

## How to connect db
### Single Line
postgres://{username}:{password}/{dbname}
### Configure with variable
DATABASE_CLIENT=postgres
DATABASE_HOST=
DATABASE_PORT=
DATABASE_NAME=
DATABASE_USERNAME=
DATABASE_PASSWORD=
DATABASE_SSL=false
