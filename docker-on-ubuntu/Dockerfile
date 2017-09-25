FROM ubuntu:latest

RUN apt-get update && \
    apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common -y && \
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add - && \
    add-apt-repository \
        "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
        $(lsb_release -cs) \
        stable" && \
    apt-get update && \
    apt-get install docker-ce -y && \
    curl -L https://github.com/docker/machine/releases/download/v0.12.2/docker-machine-`uname -s`-`uname -m` >/tmp/docker-machine && \
        chmod +x /tmp/docker-machine && \
        cp /tmp/docker-machine /usr/local/bin/docker-machine && \
    curl -L \
        https://github.com/docker/compose/releases/download/1.16.1/docker-compose-`uname \
        -s`-`uname -m` -o /usr/local/bin/docker-compose && \
        chmod +x /usr/local/bin/docker-compose

RUN rm -rf /var/lib/apt/lists/* && apt-get clean
