## Ubuntu Dockerfile


This repository contains **Dockerfile** of [Ubuntu](http://www.ubuntu.com/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/dockerfile/ubuntu/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [ubuntu:14.04](https://registry.hub.docker.com/u/library/ubuntu/)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/dockerfile/ubuntu/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull dockerfile/ubuntu`

   (alternatively, you can build an image from Dockerfile: `docker build -t="dockerfile/ubuntu" github.com/dockerfile/ubuntu`)


### Usage

    docker build -t ubuntu .
    docker run -t -d ubuntu  /bin/bash
    docker exec -ti <container_id> /bin/bash

    sudo docker commit b1c61634132e338dc9999356bbb1c6158488453636b859e3217f52018ce88315 ubuntu-near:latest
   
   Then go to Dockerfile and change to 
   # Pull base image.
   FROM ubuntu-near:latest

   Each time you do a change please don't forget to commit otherwise the changes won't be persisted