# Format
The packet of message has the following format:

| 2 bytes | N bytes |
|---------|---------|

The first two bytes are unsigned short integer (little endian byte order) which are called **actionId** and other bytes are entitled as **payload**

Extract actionId and unpack payload according to [lookup table](proto/README.md)