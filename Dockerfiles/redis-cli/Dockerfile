FROM ubuntu:20.04
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get upgrade -y && apt-get install -y build-essential \
    pkg-config \
    libssl-dev \
    tcl \
    libjemalloc-dev \
    wget
RUN wget http://download.redis.io/redis-stable.tar.gz && \
    tar xvzf redis-stable.tar.gz && \
    cd redis-stable && \
    make distclean && \
    make BUILD_TLS=yes && \
    cp /redis-stable/src/redis-cli /usr/local/bin/ && \
    chmod +x /usr/local/bin/redis-cli

