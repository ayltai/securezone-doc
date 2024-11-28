# Hardware acceleration

Hardware acceleration is a feature that enables the use of GPU resources to speed up the processing of certain tasks, such as object detection and video encoding. SecureZone supports hardware acceleration for improved performance and efficiency.

Hardware acceleration is automatically enabled if your host computer meets the necessary hardware and software prerequisites. Note that SecureZone will run just fine without hardware acceleration, but enabling it can significantly improve performance.

## Software prerequisites

Before enabling hardware acceleration, make sure you have the following prerequisites:

* An Intel, AMD, or NVIDIA GPU
* The latest GPU drivers installed on your host computer
* Any of the following software installed on your host computer:
    * FFmpeg with hardware acceleration support enabled
    * GStreamer with VA-API plugin installed
    * (Windows) Microsoft Media Foundation (MSMF)
* Any of the following API/SDKs installed on your host computer:
    * (Linux) [VA-API](https://www.intel.com/content/www/us/en/developer/articles/technical/linuxmedia-vaapi.html)
    * (Windows) [DXVA2](https://learn.microsoft.com/en-us/windows/win32/medfound/directx-video-acceleration-2-0)
    * [NVIDIA Video Codec SDK](https://developer.nvidia.com/video-codec-sdk)
    * [AMD Advanced Media Framework (AMF)](https://gpuopen.com/advanced-media-framework/)

## Hardware prerequisites

Ensure that your host computer meets the following hardware prerequisites:

* Any of the following GPUs:
    * Intel GPU with Intel [Quick Sync Video (QSV)](https://en.wikipedia.org/wiki/Intel_Quick_Sync_Video) support
    * AMD GPU with AMD [Video Core Next](https://en.wikipedia.org/wiki/Video_Core_Next) support
    * NVIDIA GPU with [CUDA](https://en.wikipedia.org/wiki/CUDA), [NVDEC](https://en.wikipedia.org/wiki/Nvidia_NVDEC) and [NVENC](https://en.wikipedia.org/wiki/Nvidia_NVENC) support
