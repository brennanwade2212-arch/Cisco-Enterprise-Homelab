# Cisco-Enterprise-Homelab

Overview

This repository documents my physical Cisco networking home lab built to gain hands-on experience with enterprise networking, wireless infrastructure, network segmentation, and troubleshooting.

The lab uses a Cisco Catalyst 3850 switch, Cisco 2504 Wireless LAN Controller, four Cisco Aironet 2802 access points, and a TP-Link ER605 router.

I designed and configured the network from the ground up, including VLANs, 802.1Q trunking, DHCP, multiple wireless networks, firewall policies, and network segmentation.

I am CompTIA A+ certified and currently studying for the Cisco CCNA. This lab allows me to apply networking concepts to physical equipment rather than relying only on simulations.

⸻

Network Topology

Network topology diagram coming soon.

The TP-Link ER605 connects to the Cisco Catalyst 3850 using an 802.1Q trunk carrying VLANs 10, 20, 30, and 99.

The Catalyst 3850 provides connectivity to the Cisco 2504 Wireless LAN Controller and four Cisco Aironet 2802 lightweight access points.

⸻

Hardware

Device	Role
TP-Link ER605	Router, DHCP, inter-VLAN routing, and firewall
Cisco Catalyst 3850	Core switch and VLAN trunking
Cisco 2504 WLC	Centralized wireless management
4x Cisco Aironet 2802	Wireless access points

⸻

VLAN & IP Addressing

I divided the network into four VLANs to separate devices based on their purpose.

VLAN	Name	Network	Gateway
- 10	Main-Network	192.168.10.0/24	192.168.10.1
- 20	Guest-Network	192.168.20.0/24	192.168.20.1
- 30	IoT-Network	192.168.30.0/24	192.168.30.1
- 99	Management	192.168.99.0/24	192.168.99.1

The TP-Link ER605 serves as the default gateway for each subnet and handles routing and firewall policies between VLANs.

⸻

## Wireless Networks

The Cisco 2504 WLC centrally manages the wireless network and the four Cisco Aironet 2802 access points.

Each wireless network is mapped to its designated VLAN:

SSID	VLAN	Purpose
- Elam-Main	VLAN 10	Trusted devices
- Elam-Guest	VLAN 20	Guest devices
- IOT-Network	VLAN 30	IoT devices
- Management	VLAN 99	Management network

This design allows wireless devices to be separated into different network segments based on the SSID they connect to.

⸻

Network Segmentation

The network is segmented to separate trusted, guest, IoT, and management traffic.

The TP-Link ER605 handles inter-VLAN routing and firewall policies that control communication between the networks.

This allows me to maintain separate network environments while still providing the connectivity required for each type of device.

⸻

DHCP & AP Discovery

The TP-Link ER605 provides DHCP services for each VLAN.

I also configured DHCP Option 43 to assist the Cisco Aironet lightweight access points with discovering the Cisco 2504 Wireless LAN Controller.

⸻

Troubleshooting

Building the lab required troubleshooting several real networking issues, including:

* VLAN tagging and trunk configuration
* Native VLAN configuration
* DHCP connectivity
* Default gateway connectivity
* Inter-VLAN communication
* WLC management connectivity
* Lightweight AP discovery
* DHCP Option 43
* SSID-to-VLAN mapping

One issue involved losing access to the Cisco 2504 WLC management interface after changing VLAN and trunk configurations. Troubleshooting the native VLAN and switch port configuration allowed me to restore management connectivity.

I also troubleshot Cisco Aironet access points that were receiving DHCP addresses but were not successfully discovering the WLC. This required working through DHCP, Option 43, VLAN configuration, switch port configuration, and controller connectivity.

⸻

Skills Demonstrated

* Cisco IOS
* Cisco Catalyst switching
* VLAN configuration
* 802.1Q trunking
* Access and trunk ports
* IPv4 addressing and subnetting
* DHCP
* DHCP Option 43
* Cisco Wireless LAN Controllers
* Cisco lightweight access points
* WLAN and SSID configuration
* WLAN-to-VLAN mapping
* Inter-VLAN routing
* Network segmentation
* Firewall policies
* Layer 2 troubleshooting
* Layer 3 troubleshooting
* Network documentation

⸻

Project Documentation

More detailed documentation will be added as the project develops:

* Network topology diagram
* VLAN design
* Wireless design
* Firewall and segmentation design
* Cisco switch configurations
* Troubleshooting documentation
* Homelab photos

⸻

Future Plans

I plan to continue expanding the lab with:

* Additional CCNA labs
* Network monitoring
* Centralized logging
* Proxmox virtualization
* Windows Server and Active Directory
* Network automation
* Additional security configurations

⸻

About Me

I am a Network Administration student, CompTIA A+ certified, and currently studying for the Cisco CCNA.

I built this lab to develop practical experience designing, configuring, troubleshooting, and documenting a physical network environment.