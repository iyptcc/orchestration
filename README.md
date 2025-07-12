# Docker Compose Readme

Here some brief instructions to get everything running:

## Install Docker and Docker-Compose

* https://docs.docker.com/engine/installation/linux/ubuntu/
* https://docs.docker.com/compose/gettingstarted/

Most of the features also work with podman, except rendering of PDFs, as they require a connection to the docker api to launch pods.

## Clone everything

```
git clone https://gitlab.com/iypt/docker.git
git submodule update --init --recursive
```

## Create and run Images

```
docker compose build
docker compose up -d
```

If you want to render PDFs, make sure to uncomment the docker api mount from the celery container.


## Database

A docker volume with the name `_pgvolume14` is used for persistant storage.
It can be inspected with

```
docker volume ls
```

## Admin User

To create the initial admin user, you need to get a shell in the web container:

```
docker compose exec web bash
```

Then inside the container run:

```
cd /data/django/scripts
python3 users.py 
```

It will prompt you for an email and password. The email can be arbitrary.

Log in at http://localhost:8000 with username `root` and the password provided.


## Contact

For any questions regarding contribution, vulnerability disclosure or installation, please contact [fe-iyptcc@nlogn.org](mailto:fe-iyptcc@nlogn.org).


