
# Docker

## Building PHP image

In the terminal, go to the directory where the Dockerfile resides.
To build the PHP image from alpine base image, give following command on terminal:

`docker build -t php:latest .`

## Running Container

To use PHP with local file system, bind mount with container is necessary. Following command is appropriate for that:

`docker run -it --rm --name phpcontainer -v "$PWD:/workspace" efaa31b3de15`

# Podman

## Building PHP image

In the terminal, go to the directory where the Dockerfile resides.
To build the PHP image from alpine base image, give following command on terminal:

`podman build -t php:latest .`

## Running Container

To use PHP with local file system, bind mount with container is necessary. Following command is appropriate for that:

`podman run -it --rm --name phpcontainer --security-opt label=disable -v "$PWD:/workspace" efaa31b3de15`

<br>

****Note:** efaa31b3de15 is our created image id.*
