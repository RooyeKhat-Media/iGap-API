# WebSocket Connection
Open a WebSocket connection to the following address

    wss://secure.igap.net/hybrid/

# Format
The packet of message has the following format:

| 2 bytes | N bytes |
|---------|---------|

The first two bytes are unsigned short integer (little endian byte order) which are called **actionId** and other bytes are entitled as **payload**

Extract actionId and unpack payload according to [lookup table](proto/README.md)

# Uploading file over WebSocket
When you want to send a packet more that 50KB , you must customize WebSocket client to turn off masking otherwise, the server will close your connection