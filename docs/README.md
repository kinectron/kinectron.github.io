# About Kinectron

Kinectron is an open source tool that brings realtime, motion capture data into the browser. It works with Kinect Azure and Kinect Windows V2

<iframe width="560" height="315" src="https://www.youtube.com/embed/BV6xK3EOznI" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Overview: Node, Kinect + Electron

Kinectron has two components—an electron application to broadcast Kinect data over a peer connection, and a client-side API to request and receive that data over a peer connection. Kinectron is open source and connects to creative coding frameworks like P5.js and three.js. It is node based, and it builds on the [Node-Kinect2](https://github.com/wouterverweirder/kinect2), [Node Kinect-Azure](https://github.com/wouterverweirder/kinect-azure), and [PeerJS](http://peerjs.com/) libraries.

The application runs on a computer connected to a Kinect, a low cost motion sensing camera created by Microsoft. Once started it wirelessly broadcasts Kinect data over a network. It can send volumetric data, skeletal data, and color and infrared images. It can send one or more feed at a time.

## Credits

Kinectron is maintained by [Lisa Jamhoury](http://lisajamhoury.com) with support from [Aarón Montoya-Moraga](https://github.com/montoyamoraga). It was originally developed by [Shawn van Every](https://github.com/vanevery) and [Lisa Jamhoury](https://github.com/lisajamhoury/) at New York University's Interactive Telecommunications Program (NYU ITP) under the xStory Experiments in Storytelling Google Research Grant, which supports experiments with emerging technology in service of new forms of storytelling.

Past collaborators include [Stephanie Koltun](https://github.com/stephkoltun), [Or Fleisher](https://github.com/juniorxsound), [Tiri Kananuruk](http://xxx.tiri.xxx/), and [Dror Ayalon](https://www.drorayalon.com/).
