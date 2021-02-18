- prisma example project modified for postgresql

# Repro steps

```
$ psql
create database example;
```

```
npm install
npx migrate dev --preview-feature
```

expected: migrate dev runs
actual:

```
Environment variables loaded from prisma/.env
Prisma schema loaded from prisma/schema.prisma
Datasource "db": PostgreSQL database "example", schema "public" at "localhost:5432"

Error: P3005

The database schema for `localhost:5432` is not empty. Read more about how to baseline an existing production database: https://pris.ly/d/migrate-baseline
```
