# Encapsulation in Networking

Encapsulation is the process of wrapping data with protocol-specific information (headers/trailers) as it moves down the network stack.

Each layer adds its own metadata.

## Simple Flow

- Application -> Data
- Transport -> Segment
- Network -> Packet
- Data Link -> Frame
- Physical -> Bits

```mermaid

flowchart TD
    A["Application Layer<br>Data"]
    B["Transport Layer<br>TCP Header + Data = Segment"]
    C["Network Layer<br>IP Header + Segment = Packet"]
    D["Data Link Layer<br>MAC Header + Packet + Trailer = Frame"]
    E["Physical Layer<br>Bits (010101...)"]

    A --> B --> C --> D --> E

```

### Visualization with real Headers

```mermaid
flowchart TD
    A["Data"]
    B["[TCP Header][Data]<br>Segment"]
    C["[IP Header][TCP Header][Data]<br>Packet"]
    D["[MAC Header][IP Header][TCP Header][Data][FCS]<br>Frame"]
    E["010101010101<br>Bits"]

    A --> B --> C --> D --> E

```


### Decapsulation (Receving side)
```mermaid
flowchart TD
    A["Bits"]
    B["Frame"]
    C["Packet"]
    D["Segment"]
    E["Data"]

    A --> B --> C --> D --> E
```

## Real Example (HTTP Request)

GET /users HTTP/1.1

It becomes:

1. Application -> HTTP request
2. Transport -> TCP segment (adds port info)
3. Network -> IP packet (adds IP addresses)
4. Data Link -> Frame (adds Mac addresses)
5. Physical -> Sent as bits

## TCP 3-Way Handshake

```mermaid
sequenceDiagram
    participant Client
    participant Server

    Client->>Server: SYN (seq = x)
    Server->>Client: SYN-ACK (seq = y, ack = x+1)
    Client->>Server: ACK (ack = y+1)

    Note over Client,Server: Connection Established

```
