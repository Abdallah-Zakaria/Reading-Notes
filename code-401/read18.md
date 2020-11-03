# Sockets.io
#### What is the benefit of transforming data into packets?
An efficient way of transfering data over networks within response.

#### UDP is often refereed to as a connectionless protocol. Why is this?
This is because with UPD no connection needs to be established between the origin and destination before tranferring data.

#### Can a socket server application have multiple socket connections?
Yes

## Can a socket connection application be connected to multiple socket servers?
Each socket is connect to a separated port.

#### Can an application be both a socket server and a socket connection?
Yes, we can but its not a good practice. 


- **OSI Model**	OSI stands for Open System Interconnection. It is a conceptual framework for understanding the networking process. The seven layers of OSI are Physical, Data Link, Network, Transport, Session, Presentation, and Application.
- **TCP Model**	This is a more concise version of the OSI Model, and it consists of four layers: Application, Transport, Internet, and Network.
- **TCP**	This stands for Transmission Control Protocol. In this, the server must be listening for connections from clients.
- **UDP**	This stands for User Datagram Protocol. Unlike TCP, there is no need to establish a connection before transfering data.
- **Packets**	A unit of data that goes from one place to another over a network.
- **Socket**	A socket is an endpoint for sending and receiving data. Sometimes this refers to an internet socket, where a socket is identified to other hosts by its socket address.


## Web Sockets
WebSocket is distinct from HTTP. Both protocols are located at layer 7 in the OSI model and depend on TCP at layer 4. Although they are different, RFC 6455 states that WebSocket “is designed to work over HTTP ports 443 and 80 as well as to support HTTP proxies and intermediaries,” thus making it compatible with the HTTP protocol. To achieve compatibility, the WebSocket handshake uses the HTTP Upgrade header[1] to change from the HTTP protocol to the WebSocket protocol.

## Socket.IO
Socket.IO enables real-time bidirectional event-based communication. It works on every platform, browser or device, focusing equally on reliability and speed. Socket.IO is built on top of the WebSockets API (Client side) and Node.js. It is one of the most depended upon library on npm (Node Package Manager).