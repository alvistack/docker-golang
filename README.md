# Docker Image Packaging for Go

[![Travis](https://img.shields.io/travis/com/alvistack/docker-golang.svg)](https://travis-ci.com/alvistack/docker-golang)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-golang.svg)](https://github.com/alvistack/docker-golang/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-golang.svg)](https://github.com/alvistack/docker-golang/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/golang.svg)](https://hub.docker.com/r/alvistack/golang/)

Go (a.k.a., Golang) is a programming language first developed at Google. It is a statically-typed language with syntax loosely derived from C, but with additional features such as garbage collection, type safety, some dynamic-typing capabilities, additional built-in types (e.g., variable-length arrays and key-value maps), and a large standard library.

Learn more about Go: <https://golang.org/>

## Supported Tags and Respective `Dockerfile` Links

  - [`1.15`, `latest`](https://github.com/alvistack/docker-golang/blob/master/molecule/1.15/Dockerfile.j2)
  - [`1.14`](https://github.com/alvistack/docker-golang/blob/master/molecule/1.14/Dockerfile.j2)

## Overview

This Docker container makes it easy to get an instance of Go up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Minimized `Dockerfile` for meta data definition
  - Provision by Ansible and Molecule Docker driver in single layer
  - Handle `ENTRYPOINT` with [catatonit](https://github.com/openSUSE/catatonit)

### Quick Start

For the `VOLUME` directory that is used to store the repository data (amongst other things) we recommend mounting a host directory as a [data volume](https://docs.docker.com/engine/tutorials/dockervolumes/#/data-volumes), or via a named volume if using a docker version \>= 1.9.

Start Go:

    # Pull latest image
    docker pull alvistack/golang
    
    # Run as detach
    docker run \
        -itd \
        --rm \
        --name golang \
        alvistack/golang \
        go version

## Versioning

### `alvistack/golang:latest`

The `latest` tag matches the most recent [GitHub Release](https://github.com/alvistack/docker-golang/releases) of this repository. Thus using `alvistack/golang:latest` or `alvistack/golang` will ensure you are running the most up to date stable version of this image.

### `alvistack/golang:<version>`

The version tags are rolling release rebuild by [Travis](https://travis-ci.com/alvistack/docker-golang) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
