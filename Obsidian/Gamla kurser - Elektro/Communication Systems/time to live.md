---
aliases: [TTL]
tags: [komsys]
---
# Time to Live
TTL stands for "Time to Live" and is a field in IP (Internet Protocol) packets that specifies the maximum number of network hops (routers) that a packet can pass through before being discarded. Each time a router receives a packet, it decrements the TTL field by one. When the TTL field reaches zero, the router discards the packet and sends an ICMP (Internet Control Message Protocol) message back to the sender indicating that the packet has expired. The purpose of TTL is to prevent packets from circulating indefinitely in the network, which could cause congestion and affect network performance.