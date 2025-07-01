# Data Encapsulation Process

## The Five Steps of Data Encapsulation

### 1. Application Layer: User Data
- **Process**: 
  - User creates data (email, file transfer, web request)
  - Application protocol (HTTP, FTP, SMTP) formats the data
- **PDU (Protocol Data Unit)**: Message
- **Example**: 
  - HTTP GET request for a webpage
  - Email body and headers

### 2. Transport Layer: Segment/Datagram
- **Process**:
  - Adds transport layer header
  - TCP: Sequence numbers, ports, flags (SYN, ACK)
  - UDP: Simpler header with just ports
- **PDU**: Segment (TCP) or Datagram (UDP)
- **Key Fields Added**:
  - Source/destination port numbers
  - Sequence numbers (TCP)
  - Checksum
  - Window size (TCP flow control)

### 3. Network Layer: Packet
- **Process**:
  - Adds IP header with logical addressing
  - Determines best path (routing)
- **PDU**: Packet
- **Key Fields Added**:
  - Source/destination IP addresses
  - Protocol identifier (TCP=6, UDP=17)
  - TTL (Time To Live)
  - Header checksum

### 4. Data Link Layer: Frame
- **Process**:
  - Adds frame header and trailer
  - MAC addressing for local delivery
  - Error detection (CRC in trailer)
- **PDU**: Frame
- **Key Fields Added**:
  - Source/destination MAC addresses
  - Frame type (IPv4, ARP, etc.)
  - CRC (Cyclic Redundancy Check)

### 5. Physical Layer: Bits
- **Process**:
  - Converts frame to bits
  - Transmits as electrical/optical signals
- **PDU**: Bits
- **Characteristics**:
  - Encoding scheme (Manchester, 4B/5B)
  - Physical medium specifications

## Decapsulation Process (Reverse)
1. Physical layer converts signals to bits
2. Data link layer checks MAC, removes header/trailer
3. Network layer checks IP, removes header
4. Transport layer reassembles segments
5. Application layer presents data to user

## Protocol Data Units (PDUs) at Each Layer

| OSI Layer       | PDU Name      | Added Information                          |
|-----------------|---------------|--------------------------------------------|
| Application     | Message       | Application-specific headers               |
| Presentation    | Message       | Encryption/compression headers             |
| Session         | Message       | Session control information                |
| Transport       | Segment/Datagram | Port numbers, sequence numbers           |
| Network         | Packet        | IP addresses, TTL                          |
| Data Link       | Frame         | MAC addresses, error checking              |
| Physical        | Bits          | Signal encoding                            |

## Real-world Example: Sending an Email
1. User composes email (Application)
2. SMTP adds headers (Presentation/Session)
3. TCP breaks into segments (Transport)
4. IP adds addressing (Network)
5. Ethernet frames it (Data Link)
6. NIC converts to electrical signals (Physical)
