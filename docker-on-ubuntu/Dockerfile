FROM ubuntu:latest

RUN apt-get update
RUN apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common -y

RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -
RUN add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

RUN apt-get update

RUN apt-get install docker-ce -y