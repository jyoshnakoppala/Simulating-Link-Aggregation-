# Simulating-Link-Aggregation-
Implementation of Link Aggregation using various protocols such as LACP, PAgP and EtherChannel(manual) in Cisco Packet Tracer

A link aggregation group (LAG) is the combined collection of physical ports.
Other umbrella terms used to describe the concept include trunking,
bundling, bonding, channelling or teaming. Link aggregation increases the
bandwidth and resilience of Ethernet connections. Using EtherChannel,
LACP and PAgP we will show how link aggregation works.


EtherChannel is a technology that was originally developed by Cisco as a
LAN switch-to-switch technique of grouping several Fast or Gigabit Ethernet
ports into one logical channel and redundancy without being blocked by the
Spanning Tree Protocol. EtherChannel configuration has one mode known
as the On mode.
  • On mode forces the connection to bring all links up without using a
protocol to negotiate connections. This mode can only connect to
another device that is also set to on. When using this mode, the
switch does not negotiate the link using either PAgP or LACP.

LACP
Link Aggregation Control Protocol (LACP) is part of an IEEE specification
(802.3ad) that allows several physical ports to be bundled together to form
a single logical channel. LACP allows a switch to negotiate an automatic
bundle by sending LACP packets to the peer. LACP has 2 modes Active and
Passive.
  • Active mode sets the interface to actively attempt to negotiate
connections with other LACP devices.
  • Passive mode sets the interface to respond to LACP data if it
receives negotiation requests from other systems.


PAgP
Port Aggregation Protocol (PAgP) provides the same negotiation benefits as
LACP. PAgP is a Cisco proprietary protocol, and it will work only on Cisco
devices. PAgP packets are exchanged between switches over EtherChannelcapable ports. PAgP also has 2 modes Auto and Desirable.
  • Auto mode sets the interface to respond to PAgP negotiation
packets, but the interface will not start negotiations on its own.
  • Desirable mode sets the interface to actively attempt to negotiate a
PAgP connection.


Link Aggregation has many benefits:
Increased Bandwidth: Use EtherChannel and combine two or four links into
one logical link. It will double or quadruple your bandwidth. For example,
four 100Mb Fast Ethernet connections bonded into one could provide you
up to 800Mb/second, full duplex.
Provides Redundancy: Since there are many Ethernet links combined into
one logical channel, it automatically allows more available links in case one
or more links go down.
Load Balance Traffic: EtherChannel balances the traffic load across the
links, thereby increasing efficiency on your networks.


To design the project, we used the following steps:

1. Take 3 switches and 6 PCs
2. Connect PC0 and PC1 to Switch S1and similarly connect PC2 and
PC3 to Switch S2 andPC4 and PC5 to S3.
3. Configure VLANs such that PC0, PC2, PC4 belong to VLAN 10 and
PC1, PC3, PC5 belong to VLAN 20.
4. Connect the cables for S1 and S2 by connect the correct respective
ports (g0/1 of S1 to g0/1 of S2 and so on).
5. After this configure LACP by setting Active mode on S1 and Passive
mode on S2.
6. Connect the cables for S2 and S3 by connect the correct respective
ports (f0/21 of S2 to f0/21 of S3 and so on).
7. After this configure PAgP by setting Auto mode on S2 and Desirable
mode on S3.
8. Connect the cables for S1 and S3 by connect the correct respective
ports (f0/17 of S2 to f0/17 of S3 and so on).
9. After this configure EtherChannel by setting On mode for both S1
and S3.

