# Docker Basics
In this exercise you will build your own docker image
It is strongly advised to complete 0_docker_basics before proceeding to 3_docker-basics

# Building own Docker Image
```bash
# docker build command is used to build docker images
# usually, docker images are built from a prebuilt base os image
# the base images are built from scratch

# lets serve a webserver with our own custom content from the base nginx image
# Dockerfile has the instruction to build docker image
# docker build --rm --tag <DOCKER_REGISTRY>/<DOCKER_REPOSITORY>:<IMAGE_TAG> <Docketfile_path>
cd /root/containerization-demo/exercises/3_building_docker_image
docker build --rm --tag docker.io/<ur_name>/mynginx:1.0.0 .

# after successful build, a new docker image will be present in docker images
docker imaes

# run this new container
docker run --name custom-welcome --rm -d -p 8080:8081 docker.io/<ur_name>/mynginx:1.0.0

# open the port 8081 from ui and check the results  
```