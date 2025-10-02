Designed and implemented a secure, scalable, and reliable enterprise network for a fictional company (Cairo Telco) using Cisco Packet Tracer. The project aimed to meet organizational requirements of high performance, robust security, seamless cloud connectivity, and future scalability.

The Challenge

Cairo Telco operates across two floors with multiple departments.

Needed a complete network infrastructure from the ground up.

Key requirements: performance, security, scalability, and Azure cloud connectivity.

My Approach

I adopted the Hierarchical Network Design Model (Core, Distribution, and Access layers) to ensure redundancy, scalability, and simplified troubleshooting.

Key Features
🔒 Security First

Deployed a Cisco ASA Firewall for traffic control between LAN, DMZ, and the internet.

Configured a DMZ zone for Email, ERP, and File servers.

Enabled PortFast on access ports and BPDU Guard to protect against rogue switches.

Implemented a Standard ACL to restrict SSH access exclusively to IT staff.

⚡ Reliability & Performance

Implemented VLAN segmentation:

Data – VLAN 50

Wireless – VLAN 60

Voice – VLAN 101

Configured LACP EtherChannel for redundancy and higher bandwidth between switches.

Used OSPF dynamic routing for efficient path selection.

📞 Unified Communications & Services

Integrated a VoIP system with a Cisco Voice Gateway for IP telephony.

Deployed a Cisco WLC for centralized wireless management.

Configured DHCP server for automatic IP assignment; DMZ servers used static IPs.

Network Topology

(Include your Packet Tracer diagram here for visualization)

IP Addressing Scheme

LAN: 192.168.10.0/24

WLAN: 10.20.0.0/16

Voice: 172.16.10.0/24

DMZ: 10.10.10.0/28

Public: 197.200.100.0

Core Technologies

Simulation Tool: Cisco Packet Tracer

Hardware (Simulated): Cisco ASA 5525-X Firewall, Catalyst 3850 & 2960 Switches, Cisco 2811 Voice Gateway, Cisco WLC

Protocols & Concepts: OSPF, VLANs, Inter-VLAN Routing, LACP (EtherChannel), STP (PortFast, BPDU Guard), DHCP, VoIP, ACLs, Firewall Security Zones
