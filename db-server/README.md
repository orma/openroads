### Dependencies 

- [Docker](https://docs.docker.com/installation/#Installation)

On Ubuntu, it is necessary to install the Docker maintained package, since the one maintained by Ubuntu is outdated.

### Installation
> From https://github.com/openstreetmap/osmosis/tree/master/db-server

This directory contains the scripts to create a docker-based database server to be used for unit testing. In order to use this server, docker must be installed on the local workstation.  Beyond that, no additional configuration should be required.

To build the docker image, run the following script.

``` sh
./build.sh
```

### Running the image
To run the docker image, run the following command.  To stop the server, press Ctrl-C.

```sh
docker run -ti --rm=true --name osmosis-build -p 5432:5432 bretth/osmosis-build
```

### Troubleshooting
If you wish to troubleshoot a running server, you may run the following command to get a bash prompt inside the docker container.

```sh
docker exec -ti osmosis-build /bin/bash
```