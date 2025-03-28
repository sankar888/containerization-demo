# Docker Basics
In this exercise you will explore the basics of docker. 
Login to [Docker labs](https://labs.play-with-docker.com/) using your google account
ctrl + + to increase font size


# Basic Docker Commands

```bash
# Ensure docker is available
docker --version

# dockerd and containerd are the container runtimes (docker engine) 
ps -ef | grep docker

# list down the images in your local
docker images

# list down the container running in your local machine
docker ps

# pull a docker image from remote central docker repository, then list the docker images
docker pull docker.io/docker/getting-started:pwd

# run the container using docker image and then check the docker ps
docker run --name mycontiner -d -p 80:80 docker.io/docker/getting-started:pwd
docker ps

# when the container is running '80' port will be opened from container to host. open the port using "Open port" button at the top of the labs page.
# refresh twice or thrice, it might take some time for the port to exposed to internet
# you will see a docker getting started tutorials page  

# stop the container, you could user either CONTAINER ID or NAMES to refer individual container
# Ex. docker stop <CONTAINERID or NAMES>
docker stop mycontainer

# the stooped container will still be available, -a option will show containers in all state 
docker ps -a

# start the stopped container
docker start mycontainer
```