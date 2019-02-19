# docker-essentials


# Useful commands

### build docker image
`docker build -t image_name path/to/project`

### run container
`docker run -p <hostPort>:<containerPort> --name container_name image_name`

### Run container in background
`docker run -d -p <hostPort>:<containerPort> --name container_name image_name`

### remove all docker unused images
`docker rmi $(docker image ls -q)`

### remove all docker unused container
`docker rm $(docker ps -q)`

### get docker container ip
`docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container_id>`

### ssh to docker container
`docker exec -i -t <container_id> /bin/bash`
