# Kinect Azure Server Options 

### Choosing A Feed

Kinectron for Azure only supports broadcasting one feed (frame) at a time. Multiframe and record functionality will be added in the future.

#### Single Frame

Kinectron starts by default in single frame mode.

To start a frame, click the corresponding button. The frame will start automatically. If you click a different button, Kinectron will automatically stop the current frame and begin the new frame.

These are the single frames that are currently available:

- "Color" returns a webp from the color camera.
- "Depth" returns a webp of the depth mapped to a grayscale (0-255) image.
- "Raw Depth" returns an array of values ranging from 0 - 3860. The values correspond to depth in millimeters. It displays a lossless webp image in the application for testing and feedback.
- "Skeleton (Tracked Bodies)" returns all tracked bodies one at a time. It does not differentiate between tracked bodies. For troubleshooting, Kinectron by default will draw the tracked bodies on the application interface, however, only the body data is sent over the peer connection as a JSON object.
- "All Bodies" returns an array of all bodies tracked. For troubleshooting, Kinectron by default will draw the tracked bodies on the application interface, however, only the data is sent over the peer connection as a JSON object.
- "Key" returns a png of the image of the tracked bodies on a transparent background. It has the effect of a green screen.
- "Depth Key" returns an array of raw depth values corresponding to the tracked bodies. The values range from 0 - 3860. The values correspond to depth in millimeters. It displays a lossless webp image in the application for testing and feedback.
- "RGBD" returns a webp with the color image registered to the depth feed and the 8-bit depth feed stored in the alpha channel.
- "Stop All" stops the current frame.

### Recording

The Kinectron application can record Kinect data to your desktop.

#### Recording Single Frames

To record a single frame, click the button corresponding to the frame that you want to record. Once the broadcast has started, click "Start Record" to begin recording. Click the button a second time "Stop Record" to end recording. The file will be saved automatically to your home folder in "Kinectron Recordings."

#### Recording Multiple Frames

Multiple frames are not yet supported for the Kinect Azure!

To record multiple frames, start the frames you wish to record, then click "Start Record" to begin recording. Click the button a second time "Stop Record" to end recording. The files will be saved automatically to your home folder in "Kinectron Recordings."

#### Recorded File Types

The recorded frames result in the following file types. These vary slighty if recording with the API. See API documentation.

- Color: webm
- Depth: webm
- Raw Depth: webm
- Skeleton: webm (joints drawn to canvas) and JSON (joint data)\*
- All Bodies: webm (joints drawn to canvas) and JSON (joint data)\*

\*JSON files with joint data include a timestamp.

### Advanced Options

#### Peer Server

Kinectron uses a peer server to establish a connection between the server and the browser. The peer server can be accessed in four ways:

1. Connect on localhost. By default the application creates a peer connection using peer.js on localhost at port 9001 with "kinectron" as username. This is used to connect on the same computer.

2. Connect on local network. Kinectron displays the local IP address at the top of the application. This can be used in the client-side API to connect over your local wifi network. See "Creating an Instance of Kinectron" in the API documentation.

3. Connect on a public network. The public address exposes your Kinectron server on the public internet over https. You will use either your private or public address to connect your Kinectron client to your server. To create a public address, just click the Create Public Address button in the server application. This can be used in the client-side API to connect to your Kinectron server over the public internet using https. See "Creating an Instance of Kinectron."

> A word of warning: The public address is created using [ngrok](https://ngrok.com/), which creates a secure tunnel using https to your localhost at port 9001. This is safe in theory, but could be used for malicious purposes if there are any security flaws in the Kinectron application. The one developer actively maintaining this tool has never had a problem herself, but can't gaurantee your safety. You are welcome to contribute to help keep Kinectron secure :).

4. Connect on personal peer network. Use your own peer server by entering and submitting your ID and server details as follows:

> Name: myname <br>
> Server Details: {"host": "myserver.com", "port": "9000", "path": "/", "secure": "true"} <br><br> **Important!** In order to parse correctly, server details must be enclosed within curly brackets and properties must be in double quotes.

#### Image Size

The Kinectron Azure application displays and broadcasts images at the following sizes. It is not currently possible to change the Kinectron output dimensions for the Azure Kinect. (This functionality coming soon!)

The native dimensions of the Kinect Azure feeds are:

> Color: 3840 x 2160 <br>
> Depth: 640 x 576

Kinectron outputs them at the following dimensions by default:

> Color: 1280 x 720 <br>
> Depth: 640 x 576 <br>
> Raw Depth: 320 x 280 <br>
> RGBD: 512 x 512

#### Allow/Block API Calls

By default the Kinectron application listens for calls from the client-side API.

Block API calls by clicking the "Block API Calls" button under Advanced Options. Blocking API calls will allow you to continue to broadcast to clients, but clients will not be able to make changes to the application settings through the API.

To allow API calls, click "Allow API Calls." This immediately allows API calls again.

> Blocking API calls is especially helpful in a teaching context. This allows a teacher to broadcast Kinect data to several students experimenting with the API at the same time without allowing them from making changes to the application.
