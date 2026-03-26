# 🔗 Networking Mastery — Data Link Layer (02)

The Data Link Layer is responsible for **node-to-node communication** within the same network segment.

This is where frames, MAC addresses, switches, and ARP live — and where many real-world outages actually happen.



##  Goals

- Understand how devices communicate on the same local network
- Learn how switches forward traffic
- Master MAC addressing and ARP behavior
- Diagnose Layer 2 issues like loops, storms, and misconfigurations



##  Topics Overview


###  Ethernet Fundamentals

- What is Ethernet
- Ethernet frame structure
- Frame header fields
- Source and destination MAC
- EtherType field
- Payload and padding
- Frame Check Sequence (FCS)
- Minimum and maximum frame size
- Jumbo frames



###  MAC Addressing

- MAC address structure (OUI + device)
- Unicast, broadcast, multicast MAC
- MAC address uniqueness
- MAC address spoofing
- MAC address randomization
- MAC vs IP addressing
- Vendor lookup (OUI)



###  ARP (Address Resolution Protocol)

- What is ARP
- ARP request/response flow
- ARP cache
- Gratuitous ARP
- Proxy ARP
- ARP timeouts
- ARP cache poisoning
- ARP spoofing attacks
- Debugging ARP issues
- ARP in Linux (`ip neigh`)



###  Switching Fundamentals

- What is a network switch
- Frame forwarding logic
- Learning MAC addresses (CAM table)
- Flooding unknown destinations
- Unicast vs broadcast forwarding
- Switch forwarding methods (store-and-forward vs cut-through)
- Switching vs routing
- Hardware vs software switching



### CAM Table (MAC Table)

- What is CAM table
- MAC learning process
- MAC aging
- MAC table overflow
- MAC flooding attack
- Static vs dynamic MAC entries
- Viewing MAC tables
- Troubleshooting MAC issues



###  VLANs (Virtual LANs)

- What is VLAN
- VLAN tagging (802.1Q)
- Access ports vs trunk ports
- Native VLAN
- VLAN IDs
- Inter-VLAN communication
- VLAN isolation
- VLAN hopping attacks
- QinQ (802.1ad)
- VLAN configuration concepts



###  Loop Prevention & Spanning Tree

- Network loops problem
- Broadcast storms
- Spanning Tree Protocol (STP)
- Root bridge election
- Port roles and states
- Convergence process
- Rapid STP (RSTP)
- Multiple STP (MSTP)
- BPDU frames
- STP failures and misconfigurations



###  Link Aggregation

- What is link aggregation
- LACP basics
- Static vs dynamic aggregation
- Load balancing strategies
- Failure handling
- Hashing algorithms
- LAG troubleshooting



###  Layer 2 Discovery Protocols

- LLDP (Link Layer Discovery Protocol)
- CDP (Cisco Discovery Protocol)
- Neighbor discovery basics
- Topology mapping
- Use cases in debugging



###  Frame Handling & Behavior

- Frame buffering
- Queueing
- Head-of-line blocking
- Priority tagging (802.1p)
- QoS at Layer 2
- Traffic classification
- Frame drops
- Congestion at L2



###  Linux Layer 2 Networking

- Linux bridge
- `brctl` and `ip link`
- TAP/TUN interfaces
- Open vSwitch (OVS) basics
- Network namespaces (L2 perspective)
- Virtual Ethernet pairs (veth)
- Packet flow in Linux bridge
- ebtables basics



###  Observability & Debugging

- Capturing Ethernet frames (`tcpdump -e`)
- Promiscuous mode
- Port mirroring (SPAN)
- Network TAPs
- Inspecting MAC tables
- Debugging ARP issues
- Detecting loops
- Identifying broadcast storms
- Interface statistics analysis
- Dropped frame analysis



###  Failures & Attacks

- Broadcast storms
- MAC flooding
- ARP spoofing
- VLAN hopping
- STP manipulation
- Duplicate MAC issues
- Misconfigured trunks
- Loop-induced outages
- Switch overload
- Frame corruption



##  Suggested Labs

- Capture Ethernet frames with MAC addresses
- Inspect ARP table (`ip neigh`)
- Simulate ARP spoofing in a lab
- Create VLANs using Linux bridge or OVS
- Build two VLANs and isolate traffic
- Simulate broadcast storm
- Observe MAC learning behavior
- Configure link aggregation (LACP)
- Use network namespaces to simulate hosts
- Debug a broken ARP scenario

