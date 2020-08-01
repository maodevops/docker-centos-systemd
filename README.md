# Docker CentOS Systemd

[![build status](https://img.shields.io/docker/cloud/build/maodevops/centos-systemd)](https://hub.docker.com/repository/docker/maodevops/centos-systemd)

CentOS image that has systemd enabled.

## Branches

Each branch in repository is used for building specific versions.

| Branch | CentOS Version | FROM Docker image tag |
| ------ | -------------- | --------------------- |
| master | latest (8.2)   | latest                |
| 8.2    | 8.2            | 8.2.2004              |
| 7.8    | 7.8            | 7.8.2003              |

## Usage

### Run it

```bash
docker run -d \
  --tty \
  --privileged \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  --name maodevops-centos8.2-systemd \
  maodevops/centos-systemd:8.2
```

### Enter it

```bash
docker exec -it maodevops-centos8.2-systemd /bin/bash
```

### Remove it

```bash
docker rm -f maodevops-centos8.2-systemd
```
