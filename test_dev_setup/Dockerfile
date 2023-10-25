FROM ubuntu:focal
ARG TAGS
WORKDIR /root
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y software-properties-common curl git build-essential && \
    apt-get update && \
    apt-get install -y software-properties-common curl git ansible build-essential && \
    apt-get clean autoclean && \
    apt-get autoremove --yes

RUN curl -s https://go.dev/dl/go1.21.3.src.tar.gz | tar -v -C /usr/local -xz
ENV PATH %PATH:/usr/local/go/bin
CMD ["go", "version"]
