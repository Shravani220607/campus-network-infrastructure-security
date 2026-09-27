Campus Network Infrastructure and Security Architecture

Designed and implemented a scalable enterprise-style campus network in Cisco Packet Tracer featuring segmented departmental networks, centralized Layer 3 routing, dynamic routing, secure management, access control enforcement, and core network services.






Overview

Modern campus environments require network segmentation, centralized management, secure access controls, and reliable service delivery across multiple departments.

This project simulates the design and deployment of a campus-scale network supporting:

Administrative Operations
Faculty Resources
Student Access Networks
Guest Connectivity
Centralized Server Infrastructure
Network Management Services

The architecture follows enterprise networking principles by combining Layer 2 switching, Layer 3 routing, dynamic route exchange, centralized services, and multiple security controls into a unified network infrastructure.

Architecture Highlights
Network Segmentation

The campus network is divided into dedicated VLANs to reduce broadcast domains, improve security, and simplify administration.

VLAN	Purpose	Subnet
10	Administration	10.0.10.0/24
20	Faculty	10.0.20.0/24
30	Student	10.0.30.0/24
40	Server Farm	10.0.40.0/24
50	Guest Network	10.0.50.0/24
99	Management	10.0.99.0/24
Core Infrastructure

The network is built around a Layer 3 core switch responsible for:

Inter-VLAN Routing
Centralized Gateway Services
ACL Enforcement
DHCP Relay Operations
OSPF Route Advertisement

Additional infrastructure components include:

Core Layer 3 Switch
Distribution Access Switches
Edge Router
Upstream Router
DHCP Server
DNS Server
Internal Web Server
Technical Implementation
Layer 2 Technologies
VLAN Segmentation

Implemented departmental isolation through VLAN-based segmentation to separate administrative, faculty, student, guest, server, and management traffic.

802.1Q Trunking

Configured trunk links between switches to transport multiple VLANs across the campus backbone while maintaining VLAN separation.

Spanning Tree Protocol (STP)

Implemented STP to eliminate Layer 2 switching loops and maintain a stable, loop-free topology.

Layer 3 Technologies
Inter-VLAN Routing

Configured Switch Virtual Interfaces (SVIs) on the Layer 3 core switch to provide routing services between VLANs.

OSPF Dynamic Routing

Implemented OSPF for dynamic route exchange between Layer 3 devices, enabling automated route propagation and scalable network growth.

Network Services
DHCP

Centralized DHCP infrastructure dynamically assigns IP addresses to client devices across multiple VLANs.

DHCP Relay

DHCP requests are forwarded across routed boundaries using helper addresses, enabling centralized address management.

DNS

Internal DNS services provide hostname resolution for campus resources.

Example:

www.campus.local
Web Services

An internal web server hosts campus resources and demonstrates application availability across segmented networks.

Security Architecture

Security was implemented using a defense-in-depth approach.

Access Control Lists (ACLs)

Extended ACLs were deployed to enforce inter-department communication policies.

Examples include:

Restricting Guest VLAN access to internal networks.
Restricting Student VLAN access to administrative resources.
Protecting critical infrastructure services.
Secure Device Management

SSH Version 2 was configured for encrypted remote administration.

Features include:

RSA Key Infrastructure
Local Authentication
Secure Remote Access
Port Security

Port Security was implemented on access ports to prevent unauthorized endpoint connections.

Features:

Sticky MAC Learning
MAC Address Limitation
Violation Detection
Unauthorized Device Mitigation
Validation and Testing

Comprehensive testing was performed throughout deployment.

Connectivity Validation
Inter-VLAN communication testing
Gateway reachability testing
End-to-end path verification
Service Validation
DHCP lease allocation
DNS name resolution
Web application accessibility
Security Validation
ACL policy verification
Port Security violation testing
SSH authentication testing
Routing Validation
OSPF neighbor establishment
Dynamic route propagation
Routing table verification
Key Technologies
Networking
VLANs
802.1Q Trunking
Layer 3 Switching
Inter-VLAN Routing
OSPF
Security
ACLs
SSH
Port Security
Traffic Segmentation
Services
DHCP
DHCP Relay
DNS
Web Services
Operations
Network Validation
Monitoring
Troubleshooting
Connectivity Analysis
Project Deliverables
campus-network-infrastructure-security
│
├── Campus_Network_Project.pkt
├── README.md
├── topology/
├── screenshots/
└── configs/
Future Enhancements

Planned improvements include:

NAT/PAT
EtherChannel
HSRP Gateway Redundancy
Syslog Integration
NTP Synchronization
Network Monitoring Infrastructure
Results

Successfully designed and deployed a segmented campus network capable of supporting multiple departments, centralized services, dynamic routing, and layered security controls while maintaining scalability, manageability, and operational reliability.