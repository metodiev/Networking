#  Networking Mastery — Foundations (00)

This module builds the **core mental model of networking**.  
Before diving into TCP, DNS, or packet captures, you must deeply understand these fundamentals.


##  Goals

- Understand how networks actually work end-to-end
- Build intuition for packets, latency, and data flow
- Learn the language used in advanced networking topics
- Prepare for deep dives into TCP/IP, DNS, and system-level networking


##  Topics Overview

###  Core Concepts

- What is networking
- Why networking exists
- Evolution of computer networks
- Internet vs intranet
- Client-server model
- Peer-to-peer (P2P) model
- Centralized vs decentralized systems



###  Models & Abstractions

- OSI Model (7 layers)
- TCP/IP Model (4 layers)
- OSI vs TCP/IP differences
- Why abstraction layers matter
- Encapsulation and decapsulation
- Data flow across layers


###  Data Units & Terminology

- Packet vs segment vs frame
- Payload
- Headers and metadata
- Protocol definition
- Protocol stack
- Flow vs connection


### ⚡ Performance Fundamentals

- Bandwidth (capacity)
- Throughput (actual rate)
- Goodput (useful data)
- Latency (delay)
- Jitter (latency variation)
- Packet loss
- Network congestion


###  Size & Limits

- MTU (Maximum Transmission Unit)
- MSS (Maximum Segment Size)
- Fragmentation basics
- Reassembly basics
- Impact of MTU on performance


###  Binary & Data Representation

- Bits and bytes
- Binary representation
- Hexadecimal basics
- Endianness (big vs little endian)
- Encoding data in packets



###  Reliability Basics

- Checksums overview
- Error detection vs correction
- Retransmission concept
- Ordering guarantees
- Idempotency in networking



###  Internet Fundamentals

- What is the Internet
- How data travels globally
- Autonomous Systems (AS)
- High-level routing concept
- ISPs and backbone networks



###  Network Design Basics

- Network topologies (star, mesh, bus, ring)
- Physical vs logical topology
- Circuit switching vs packet switching
- Stateless vs stateful communication



### ⏱ Time & Behavior

- Round Trip Time (RTT)
- Timeouts
- Retries
- Backoff strategies (exponential backoff)



###  Standards & Governance

- What is an RFC
- IETF overview
- How protocols are standardized
- Reading RFCs effectively


###  Debugging Mindset

- Thinking in packets
- Layer-by-layer debugging
- Observability basics
- Cause vs symptom in networking issues



###  Tools Overview (Intro Only)

- ping
- traceroute
- curl
- netstat / ss
- tcpdump (preview)
- Wireshark (preview)



##  Suggested Labs

- Measure latency using `ping`
- Compare latency across different hosts
- Use `traceroute` to visualize packet path
- Observe packet size differences with MTU changes
- Convert IPs between binary and decimal
- Capture first packets using `tcpdump` (basic)


