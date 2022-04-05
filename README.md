# Peer to Peer Chat Hackathon

The following readme contains information about my peer to peer chat application.

## Application

This will be a mobile application built via REACT Native. No chat data will be stored in a server. This application uses WebRTC for real time communication. 

## Discovery of clients

There needs to be a connection between 2 peers for them to chat with each other. Clients are discovered via a **signaling server**. The server uses a set of underlying protocols to discover the peers and negotiate/terminate a connection between them. Signaling exchanges configuration information and manages connections between peers.

## Session Initiation 

How it works is that a peer, lets call it peer1, that wishes to talk to peer 2 will offer a connection to the signal server. The recieving peer accepts the offer of the initiating peer from the signal server. After this, a connection is set up between the 2 peers and they can now chat with each other. See ```server.js``` for the code.

## Explanation of Code

```screens/Home.js``` - home screen of the app. An initiating peer will generate a room and share the room id/code with the peer he wishes to talk to. The receiving peer will enter the code in the field provided and they will get connected and the page will turn to ```screens/Chat.js``` where they can talk in real time.

<img width="261" alt="home_page" src="https://user-images.githubusercontent.com/42751267/161842341-f580896f-8913-47ea-bd05-c3d2e5b331cc.PNG">

```screens/Chat.js``` - chat screen of the app. Peers can communicate in real time.

<img width="267" alt="caht" src="https://user-images.githubusercontent.com/42751267/161842427-fc546755-8fb8-4aaf-9e4c-f35d5e69bf78.PNG">

## Communication 

2 peers can chat in real time.
Every time a message is typed. It should go to the backend through REST API code present in my github repository Patient-Monitoring-System-with-Django. It will be placed in the AWS database (See code present in github repository Patient-Monitoring-System-with-Django) through a POST command. 

## Testing

Ran code on an android emulator through expo CLI and Android Studio. See pictures pasted above. 

### References:

https://medium.com/nerd-for-tech/peer-to-peer-chat-app-using-webrtc-and-react-native-6c15759f92ec
https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API
https://www.tutorialspoint.com/unix_sockets/what_is_socket.htm
