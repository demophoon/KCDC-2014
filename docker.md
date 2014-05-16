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

vim: ft=markdown tw=80 sts=2 colorcolumn=80
