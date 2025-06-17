___
#flashcards/ComArk/14_Network-Layer

## Network Layer Overview

What are the main responsibilities of the Network Layer? ::Logical addressing, routing, fragmentation & reassembly, path selection, traffic control.
<!--SR:!2025-06-19,2,239-->

What are common protocols used at the network layer? ::IPv4, IPv6, ICMP, IGMP, OSPF, BGP.
<!--SR:!2025-07-10,24,250-->

Does IP guarantee delivery or ordering? ::No, IP is connectionless and does not guarantee delivery, ordering, or integrity.
<!--SR:!2025-06-18,2,239-->

## IP Addressing

To what are IP addresses assigned? ::Interfaces.
<!--SR:!2025-06-19,2,239-->

What is the format of an IPv4 address? ::32-bit, written as a.b.c.d in dotted-decimal notation.
<!--SR:!2025-06-18,2,239-->


What is CIDR notation? ::A compact way to represent subnet masks using a slash and prefix length (e.g., 192.168.1.0/24).
<!--SR:!2025-06-18,2,239-->

How is an IPv6 address written? ::128-bit, written in colon-hex format (e.g., 2001:0db8::/32).
<!--SR:!2025-06-19,2,239-->

What key features does IPv6 include over IPv4? ::No broadcasts, multicast use, auto-configuration, IPsec support.
<!--SR:!2025-06-19,2,239-->

## IP Header Structure

What does IHL stand for in the IP header? ::Internet Header Length (in 32-bit words).
<!--SR:!2025-06-19,2,239-->

What is TTL in the IP header? ::Time To Live - a hop limit.
<!--SR:!2025-07-04,18,250-->

What does the Protocol field in the IP header specify? ::The higher-layer protocol (e.g., 6 = TCP, 17 = UDP).
<!--SR:!2025-06-19,2,239-->

What is the function of the header checksum? ::To detect errors in the header.
<!--SR:!2025-07-07,21,250-->

## Fragmentation

Why is IP fragmentation necessary? ::To adapt to varying MTU sizes across networks.
<!--SR:!2025-06-19,2,239-->

What approach to fragmentation does IP use? ::Per-path fragmentation: source fragments and destination reassembles.
<!--SR:!2025-06-19,2,239-->

What do all fragments of an IP packet share? ::Same identification, source & destination address, and protocol.
<!--SR:!2025-06-19,2,239-->

How is the position of a fragment indicated? ::Using the Offset field (Offset × 8 = byte offset).
<!--SR:!2025-06-19,2,239-->

Why must fragment sizes be multiples of 8 bytes? ::To maintain alignment and allow proper reassembly.
<!--SR:!2025-06-19,2,239-->

## Subnets

What is a subnet? ::A logical subdivision of an IP network.
<!--SR:!2025-06-19,2,239-->

Why are subnets used? ::Management, security, performance, efficiency.
<!--SR:!2025-06-19,2,239-->

What is the role of a subnet mask? ::To separate the network and host portions of an IP address.
<!--SR:!2025-06-19,2,239-->

How do routers use subnet masks? ::To determine the correct subnet and forward packets accordingly.
<!--SR:!2025-06-19,2,239-->

## Network Address Translation (NAT)

What is NAT? ::A technique that allows multiple private devices to share one public IP.
<!--SR:!2025-06-19,2,239-->

Why is NAT important? ::IPv4 address conservation and added security.
<!--SR:!2025-06-19,2,239-->

How does NAT modify outgoing traffic? ::It replaces the private IP with the public IP and tracks the mapping.
<!--SR:!2025-06-19,2,239-->

What is Port Address Translation (PAT)? ::NAT Overload - multiple devices share one IP using different ports.
<!--SR:!2025-06-19,2,239-->

## Dynamic Host Configuration Protocol (DHCP)

What does DHCP do? ::Automatically assigns IP addresses and settings.
<!--SR:!2025-06-18,2,190-->

Why use DHCP? ::Reduces manual setup, prevents conflicts, centralizes management.
<!--SR:!2025-06-19,2,239-->

What are the steps in the DHCP DORA process? ::Discover, Offer, Request, Acknowledge.
<!--SR:!2025-06-19,2,239-->

What kind of settings can DHCP provide? ::IP, subnet mask, gateway, DNS.
<!--SR:!2025-06-19,2,239-->

## Internet Control Message Protocol (ICMP)

What is ICMP used for? ::To check/report network status and reachability.
<!--SR:!2025-06-19,2,239-->

How does traceroute work? ::Uses TTL values and ICMP to discover routing paths.
<!--SR:!2025-06-18,2,210-->

## Routing Algorithms

What is the purpose of routing algorithms? ::To determine the best path for packets to travel.
<!--SR:!2025-07-09,23,250-->

What are the three main types of routing algorithms? ::Distance Vector, Path Vector, Link State.
<!--SR:!2025-06-19,2,239-->

What does Distance Vector Routing rely on? ::Routers exchange distance (cost) vectors with neighbors.
<!--SR:!2025-06-19,2,239-->

What does Link State Routing use? ::Full topology maps and Dijkstra's algorithm.
<!--SR:!2025-06-19,2,239-->

What are some problems with Distance Vector Routing? ::Loops, slow convergence (count to infinity).
<!--SR:!2025-06-18,2,239-->

What is Split Horizon? ::A router does not advertise routes back to the source of those routes.
<!--SR:!2025-06-19,2,239-->

What is Triggered Updates? ::Immediate routing updates on changes instead of waiting.
<!--SR:!2025-06-19,2,239-->

What is the purpose of Hold Down in routing? ::To prevent trusting unstable route changes immediately.
<!--SR:!2025-06-19,2,239-->

How are loops prevented in Link State Routing? ::By labeling and discarding duplicate messages.
<!--SR:!2025-06-18,2,190-->

Why is Link State Routing preferred in large networks? ::It converges faster and offers more accurate routing.
<!--SR:!2025-06-19,2,239-->