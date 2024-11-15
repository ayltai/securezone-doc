---
icon: microchip
cover: >-
  https://images.unsplash.com/photo-1694444070793-13db645409f4?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwxMHx8Y29tcHV0ZXIlMjBoYXJkd2FyZXxlbnwwfHx8fDE3MzE2Nzg3NTJ8MA&ixlib=rb-4.0.3&q=85
coverY: -20
---

# Requirements

## Hardware

### Cameras

Cameras that support RTSP or HTTP/S streaming are compatible with SecureZone. We recommend cameras that support RTSP streaming for better performance. It helps improve the overall system performance and minimise network load to have cameras that support H.264 or H.265 video encoding. It also helps if your camera supports multiple substreams with a resolution of 1080p or lower.

Additionally, cameras that are added to Synology Surveillance Station are compatible with SecureZone. SecureZone can access the video streams from Synology Surveillance Station using Synology DSM API. This allows you to use cameras that are not directly supported by SecureZone.

Cameras with built-in motion detection are not required. SecureZone has its own object detection mechanism that is more accurate, reliable and efficient than the motion detection feature of most cameras.

It is recommended to use cameras that support night vision for better performance in low light conditions. Cameras with built-in infrared LEDs are ideal for this purpose. SecureZone can work with cameras that have no night vision capabilities, but the performance may be affected in low light conditions.

High-end cameras with advanced features like PTZ (Pan-Tilt-Zoom) are supported by SecureZone. However, these features are not required. SecureZone is designed to work with low-end cameras that support RTSP or HTTP streaming with a resolution of 640x360 or higher.

The cameras should be accessible from the SecureZone server. If the cameras are behind a firewall, you will need to configure port forwarding on the firewall to allow SecureZone to access the cameras.

Wireless cameras are supported by SecureZone. In case of connection loss, SecureZone will automatically reconnect to the camera when the connection is restored.

### Server

SecureZone is designed to run as effeciently as possible on a low-end server. The server should have at least 512MB of RAM and a dual-core processor. It helps to have a solid-state drive (SSD) for better performance. The server should have a stable Internet connection with a minimum upload speed of 1Mbps. The server should be running a 64-bit version of Linux, Windows or macOS. SecureZone is not supported on 32-bit systems. The server should be given access to the cameras and the Internet.

#### CPU architecture

SecureZone is designed to run on x86-64 and ARM64 processors. It has been tested to run smoothly on servers with Intel, AMD and ARM processors.

#### Minimum CPU and RAM requirements

SecureZone is designed to run on a multi-core processor. The more cores the processor has, the better the performance of SecureZone. It has been tested to run smoothly for monitoring one camera video stream using a Synology DS220j NAS with a dual-core Realtek RTD1296 processor and 512MB of RAM. For monitoring multiple camera video streams, a server with a quad-core processor and at least 1GB of RAM is recommended.

#### Recommended CPU and RAM requirements

For better performance and scalability, we recommend a server with a decent multi-core processor and at least 4GB or RAM. SecureZone has been tested to run smoothly for monitoring 6 camera video streams using a £120 mini PC with an Intel N100 CPU and 12GB of RAM. Any pre-owned or refurbished server that costs around £60 to £100 with a quad-core processor and 4GB of RAM should be sufficient for monitoring 2 to 4 camera video streams.

#### GPU

A dedicated GPU is not required for SecureZone.

#### Network

SecureZone requires a stable Internet connection with a minimum upload speed of 1Mbps. The server should be connected to the Internet via a wireless or a wired connection.

In order to access the UI, the server should have TCP port 8002 open.

#### Storage

SecureZone requires at least 7GB of free disk space for installation. The storage requirements for snapshots and video recordings depend on the number of cameras, the resolution of the video streams, the frame rate, the compression rate, and the duration of the recordings. SecureZone has been tested to run smoothly with a 128GB SSD for monitoring 6 camera video streams with a resolution of 640x360 at 15fps.

## Software

### Operating System

SecureZone is supported on the following operating systems:

* Linux, x86-64 and ARM64
* Windows 10 and 11, x86-64 and ARM64
* macOS, 64-bit Intel CPU
* macOS, 64-bit Apple Silicon CPU

SecureZone is not supported on 32-bit systems.
