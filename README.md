## Ubuntu Dockerfile


This repository contains **Dockerfile** of [Ubuntu](http://www.ubuntu.com/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/dockerfile/ubuntu/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [ubuntu:14.04](https://registry.hub.docker.com/u/library/ubuntu/)


### Usage

    docker build -t ubuntu .
    docker run -t -d ubuntu  /bin/bash
    docker exec -ti <container_id> /bin/bash
    Inside the container
        sudo apt update
        sudo apt install npm
    
    When finished with the container, please exit and commit
    sudo docker commit <container_id> ubuntu-near:latest
   
   Then go to Dockerfile and change to 
   # Pull base image.
   FROM ubuntu-near:latest

   Each time you do a change please don't forget to commit otherwise the changes won't be persisted
