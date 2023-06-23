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

### MongoDB
Create mongo volume
```
docker volume create --name=mongodata
```

Docker run
```
docker run -d -p 27017:27017 --volume mongodata:/data/db --name mongodb mongo:4.2.5
```

### RabbitMQ
Docker run
```
docker run -d --name my-rabbit -p 5672:5672 -p 15672:15672 rabbitmq:3-management
```
