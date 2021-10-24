# CRUD
## Django CRUD app    

This is a simple Django CRUD application that allows to create, retrieve, update and delete a post. The application is dockerized to learn the concept of docker workflow.

## Installation

First, [install Docker](https://docs.docker.com/installation/). If you're new to Docker, you might also want to check out the [Hello, world! tutorial](https://docs.docker.com/userguide/dockerizing/).

Next, clone this repo:

    $ git clone https://github.com/Dibae101/To-Do.cker-.git
    $ cd To-Do.cker-


Run `docker ps` to make sure your Docker host is running. If it's not, run:

    $ docker-machine start <dockerhostname>
    $ eval "$(docker-machine env <dockerhostname>)"

Build the Docker image (you should be in the `python-django/` directory, which contains the `Dockerfile`):

    $ docker build -t <yourname>/python-django .

Run the Docker image you just created (the command will be explained in the `Development workflow` section below):

    $ docker run --publish 8000:8000 python-django

Run `docker ps` to verify that the Docker container is running:

    CONTAINER ID        IMAGE                      COMMAND                  CREATED             STATUS              PORTS                          NAMES
    2830610e8c87        <yourname>/python-django   "/usr/bin/supervisord"   25 seconds ago      Up 25 seconds       0.0.0.0:80->80/tcp, 8000/tcp   focused_banach
