The Multi-Client Chat Application is a real-time messaging system developed using socket programming and multithreading. It allows multiple clients to connect to a central server and exchange messages with each other concurrently. The server handles each client in a separate thread, ensuring smooth and uninterrupted communication regardless of the number of active clients.


How It Works


Server Side:

A socket server is initialized and listens for incoming client connections.

Upon each new connection, the server spawns a new thread to handle that specific client.

The thread constantly listens for messages from that client and broadcasts them to all other connected clients.

Client Side:

The client connects to the server using a socket.

Two threads are used on the client side:

One thread for sending messages to the server.

Another thread for receiving messages from the server.

This dual-thread model ensures that the client can both send and receive messages at the same time without blocking.
