___
#flashcards/ComArk/11_Intro-to-Networks

What are the four main layers typically discussed in computer networks?
?
LAN (link layer), IP (internet layer), TCP (transport layer), and application layer (software).
<!--SR:!2025-07-16,30,230-->

What are the purpose of each layer in the 4-layer network model?
?
1. **Link layer**: Transmits raw bits over physical media (e.g., Ethernet, Wi-Fi), provides MAC addressing and error detection, determines if a message is for this device or should be ignored.
2. **Internet/Network layer**: Provides **logical addressing** (IP addresses), routes packets from source to destination across networks, handles fragmentation and reassembly.
3. **Transport layer**: Determines delivery method in which the port routes to the right app, once data has reached the right device.
4. **Application layer**: Provides user-facing services and application-level protocols (e.g., HTTP, FTP, DNS, SMTP) so software can communicate over the network.
<!--SR:!2025-06-18,2,238-->


How is the LAN layer divided?
?
Into physical (analog signals) and logical (digital operations) sublayers.
<!--SR:!2025-07-03,17,225-->

What are the two additional layers within the application layer in the OSI model?
?
The session layer (manages sessions) and presentation layer (handles data formatting and representation).
<!--SR:!2025-07-01,15,245-->

What is the full 7-layer OSI networking model?
?
1. Physical, 2. Data Link, 3. Network, 4. Transport, 5. Session, 6. Presentation, 7. Application.
<!--SR:!2025-06-28,12,225-->

What is the internet in simple terms?
?
A global computer network that connects devices like servers and clients (end systems), enabling message exchange.
<!--SR:!2025-07-11,25,265-->

What is a packet?
?
A unit of data transmission in networks, containing a header with metadata and a payload with the actual data.
<!--SR:!2025-06-28,33,245-->

What does the packet header include?
?
Source and destination addresses, routing info, and protocol metadata. Each network layer adds its own header.
<!--SR:!2025-08-14,58,265-->

What byte order does IP use?
?
Big Endian (network byte order).
<!--SR:!2025-06-29,13,245-->

What is the role of Internet Service Providers (ISPs)?
?
They serve as the gateway to the internet, connecting end systems to the wider network.
<!--SR:!2025-08-07,52,265-->

What is datagram forwarding?
?
Routers use forwarding tables to send packets step by step toward their destination.
<!--SR:!2025-07-02,16,205-->

What is the difference between data rate and throughput?
?
Data rate is the raw bit transfer rate (e.g., Mbps), while throughput measures actual data (i.e. excluding overhead s.a. headers) delivery over time.
<!--SR:!2025-06-23,7,205-->

What does goodput measure?
?
The useful application-level data rate, excluding headers and retransmissions.
<!--SR:!2025-06-23,7,190-->

What is bandwidth delay and how is it calculated?
?
The time to transmit all bits onto the link: $\frac{\text{size}}{\text{bandwidth}}$.
<!--SR:!2025-06-23,7,210-->

What is propagation delay and how is it calculated?
?
The time a signal takes to travel: $\frac{\text{distance}}{\text{propagation speed}}$ .
<!--SR:!2025-06-24,8,205-->

What is store-and-forward delay?
?
Time needed to receive the entire packet at a switch before forwarding it.
<!--SR:!2025-06-27,11,225-->

What is Round Trip Time (RTT)?
?
The time it takes for a signal to go from sender to receiver and back again.
<!--SR:!2025-06-27,32,270-->
