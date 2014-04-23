# docker-node

Docker with Node v0.10.26 installed. 

**Note:** the Dockerfile uses `ONBUILD` and assumes you have a node.js project within an `app` sub-directory.

## Build

You can build the base container by typing the following into terminal:

    docker build -t urban/node .

## Example

To build an application using this container, type the following into terminal:

Build the container:

    docker build -t urban/node-app ./example

Run the container:

    docker run -d -p 80:80 urban/node-app

For development, you can run the container and mount the app directory as a shared volume with the following:

    docker run -d -p 80:80 -v `pwd`/example/app:/opt/app urban/node-app


