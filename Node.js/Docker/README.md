# Docker
Docker is a container-providing software technology promoted by Docker, Inc. Docker provides an additional layer of operating system-level virtualization abstraction and automation on Windows and Linux.

## Commands

```bash
# view all running databases
docker ps
# view all databases
docker ps -a
# stop the execution of all databases
docker stop databases
# start a database
docker start "nameBd"
```

## Create images
```bash
# run a postgres image
docker run --name database -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres

# run a mongoDb image
docker run --name mongobarber -p 27017:27017 -d -t mongo

# run a redis image
docker --run redisbarber -p6379:6379 -d -t redis:alpine
```
