---
tags: [komsys]
---
# Traceroute
Traceroute is a diagnostic tool used to trace the path of a packet as it travels through an IP network from its source to its destination. It works by sending packets with gradually increasing [[time to live|TTL]] (Time To Live) values, causing each router along the path to send back an [[internet control message protocol|ICMP]] "Time Exceeded" message indicating that the TTL has expired. By receiving these messages and recording the sender's IP address, traceroute can build a list of all the routers along the path that the packet takes. This information can be useful for diagnosing network problems, determining routing paths, and optimizing network performance.