Alibaba Cloud  
Apsara Stack  
cloud gateway  
Product Introduction  
Product Version: V3.18.6  
Document Version: 20260310

**Table of Contents**

- [1.Cloud Gateway](#section-1)
- [2.Service description](#section-2)
- [3.Benefits](#section-3)
- [4.Functions and features](#section-4)

<a id="section-1"></a>

# 1.Cloud Gateway

Cloud Gateway (CGW) is designed to provide scenario-specific network services to help you efficiently build hybrid clouds and migrate workloads to the clouds. CGW is an ideal service for migrating your infrastructure from a public or private cloud to a hybrid cloud.

<a id="section-2"></a>

# 2.Service description

Cloud Gateway (CGW) provides scenario-specific network access services to help enterprises efficiently build hybrid clouds and migrate workloads to clouds.

**ONSP**

**Capabilities**

- Allows you to create and delete service clusters.

- Allows you to manage resources.

- Allows you to route network traffic from VPCs to service clusters.

**Supported services**

- Load balancing: allows you to configure load balancing services of ecosystem partners, such as F5 load balancers, Sangfor Technologies load balancers, and Radware load balancers, for VPCs.

- Virtual firewalls: allows you to protect traffic between VPCs and traffic between a data center and a VPC and enable address translation. Hillstone firewalls are supported.

- Network performance monitoring (NPM): allows you to collect and analyze network traffic by using third-party services, such as DeepFlow provided by Yunshan Networks and Network Performance Management (NPM) provided by Netis.

<a id="section-3"></a>

# 3.Benefits

Cloud Gateway (CGW) provides you with comprehensive, efficient, secure, easy-to-use, and visual network services.

**ONSP**

ONSP allows you to connect to, deploy, and manage network elements from ecological partners.

- Automatic deployment: Virtual network elements from ecological partners can be automatically deployed by using standard procedures and models.

- High reliability: Virtual network elements can be deployed in active/standby clusters, which support automatic switchover for network traffic.

- Centralized management: Virtual network elements can be deployed in an exclusive VPC. You can centrally manage the virtual network elements at a low cost.

<a id="section-4"></a>

# 4.Functions and features

Cloud Gateway (CGW) provides scenario-specific networking services to help enterprises efficiently build hybrid clouds and migrate workloads to clouds. This topic describes the functions and features of CGW.

**Hybrid cloud network - Platform**

**Feature**

**Description**

Supports DNS forwarding, automated issuance of A records, and an management interface in

Dynamic DNS

hybrid cloud scenarios, improving the efficiency of hybrid cloud networking.

Provides network access to cloud services, configurations of virtual IP addresses (VIPs) and DNS, and mutual access between cloud services in multiple clouds, data centers, and Apsara

Dynamic VIPs

Stack. Supports dynamic VIPs. Both dynamic

Cloud service

and static VIPs are recorded in Apsara

interconnection

Infrastructure Management. This allows the system to flexibly use VIPs to provide external services.

Generates detailed access matrix requirements for cloud instances based on predefined access matrix metadata and rules. This provides

Cross-cloud access

accurate input for cloud service interconnection and helps improve the efficiency of hybrid cloud networking.

Collects and displays information about IP

IP address pools

address pools on Apsara Stack.

Dynamically collects interconnection information of network devices within a single data center on Apsara Stack, and statically adds

Physical topology

interconnection information between devices across data centers or between internal devices in customer data centers.

Hybrid cloud resources

Allows you to manage network devices on

Network element

Apsara Stack and those in customer data

management

centers (with limited support).

<table>
  <tr>
    <td rowspan="3">North-south security protection policies</td>
    <td>Security protection policies (north-south)</td>
    <td>Maintains north-south security protection policies for cloud platforms, including system-generated default policies and manually added policies. You can also use the hardware firewalls deployed by the "default border security" policy to issue and manage security protection policies.</td>
  </tr>
  <tr>
    <td>NAT management</td>
    <td>Allows you to manage the network address translation (NAT) capabilities of cloud platforms for outbound access from the classic network to environments outside Apsara Stack, and supports address pool management and NAT policy management.</td>
  </tr>
  <tr>
    <td>Boundary firewall management</td>
    <td>Allows you to manage hardware firewalls deployed by the "default border security" policy, and supports password-free logon redirection to the native management interface of the firewalls.</td>
  </tr>
</table>

**Network open platform**

**Feature**

**Description**

Provides network functions virtualization (NFV)-based network service lifecycle management

Network element lifecycle

capabilities for ecosystem partners based on

management

Open Network Service Platform (ONSP) in hybrid cloud scenarios.

Basic features

Enables east-west traffic, as well as part of

Traffic redirection

north-south traffic, to be redirected by ONSP to

management

third-party network elements for processing.

Integrates with CloudMonitor to report abnormal

Monitoring by

status alerts of asynchronous tasks and network

CloudMonitor

elements to CloudMonitor.

O&M monitoring capabilities

Integrates with TianjiMon to report alerts of

Monitoring by TianjiMon

ONSP to TianjiMon.

Allows network element administrators to share

Network element sharing

network elements with other tenants.

Supports multiple tenants, each managing their

Multi-tenancy

own network elements.

Supports Elastic Compute Service (ECS)

ECS specification filtering

specification filtering.

Advanced features

Dynamic refresh of virtual

Supports dynamic refresh of VPC IDs and

private cloud (VPC) IDs

vSwitch names.

and vSwitch names

Bypass with a few clicks

Supports bypass with a few clicks.

Multi-VPC security

Supports security protection across multiple

protection

VPCs.

Intel

Supports Intel chip architecture.

Hygon

Supports Hygon chip architecture.

Domestically innovative architectures

Kunpeng

Supports Kunpeng chip architecture.

Phytium

Supports Phytium chip architecture.

**Bare metal network**

**Feature**

**Description**

Supports attachment of bare metal instances to the backend of internal-facing Server Load

Service reliability

Balancer (SLB) instances that can be accessed from a VPC.

Allows customers to access bare metal instances from office networks or legacy data centers by using leased lines (the VPC to be

Bare metal service

connected to by using a leased line must be the

deployment and

same as that in which the required bare metal

operations

instance resides). Allows customers to log on to bare metal instances by using ECS. (the ECS instance to use and the bare metal instance to log on to must reside in the same VPC).

Supports applications for and release of bare metal instances in VPCs, communication between bare metal instances in the same VPC

Connection of bare metal

and different vSwitches, communication

instances to VPCs

between bare metal instances and ECS instances in the same VPC, and communication

Basic features

between bare metal instances in different VPCs.

Supports access from bare metal instances to

Access from bare metal

OPS-DNS, Network Time Protocol (NTP) serves,

instances to cloud services

ApsaraDB RDS instances, Object Storage Service (OSS), and File Storage NAS (NAS).

Supports access from bare metal instances to

Access from bare metal

the Internet by using SNAT entries of NAT

instances to the Internet

gateways.

Supports attachment of bare metal instances to the backend of Internet-facing SLB instances,

Public access to bare

and supports public access to bare metal

metal instances

instances by using DNAT entries of NAT gateways to map specified bare metal IP addresses.

Supports the management of a group of hybrid

License-based

Authorization

switches (HSWs) for each license and allows

authorization

management

access for up to 48 NIC bare metal instances

management

with two network interface controllers (NICs).

Supports 10 GE servers, which require port

10 GE optical port

aggregation based on Link Aggregation Control Protocol (LACP).

Bare metal port types

Supports 10 GE or 25 GE servers, which require

25 GE optical port

port aggregation based on LACP.

Zone-disaster recovery with dual data centers

Deployment modes

Multi-region deployment (unit-based deployment)

Supports de-stacking architecture on HSWs

De-stacking

managed by bare metal instances.

**Topology visualization for cloud networking services**

**Feature**

**Description**

VPC topology

Subnet information within

Displays information about ECS instances within

a VPC

a subnet.

Display of a

NAT gateway information

Displays NAT gateway information within a VPC.

specified VPC topology

Express Connect

Displays VPC peering connection information.

information within a VPC

Obtaining VPC topology

Allows you to obtain information about a VPC

information by calling API

topology by calling API operations.

operations

VPC peering

Displays the quantity and supports redirection.

VBR uplink

Displays the quantity and supports redirection.

NAT gateways

Displays the quantity and supports redirection.

Displays the quantity of Internet-facing SLB

Internet-facing SLB

instances to which ECS instances that reside in

instances

the current VPC are attached.

Display of areas outside a VPC

Displays the quantity of EIPs with which ECS

EIPs

instances that reside in the current VPC are associated.

Displays the quantity of VPN gateways

VPN gateways

associated with the current VPC.

Displays the quantity of IPv6 gateways of the

IPv6 gateways

current VPC.

Visualization of VPC

Display of VPCs

topologies and selection of VPCs

Route table IDs

Displays route table IDs.

Display of routers

Route table names

Displays route table names.

Router IDs

Displays router IDs.

Display of all

All routers

Displays all routers in a list.

routers

<table>
  <tr>
    <td rowspan="5">Display of vSwitches</td>
    <td>vSwitch IDs</td>
    <td>Displays vSwitch IDs.</td>
  </tr>
  <tr>
    <td>vSwitch names</td>
    <td>Displays vSwitch names.</td>
  </tr>
  <tr>
    <td>Zones of vSwitches</td>
    <td>Displays the zones of vSwitches.</td>
  </tr>
  <tr>
    <td>IPv4 CIDR blocks of vSwitches</td>
    <td>Displays the IPv4 CIDR blocks of vSwitches.</td>
  </tr>
  <tr>
    <td>IPv6 CIDR blocks of vSwitches</td>
    <td>Displays the IPv6 CIDR blocks of vSwitches.</td>
  </tr>
  <tr>
    <td rowspan="4">Display of cloud resources under vSwitches.</td>
    <td>ECS instances</td>
    <td>Displays the quantity and supports redirection.</td>
  </tr>
  <tr>
    <td>ApsaraDB RDS instances</td>
    <td>Displays the quantity and supports redirection.</td>
  </tr>
  <tr>
    <td>Internal-facing SLB instances</td>
    <td>Displays the quantity and supports redirection.</td>
  </tr>
  <tr>
    <td>All vSwitches</td>
    <td>Displays all vSwitches in a list.</td>
  </tr>
</table>

**Traffic visualization for hybrid cloud network**

**Feature**

**Description**

Supports traffic ranking and displays the top N

Traffic trends

applications.

Displays type distributions of the top N applications, the number of application types,

Traffic analysis

Traffic analysis

average traffic size, and total traffic size.

Supports vSwitch port mirroring, which

Supported data sources

indicates traffic mirroring in both ingress and egress directions of vSwitch ports.

Allows you to lower the traffic priority of low-

Emergency scheduled

priority, high-bandwidth applications to ensure

Traffic scheduling

traffic shifting for zone-

bandwidth for high-priority applications (Apsara

disaster recovery

Stack V3.17 supports only ODPS).

Analyzer adding

Allows you to add a traffic analyzer.

Analyzer modification

Allows you to modify a traffic analyzer.

Analyzer removal

Allows you to remove a traffic analyzer.

Analyzer viewing

Allows you to view a traffic analyzer.

Analyzer

Allows you to add an analysis port for an

Analysis port adding

management

analyzer.

Allows you to modify an analysis port for an analyzer.

Analysis port modification

Allows you to remove an analysis port from an

Analysis port removal

analyzer.

Allows you to view an analysis port of an

Analysis port viewing

analyzer.

Rule creation

Allows you to create a traffic analysis rule.

Rule modification

Allows you to modify a traffic analysis rule.

Rule management

Rule deletion

Allows you to delete a traffic analysis rule.

Rule viewing

Allows you to view a traffic analysis rule.

Scenario creation

Allows you to create a traffic analysis scenario.

Scenario modification

Allows you to modify a traffic analysis scenario.

Scenario management

Scenario deletion

Allows you to delete a traffic analysis scenario.

Scenario viewing

Allows you to view a traffic analysis scenario.

Multi-data center

Multi-zone deployment for

deployment

traffic visualization

Network asset analysis for

Network assets

traffic visualization

<table>
  <tr>
    <td>Security integration</td>
    <td>Integration with Galaxy Security Gateway for traffic visualization</td>
    <td>Supports data export to third-party platforms.</td>
  </tr>
</table>
