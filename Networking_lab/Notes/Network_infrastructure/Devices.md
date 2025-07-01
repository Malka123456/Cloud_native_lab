# Network Devices

## Core Networking Devices

### 1. Modem
- **Function**: Modulates/Demodulates signals between digital and analog
- **Layer**: Physical layer
- **Types**:
  - DSL modems (for telephone lines)
  - Cable modems (for coaxial cables)
  - Fiber optic modems
- **Key Feature**: Connects home network to ISP

### 2. Router
- **Function**: Routes packets between different networks
- **Layer**: Network layer (Layer 3)
- **Key Features**:
  - Uses IP addresses for routing decisions
  - Contains routing tables
  - Often includes NAT (Network Address Translation)
  - May include firewall capabilities
- **Enterprise vs Home**: 
  - Home routers often combine multiple functions
  - Enterprise routers are more powerful and specialized

### 3. Switch
- **Function**: Connects devices within a local network
- **Layer**: Data Link layer (Layer 2)
- **Types**:
  - Unmanaged switches (plug-and-play)
  - Managed switches (configurable, VLAN support)
  - PoE switches (Power over Ethernet)
- **Key Features**:
  - Uses MAC addresses for forwarding
  - Reduces network collisions compared to hubs
  - Can provide network segmentation

### 4. Hub
- **Function**: Basic network connector (largely obsolete)
- **Layer**: Physical layer
- **Key Characteristics**:
  - Broadcasts data to all ports
  - No traffic filtering
  - Single collision domain
  - Considered a "dumb" device

### 5. Wireless Access Point (WAP)
- **Function**: Provides wireless connectivity
- **Layer**: Data Link layer
- **Key Features**:
  - Converts wired signals to wireless
  - Supports various WiFi standards (802.11ac, ax)
  - Often integrated into routers

## Specialized Devices

### 6. Firewall
- **Function**: Network security device
- **Layer**: Network/Transport layers
- **Types**:
  - Stateless (filters based on static rules)
  - Stateful (tracks active connections)
  - Next-Generation (NGFW with deep packet inspection)
- **Key Features**:
  - Packet filtering
  - VPN support
  - Intrusion prevention

### 7. Load Balancer
- **Function**: Distributes network traffic
- **Layer**: Transport/Application layers
- **Types**:
  - Hardware-based
  - Software-based
- **Algorithms**:
  - Round-robin
  - Least connections
  - IP hash

### 8. Network Interface Card (NIC)
- **Function**: Connects device to network
- **Layer**: Physical/Data Link
- **Types**:
  - Ethernet
  - WiFi
  - Fiber optic
- **Key Feature**: Each has unique MAC address

## Comparison Table

| Device      | OSI Layer | Addressing Used | Intelligence Level |
|-------------|-----------|-----------------|--------------------|
| Hub         | Physical  | None            | None               |
| Switch      | Data Link | MAC             | Medium             |
| Router      | Network   | IP              | High               |
| Firewall    | Network+  | IP/Port         | High               |
