# What is Networking

## What is Networking

Networking is the practice of connecting computers and devices so they can communicate and share data. This communication happens through defined rules called protocols, over physical or wirless connections.
At its core, networking enables:

- Data exchange (files, messages, streams)
- Resource sharing (printers, servers)
- Distributed systems (cloud, microservices)\

## Simple Explanation

Think of networking like a postal system:

- devices = houses
- IP address = home address
- Protocols = rules for sending letters
- Routers - post offices directing traffic

## Key Components

1. Devices
 - Client (your laptop, phone)
 - Servers (backend systems, APIs)
 - Routers and switches

 2. Protocols

 Rules that define communication:

 - HTTP / HTTPS -. Web Traffic
 - TCP / UDP - Transport Layer
 - IP - Addressing

 3. Transmission Media
 - Ethernet cables
 - Fiber optics
 - Wi-Fi

 ## Types of Networks 

 - LAN - Local Area Network
 - WAN - Wide Area Network 
 - MAN - Metropolitan Area Network


 ## Networking Models

 OSI Model - 7 Layers

 1. Physical
 2. Data Link
 3. Network
 4. Transport
 5. Session
 6. Presentation
 7. Application

 OSI Model visualization

 ```mermaid
flowchart TD
   A["7. Application<br>HTTP, FTP"]
   B["6. Presentation<br>Encryption"]
   C["5. Session<br>Sessions"]
   D["4. Transport<br>TCP / UDP"]
   E["3. Network<br>IP Routing"]
   F["2. Data Link<br>MAC"]
   G["1. Physical<br>Signals"]

   A --> B --> C --> D --> E --> F --> G

   classDef layer fill:#1e293b,color:#fff,stroke:#38bdf8
   class A,B,C,D,E,F,G layer
 ```

 ### TCP/IP Model (Practical Version)

 - Application
 - Transport
 - Internet
 - Network Access

## Why Networking Matters (Real-World Context)

For someone like you (backend / distributed systems / data pipelines):

- Microservices communicate over network (REST, gRPC)
- Databases are often remote
- Cloud = networking at scale
- Latency, throughput, and reliability directly affect system performance


## Code

```java
import java.net.Socket;

public class SimpleClient {

public static void main(String[] args) throws Exception {
  Socket socket = new Socket ("example.com", 80);
  System.out.println("Connected to server");
  socket.close();
}


}

```


 
