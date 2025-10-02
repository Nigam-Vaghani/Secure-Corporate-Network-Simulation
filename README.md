# Cairo Telco: A Secure Enterprise Network Simulation

Welcome to my Cairo Telco network project!  This is a comprehensive simulation I built in Cisco Packet Tracer to design and implement a secure, scalable, and robust network for a growing company.

## The Challenge

 The scenario involves a fictional company, Cairo Telco, a fast-growing telecommunication company in Cairo, Egypt.  The company occupies the fourth and fifth floors of a building, hosting six different departments: HR and Finance, Product Brand and Marketing, Admin and Corporate, IT Network & Support, Software Engineering, and Cloud Engineering.

They needed a complete network infrastructure from the ground up.  The main requirements were high performance, redundancy, scalability, and availability.  A critical part of the project was ensuring secure connectivity to their Microsoft Azure cloud resources, which are core to their business functions\.

 My goal was to design and configure a network that not only met these technical demands but was also well-organized and easy to manage, following best practices.

## My Approach & Key Features

 I decided to build the network using a **hierarchical model** to ensure it was redundant and scalable. This separates the network into core, distribution, and access layers, which makes it much easier to troubleshoot and expand.

Here are some of the key decisions and features I implemented:

* **Security First:** Security was the top priority.
    *  I placed a **Cisco ASA Firewall** at the edge to manage traffic between the internal network, the internet, and a dedicated DMZ for the company's servers.  The DMZ hosts the internally hosted ERP system, Email server, and File server.
    *  On the switches, I enabled **STP PortFast** on access ports for faster device connectivity and **BPDU Guard** to prevent unauthorized switches from being added to the network.
    *  I wrote a standard **ACL to lock down SSH access**, so only the ICT department can manage devices remotely.

* **Building for Reliability and Speed:**
    *  I segmented the network using **VLANs** to keep traffic for LAN (VLAN 50), WLAN (VLAN 60), and Voice (VLAN 101) separate. This improves both security and performance.
    *  To boost performance and add redundancy between my switches, I configured **LACP EtherChannel**, which bundles multiple links into one logical connection.
    *  I used **OSPF** as the dynamic routing protocol to ensure that all parts of the network could find the best path to communicate with each other automatically.

* **Unified Communications & Services:**
    *  The design includes a full **VoIP system**, with a Cisco Voice Gateway providing telephony services to IP phones in each department.
    *  I set up a **centralized wireless network** using a Cisco Wireless LAN Controller (WLC) to manage all the access points, providing seamless Wi-Fi across both floors.
    *  A central Windows Server 2022 handles **Active Directory, DNS, and DHCP**, so devices can get an IP address automatically , while servers in the DMZ have **static IPs**.

## Network Topology

![Network Topology Diagram](screenshot1.png)
![part 1](screenshot2.png)
![part 2](screenshot3.png)



### IP Addressing Plan

 This was the IP address scheme I was given for the project:
*  **WLAN:** `10.20.0.0/16` 
*  **LAN:** `192.168.10.0/24` 
*  **Voice:** `172.16.10.0/24` 
*  **DMZ:** `10.10.10.0/28` 
*  **Public:** `197.200.100.0` 

### Core Technologies Used

*  **Simulation Tool:** Cisco Packet Tracer 
*  **Key Hardware (Simulated):** Cisco ASA 5525-X Firewall , Catalyst 3850 & 2960 Switches  , Cisco 2811 Voice Gateway  , Cisco WLC, and Lightweight APs.
*  **Protocols & Concepts:** OSPF , LACP EtherChannel, STP (PortFast, BPDU Guard) , VLANs , Inter-VLAN Routing , DHCP , VoIP , Standard ACLs , Firewall Security Zones.
