# MySQL server

```
version: '3.9'
services:
   mysql:
    container_name: mysql_flyway
    image: mysql:8.0
    restart: unless-stopped
#    env_file: .env
    environment:
      #MYSQL_ALLOW_EMPTY_PASSWORD: 'true'
      #MYSQL_DATABASE: ${MYSQL_DATABASE}
      #MYSQL_PASSWORD: ${MYSQL_PASSWORD}
      MYSQL_ROOT_PASSWORD: ${MYSQL_ROOT_PASSWORD}
    ports:
      - "3306:3306"
    volumes:
      - db-mysql:/var/lib/mysql
volumes:
    db-mysql: {}
```

# PostgreSQL

```
version: '3.9'
services:
  postgresql:
    container_name: postgres_flyway
    image: postgres:14.1-alpine
    restart: unless-stopped
    environment:
      - POSTGRES_USER=root
      - POSTGRES_PASSWORD=1234
      - POSTGRES_LOGGING=true
      - POSTGRES_INITDB_ARGS=--auth-host=scram-sha-256
    ports:
      - "5432:5432"
    volumes:
      - db:/var/lib/postgresql/data
volumes:
    db: {}
```

