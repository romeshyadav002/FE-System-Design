`Communication Protocol`

Guidelines under which two system communicates

* `HTTP`
 1. TCP connection :- confirmation that we want to connect with you
 2. HTTP Request
 3. HTTP Response

 - use cases :- web browsing

* `HTTP/3 (QUIC)`
 1. UDP Connection

 - Header compression happens
 - Faster
 - Improved Performance
 - Better Network Congestion

 - use cases :- IoT, Virtual Reality

* `HTTPS (HyperText Transfer Protocol Secure)`
 1. TCP connection
 2. public key
 3. session key
 4. encrypted data

 - Handshake Process: When a client connects to a server using HTTPS, they initiate an SSL/TLS handshake. During this handshake:

 - The server provides its SSL certificate.
 - The client verifies the authenticity of the certificate (making sure it’s valid and issued by a trusted CA).
 - They agree on encryption protocols and exchange encryption keys.
 - Encryption of Data: After the handshake, data is exchanged between the client and server using encryption, making the connection secure.

 - Secure Data Transfer: From this point, all the data exchanged is encrypted and cannot be easily intercepted or tampered with.

 - use cases :- web browsing

* `WebSocket`
 1. HTTP Upgrade Full Duplex

 - use cases :- Live Chat, Real-Time Data Transmission

* `TCP`
 1. SYN (Synchronize): The client sends a SYN message to the server, requesting a connection.
 2. SYN-ACK (Synchronize-Acknowledge): The server responds with a SYN-ACK, acknowledging the client's request.
 3. ACK (Acknowledge): The client sends an ACK message back to the server, confirming the connection is established.

 How TCP Works:
 - Segmentation: TCP breaks large amounts of data into smaller chunks called segments. Each segment is numbered for proper sequencing.

 - Transmission: Segments are transmitted across the network. TCP handles the retransmission of any lost or corrupted segments.

 - Acknowledgment: The receiver sends an acknowledgment (ACK) for each segment received. If the sender doesn’t receive an acknowledgment for a particular segment, it assumes it was lost and retransmits it.

 - Reordering: At the destination, the received segments are reordered (if necessary) based on their sequence numbers and reassembled into the original message.

 - use cases :- web browsing, Email Protocols

 TCP: Best for applications that require reliable, ordered, and error-free data delivery (e.g., web browsing, file downloads, emails).

* `UDP (User Datagram Protoco)`
 - Request
 - Response

Key Features of UDP:
 - Connectionless: UDP does not establish a connection before sending data, meaning it can send packets to the destination without any handshake. This makes it faster than TCP.

 - Unreliable: There’s no guarantee that data will arrive at its destination, and if it does, there’s no guarantee that it will be in the correct order. There’s no mechanism for resending lost packets or reordering them.

 - No Congestion Control: UDP does not have flow or congestion control, so it does not adjust its transmission rate based on network traffic conditions.

 - Low Latency: Because UDP skips connection setup and error-checking mechanisms, it has lower latency, making it suitable for real-time applications where speed is crucial.

 - Message-Oriented: UDP is message-oriented, meaning it sends data in discrete messages (datagrams), maintaining message boundaries.

 - Lightweight Header: The UDP header is only 8 bytes, much smaller compared to TCP's header (20 bytes), further reducing overhead.
  
 UDP: Best for real-time applications where speed is essential and occasional data loss can be tolerated (e.g., live video streaming, gaming).

 - use cases :- video conferencing

* `SMTP`
 1. sender --> SMTP Server --> receiver

 - use cases :- sending/receiving Emails

* `FTP` 
 1. Control Panel
 2. data Channel

 - use cases :- upload/download files