# Packet vs Segment vs Frame

These are the same data at different layers, just wrapped differently:

- Segment -> Transport layer (TCP/UDP)
- Packet -> Network Layer (IP)
- Frame -> Data Link Layer (Ethernet)

```mermaid
flowchart TD
    A["Application Data"]

    B["Segment<br>(TCP Header + Data)"]
    C["Packet<br>(IP Header + Segment)"]
    D["Frame<br>(MAC Header + Packet + Trailer)"]

    A --> B --> C --> D
```

## Layer Mapping 

| Unit    | Layer     | Protocol Example |
| ------- | --------- | ---------------- |
| Segment | Transport | TCP / UDP        |
| Packet  | Network   | IP               |
| Frame   | Data Link | Ethernet         |
