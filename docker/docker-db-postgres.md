## Run Postgres and pgAdmin4 in Containers

* Start Postgres 
```bash
docker run -d --name postgres -e POSTGRES_PASSWORD=postgres bitnami/postgres
```

> `bitnami/postgres` image is in smaller size than the official `postgress`

* Start Postgres and pgAdmin
```bash
cd docker-compose
docker-compose -f pg-and-admin.yml up -d
```

* Stop
```bash
docker-compose  -f pg-and-admin.yml stop
```

Use ip from `docker inspect postgres | grep IPAddress` for connections setup in pgAdmin4

*Reference*
* https://hub.docker.com/r/bitnami/postgresql/
* https://towardsdatascience.com/how-to-run-postgresql-and-pgadmin-using-docker-3a6a8ae918b5

## Use replications

```bash
docker-compose -f pg-replications.yml up -d
```

```bash
docker-compose -f pg-replications.yml up -d --scale postgres-master=1 --scale postgresql-slave=3
```