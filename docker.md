## Docker

### List Containers
List running containers
```sh
docker ps
```
List all containers
```sh
docker ps -a
```

### Docker Build Images
To execute `Dockerfile` to generate an image, just do:
```sh
docker build -t [IMAGE_NAME] [DOCKER_FILE_PATH]
```
like:
```sh
docker build -t example .
```

### Remove Container
```sh
docker rm [CONTAINER_ID]
```

### Run Container
```sh
docker -p [PORT_IN_LOCAL]:[PORT_IN_CONTAINER] [IMAGE_NAME]
```
like:
```sh
docker -p 3333:3333 example
```

### Access Container Terminal
```sh
docker exec -it [CONTAINER_NAME] /bin/bash
```
like:
```sh
docker exec -it example /bin/bash
```

## Docker compose

### Run Docker Compose
```sh
docker-compose up
```