# Real-World Networking Examples

## 1. Web Browsing (HTTP/HTTPS)
### Process Flow:
1. DNS Resolution (URL → IP)
2. TCP 3-way Handshake
3. TLS Handshake (HTTPS)
4. HTTP GET Request
5. Server Response with Webpage
6. TCP Connection Termination

### Key Protocols:
- DNS (UDP port 53)
- HTTP (TCP 80) / HTTPS (TCP 443)
- TCP (Reliable delivery)
- IP (Routing)

## 2. Email Communication
### SMTP Email Send:
1. Client → SMTP Server (TCP 25)
2. Server verifies recipient
3. Server forwards to recipient's mail server
4. Recipient retrieves via POP3/IMAP

### Protocols Involved:
- SMTP (Sending)
- POP3 (Receive, port 110)
- IMAP (Receive with sync, port 143)
- DNS (MX record lookup)

## 3. Video Conferencing
### Implementation:
1. UDP for real-time video/audio
2. TCP for control signals
3. STUN/TURN for NAT traversal
4. QoS prioritization for smooth experience

### Why UDP?
- Tolerates packet loss
- Lower latency
- No retransmission delays

## 4. Cloud File Storage
### Technical Process:
1. Chunking (Divide files into blocks)
2. Parallel TCP connections
3. Checksum verification
4. Distributed storage across servers

### Protocols Used:
- HTTP/REST API
- TLS for encryption
- TCP for reliable transfer

## 5. IoT Device Communication
### Typical Implementation:
1. MQTT (Message Queuing Telemetry Transport)
2. CoAP (Constrained Application Protocol)
3. Lightweight TCP/IP stack
4. Often uses 6LoWPAN for IPv6 over low-power networks

## Enterprise vs Home Networking
| Aspect          | Enterprise                     | Home                          |
|-----------------|--------------------------------|-------------------------------|
| Topology        | Hierarchical (Core/Distribution/Access) | Simple star          |
| Devices         | Enterprise-grade switches/routers | Consumer combo devices   |
| Security        | Firewalls, IDS/IPS, VLANs      | Basic NAT firewall           |
| Redundancy      | Dual WAN, backup links         | Single connection            |
| Management      | SNMP, NetFlow, centralized     | Basic web interface          |
