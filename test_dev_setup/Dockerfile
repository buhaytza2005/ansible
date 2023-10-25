FROM ubuntu:focal
ARG TAGS
WORKDIR /root
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get install -y software-properties-common curl git ansible build-essential && \
    apt-get clean autoclean && \
    apt-get autoremove --yes
RUN curl -L -s https://go.dev/dl/go1.21.3.linux-amd64.tar.gz | tar -v -C /usr/local/ -xz
RUN apt-get install -y vim 
RUN echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc 
RUN apt-get install -y ca-certificates curl gnupg
RUN mkdir -p /etc/apt/keyrings
RUN curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg

