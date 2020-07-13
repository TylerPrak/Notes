# Docker

* Docker daemon 
  * API request Listen/manage objects + Communicate w/other daemon to manage Docker Services 
* Docker client 
  * Primary way for interact w/docker
  * ``Docker`` command uses docker API - e.g docker run commands sent to docker daemon
* Docker registry
* Docker objects
  * Images, containers, networks and volumes + services

Image

* Read only template based on another image for OS -- aka Dockerfile 
* Each line/command = layer 

## Dockerfile instructions 

* RUN
* FROM
* EXPOSE - opens a port
  * e.g EXPOSE 80
* ENTRYPOINT
* LABEL - adds metadata w/ key-pair values 
  * e.g LABEL maintainer=tyler
* CMD["<command"] 
  * e.g CMD["ls"]

## Concepts

DOCKER IMAGE > 

* ``docker create`` = creates a stopped container 
* ``docker start`` = start container
* ``docker run`` = create a running container
* ``docker stop`` = stop container 

### Container 

* Created form of an image that can be run - ``Docker`` [create| start| stop| move| delete] 

### Layers

* Affects speed 



``docker build -t``

* t used for name of image

``docker images``

* list images

---

If you don't want to use the cache as part of the build then set the option *--no-cache=true* as part of the `docker build` command.

---

Using *-e* option, you can set the name and value as *-e NODE_ENV=production*

environment var

---

## .dockerignore

https://docs.docker.com/engine/reference/builder/#dockerignore-file

---

## Escape 

``# escape =\`` sets escape character in dockerfile but \ is the default 

* problem with windows -- 1) path delimiter is backslash 2) newline char ``\n`` cannot be escaped
* solution = escape backtick

can also be used to escape newlines for which instructions span multiple lines 