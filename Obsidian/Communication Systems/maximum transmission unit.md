---
tags: [komsys]
aliases: [MTU]
---
# Maximum Transmission Unit
MTU stands for Maximum Transmission Unit and refers to the largest size of a data packet that can be transmitted over a network in a single frame or packet.

When a sender wants to send data over a network, it breaks the data into smaller chunks called packets, which are then transmitted over the network. Each packet has a header that includes routing and addressing information, as well as the actual data being sent.

Different networks and protocols have different maximum sizes for the packets they can handle, which is the MTU. For example, Ethernet networks have an MTU of 1500 bytes, while some DSL networks have a smaller MTU of around 1480 bytes.

If a packet is larger than the MTU of a network, it will need to be fragmented into smaller packets before being transmitted. This can result in increased overhead and decreased network performance. **Therefore, it is important to ensure that the packet size does not exceed the MTU of the network being used.**