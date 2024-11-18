---
icon: docker
cover: >-
  https://images.unsplash.com/photo-1646627927863-19874c27316b?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHw1fHxkb2NrZXJ8ZW58MHx8fHwxNzMxNjc5Mjk5fDA&ixlib=rb-4.0.3&q=85
coverY: 52
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Docker

SecureZone runs as a Docker container on a Docker engine. This guide will walk you through the steps to install SecureZone using Docker.

## Prerequisites

* The latest version of Docker installed and working. We recommend following the [official Docker installation guide](https://docs.docker.com/engine/install/) for your platform.

## Instalation

First, pull the SecureZone Docker image from the Docker Hub:

```bash
docker pull ayltai/geekylifehacks:securezone-1.0.0
```

Next, create the volume that SecureZone will use to store its data:

```bash
docker volume create securezone-data
```

Finally, run the SecureZone container:

```bash
docker run --name SecureZone -d -p 8002:8002 -v securezone-data:/data --restart=always ayltai/geekylifehacks:securezone-1.0.0
```

SecureZone should now be running on your Docker engine. You can access it by navigating to `http://localhost:8002/web` in your web browser.

## Configuration

### Storage

SecureZone uses a Docker volume to store its data. This volume is created when you run the `docker volume create` command. The following Docker volume mappings are required:

* `/data`: The directory where SecureZone stores its data.

### Ports

By default, SecureZone exposes the UI on port 8002. You can change this by modifying the `-p` flag in the `docker run` command.
