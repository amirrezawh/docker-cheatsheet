# docker-cheatsheet
#### Little cheatsheet for Docker!
---
## Display Docker client information
`docker info`

## Display all image information
For example, you wanna display `mysql:8` information:

`docker inspect mysql:8`

## Pull image

`docker pull <image-name>`

## Save image

`docker save <image-name> > foo.tar`

All image data will save in `foo.tar`.

## Load image

`docker load < foo.tar`

Image will load from `foo.tar`. 

## Export image

`docker export <container-name-or-id> > foo.tar`

Warning: You can only use export for running containers.

## Import image

`docker import <image-name> > foo.tar`

## Remove dangling images

`docker system prune -a`

Warning: DO NOT use this command in production environment.

## Access to shell container

For example we want to access alpine's shell:

`docker container run -it alpine /bin/sh`

## Save container id in any file

`docker ps --format "{{.ID}}" --filter name=<container-name> > <filename>`

## Run container with resource limitation

`docker run --memory="512m" --cpus="1.5" --memory-swap="256m" --cpuset-cpus="0,2" <image>`

## Set ENV in run command

`docker container run --env CLASS=dws --env NAME=amirreza -it alpine /bin/sh`

You can type `env` in alpine's shell to display your environments variables.

## Set volume in run command

`docker container run -v $(pwd):/data -it alpine /bin/sh`

This command will mount /data in your current directory(pwd).


[@dwsclass](https://github.com/dwsclass) dws-ops-005-docker
[@dwsclass](https://github.com/dwsclass) dws-ops-006-docker
