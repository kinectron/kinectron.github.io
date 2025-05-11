# About Kinectron Version 0 

<b>NOTE! This version of Kinectron (Version 0) is no longer supported!!! See Version 1 Documentation on <a href="https://github.com/kinectron/kinectron">GitHub</a></b>

Kinectron is an open source tool that brings realtime, motion capture data into the browser. 

It works with [Kinect Azure](https://azure.microsoft.com/en-us/services/kinect-dk/) and [Kinect Windows V2](https://developer.microsoft.com/en-us/windows/kinect/).

<style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style><div class='embed-container'><iframe src='https://www.youtube.com/embed//BV6xK3EOznI' frameborder='0' allowfullscreen></iframe></div>

## Overview: Node, Kinect + Electron

Kinectron has two components—an electron application to broadcast Kinect data over a peer connection, and a client-side API to request and receive that data over a peer connection. Kinectron is open source and connects to creative coding frameworks like P5.js and three.js. It is node based, and it builds on the [Node-Kinect2](https://github.com/wouterverweirder/kinect2), [Node Kinect-Azure](https://github.com/wouterverweirder/kinect-azure), and [PeerJS](http://peerjs.com/) libraries.

The application runs on a computer connected to a Kinect, a low cost motion sensing camera created by Microsoft. Once started it wirelessly broadcasts Kinect data over a network. It can send volumetric data, skeletal data, and color and infrared images. It can send one or more feed at a time.

## Credits

Kinectron is maintained by [Lisa Jamhoury](http://lisajamhoury.com) with support from [Aarón Montoya-Moraga](https://github.com/montoyamoraga). It was originally developed by [Shawn van Every](https://github.com/vanevery) and [Lisa Jamhoury](https://github.com/lisajamhoury/) at New York University's Interactive Telecommunications Program (NYU ITP) under the xStory Experiments in Storytelling Google Research Grant, which supports experiments with emerging technology in service of new forms of storytelling.

Past collaborators include [Stephanie Koltun](https://github.com/stephkoltun), [Or Fleisher](https://github.com/juniorxsound), [Tiri Kananuruk](http://xxx.tiri.xxx/), and [Dror Ayalon](https://www.drorayalon.com/).
