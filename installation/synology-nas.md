---
icon: hard-drive
cover: >-
  https://images.unsplash.com/photo-1577538926988-7926820ed209?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwzfHxzeW5vbG9neXxlbnwwfHx8fDE3MzE2ODA1NTZ8MA&ixlib=rb-4.0.3&q=85
coverY: 67
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 2.1 Synology NAS

SecureZone can be installed on a Synology NAS using the [Container Manager](https://www.synology.com/en-uk/dsm/feature/docker) package. This guide will walk you through the steps to install SecureZone on your Synology NAS.

This [website](https://www.synology.com/en-uk/dsm/packages/ContainerManager) lists the supported Synology NAS models for the Container Manager package.

## Prerequisites

* A Synology NAS running DSM 6.2 or later.
* The Container Manager package installed on your Synology NAS. You can install this package from the Package Center in DSM.

## Installation

First, open the Container Manager package on your Synology NAS.

Next, click on the **Container** menu item in the left-hand sidebar. Click 'Create' and then fill in the following details:

* **Image**: `ayltai/geekylifehacks:securezone-1.0.2`
* **Container Name**: `SecureZone`
* **Enable auto-restart**: Checked

Click **Next** to configure a volume. Click **Add Folder** and then select a folder on your Synology NAS to store the SecureZone data. It should be mapped to `/data` in the container. Give the volume read-write permissions.

Click **Next** to configure the network. Select **Use the same network as Docker Host**.

Click **Apply** to create the container. Once the container is created, click **Run** to start it.

SecureZone should now be running on your Synology NAS. You can access it by navigating to `http://<your-synology-nas-ip>:8002/web` in your web browser.

## Configuration

### Storage

SecureZone uses a Docker volume to store its data. This volume is created when you configure the volume in the Container Manager. The following Docker volume mappings are required:

* `/data`: The directory where SecureZone stores its data.

### Ports

SecureZone exposes the UI on port 8002 on your Synology NAS.
