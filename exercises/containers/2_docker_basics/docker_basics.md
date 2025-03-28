# Docker Basics
In this exercise you will understand the docker run options
It is strongly advised to complete 0_docker_basics before proceeding to 2_docker-basics

# Basic Docker Commands

```bash
# Docker run command runs the docker image. it will pull image from remote repository if it is not available in local
# docker run <FULLY_QUALIFIED_IMAGE_NAME>
docker run --name welcome --rm -d -p 8080:8080 --memory=1024m --cpus=2 docker.io/library/nginx:1.27.4-alpine   

# --name - gives a container a name. will be helpful when referring the container
# --rm - deletes the container when the container is stopped. if this option is used it will not be available in docker ps -a
# -d - runs the container in background
# -p maps the <container_port>:<host_port>. this is necessary for accessing the process outside the container
# --memory - limits the container memory up to this limit
# --cpus -  limits the cpu usage up to this limit 
# Explore the meaning of various options using docker run --help 

# to view logs
docker logs --tail 1000 -f welcome

# it is also possible to get into the container and check its file system, 
# execute commands from inside the running container
docker exec -it welcome sh

# check the hostname, this will point to container id
hostname

# check the /usr/share/nginx/html directory.
# web contents will be served from this directory
cd /usr/share/nginx/html
ls -al

# exit to exit th container
```