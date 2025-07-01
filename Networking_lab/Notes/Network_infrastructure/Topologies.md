# Network Topologies

## Physical Topologies

### 1. Bus Topology
- **Description**: All devices connected to a single backbone cable
- **Advantages**:
  - Simple to implement
  - Low cost (less cabling)
- **Disadvantages**:
  - Single point of failure (backbone)
  - Difficult to troubleshoot
  - Performance degrades with many devices
- **Collision Handling**: Uses CSMA/CD (Carrier Sense Multiple Access with Collision Detection)

### 2. Star Topology
- **Description**: All devices connect to a central device (switch/hub)
- **Advantages**:
  - Easy to add/remove devices
  - Fault isolation (one cable failure doesn't affect others)
  - Centralized management
- **Disadvantages**:
  - Single point of failure (central device)
  - Requires more cabling than bus
- **Modern Usage**: Most common in modern LANs

### 3. Ring Topology
- **Description**: Devices connected in a circular fashion
- **Types**:
  - Unidirectional (Token Ring)
  - Bidirectional (FDDI)
- **Advantages**:
  - Equal network access for all devices
  - No collisions
- **Disadvantages**:
  - Single break can disrupt entire network
  - Difficult to add/remove devices

### 4. Mesh Topology
- **Description**: Every device connected to every other device
- **Types**:
  - Full mesh (every device connected to all others)
  - Partial mesh (some redundant connections)
- **Advantages**:
  - High redundancy
  - Multiple paths for data
- **Disadvantages**:
  - Expensive (many cables/interfaces)
  - Complex to manage
- **Usage**: Critical network backbones

### 5. Tree Topology
- **Description**: Hierarchical combination of star topologies
- **Advantages**:
  - Scalable
  - Easy to isolate problems
- **Disadvantages**:
  - Dependent on root node
  - Complex cabling

### 6. Hybrid Topology
- **Description**: Combination of two or more topologies
- **Example**: Star-bus (multiple stars connected via bus)
- **Advantages**: Flexibility to meet specific needs
- **Disadvantages**: Complex design and implementation

## Logical Topologies

### 1. Ethernet (Logical Bus)
- **Characteristics**:
  - All devices see all traffic
  - Uses MAC addresses for delivery

### 2. Token Ring (Logical Ring)
- **Characteristics**:
  - Devices take turns sending data
  - Uses token passing mechanism

## Topology Selection Factors

1. **Cost**: Cabling and equipment expenses
2. **Scalability**: Ability to grow the network
3. **Reliability**: Fault tolerance requirements
4. **Performance**: Speed and latency needs
5. **Management**: Ease of troubleshooting
