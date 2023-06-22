# docker run

### PostgreSQL
Create postgres volume
```
docker volume create --name=postgresdata
```

Docker run
```
docker run -d -p 5432:5432 -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres --volume postgresdata:/data/db --name postgresql postgres
```
