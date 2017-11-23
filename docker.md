## Docker commands
# Start docker service (Ubuntu only?)
`sudo service docker start`

## Docker images
# View downloaded images
`docker images`

# Remove intermediate images built during a build
`docker rmi $(docker images -f "dangling=true" -q)`

## Containers
# View running containers
`docker ps`

# Remove all containers not running
`docker rm $(docker ps -q -f status=exited)`


# Build
Assuming you are in the same directory as the project with 'Dockerfile':
`docker build --no-cache --rm . -t <<docker-image-name>>:0.1 -t <<docker-image-name>>:latest`

# Run
You can then run it by:
`docker run --rm docker-image-name`

# Inspecting status of the docker image and network setup
`docker inspect <CONTAINER-NAME>`
`docker network ls`
`docker network inspect bridge`

# Commands for a running container
## Start bash shell in running container
You can enter a new bash terminal in the container using:
`docker exec -i -t <CONTAINER-NAME> /bin/bash`

## Copy file from docker container

