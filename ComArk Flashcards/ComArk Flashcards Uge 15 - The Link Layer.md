___
#flashcards/ComArk/15_Link-Layer

## Link Layer Overview

What is the purpose of the link layer? ::To connect physical devices and enable final routing of data through network interfaces.
<!--SR:!2025-06-18,2,243-->

Where is the link layer primarily implemented? ::In the network interface hardware.
<!--SR:!2025-06-25,9,250-->

What happens to an IP packet at each hop in the network? ::It is wrapped and unwrapped in a new link-layer frame.
<!--SR:!2025-06-18,2,243-->

## Link Layer Packet Format

What is the size of MAC addresses? ::48 bits.
<!--SR:!2025-06-18,2,243-->

What is the maximum length of a link-layer packet? ::1500 bytes.
<!--SR:!2025-06-18,2,243-->

What does the preamble in Ethernet do? ::Helps receivers synchronize with the sender's clock.
<!--SR:!2025-06-18,2,243-->

What are broadcast, promiscuous mode, and multicast in Ethernet? ::Broadcast: all nodes; Promiscuous: listen to all; Multicast: group communication.
<!--SR:!2025-06-18,2,244-->

## Collisions and CSMA/CD

What is the Ethernet collision window? ::512 bits.
<!--SR:!2025-06-18,2,243-->

What happens if a collision is not detected during the collision window? ::The transmission is considered successful.
<!--SR:!2025-06-18,2,244-->

What is the minimum Ethernet frame size and why? ::512 bits to allow detection of collisions.
<!--SR:!2025-06-18,2,243-->

What are the steps of CSMA/CD? ::Listen, transmit and listen, jam if collision, backoff using exponential delay.
<!--SR:!2025-06-18,2,243-->

## Address Resolution Protocol (ARP)

What is the purpose of ARP? ::To map IP addresses to MAC addresses.
<!--SR:!2025-06-18,2,243-->

What type of message is used in an ARP request? ::Broadcast.
<!--SR:!2025-06-18,2,243-->

What type of message is used in an ARP reply? ::Unicast.
<!--SR:!2025-06-19,3,263-->

What is stored in the ARP cache? ::(IP, MAC) address pairs.
<!--SR:!2025-06-18,2,210-->

What is the purpose of a Self-ARP? ::To detect duplicate IP addresses on the network.
<!--SR:!2025-06-18,2,244-->

## Ethernet Learning and Switching

What role do switches play in Ethernet? ::They forward packets based on MAC addresses and support more complex topologies.
<!--SR:!2025-06-18,2,244-->

What can cause switch flooding in large networks? ::Lack of learned addresses or looped paths.
<!--SR:!2025-06-18,2,243-->

## Spanning Tree Protocol (STP)

Why is the Spanning Tree Protocol used? ::To eliminate loops in networks with switches.
<!--SR:!2025-06-18,2,244-->

What does the BPDU algorithm elect in STP? ::A root switch and forwarding paths.
<!--SR:!2025-06-18,2,243-->

What states can ports be in under STP? ::Root port, designated port, or blocking.
<!--SR:!2025-06-19,2,210-->

## Wi-Fi and Wireless Networks

What medium does Wi-Fi operate on? ::A shared wireless medium.
<!--SR:!2025-06-18,2,244-->

Why are collisions a problem in Wi-Fi? ::Because of signal interference and limited detection capabilities.
<!--SR:!2025-06-18,2,243-->

What devices interfere with the 2.4 GHz band? ::Phones, Bluetooth, microwaves, wireless devices.
<!--SR:!2025-06-18,2,244-->

What role do ACK packets play in Wi-Fi? ::They confirm local delivery at the link layer.
<!--SR:!2025-06-18,2,244-->

What are the timing intervals used in Wi-Fi transmission? ::DIFS (before sending), SIFS (for ACKs).
<!--SR:!2025-06-18,2,243-->

What is the Hidden Node Problem? ::Nodes out of each other's range may still interfere with a common receiver.
<!--SR:!2025-06-18,2,243-->

How does RTS/CTS help in Wi-Fi? ::Coordinates access to reduce hidden node collisions.
<!--SR:!2025-06-18,2,244-->

Why is RTS/CTS often disabled? ::It adds overhead and reduces performance in many practical networks.
<!--SR:!2025-06-18,2,243-->