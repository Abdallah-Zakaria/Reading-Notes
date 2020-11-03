# Message Queues

#### What does it mean that web sockets are bidirectional? Why is this useful?
Available for the user and client to communicate with others
#### Does socket.io use HTTP? Why?
No, socket.io uses the WebSocket protocol instead of HTTP,
#### What happens when a client emits an event?
The only server will listen for that event.
#### What happens when a server emits an event?
All connect sockets will listen for it.
#### What happens if a client “misses” an event?
Conflict in the app
#### How can we mitigate this?

- **Web Socket**	The communication protocol that allows a client and a server to connect over a TCP protocol. The Web Socket remains open to allow real time data transfer.
- **Socket.io**	Socket.io broadcasts mulitple sockets at a time, and it works on all platforms.
- **Client**	The client is the one asking for information or data, and the server is providing it.
- **Server**	A server provides functionality, data, and information to clients. A single server can serve mulitple clients.

## Socket.io Emit Cheatsheet
```
io.on('connect', onConnect);

function onConnect(socket){

  // sending to the client
  socket.emit('hello', 'can you hear me?', 1, 2, 'abc');

  // sending to all clients except sender
  socket.broadcast.emit('broadcast', 'hello friends!');

  // sending to all clients in 'game' room except sender
  socket.to('game').emit('nice game', "let's play a game");

  // sending to all clients in 'game1' and/or in 'game2' room, except sender
  socket.to('game1').to('game2').emit('nice game', "let's play a game (too)");

  // sending to all clients in 'game' room, including sender
  io.in('game').emit('big-announcement', 'the game will start soon');

  // sending to all clients in namespace 'myNamespace', including sender
  io.of('myNamespace').emit('bigger-announcement', 'the tournament will start soon');

  // sending to a specific room in a specific namespace, including sender
  io.of('myNamespace').to('room').emit('event', 'message');

  // sending to individual socketid (private message)
  io.to(socketId).emit('hey', 'I just met you');

  // WARNING: `socket.to(socket.id).emit()` will NOT work, as it will send to everyone in the room
  // named `socket.id` but the sender. Please use the classic `socket.emit()` instead.

  // sending with acknowledgement
  socket.emit('question', 'do you think so?', function (answer) {});

  // sending without compression
  socket.compress(false).emit('uncompressed', "that's rough");

  // sending a message that might be dropped if the client is not ready to receive messages
  socket.volatile.emit('maybe', 'do you really need it?');

  // specifying whether the data to send has binary data
  socket.binary(false).emit('what', 'I have no binaries!');

  // sending to all clients on this node (when using multiple nodes)
  io.local.emit('hi', 'my lovely babies');

  // sending to all connected clients
  io.emit('an event sent to all connected clients');

};
```