# Cairo Telco: A Secure Enterprise Network Simulation

Welcome to my Cairo Telco network project! [cite_start]This is a comprehensive simulation I built in Cisco Packet Tracer to design and implement a secure, scalable, and robust network for a growing company[cite: 25, 27, 32].

## The Challenge

[cite_start]The scenario involves a fictional company, Cairo Telco, a fast-growing telecommunication company in Cairo, Egypt[cite: 5, 6]. [cite_start]The company occupies the fourth and fifth floors of a building, hosting six different departments: HR and Finance, Product Brand and Marketing, Admin and Corporate, IT Network & Support, Software Engineering, and Cloud Engineering[cite: 7, 8, 9, 10].

They needed a complete network infrastructure from the ground up. [cite_start]The main requirements were high performance, redundancy, scalability, and availability[cite: 29]. [cite_start]A critical part of the project was ensuring secure connectivity to their Microsoft Azure cloud resources, which are core to their business functions[cite: 20, 21, 22].

[cite_start]My goal was to design and configure a network that not only met these technical demands but was also well-organized and easy to manage, following best practices[cite: 26].

## My Approach & Key Features

[cite_start]I decided to build the network using a **hierarchical model** to ensure it was redundant and scalable[cite: 33]. This separates the network into core, distribution, and access layers, which makes it much easier to troubleshoot and expand.

Here are some of the key decisions and features I implemented:

* **Security First:** Security was the top priority.
    * [cite_start]I placed a **Cisco ASA Firewall** at the edge to manage traffic between the internal network, the internet, and a dedicated DMZ for the company's servers[cite: 24, 52]. [cite_start]The DMZ hosts the internally hosted ERP system, Email server, and File server[cite: 16, 17].
    * [cite_start]On the switches, I enabled **STP PortFast** on access ports for faster device connectivity and **BPDU Guard** to prevent unauthorized switches from being added to the network[cite: 39, 56].
    * [cite_start]I wrote a standard **ACL to lock down SSH access**, so only the ICT department can manage devices remotely[cite: 51].

* **Building for Reliability and Speed:**
    * [cite_start]I segmented the network using **VLANs** to keep traffic for LAN (VLAN 50), WLAN (VLAN 60), and Voice (VLAN 101) separate[cite: 23, 37, 55]. This improves both security and performance.
    * [cite_start]To boost performance and add redundancy between my switches, I configured **LACP EtherChannel**, which bundles multiple links into one logical connection[cite: 38, 56].
    * [cite_start]I used **OSPF** as the dynamic routing protocol to ensure that all parts of the network could find the best path to communicate with each other automatically[cite: 50, 58].

* **Unified Communications & Services:**
    * [cite_start]The design includes a full **VoIP system**, with a Cisco Voice Gateway providing telephony services to IP phones in each department[cite: 17, 18, 36, 49].
    * [cite_start]I set up a **centralized wireless network** using a Cisco Wireless LAN Controller (WLC) to manage all the access points, providing seamless Wi-Fi across both floors[cite: 18, 19, 35].
    * [cite_start]A central Windows Server 2022 handles **Active Directory, DNS, and DHCP**, so devices can get an IP address automatically [cite: 14, 15, 16, 45][cite_start], while servers in the DMZ have **static IPs**[cite: 47, 57].

## Network Topology

Here's a visual look at the final network design. For this image to display correctly on GitHub, ensure `image_2d2edf.png` is in the same repository.

![Network Topology Diagram](image_2d2edf.png)

### IP Addressing Plan

[cite_start]This was the IP address scheme I was given for the project[cite: 30]:
* [cite_start]**WLAN:** `10.20.0.0/16` [cite: 30]
* [cite_start]**LAN:** `192.168.10.0/24` [cite: 30]
* [cite_start]**Voice:** `172.16.10.0/24` [cite: 30]
* [cite_start]**DMZ:** `10.10.10.0/28` [cite: 30]
* [cite_start]**Public:** `197.200.100.0` [cite: 30]

### Core Technologies Used

* [cite_start]**Simulation Tool:** Cisco Packet Tracer [cite: 32]
* [cite_start]**Key Hardware (Simulated):** Cisco ASA 5525-X Firewall [cite: 12][cite_start], Catalyst 3850 & 2960 Switches [cite: 12, 13][cite_start], Cisco 2811 Voice Gateway [cite: 46][cite_start], Cisco WLC, and Lightweight APs[cite: 14].
* [cite_start]**Protocols & Concepts:** OSPF [cite: 50][cite_start], LACP EtherChannel [cite: 38][cite_start], STP (PortFast, BPDU Guard) [cite: 39][cite_start], VLANs [cite: 37][cite_start], Inter-VLAN Routing [cite: 42][cite_start], DHCP [cite: 45][cite_start], VoIP [cite: 36][cite_start], Standard ACLs [cite: 51][cite_start], Firewall Security Zones[cite: 52].
