# Docker Basics
In this exercise you will understand the docker image name and container registry.
It is strongly advised to complete 0_docker_basics before proceeding to 1_docker-basics

# Basic Docker Commands

```bash
# to create a container, you need respective image in your local
# The fully qualified name of image is comprised of
# DOCKER_REGISTRY - the central repo where docker images are stored
# DOCKER_REPOSITORY (or) IMAGE_NAME - the name of the image
# IMAGE_TAG - the version of the image  

# Try pulling different docker images from docker hub (https://hub.docker.com/)
# search for images like nginx, started
# use one of the various tags used in image home page
# Ex. docker pull <DOCKER_REISTRY>/<DOCKER_REPOSITORY>:<IMAGE_TAG> 

docker pull docker.io/library/nginx:1.27.4-alpine
docker pull docker.io/library/nginx:latest # latest tag will always point to latest version

# if the DOCKER_REGISTRY is omitted, by default it will point to docker hub (docker.io)
docker pull alpine:latest

# it is also possible to point to our custom registry.
# Google hosts its own public container registry. (https://console.cloud.google.com/gcr/images/google-containers/GLOBAL?invt=AbtMzA&walkthrough_id=panels--container-registry--images)
# check the list of images and try pulling some images from google container registry using docker pull command
```