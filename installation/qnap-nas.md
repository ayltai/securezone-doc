---
icon: hard-drive
cover: >-
  https://images.unsplash.com/photo-1620361421000-64328420819f?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxfHxxbmFwfGVufDB8fHx8MTczMTY4MDU4NXww&ixlib=rb-4.0.3&q=85
coverY: -12
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

# 2.2 QNAP NAS

SecureZone can be installed on a QNAP NAS using the [Container Station](https://www.qnap.com/en/software/container-station) app. This guide will walk you through the steps to install SecureZone on your QNAP NAS.

This [website](https://www.qnap.com/en/software/container-station) lists the supported QNAP NAS models for the Container Station app.

## Prerequisites

* A QNAP NAS running QTS 4.3.4 or later.
* The Container Station app installed on your QNAP NAS. You can install this app from the App Center in QTS.

## Installation

First, open the Container Station app on your QNAP NAS.

Next, click on the **Containers** menu item in the left-hand sidebar. Click **Create** and then fill in the following details:

* **Image**: `ayltai/geekylifehacks:securezone-1.0.2`

Click **Next** and fill in the following details:

* **Name**: `SecureZone`
* **Auto start policy**: `Always`

Click **Advanced Settings** and fill in the following details:

* **Network**: Use the same network as Docker Host
* **Storage**: Click **Add Volume** to create a volume. Specify `/data` as the mount path. Specify `RW` as the access mode. Click **Apply** to create the volume.

Click **Next**, review the settings, and click **Finish** to create the container.

Once the container is created, click **Start** to start it.

SecureZone should now be running on your QNAP NAS. You can access it by navigating to `http://<your-qnap-nas-ip>:8002/web` in your web browser.

## Configuration

### Storage

SecureZone uses a Docker volume to store its data. This volume is created when you configure the volume in the Container Station. The following Docker volume mappings are required:

* `/data`: The directory where SecureZone stores its data.

### Ports

SecureZone exposes the UI on port 8002 on your QNAP NAS.
