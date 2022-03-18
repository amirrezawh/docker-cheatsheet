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