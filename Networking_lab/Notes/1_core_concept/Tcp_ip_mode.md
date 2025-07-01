# TCP/IP Model

## Overview
TCP/IP (Transmission Control Protocol/Internet Protocol) is the **foundation of the internet**. It is a **practical and robust** model with 4 layers that map closely to the OSI model.

## Layers of TCP/IP Model

### 1. Application Layer
- Combines OSI layers 5, 6, and 7.
- Provides services to the user.
- Protocols: HTTP, FTP, SMTP, DNS, SSH

### 2. Transport Layer
- Manages end-to-end communication.
- Protocols: TCP (reliable), UDP (fast but no guarantee)
- Handles port numbers and segments.

### 3. Internet Layer
- Handles logical addressing and routing.
- Protocols: IP (IPv4/IPv6), ICMP
- Devices: Routers

### 4. Network Access Layer (Link Layer)
- Combines Data Link + Physical layers of OSI.
- Responsible for MAC addressing, framing, and bit transmission.

> 🔄 Data flow in TCP/IP is also based on **encapsulation and decapsulation**.

## Key TCP/IP Protocols

### TCP (Transmission Control Protocol)
- Reliable, connection-oriented.
- Ensures packets arrive in order and without loss.
- Example: Web browsing, file transfers.

### UDP (User Datagram Protocol)
- Unreliable, connectionless.
- Fast and lightweight; suitable for real-time applications.
- Example: Streaming, VoIP.

### IP (Internet Protocol)
- Routes data from source to destination.
- **IPv4**: 32-bit (4.3B addresses), **IPv6**: 128-bit (massive scale)

## TCP Connection: Three-Way Handshake
1. **SYN**: Client requests connection
2. **SYN-ACK**: Server acknowledges
3. **ACK**: Client confirms → connection established

## OSI vs TCP/IP

| OSI Model | TCP/IP Model |
|-----------|--------------|
| 7 layers  | 4 layers     |
| Theoretical | Practical |
| Separates Presentation, Session | Combines into Application |
| Rarely implemented as-is | Internet standard |

---
