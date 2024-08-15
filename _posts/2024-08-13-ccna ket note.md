---
title: 'CCNA Key points'
date: 2024-08-13
permalink: /posts/2024/08/CCNA_noted/
tags:
  - CCNA
  - Key points
---
expired - 24/08/19

## Routing
Back_up_route = default_gateway

## CDP
```
#cdp run //global
#cdp enable // interface

#sh cdp nei de //ip 볼수있음
#sh cdp nei //간략
```
cdp(cisco) vs lldp(multibender)
## AAA

-Autehntication
validation , verifies
verifies acess rights
validates user credentials
secures access to routers
identify and  verifies a user who

-Authorization
It grants access to network asset such as FTP servers
It restricts the CLI commands that a user is able to perform
limits the user's access permissions
allows the user to change to enable mode
tasks the user can perform

-Accounting
track activity
records user commands
log session statistics
track user service

-CoA
updates session attributes

## TCP/IP
L2
802.1X, WPA+WPA2
L3
web policy,Passthrough


## Controller-Based NET
north bound(aplication REST) & south bound(edge device) APIs
configured using the physical infrastucture
leverages controllers to handle network meangement
centralized view of the network
multiple device
task automation <- limit recurrent managemnet cost <- software upgrade(in deploy)
increased scalability and managemnet options
better control over, reduce complexity
centralization of key 
setting packet-handling policies


## vs Traditional NET
distributed control plane
distributed management plane
resources from a centralized location
implements changes individually at each device
Maintenance costs are higher than with networking options
increased error

## TCP

## UDP

## collasped Core
single, cost-effective, small net

## Three-Tire
enhances, separate

## DHCP snooping
trust - internal
untrusted - default state all int
spurious dhcp serv - unknown dhcp serv
dhcp serv - propagates ip
snooping binding DB - list of hosts in unknown domain

## northbound 
1 - auto
2 - aplication
3 - data sharing
4 - REST

## HSRP
Active - forward
Learn - heard neighbor & receive hello
Listen - waiting
Speak - transmit & receive hello
Standy - ready to forward if fails
first hop redundancy(default gateway failure) - share virtual MAC & IP
two router - active to standby / share virtual IP


## FHRP
auto faliover default gateway
multi device -> single virtual IP

## cisco DNA Center DevM
cloud, NetFlow, multiple
Centralized
APIS
deploy a network faster(diff)

## vs Traditional DevM
SSH, per-device, (firewall. VPN, IPS)

## Link-Local
conf only one, single subnet

## Unique Local
prefix FC00:7, internally without internet

## Ansible
SSH,YAML, push config , operating without agent

## attack-mitigation
802.1q double_tagging Vlan_hopping attac - conf native Vlan(expect default)
MAC flooding attack - conf 802.x auth
man in the middle - conf DHCP snooping
switch_spoofing VLAN_hopping attack - disable DTP

## role of the root port in a swithch
best path to non root 

## WPA2-PSK
ASCII(minimun - 8) hex
PSK - personal 

## RADIUS
merge auth
access-request packet <-> password

## TACAS+
separates authentication and authonzation

## OSPF
hello 10 dead 40 (default)
broadcast (if p2p no advertise)
router ID - select highest ID (if has lookback <- highest)
bandwidth(metric)

## WLC(Wireless Lan Control)
AAA override allow(VLAN) <-data path
CAPWAP(light weight - management,roaming,SSID)
LAG - link redundancy & load balancing 
man in the middle - telnet


## query-response model
TCP - establish
UDP - immdiately

## AD value
Connected interface	0C
Static route	1
Enhanced Interior Gateway Routing Protocol (EIGRP) summary route	5
Internal EIGRP	90
IGRP	100
OSPF	110
Intermediate System-to-Intermediate System (IS-IS)	115
Routing Information Protocol (RIP)	120

## ip route
Codes: L - local,  - connected, S - static, R - RIP
       D - EIGRP, EX - EIGRP external, O - OSPF, IA - OSPF inter area 
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2, i - IS-IS

# port security
SNMP trap - restrict

# Qos
congestion - PQ,CVWFQ
low-latency - voice & video
exceed commit - policing
MAX bandwidth - traffic shaping

# inspection
address binding

# SNMP
MIB NMS 
UDP aplication layer

# Ansible
Playbook, Task
TCP 22

# TFTP
firmware upgrade

# IEEE 802
802.11 - response via Management

# late collision
transmit frame same time, cable length limit exceed, one half duplex(duplex missmating)

# VPN
IPSEC site to site - tunnel ESP
GRE<- muticast traffic + IPSEC(encrpt)

# SSH
ip (Domain_Name) (domain) <-before RSA
K9(crypto)

# WLAN
profile name, SSID

# datacenter 
security - phsical access control

# virtual machine
prepare <- resource, CPU, memory limit

# flex
disconnect WLAN - flexconnect

# lose smart phone
PIN <- before second factor

# what is reason...
the cable connection betwwen the two devices is faulty.

# portfast
STP - learning, listenling, broadcast storm

# trouble shooting
err_disabled - link flapping

# Random Early Detection 
mitigate congestion by preventing  the queue from filing up
drops lower-priority packets before it drops higher-priority packets

# Privacy
malicious code allow access by an unauthorized user
multifactor - authentication app

# cable
SFP - Hot swap

# virtu

# Zeroday exploit
new net vulnerability discover before fix it