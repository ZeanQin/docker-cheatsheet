## Image

### Inspect history of a docker image

```bash
docker history [<repository>:<tag> | <image_id>]
```
### Inspect a docker image

```bash
docker inspect [<repository>:<tag> | <image_id>]
```

## Container

### Start a container from image and connect to it

```bash
docker run -it [<repository>:<tag> | <image_id>] sh
```

### Navigate inside a running container

```bash
docker container exec -it <container_id> sh
```

The above command starts a new `sh` process in the container i.e. when running `ps` in the container, there'll be a process called `sh`.

### Detach from a container without stopping it

```bash
ctrl + p + q
```

> The command above allows us to get out of a container without terminating its main process 
> 
> `exit` terminates the main process. If there's only one process in the container, the container will be stopped.


### Delete all containers on the system

```bash
docker rm $(docker ps -aq) -f
```

## Docker Compose

### delete containers, networks, volumes and images

```bash
docker compose down --volumes --rmi all
```
