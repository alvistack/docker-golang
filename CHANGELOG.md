# Docker Image Packaging for Go

## 1.14.4-XalvistackY - TBC

### Major Changes

## 1.14.4-4alvistack2 - 2020-06-10

### Major Changes

  - Revamp `create`, `side_effect`, `verify` and `destroy` logic
  - Replace `tini` with `catatonit`
  - Rename `post_tasks.yml` as `side_effect.yml`
  - Upgrade base image to Ubuntu 20.04

## 1.14.0-4alvistack1 - 2020-03-06

  - Ubuntu 18.04 based
  - Minimized `Dockerfile` for meta data definition
  - Provision by Ansible and Molecule Docker driver in single layer
  - Handle `ENTRYPOINT` with [tini](https://github.com/krallin/tini)
