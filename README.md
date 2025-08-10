# Enterprise-Network-Setup-CISCO
Designed and configured enterprise network with cisco switches and routers. Used pc endpoints to ensure undisrupted network access and internal network framework. 

Project Overview

This project simulates a enterprise business network where different departments, such as IT, HR, and Finance, are kept separate on their own virtual networks called **VLANs**. The primary goal is to **segment network traffic** to improve security and efficiency. Even though the departments are on separate networks, they still need to communicate with each other. This is accomplished using a technique called **inter-VLAN routing**.

A single router is used to route traffic between the VLANs, a method known as **"Router-on-a-Stick"**. The network also uses **DHCP** to automatically assign IP addresses to devices, which simplifies administration.

* **VLAN (Virtual Local Area Network):** Think of a VLAN as a virtual switch within a physical switch. It allows you to logically group devices together, regardless of their physical location. All devices in the same VLAN can communicate as if they were on the same physical network, while being completely isolated from devices in other VLANs. This segmentation prevents unauthorized access to sensitive data and reduces network broadcast traffic.

* **Trunk Port:** A trunk port is a special type of switch port that can carry traffic for multiple VLANs simultaneously. These ports are essential for connecting switches to each other and for connecting a switch to a router that handles inter-VLAN routing. They use a tagging protocol (like 802.1Q) to identify which VLAN each data packet belongs to.

* **Router-on-a-Stick:** This is an efficient and cost-effective method of performing inter-VLAN routing. Instead of using a separate physical router interface for each VLAN, you use just one physical interface. This single interface is configured with multiple logical subinterfaces, with each subinterface acting as the default gateway for one of the VLANs. The trunk port on the switch connects to this single physical router interface, carrying all the VLAN traffic to be routed.

* **DHCP (Dynamic Host Configuration Protocol):** DHCP is a network protocol that automates the process of assigning IP addresses and other network configurations to devices. In a multi-VLAN environment, you configure a separate DHCP pool for each VLAN. The router, acting as a DHCP server, will automatically give devices the correct IP address for their VLAN, which eliminates the need for manual configuration and reduces the chance of errors.
