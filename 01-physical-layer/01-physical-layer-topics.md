# Networking Mastery — Physical Layer (01)

The Physical Layer is where networking becomes **real** — electricity, light, radio waves, and hardware.

This module focuses on how bits are physically transmitted, what can go wrong, and how it impacts everything above.



##  Goals

- Understand how data is physically transmitted
- Learn limitations of real-world media (cables, fiber, wireless)
- Identify hardware-level bottlenecks and failures
- Build intuition for latency, noise, and signal degradation


##  Topics Overview



###  Electrical & Signal Fundamentals

- What is a signal
- Analog vs digital signals
- Voltage levels and signaling
- Signal propagation
- Signal attenuation
- Noise and interference (EMI)
- Signal-to-noise ratio (SNR)
- Crosstalk
- Distortion
- Bit error rate (BER)


### Encoding & Transmission

- Bit encoding basics
- NRZ (Non-return-to-zero)
- Manchester encoding
- 4B/5B encoding
- 8b/10b encoding
- Line coding vs block coding
- Clock synchronization
- Baud rate vs bit rate
- Error detection at physical layer (CRC overview)


### Copper Networking

- Twisted pair cables
- Cat5, Cat5e, Cat6, Cat6a, Cat7, Cat8 differences
- Shielded vs unshielded cables (STP vs UTP)
- RJ45 connectors
- Cable pinouts (T568A vs T568B)
- Maximum cable lengths
- Signal degradation over copper
- Power over Ethernet (PoE)
- Cable testing tools
- Common cable failures


### Fiber Optics

- Fiber basics (light transmission)
- Single-mode vs multi-mode fiber
- Wavelengths
- Optical attenuation
- Fiber connectors (LC, SC, ST)
- SFP / SFP+ / QSFP modules
- Fiber transceivers
- Fiber vs copper trade-offs
- Bending losses
- Fiber installation issues


### Wireless Fundamentals

- Radio frequency basics
- Electromagnetic spectrum
- Frequency vs wavelength
- Signal propagation in air
- Interference sources
- Wi-Fi basics (802.11 overview)
- Channels and channel overlap
- Signal strength (RSSI)
- Noise floor
- Bluetooth basics
- Wireless latency characteristics



### Network Interface Hardware

- Network Interface Card (NIC)
- MAC address burning
- NIC buffers
- Interrupts and polling
- DMA (Direct Memory Access)
- Hardware offloading (checksum, segmentation)
- NIC queues
- Ring buffers
- Driver basics



### Physical Topologies & Devices

- Bus topology
- Star topology
- Ring topology
- Mesh topology
- Hybrid topologies
- Repeaters
- Hubs (and why they are obsolete)
- Media converters
- Patch panels
- Physical redundancy


### Performance & Limits

- Physical latency sources
- Speed of light limitations
- Serialization delay
- Transmission delay
- Propagation delay
- Impact of cable length
- Bandwidth limitations by medium
- Half-duplex vs full-duplex
- Auto-negotiation


###  Failures & Troubleshooting

- Cable breaks
- Loose connectors
- Signal degradation
- Duplex mismatches
- Hardware faults
- Interference issues
- Packet corruption at physical level
- Diagnosing link failures
- Link flapping
- CRC errors


###  Tools & Diagnostics

- Cable testers
- Time-domain reflectometer (TDR)
- Loopback testing
- NIC diagnostics
- ethtool basics
- dmesg for hardware issues
- Monitoring link status
- Checking interface errors



##  Suggested Labs

- Inspect NIC details using `ethtool`
- Simulate duplex mismatch and observe behavior
- Measure latency differences between interfaces
- Analyze interface error counters
- Test different Ethernet cables
- Observe link up/down events
- Compare Wi-Fi vs Ethernet latency
- Capture CRC/frame errors from interface stats

