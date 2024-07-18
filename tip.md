## Create snapshot of dockerized postgres

```
docker run --name postgres-container -d postgres

docker exec -it postgres-container cp -r /var/lib/postgresql/data postgres-data

docker commit postgres-container postgres-with-data

docker run —env PGDATA=postgres-data -d postgres-with-data
```


