## xptMiner Dockerfile
Dockerfile for xptMiner (riecoin)

This repository contains **Dockerfile** for [xptMiner](https://github.com/dave-andersen/fastrie.git)

### Base Docker Image

* [ubuntu/xenial](https://hub.docker.com/r/library/ubuntu/tags/xenial/)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://hub.docker.com/r/rusa959/xpt-miner/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull rusa959/xpt-miner`

   (alternatively, you can build an image from Dockerfile: `docker build -t="rusa959/xpt-miner" github.com/mubarakzyanov/xpt-miner`)

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
