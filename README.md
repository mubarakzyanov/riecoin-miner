## xptMiner Dockerfile
Dockerfile for xptMiner (riecoin)

This repository contains **Dockerfile** for [xptMiner](https://github.com/dave-andersen/fastrie.git)

### Base Docker Image

* [ubuntu/xenial](https://hub.docker.com/r/library/ubuntu/tags/xenial/)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Build an image from Dockerfile: `docker build . -t private/riecoin-miner`

### Usage

#### Run `xptminer`

    docker run \
        --detach \
        --name worker \
        --env POOL_USER=$USERNAME \
        --env POOL_PASSWORD=$PASSWORD \
        --env POOL_ADDRESS=$POOL_ADDRESS \
        --env THREAD_COUNT=$THREAD_COUNT \
        private/riecoin-miner
