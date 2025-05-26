# CodeAlpha_Basic_Network_Sniffer
A project I made as an intern at CodeAlpha

This repository contains a simple yet effective network packet sniffer written in Python.
This Python script acts like a digital detective, sniffing out and decoding the secrets of your network traffic!
It's designed to capture and parse raw network packets, providing insights into the different layers of the network stack.

Key Features:

* Ethernet Frame Parsing: Extracts destination MAC, source MAC, and EtherType.
* IPv4 Packet Decoding: Identifies IP version, header length, TTL, protocol (ICMP, TCP, UDP), source IP, and destination IP.
* ICMP Packet Analysis: Displays ICMP type, code, and checksum.
* TCP Segment Dissection: Parses source port, destination port, sequence and acknowledgment numbers, and various TCP flags (URG, ACK, PSH, RST, SYN, FIN).
* UDP Segment Extraction: Shows source port, destination port, and length.
* Hexdump-like Data Representation: Formats raw packet data for easy readability.

How it Works:

The script utilizes `socket.socket(socket.AF_PACKET, socket.SOCK_RAW, socket.ntohs(3))` to create a raw socket, allowing it to capture all incoming network traffic at the data link layer. It then systematically unpacks the various protocol headers using the `struct` module, presenting the information in a human-readable format.
And then indents the output of the code to make it easily readable and understandable

Tools Used:

'Vim' - Kali Virtual Box

Programming Language Used:

'Python'

Usage:

To run the sniffer, you'll likely need root/administrator privileges as raw sockets require elevated permissions.

On 'zshell', run 'sudo python network_sniffer.py'
