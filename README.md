# simplewebrtc
Simple WebRTC video chat with local signaling server.

In this NodeJS app an express server is used for serving the HTML file and for forwarding messages between clients via websockets. For this socket.io is used with a self written signaling mechanism.

There is no need to use external ICE / TURN / STUN servers so you can install this on a local machine in your office or home (e.g. on a Raspberry PI), open the main URL and you can talk to each other in a video chat.

Optimized for Chrome on Windows and Android. Currently there is no support for other browsers or platforms.

## Installation and running

1. Download and install [NodeJS](https://nodejs.org)
2. Clone this repository somewhere on your disk
3. Run ```npm install``` in the main directory, where the file ```package.json``` resides
4. Run ```node app.js``` from the same directory
5. Open a browser to ```https://localhost``` (Do not forget the "s" in "https") or to the specific IP of your computer
6. Open another browser on a different device pointing to ```https://<IP-OF-COMPUTER-WITH-APP>```


Maybe you need to adapt the HTTPS port where the application runs on in ```app.js``` on line 6 and maybe you need to configure your computer's firewall to accept incoming connections at this port.