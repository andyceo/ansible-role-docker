# Ansible Role: docker

Install docker and provide usefull settings for it.

## Requirements

Ubuntu 16.04

## Tags

- **docker-orchestrate**: Only orchestrate docker containers given by `docker.containers`.
- **docker-networks**: Only create user-defined docker networks of type bridge, given by `docker.networks`.
- **docker-compose**: Only install/update/actualize docker-compose utility with given version `docker.compose.version`.
- **docker-repository**: Only add actual docker repository key and repository itself to `/etc/apt/sources.list.d/docker.list` (if no defaults were redefined, see options `docker.repositories`), install all needed python modules for ansible apt* modules. Also remove outdated repositories and keys.
- **docker-repository-key**: Only add actual docker repository key and remove outdated keys.
- **docker-config**: Create crossplatform docker configuration file (default Linux location is `/etc/docker/daemon.json`)
