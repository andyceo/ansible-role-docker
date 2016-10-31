# Ansible Role: docker

Install docker and provide usefull settings for it.

## Requirements

Ubuntu 14.04

## Tags

- **docker-orchestrate**: Orchestrate docker containers given by `docker.containers`.
- **docker-networks**: Create user-defined docker networks of type bridge, given by `docker.data.networks`.
- **docker-compose**: Install/update/actualize docker-compose utility with given version `docker.data.docker_compose_version`.
- **docker-repository**: Only add docker repository to `/etc/apt/sources.list.d/docker.list` (if no defaults were redefined, see options `docker.data.apt_keyserver`, `docker.data.apt_key_sig`, `docker.data.apt_repository`, `docker.data.apt_repository_filename`), install all needed python modules for ansible apt* modules.
