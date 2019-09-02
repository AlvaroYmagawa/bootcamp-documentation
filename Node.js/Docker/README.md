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

## Start databases
```bash
# up a container to run a image of mongoDb
docker run --name mongobarber -p 27017:27017 -d -t mongo

# run a image of redis
docker --run redisbarber -p6379:6379 -d -t redis:alpine
```
