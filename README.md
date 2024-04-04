# Dockerfiles for Roc Toolkit

[![build](https://github.com/jevinskie/rock-streaming-dockerfiles/actions/workflows/build.yml/badge.svg?branch=jevinskie/main)](https://github.com/jevinskie/rock-streaming-dockerfiles/actions/workflows/build.yml)

This repo provides dockerfiles for CI builds and end-user images for cross-compilation.

Docker images are built using Github Actions and then pushed to Docker Hub. The corresponding Docker Hub organization is [jevinskie](https://hub.docker.com/u/jevinskie).

Documentation for this process is [available here](https://jevinskie.github.io/roc-streaming-site/toolkit/docs/development/continuous_integration.html).

To build image(s) locally, run:

```
./make.sh [OPTIONS...] IMAGE[:TAG]...
```

For example (build all tags of `env-ubuntu`):

```
./make.sh env-ubuntu
```

Or (build all tags of `env-fedora` and two specific tags of `env-ubuntu`):

```
./make.sh env-fedora env-ubuntu:20.04 env-ubuntu:22.04
```

To build all images, run:

```
./make.sh [OPTIONS...]
```

Use `-n` flag to see what's going to happen without actually doing anything, for example:

```
./make.sh -n
```

For the full list of available options, run:

```
./make.sh --help
```
