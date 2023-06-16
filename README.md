# IdleRQ
Idle RQ protocol implementation using sockets library to send a .jpg from a primary host to secondary host.

Developed with MW and KF for Network Comms



Primary (client): 

- fragment buffer into packets of 1024 bytes

- send each packet as unreliable data gram

- includes timer to introduce timeout errors for testing purposes

Secondary (server):

- receive data packets and ack sequence number to receive the next packet

- reassemble data in data packets into a buffer

- save buffer to a file

