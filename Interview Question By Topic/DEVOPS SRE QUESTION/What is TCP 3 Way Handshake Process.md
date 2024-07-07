FOR SENDING DATA TO CLIENT TO SERVER , TCP CONNECTION IS ESTABLISH

IT IS DUPLEX CONNECTION SO BIDIRECTIOAL PROTOCOL

### TCP 3-Way Handshake Process

1. **Definition**:
   - The TCP 3-way handshake is a process used to establish a connection between a client and a server in a TCP/IP network.

2. **Steps in the Handshake**:
   - **Step 1: SYN (Synchronize)**
     - The client sends a TCP segment with the SYN flag set to 1.
     - This indicates the client's intention to establish a connection and includes an initial sequence number (ISN).
   - **Step 2: SYN-ACK (Synchronize-Acknowledge)**
     - The server responds with a TCP segment with both the SYN and ACK flags set to 1.
     - The SYN flag is set to acknowledge the client's SYN segment, and the ACK flag acknowledges the receipt of the client's SYN.
     - The server also sends its own initial sequence number (ISN).
   - **Step 3: ACK (Acknowledge)**
     - The client sends a TCP segment with the ACK flag set to 1.
     - This segment acknowledges the server's SYN-ACK and includes the next sequence number expected by the server.
     - The connection is now established, and data transfer can begin.

3. **Key Points**:
   - **SYN (Synchronize)**: Initiates the connection and synchronizes sequence numbers.
   - **ACK (Acknowledge)**: Confirms the receipt of SYN or SYN-ACK segments.
   - **Sequence Numbers**: Used to keep track of data segments and ensure reliable delivery.
   - **Three Segments**: The process involves three segments (SYN, SYN-ACK, and ACK), hence the name "3-way handshake."

4. **Purpose**:
   - To synchronize sequence numbers between client and server.
   - To establish a reliable connection for data transfer.

5. **Importance in DevOps/SRE**:
   - Understanding the TCP 3-way handshake is crucial for diagnosing network connectivity issues.
   - It helps in troubleshooting and ensuring reliable communication between distributed systems.

6. **Diagram**:

```
Client                   Server
  |                        |
  | ----- SYN --------->   |
  |                        |
  | <---- SYN-ACK -----    |
  |                        |
  | ----- ACK --------->   |
  |                        |
Connection Established
```

### Additional Interview Tips
- Be prepared to explain how TCP handles retransmissions and error recovery.
- Understand how TCP connections are closed (4-way handshake or FIN-ACK process).
- Be familiar with tools like Wireshark to analyze TCP handshakes and troubleshoot network issues.