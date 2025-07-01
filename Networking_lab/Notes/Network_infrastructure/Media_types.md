# Network Media Types

## Guided Media (Wired)

### 1. Twisted Pair Cable
- **Types**:
  - UTP (Unshielded Twisted Pair)
    - Categories: Cat5e (1Gbps), Cat6 (10Gbps), Cat6a, Cat7
    - Maximum length: 100m (328ft)
    - Common uses: Ethernet networks, telephone
  - STP (Shielded Twisted Pair)
    - Additional shielding against EMI
    - Used in industrial environments
- **Connectors**: RJ45 (8P8C)
- **Advantages**:
  - Inexpensive
  - Easy to install
- **Disadvantages**:
  - Susceptible to interference (especially UTP)
  - Limited bandwidth compared to fiber

### 2. Coaxial Cable
- **Types**:
  - RG-6: For cable TV, satellite
  - RG-58: Thin Ethernet (10BASE2)
  - RG-8: Thick Ethernet (10BASE5)
- **Connectors**: BNC, F-type
- **Characteristics**:
  - Better shielding than twisted pair
  - Higher bandwidth
- **Usage**:
  - Cable internet
  - CCTV systems
  - Legacy Ethernet (largely obsolete)

### 3. Fiber Optic Cable
- **Types**:
  - Single-mode:
    - Small core (8-10μm)
    - Long distance (up to 100km)
    - Uses laser light source
  - Multi-mode:
    - Larger core (50-62.5μm)
    - Shorter distance (up to 2km)
    - Uses LED light source
- **Connectors**:
  - LC, SC, ST, MTP/MPO
- **Advantages**:
  - Extremely high bandwidth
  - Immune to EMI
  - Secure (difficult to tap)
  - Long distance without repeaters
- **Disadvantages**:
  - Expensive
  - Difficult to install/splice
- **Applications**:
  - Internet backbones
  - Data center interconnects
  - FTTx (Fiber to the Home/Premises)

## Unguided Media (Wireless)

### 1. Radio Frequency
- **Types**:
  - WiFi (802.11 standards)
    - 2.4GHz (longer range, more interference)
    - 5GHz (faster, less interference)
    - 6GHz (WiFi 6E)
  - Cellular (4G LTE, 5G)
  - Bluetooth (short-range)
- **Characteristics**:
  - No physical connection needed
  - Subject to interference
  - Security concerns

### 2. Microwave
- **Types**:
  - Terrestrial (tower-to-tower)
  - Satellite (ground-to-space)
- **Applications**:
  - Long-distance communications
  - Remote area connectivity

### 3. Infrared
- **Characteristics**:
  - Line-of-sight required
  - Short range
  - Secure (doesn't penetrate walls)
- **Usage**: Remote controls, some short-range data transfer

## Media Comparison Table

| Media Type       | Speed          | Distance       | Cost     | EMI Resistance |
|------------------|----------------|----------------|----------|----------------|
| UTP Cat6         | Up to 10Gbps   | 100m           | Low      | Low            |
| STP Cat6a        | Up to 10Gbps   | 100m           | Medium   | Medium         |
| Coaxial RG-6     | Up to 1Gbps    | 500m           | Low      | High           |
| Single-mode Fiber| 100Gbps+       | 100km          | High     | Complete       |
| Multi-mode Fiber | Up to 100Gbps  | 2km            | Medium   | Complete       |
| WiFi 6 (5GHz)    | Up to 9.6Gbps  | 50m (indoor)   | Low      | Medium         |
| 5G mmWave        | Up to 2Gbps    | 500m           | Medium   | High           |

## Selection Criteria

1. **Bandwidth Requirements**: Higher speeds need fiber or high-grade copper
2. **Distance**: Fiber for long runs, copper for short
3. **Environment**: Industrial areas may need STP or fiber
4. **Cost**: Budget constraints may dictate UTP over fiber
5. **Future Growth**: Scalability considerations
6. **Security**: Fiber is more secure than wireless
