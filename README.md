# Docker Image Packaging for Go

<a href="https://alvistack.com" title="AlviStack" target="_blank"><img src="/alvistack.svg" height="75" alt="AlviStack"></a>

[![GitLab pipeline status](https://img.shields.io/gitlab/pipeline/alvistack/docker-golang/master)](https://gitlab.com/alvistack/docker-golang/-/pipelines)
[![GitHub tag](https://img.shields.io/github/tag/alvistack/docker-golang.svg)](https://github.com/alvistack/docker-golang/tags)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-golang.svg)](https://github.com/alvistack/docker-golang/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/golang-1.19.svg)](https://hub.docker.com/r/alvistack/golang-1.19)

Go (a.k.a., Golang) is a programming language first developed at Google. It is a statically-typed language with syntax loosely derived from C, but with additional features such as garbage collection, type safety, some dynamic-typing capabilities, additional built-in types (e.g., variable-length arrays and key-value maps), and a large standard library.

Learn more about Go: <https://golang.org/>

## Supported Tags and Respective Packer Template Links

  - [`alvistack/golang-1.19`](https://hub.docker.com/r/alvistack/golang-1.19)
      - [`packer/docker-1.19/packer.json`](https://github.com/alvistack/docker-golang/blob/master/packer/docker-1.19/packer.json)
  - [`alvistack/golang-1.18`](https://hub.docker.com/r/alvistack/golang-1.18)
      - [`packer/docker-1.18/packer.json`](https://github.com/alvistack/docker-golang/blob/master/packer/docker-1.18/packer.json)
  - [`alvistack/golang-1.17`](https://hub.docker.com/r/alvistack/golang-1.17)
      - [`packer/docker-1.17/packer.json`](https://github.com/alvistack/docker-golang/blob/master/packer/docker-1.17/packer.json)

## Overview

This Docker container makes it easy to get an instance of Go up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Packaging by Packer Docker builder and Ansible provisioner in single layer
  - Handle `ENTRYPOINT` with [catatonit](https://github.com/openSUSE/catatonit)

### Quick Start

For the `VOLUME` directory that is used to store the repository data (amongst other things) we recommend mounting a host directory as a [data volume](https://docs.docker.com/engine/tutorials/dockervolumes/#/data-volumes), or via a named volume if using a docker version \>= 1.9.

Start Go:

    # Pull latest image
    docker pull alvistack/golang-1.19
    
    # Run as detach
    docker run \
        -itd \
        --rm \
        --name golang \
        alvistack/golang-1.19 \
        go version

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub Release](https://github.com/alvistack/docker-golang/tags) of this repository. Thus using these tags will ensure you are running the most up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab pipeline](https://gitlab.com/alvistack/docker-golang/-/pipelines) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
