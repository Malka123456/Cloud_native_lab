# OSI (Open Systems Interconnection) Model

## Overview
The OSI model is a **conceptual framework** that standardizes how different network systems communicate across diverse platforms. It has **7 layers**, each responsible for specific tasks in the data communication process.

> 🧠 Mnemonic: **All People Seem To Need Data Processing**

## The 7 Layers Explained

### 1. Application Layer (Layer 7)
- Interface for end-users and software.
- Protocols: HTTP, SMTP, FTP, DNS
- Devices: Computers, smartphones

### 2. Presentation Layer (Layer 6)
- Data translation, encryption, and compression.
- Converts between data formats like JPEG, MP4, ASCII.

### 3. Session Layer (Layer 5)
- Manages sessions between devices.
- Handles authentication and reconnections.

### 4. Transport Layer (Layer 4)
- Reliable delivery of data segments.
- Protocols: TCP (reliable), UDP (unreliable)
- Ensures flow control and error recovery.

### 5. Network Layer (Layer 3)
- Logical addressing and routing of packets.
- Protocols: IP, ICMP
- Devices: Routers

### 6. Data Link Layer (Layer 2)
- Physical addressing (MAC), framing, and error detection.
- Protocols: Ethernet, ARP
- Devices: Switches, bridges

### 7. Physical Layer (Layer 1)
- Deals with the **raw bit transmission** over physical mediums.
- Includes: Voltages, cable types, connectors.
- Devices: Cables, hubs, NICs

## Data Encapsulation Process
When data is sent:
- Each layer **adds its own header** (encapsulation).
- Sent as bits from the Physical Layer.
- Receiver decapsulates and reads data layer by layer.

> 📌 Example: Sending an email goes through all 7 layers from sender to receiver.

---
