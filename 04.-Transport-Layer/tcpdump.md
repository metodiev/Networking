# TCP Dump

A TCP dump is a packet capture done by OS/Network stack using tools like:

- tcpdump (Linux CLI tool)
- Wireshark (GUI tool)

These tools capture raw packets (TCP/UDP/IP) before your Java app processes them.

## Capture TCP Traffic (real Transport Layer dump)

```bash
sudo tcpdump -i any tcp port 8080 -w capture.pcap
```

- -i any → listen on all interfaces
- tcp port 8080 → filter your Java app port
- -w capture.pcap → save file

TCP handshake (SYN, ACK)
retransmissions
latency
packet-level issues

## Use libraries for packet capture 

You can integrate native-level capture using:

```java

Pcap4J (wrapper over libpcap)

PcapNetworkInterface nif = Pcaps.getDevByName("eth0");

PcapHandle handle = nif.openLive(
    65536,
    PcapNetworkInterface.PromiscuousMode.PROMISCUOUS,
    10
);

handle.loop(10, packet -> {
    System.out.println(packet);
});
```

