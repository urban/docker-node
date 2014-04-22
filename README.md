# docker-node

Docker with Node v0.10.26 installed. 

**Note:** the Dockerfile uses `ONBUILD` and assumes you have a node.js project within an `app` sub-directory.

## Build base container

At the project root, build the base container by typing the following into terminal:

    sudo docker.io build -t urban/node .

To build an application container, type the following into terminal:

    cd example
    sudo docker.io build -t urban/node-app .
    sudo docker.io run -d -p 80:80 urban/node-app


