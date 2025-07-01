
# Networking Lab Implementation Guide

## Basic Home Lab Setup

### 1. Physical Components
- **Router**: pfSense/OPNsense or consumer router
- **Switch**: Managed (for VLANs) or unmanaged
- **Cables**: Cat6 UTP cables
- **Devices**: 2-3 PCs, IoT devices

### 2. Logical Configuration
```network-diagram
[ISP] → [Router] → [Switch] → [Devices]
            ↓
        [WiFi AP]
```

### 3. Key Configurations
1. **Subnetting**:
   - 192.168.1.0/24 for main network
   - 192.168.2.0/24 for guest WiFi
2. **DHCP**:
   - Address pools for each subnet
   - Static IPs for servers
3. **Firewall Rules**:
   - Block incoming WAN requests
   - Allow inter-VLAN communication as needed

## Advanced Enterprise Lab

### 1. Virtual Lab (Using GNS3/EVE-NG)
- **Components**:
  - Cisco IOS routers (or VyOS)
  - Layer 3 switches
  - Firewalls (pfSense)
  - WAN emulator

### 2. Core Configurations
```cisco
! Sample Router Config
interface GigabitEthernet0/0
 ip address 10.1.1.1 255.255.255.0
!
router ospf 1
 network 10.1.1.0 0.0.0.255 area 0
```

### 3. Practical Exercises
1. **VLAN Implementation**:
   - Create VLANs for departments
   - Configure trunk ports
   - Set up inter-VLAN routing

2. **Routing Protocols**:
   - OSPF area configuration
   - BGP peering simulation
   - Route redistribution

3. **Security**:
   - ACL implementation
   - Port security
   - VPN setup (IPSec/OpenVPN)

## Packet Tracer Labs

### 1. Basic Connectivity
- Ping between devices
- Trace route analysis
- ARP table examination

### 2. Protocol Analysis
```wireshark-filter
# Common Wireshark Filters
tcp.port == 80          # HTTP traffic
icmp                    # Ping packets
dns                     # DNS queries
```

### 3. Troubleshooting Scenarios
1. **Connectivity Issues**:
   - Check physical layer (link lights)
   - Verify IP configuration
   - Test with ping/traceroute

2. **Performance Problems**:
   - Bandwidth monitoring
   - QoS configuration
   - Packet loss analysis

## Cloud Networking Lab (AWS/Azure)

### 1. Virtual Network Components
- VPC/VNet creation
- Subnet design (public/private)
- Security groups/NSGs

### 2. Hybrid Connection
- Site-to-site VPN
- Direct Connect/ExpressRoute
- BGP configuration

### 3. Monitoring Tools
- Flow logs analysis
- Network performance metrics
- Packet capture in cloud
```
