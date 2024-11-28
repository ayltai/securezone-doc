---
icon: arrows-rotate
cover: >-
  https://images.unsplash.com/photo-1602763288580-927cfda37a72?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxMHx8Y29tcHV0ZXIlMjB1cGdyYWRlfGVufDB8fHx8MTczMTkzMjc1Mnww&ixlib=rb-4.0.3&q=85
coverY: 0
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

# 2.4 Updating

SecureZone is updated regularly with new features, improvements and bug fixes so it is important to keep your SecureZone installation up to date. This guide will show you how to update SecureZone to the latest version.

## Updating on Synology Container Manager

If you are using the Synology Container Manager installation method, you can update SecureZone by pulling the latest image from Docker Hub and restarting the container. To do this, follow these steps:

1. Open Synology Container Manager.
2. Click on the **Image** menu item in the left sidebar.
3. Click on the **Update available** button next to the SecureZone image.
4. Click on the **Update** button to pull the latest image from Docker Hub.
5. Click on the **Container** menu item in the left sidebar.
6. Click on the **SecureZone** container.
7. Click on the **Action** button and select **Restart** to stop the container.

The latest version of SecureZone will now be deployed on your server. You can now access SecureZone at the same URL as before.

## Updating on QNAP Container Station

If you are using the QNAP Container Station installation method, you can update SecureZone by pulling the latest image from Docker Hub and restarting the container. To do this, follow these steps:

1. Open QNAP Container Station.
2. Click on the **Images** menu item in the left sidebar.
3. Click on the **SecureZone** image.
4. Select **Pull** from the **Action** menu to pull the latest image from Docker Hub.
5. Click on the **Containers** menu item in the left sidebar.
6. Click on the **SecureZone** container.
7. Click on the **Action** button and select **Recreate** to stop the container.

The latest version of SecureZone will now be deployed on your server. You can now access SecureZone at the same URL as before.

## Updating on Docker

If you are using the Docker installation method, you can update SecureZone by pulling the latest image from Docker Hub and restarting the container. To do this, run the following commands:

```bash
docker pull ayltai/geekylifehacks:securezone-x.x.x
dcker stop SecureZone
docker rm SecureZone
docker run --name SecureZone -d -p 8002:8002 -v securezone-data:/data --restart=always ayltai/geekylifehacks:securezone-x.x.x
```

The version number `x.x.x` will now be deployed on your server, using the persistent data from the previous version. You can now access SecureZone at the same URL as before.
