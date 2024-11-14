# Monitors

Monitors are a way to specify to configure the monitoring of a camera video stream. Monitors can be used to detect intrusions and motions in the defined area of the camera video stream. Monitors can be configured to send notifications when an intrusion or motion is detected.

## Create a monitor

To create a monitor, click on the **Monitors** menu item in the left sidebar. Then click on the **Create** button and fill in with the following information:

- **Monitor name**: The memorable name of the monitor.
- **Video source**: The type of video source to monitor. Currently, only RTSP, HTTP/S and Synology Surveillance Station are supported.
- **Connection timeout**: The timeout in seconds to wait for the video source to connect and to read video frames. If the video source does not respond within the timeout, the monitor will automatically reconnect.
- **Detection frame rate**: The frame rate in frames per second to use for motion detection. The higher the frame rate, the higher chance the motion can be detected. However, a higher frame rate also requires more CPU resources. The default frame rate is 5 frame per second.
- **Notifications**: The notifications to send when an intrusion or motion is detected. Multiple notifications can be selected.
- **Cooldown time**: The time in seconds to wait before sending another notification after a notification has been sent. This is to prevent sending too many notifications in a short period of time.
- **Minimum confidence**: The minimum confidence level to consider an object as an intrusion. The confidence level ranges from 0 (inclusive) to 1 (exclusive). The higher the confidence level, the more confident the monitor is that the object is an intrusion. The default confidence level is 0.7.
- **Minimum object size**: The minimum object size in pixels to consider an object as an intrusion. The higher the object size, the larger the object must be to be considered as an intrusion. The default object size is 5000 pixels relative to a 640x480 image.
- **Target objects**: The target objects to detect as an intrusion. Multiple target objects can be selected. If no target objects are selected.

Click on the **Configure video source** button to configure the video source.

### RTSP, HTTP/S video source

To configure an RTSP or HTTP/S video source, fill in the following information:

- **RTSP/HTTP/HTTPS URL**: The URL of the RTSP or HTTP/S video stream. For example, `rtsp://192.168.1.5:554/live/ch0`.
- **Username**: (Optional) The username to authenticate with the video source.
- **Password**: (Optional) The password to authenticate with the video source.

Click on the **Get camera streaming URL** button to get the formatted URL to use for the video source. Verify that the video stream is working by checking the video snapshot.

Click **OK** to save the video source configuration.

### Synology Surveillance Station video source

To configure a Synology Surveillance Station video source, fill in the following information:

- **Server address**: The IP address or hostname of the Synology Surveillance Station server.
- **Server port**: The port number of the Synology Surveillance Station server. The default port number is 5001 or 5000.
- **Use HTTPS**: Whether to use HTTPS to connect to the Synology Surveillance Station server.
- **DSM version**: The version of the Synology Surveillance Station server. The default version is 7.x.
- **Username**: The username to authenticate with the Synology Surveillance Station server.
- **Password**: The password to authenticate with the Synology Surveillance Station server.

Click on the **Get camera list** button to get the list of cameras available in the Synology Surveillance Station server. Select the camera to monitor. Verify that the video stream is working by checking the video snapshot.

Click **OK** to save the video source configuration.

### Defining the monitor area

After configuring the video source, a video snapshot will be displayed at the bottom of the page. Click on the snapshot image to define the monitor area. The monitor area is the area to monitor for intrusions and motions. The monitor area can be defined by drawing a polygon on the snapshot image. The polygon must have at least 3 points to be valid. The monitor area can be adjusted by dragging the points of the polygon.

An optimally configured monitor area should cover the ground area of the protected area. A smaller monitor area will reduce CPU processing time as well as the number of unintended detections.

Click **OK** to save the monitor configuration.

## Edit a monitor

To edit a monitor, click on the **Monitors** menu item in the left sidebar. Then click on the **Edit** button of the monitor to edit. Make the necessary changes and click **OK** to save the changes.

## Delete a monitor

To delete a monitor, click on the **Monitors** menu item in the left sidebar. Then click on the **Delete** button of the monitor to delete. Confirm the deletion by clicking **OK**.

## Start a monitor

To start a monitor, click on the **Monitors** menu item in the left sidebar. Then click on the **Start** button of the monitor to start. From this point on, the monitor will start detecting intrusions and motions. The monitor will also send notifications when an intrusion or motion is detected.

## Stop a monitor

To stop a monitor, click on the **Monitors** menu item in the left sidebar. Then click on the **Stop** button of the monitor to stop. From this point on, the monitor will stop detecting intrusions and motions. The monitor will not send notifications when an intrusion or motion is detected.
