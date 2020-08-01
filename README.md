# docker-centos-systemd

A Dockerfile for building CentOS images that have systemd enabled.

## Branches

Each branch in this git repository is used for building specific versions.

| Branch | CentOS Version | FROM Docker image tag |
| ------ | -------------- | --------------------- |
| master | latest (8.2)   | latest                |
| 8.2    | 8.2            | 8.2.2004              |
| 7.8    | 7.8            | 7.8.2003              |

## Usage

```
# Run it
docker run -d \
  --tty \
  --privileged \
  --volume /sys/fs/cgroup:/sys/fs/cgroup:ro \
  --name maodevops-centos-systemd \
  maodevops/centos-systemd:latest

# Enter it
docker exec -it maodevops-centos-systemd /bin/bash

# Remove it
docker rm -f maodevops-centos-systemd
```
