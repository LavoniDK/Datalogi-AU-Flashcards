___
#flashcards/ComArk/13-Transport-Layer

## OSI Transport Layer Overview

What is the role of the transport layer in the OSI model?::To control network traffic between hosts and ensure full data flows to the correct application.
<!--SR:!2025-06-20,3,253-->

Where is the transport layer located in the OSI model?::Between the network and session layers.
<!--SR:!2025-06-19,3,250-->

What is the main responsibility of the transport layer beyond delivery to a machine?::Ensuring data is delivered to the correct application on the destination machine.
<!--SR:!2025-06-20,3,250-->

## User Datagram Protocol (UDP)

What does UDP add to IP communication?::Port numbers to enable communication with specific applications.
<!--SR:!2025-06-20,3,250-->

Is UDP connection-oriented or connectionless?::Connectionless.
<!--SR:!2025-06-20,3,250-->

Why is UDP considered unreliable?::Because it does not confirm receipt or retransmit lost packets.
<!--SR:!2025-06-19,3,250-->

Why would you choose UDP over TCP?::For applications requiring low delay where some data loss is acceptable (e.g., streaming, gaming, DNS).
<!--SR:!2025-06-19,3,250-->

What are the components of a UDP header?::Source Port, Destination Port, Length, Checksum.
<!--SR:!2025-06-19,3,250-->

What Java classes are used for UDP socket programming?::DatagramSocket and DatagramPacket.
<!--SR:!2025-06-19,3,250-->

## Reliable Transport Concepts

What does reliable transport ensure?::Complete, correct, and in-order delivery of data.
<!--SR:!2025-06-19,3,250-->

What is the purpose of ACKs in reliable transport?::To confirm receipt of data.
<!--SR:!2025-06-20,3,250-->

What happens when an ACK is not received in time?::The sender retransmits the data.
<!--SR:!2025-06-20,3,250-->

Why are sequence numbers used?::To order packets correctly and detect missing ones.
<!--SR:!2025-06-19,3,250-->

What is flow control in transport protocols?::A mechanism to prevent senders from overwhelming receivers.
<!--SR:!2025-06-19,3,250-->

What is congestion control?::A technique to adjust sending rates based on network conditions.
<!--SR:!2025-06-19,3,250-->

Describe the Stop-and-Wait protocol::The sender sends one packet and waits for an ACK before sending the next.
<!--SR:!2025-06-19,3,250-->

What is the Sorcerer's Apprentice Bug?::A bug from duplicate packet retransmissions causing infinite loops if not managed.
<!--SR:!2025-06-21,4,270-->

What is the sliding window protocol?::A flow control scheme allowing multiple packets to be sent before needing an ACK.
<!--SR:!2025-06-19,3,250-->

How does the sliding window protocol use ACKs?::ACKs allow the sender to advance the window and send more data.
<!--SR:!2025-06-20,3,250-->

How is optimal window size computed?::By multiplying bandwidth with delay.
<!--SR:!2025-06-19,3,250-->

## Transmission Control Protocol (TCP)

What type of protocol is TCP?::A connection-oriented, reliable transport protocol.
<!--SR:!2025-06-19,3,250-->

How does TCP establish a connection?::Using a 3-way handshake (SYN, SYN-ACK, ACK).
<!--SR:!2025-06-21,4,270-->

What are common TCP flags?::ACK, URG, PSH, RST, SYN, FIN.
<!--SR:!2025-06-19,3,250-->

When does data transfer occur in TCP?::After the 3-way handshake is completed.
<!--SR:!2025-06-19,3,250-->

How does TCP ensure reliable delivery?::By using ACKs, sequence numbers, timeouts, and retransmissions.
<!--SR:!2025-06-19,3,250-->

What is TCP's data abstraction model?::A continuous stream of bytes.
<!--SR:!2025-06-19,3,250-->

How does TCP manage flow control?::With a sliding window to adjust the sender's rate to the receiver's capability.
<!--SR:!2025-06-21,4,270-->

What are TCP's congestion control mechanisms?::Slow start, congestion avoidance, fast retransmit, and fast recovery.
<!--SR:!2025-06-19,3,250-->

How is a TCP connection terminated?::With a 4-step FIN handshake.
<!--SR:!2025-06-19,3,250-->

What is the TIME_WAIT state?::A state ensuring old packets don't interfere and final ACK is received; lasts 2x MSL.
<!--SR:!2025-06-19,3,250-->

What is the role of the RST flag?::To immediately reset and close a connection.
<!--SR:!2025-06-21,4,270-->

What is the purpose of Delayed ACKs?::To reduce overhead by not acknowledging every single packet immediately.
<!--SR:!2025-06-20,3,253-->

What does the Nagle algorithm do? ::Combines small outgoing messages to reduce overhead.
<!--SR:!2025-06-20,3,250-->

What are common TCP attacks?::SYN floods and forged resets.
<!--SR:!2025-06-19,3,250-->

How can TCP flow control temporarily halt data transmission?::By setting the window size to zero.
<!--SR:!2025-06-21,4,270-->