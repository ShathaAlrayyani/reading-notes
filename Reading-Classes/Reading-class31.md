## Docker

- Docker is a way to run Linux containers
- Containers are a lightweight alternative to Virtual Machines
- Dockerfile is a list of instructions for creating an image
- Images are made up of one or more layers
- Containers are a running instance of an image
- docker-compose.yml controls how to run the container
- Containers are stateless and ephemeral in nature.


## How to Install Docker

To install Docker we need to download the desktop app on our computer and create a free account. The initial download of
Docker might take some time to download. It’s a big file. Feel free to stretch your legs at this point!

Once Docker is done installing we can confirm the correct version is running. It should be at least version 19.

    $ docker --version
    Docker version 19.03.5, build 633a0ea

Docker Compose is an additional tool that is automatically included with Mac and Windows downloads of Docker. However if
you are on Linux, you will need to add it manually. You can do this by running the command sudo pip install
docker-compose after your Docker installation is complete.

Now run the command below to confirm you have a working version of it, too. The version should be at least 1.24.x.

    $ docker-compose --version
    docker-compose version 1.24.1, build 4667896b
