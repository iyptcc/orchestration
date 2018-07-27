# Docker Compose Readme

Here some brief instructions to get everything running:

## Install Docker and Docker-Compose

* https://docs.docker.com/engine/installation/linux/ubuntu/
* https://docs.docker.com/compose/gettingstarted/

## Clone everything

```
git clone ssh://git@git.nlogn.org:2223/CC/docker.git
git submodule update --init --recursive
```

## Create and run Images

```
docker-compose build
docker-compose up -d
```

## Database

A docker volume with the name `_pgvolume` is used for persistant storage.
It can be inspected with

```
docker volume ls
```


