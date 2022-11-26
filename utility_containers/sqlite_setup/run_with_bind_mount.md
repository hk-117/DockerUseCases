
# Docker

## Building SQLite image

In the terminal, go to the directory where the Dockerfile resides.
To build the sqlite image from alpine base image, give following command on terminal:

`docker build -t sqliteimage:latest .`

## Running Container

To use sqlite with local file system, bind mount with container is necessary. Following command is appropriate for that:

`docker run -it --rm --name sqlitecontainer -v "/home/.../Workspace/SQLiteProject:/workspace" efaa31b3de15`

# Podman

## Building SQLite image

In the terminal, go to the directory where the Dockerfile resides.
To build the sqlite image from alpine base image, give following command on terminal:

`podman build -t sqliteimage:latest .`

## Running Container

To use sqlite with local file system, bind mount with container is necessary. Following command is appropriate for that:

`podman run -it --rm --name sqlitecontainer --security-opt label=disable -v "/home/.../Workspace/SQLiteProject:/workspace" efaa31b3de15`

<br>

****Note:** efaa31b3de15 is our created image id.*