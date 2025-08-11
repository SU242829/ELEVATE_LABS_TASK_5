 Task 5 – Capture and Analyze Network Traffic Using Wireshark


Objective
To capture live network packets and identify basic protocols and traffic types using Wireshark, gaining hands-on experience in packet analysis and protocol awareness.



Tools Used
Wireshark – Latest available version at the time of capture

Operating System – Kali Linux

Network Interface – Active interface of the host system

Capture Details
Capture Duration: ~1 minute

Capture Files:

Full Capture.pcapng – Complete raw capture

Filtered Packets.pcapng – Filtered using dns or tcp or udp or icmp or http

Procedure Followed
1. Wireshark Installation
Installed and configured Wireshark to capture packets on the main network interface.

2. Traffic Generation
Browsed websites to generate HTTP/HTTPS traffic

Executed ping commands to generate ICMP packets

3. Packet Capture
Started capture on the active network interface

Stopped after ~1 minute

4. Filtering
Applied protocol filters to focus on:
DNS, TCP, ICMP, ARP, TLSv1.2

5. Analysis
Reviewed captured packets, inspecting:

Source/Destination IPs

Packet length

Protocol details


 
 Protocols Identified
DNS (Domain Name System)

Resolves human-readable domain names into IP addresses

Example: Request to google.com from 172.20.10.1 → Response with IPv4 address

ICMPv6 (Internet Control Message Protocol, IPv6)

Used for diagnostics and IPv6 neighbor discovery

Example: Echo request/reply with hop limit 64

TLSv1.2 (Transport Layer Security)

Provides encryption for secure HTTPS connections

Example: Encrypted communication over TCP port 443

TCP (Transmission Control Protocol)

Ensures reliable, ordered data delivery

Example: TCP handshake packets and acknowledgments

ARP (Address Resolution Protocol)

Maps IPv4 addresses to MAC addresses on a LAN

Example: ARP request to resolve local network device MAC address



Sample Packet Details
Protocol	Source	Destination	Info
DNS	172.20.10.1	8.8.8.8	Query for google.com
ICMPv6	Local IPv6	Remote IPv6	Echo request (hop limit 64)
TLSv1.2	Port 443	Port 34770	Encrypted HTTPS packet



Conclusion
This task demonstrated the ability to:

Capture and filter live network traffic

Identify and analyze multiple network protocols

Understand the role each protocol plays in normal network communication

Five protocols (DNS, ICMPv6, TCP, TLSv1.2, ARP) were successfully captured and analyzed, reflecting the variety of traffic in a typical browsing session.
