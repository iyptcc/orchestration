# Docker Compose Readme

Here some brief instructions to get everything running:

## Install Docker and Docker-Compose

* https://docs.docker.com/engine/installation/linux/ubuntu/
* https://docs.docker.com/compose/gettingstarted/

## Clone everything

```
git clone https://gitlab.com/iypt/docker.git
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

## Contact

For any questions regarding contribution, vulnerability disclosure or installation, please contact [fe-iyptcc@nlogn.org](mailto:fe-iyptcc@nlogn.org).


