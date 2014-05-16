Docker Linux Containers
=======================

Lightweight linux containers that share the kernal of the underlying linux
machine.
Works with all popular linux distros
MacOS (With caveats, Must run with boottodocker)
Solaris? Windows?

Images are containers waiting to run. Containers are running images.
Restarts happen almost immediately because containers are basically just
snapshots of the images.

The preferred way of making containers is through a Dockerfile. Using the
Dockerfile you can use `docker build .` and it will build the dockerfile.

  FROM debian:jessie
  MAINTAINER Brad Urani bradurani@gmail.com
  RUN apt-get install update

You can build docker containers off of each other.

**Consider writing a service that allows you to create a heroku using docker**
Heroku push automatically updates the running containers

Checkout
--------
docker diff

Docker Projects:
  - Orchard - Super computing
  - git:CenturyLinkLabs/building - Heroku with docker
  - Fig - Fast dev environments with Docker
  - Fleet - Manages containers in a running system
  - Shipyard

"Modifying a running server is the new Anti-pattern"
----------------------------------------------------
Never login to the server to change a configuration on the production server.
Always use the docker container and push up the changes to production to let
docker handle the deployment process.

vim: ft=markdown tw=80 sts=2 colorcolumn=80
