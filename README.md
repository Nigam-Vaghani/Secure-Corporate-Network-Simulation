Cairo Telco: A Secure Enterprise Network Simulation
Welcome to my Cairo Telco network project! This is a comprehensive simulation I built in Cisco Packet Tracer to design and implement a secure, scalable, and robust network for a growing company.

The Challenge
The scenario involves a fictional company, Cairo Telco, which occupies two floors and has multiple departments. They needed a complete network infrastructure from the ground up. The main requirements were high performance, strong security, scalability for future growth, and reliable connectivity to their Microsoft Azure cloud services.



My goal was to design and configure a network that not only met these technical demands but was also well-organized and easy to manage, following best practices.

My Approach & Key Features
I decided to build the network using a 

hierarchical model to ensure it was redundant and scalable. This separates the network into core, distribution, and access layers, which makes it much easier to troubleshoot and expand.

Here are some of the key decisions and features I implemented:

Security First: Security was the top priority.

I placed a 

Cisco ASA Firewall at the edge to manage traffic between the internal network, the internet, and a dedicated DMZ for the company's servers (Email, ERP, File Server).


On the switches, I enabled 

PortFast on access ports for faster device connectivity and BPDU Guard to prevent unauthorized switches from being added to the network.

I wrote a standard 

ACL to lock down SSH access, so only the IT department can manage devices remotely.

Building for Reliability and Speed:

I segmented the network using VLANs to keep traffic for Data (VLAN 50), Wireless (VLAN 60), and Voice (VLAN 101) separate. This improves both security and performance.


To boost performance and add redundancy between my switches, I configured 

LACP EtherChannel, which bundles multiple links into one logical connection.

I used 

OSPF as the dynamic routing protocol to ensure that all parts of the network could find the best path to communicate with each other automatically.

Unified Communications & Services:

The design includes a full 

VoIP system, with a Cisco Voice Gateway providing telephony services to IP phones in each department.


I set up a 

centralized wireless network using a Cisco WLC to manage all the access points, providing seamless Wi-Fi across both floors.

A central server handles 

DHCP, so devices can get an IP address automatically , while servers in the DMZ have 

static IPs.

Network Topology
Here's a visual look at the final network design:

IP Addressing Plan
This was the IP address scheme I worked with for the project:

LAN: 192.168.10.0/24

WLAN: 10.20.0.0/16

Voice: 172.16.10.0/24

DMZ: 10.10.10.0/28

Public: 197.200.100.0

Core Technologies Used
Simulation Tool: Cisco Packet Tracer

Key Hardware (Simulated): Cisco ASA 5525-X Firewall, Catalyst 3850 & 2960 Switches, Cisco 2811 Voice Gateway, Cisco WLC.

Protocols & Concepts: OSPF, LACP (EtherChannel), STP (PortFast, BPDU Guard), VLANs, Inter-VLAN Routing, DHCP, VoIP, Standard ACLs, Firewall Security Zones.
