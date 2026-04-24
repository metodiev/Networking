# OSI model vs TCP/IP

OSI = conceptual model (teaching tool)
TCP/IP = practical model (used in real systems, the Internet)

```mermaid
flowchart LR
    subgraph OSI Model
        A1["7. Application"]
        A2["6. Presentation"]
        A3["5. Session"]
        A4["4. Transport"]
        A5["3. Network"]
        A6["2. Data Link"]
        A7["1. Physical"]
    end

    subgraph TCP/IP Model
        B1["Application"]
        B2["Transport"]
        B3["Internet"]
        B4["Network Access"]
    end

    A1 --> B1
    A2 --> B1
    A3 --> B1
    A4 --> B2
    A5 --> B3
    A6 --> B4
    A7 --> B4


```


## Side by Side Comparison


| OSI Model (7 Layers) | TCP/IP Model (4 Layers) | Notes     |
| -------------------- | ----------------------- | --------- |
| Application          | Application             | Merged    |
| Presentation         | Application             | Merged    |
| Session              | Application             | Merged    |
| Transport            | Transport               | Same      |
| Network              | Internet                | Same idea |
| Data Link            | Network Access          | Merged    |
| Physical             | Network Access          | Merged    |


## Real Protocol Mapping

```mermaid

flowchart TD
    A["Application<br>HTTP, HTTPS, DNS"]
    B["Transport<br>TCP, UDP"]
    C["Internet<br>IP, ICMP"]
    D["Network Access<br>Ethernet, ARP"]

    A --> B --> C --> D

```

## Key Differences (Short but Sharp)
1. Number of Layers
- OSI → 7 layers
- TCP/IP → 4 layers
2. Purpose
- OSI → theoretical, standardized model
- TCP/IP → real-world implementation
3. Design Philosophy
- OSI → strict separation of concerns
- TCP/IP → practical and flexible
