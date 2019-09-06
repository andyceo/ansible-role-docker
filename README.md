# Ansible Role: docker

Install docker and provide usefull settings for it.

## Requirements

Supported operating systems: see https://github.com/andyceo/ansible-role-docker/blob/master/meta/main.yml#L10

## Features

- pin to specific version

    You can pin your Docker engine to specific version (creating special file `/etc/apt/preferences.d/docker-ce`) when this configuration parameter contain version as string, for example latest known stable version is `18.03.1~ce-0~ubuntu`. By default this feature is disabled, as this Ansible role trying to install Docker engine close to it's official guide

- ...to be continued

## Tags

- **docker-containers** (or **docker-orchestrate**): Only orchestrate docker containers given by `docker.containers`.
- **docker-networks**: Only create user-defined docker networks of type bridge, given by `docker.networks`.
- **docker-compose**: Only install/update/actualize docker-compose utility with given version `docker.compose.version`.
- **docker-repository**: Only add actual docker repository key and repository itself to `/etc/apt/sources.list.d/docker.list` (if no defaults were redefined, see options `docker.repositories`), install all needed python modules for ansible apt* modules. Also remove outdated repositories and keys.
- **docker-repository-key**: Only add actual docker repository key and remove outdated keys.
- **docker-package**, **docker-packages** (alias): Allow only pin docker package version and upgrade it.
- **docker-config**: Create crossplatform docker configuration file (default Linux location is `/etc/docker/daemon.json`)
- **docker-users**: Add given users to `docker` group to make them use docker without `sudo`.
- **docker-swarm**: Execute all Docker Swarm tasks on given `docker.swarm.manager` host. Docker Swarm should be active on the target host.
- **docker-secrets**: Manage secrets. Docker Swarm should be active on the target host.
- **docker-secrets-show**: Show secrets in clear text. USE WITH CAUTION! This task executed only when this tag specified explicitly.
