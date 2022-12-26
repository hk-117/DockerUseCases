
# Docker

## Building VHDL image

In the terminal, go to the directory where the Dockerfile resides.
To build the vhdl image from ubuntu base image, give following command on terminal:

`docker build -t vhdl:latest .`

## Running Container

To use vhdl with local file system, bind mount with container is necessary. Following command is appropriate for that:

`docker run -it --rm --name vhdlcontainer -v "/home/.../Workspace/VhdlProject:/workspace" efaa31b3de15`

# Podman

## Building VHDL image

In the terminal, go to the directory where the Dockerfile resides.
To build the vhdl image from ubuntu base image, give following command on terminal:

`podman build -t vhdl:latest .`

## Running Container

To use vhdl with local file system, bind mount with container is necessary. Following command is appropriate for that:

`podman run -it --rm --name vhdlcontainer --security-opt label=disable -v "/home/.../Workspace/VhdlProject:/workspace" efaa31b3de15`

<br>

****Note:** efaa31b3de15 is our created image id.*
