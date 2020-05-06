# Docker tricks

## Finding containers

This will get you the latest 5 tags for ANY image:

```Bash

docker run --rm jess/reg:v0.15.8 tags mcr.microsoft.com/azure-cli | sort -ur | head -5

```

## Docker commands for cleaning up containers and images

- This will remove all stopped containers

```Bash
docker container prune
```

- List all containers

```Bash
docker container ls -a
```

- List all Images

```Bash
docker images
```

- Remove unused data

```Bash
docker system prune -a
```

- Get a list of all image ids and remove those images (Remove all)

```Bash
docker rmi $(docker images -a -q)
```

- Kill all running containers

```Bash
docker rm $(docker ps -a -q)
```

- Remove all containers

```Bash
docker rm $(docker ps -a -q)
```

- Get a list of IDs of the running containers

```Bash
docker ps -a -q
```

- Get a list of images

```Bash
docker images
```
