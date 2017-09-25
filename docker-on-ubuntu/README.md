# Docker on Ubuntu

Docker image based on ubuntu:latest that has docker client, docker-machine and docker compose installed. An example use case for this image is as a part of jenkins pipeline to execute docker builds.

# Running the image

```
docker run -it \
    -v /var/run/docker.sock:/var/run/docker.sock \
    vhlavacek/docker-on-ubuntu /bin/bash
```
# Building image

```
docker build . -t vhlavacek/docker-on-ubuntu
```

# Pushing image

```
docker login

docker push vhlavacek/docker-on-ubuntu
```