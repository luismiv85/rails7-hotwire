# README

| Technology | Version |
|--|--|
| Ruby | 2.7.1 |
| Ruby on Rails | 7.0.4 |
| Node | v14.2.0 |
| Yarn | 1.22.19 |
| Postgres | 14.5 |

Init Proyect
---
1. Clone project.
2. Install the versions of the technologies mentioned above. Maybe you want to use next docker-compose to install postgres.
```
version: '3.7'

services:
  db:
    image: postgres:14.5
    restart: always
    environment:
      - POSTGRES_USER=postgres
      - POSTGRES_PASSWORD=postgres
    ports:
      - '5432:5432'
    volumes:
      - db:/var/lib/postgresql/data
  adminer:
    image: adminer
    restart: always
    ports:
      - 8080:8080
volumes:
  db:
    driver: local
```
3. Configurar la conexión de base de datos en `database.yml` file.
4. Execute **`bin/setup`** script to set up the application for us: install the gems, the JavaScript dependencies, create, migrate and seed the database.
5. Run project with **`bin/dev`**



