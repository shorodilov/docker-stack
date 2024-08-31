# Docker Stacks for the Home Lab Environment

This repository contains various dockerfiles for use in the local environment.

## Networking

Since each *stack* isolates some specific containers, a proxy network is used
for communication between containers from various stacks.

This network is added to each stack as `external`, and should be created
within the `containerd` environment:

```shell
docker network create -d bridge docker_proxy01
```
