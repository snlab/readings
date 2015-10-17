It is can be a bit hard to get started to fully understand the AP processing at a network switch. One possibility is to consider each packet as a function call, with parameters in the packet headers. 

You can start with L2 only. In this case, the packet will be an Ethernet Frame:
https://en.wikipedia.org/wiki/Ethernet_frame

A key demultiplexer is the Ether Type field:
https://en.wikipedia.org/wiki/EtherType

The main types of Ethernet packets are 
- IPv4 (EtherType:0x0800), 
- IPv6:0x0x86DD, ARP:0x0806, 
- basic VLAN (802.11A):0x8100,
- provider bridging (also called stacked VLANs, QinQ):0x88A8, 
- MPLS unicast:0x8847, 
- MPLS multicast:0x8848, 
- PPPoE (your dial up), and 
- LLDP:0x88CC (for topology discovery). 

IPv4 and IPv6 are better known.

* VLAN has increasing importance. Please read basic VLAN 802.11Q (https://en.wikipedia.org/wiki/IEEE_802.1Q). To allow service provider VLAN tagging and user tagging, we have double tagging 802.11ad (see the same proceeding link). It also helps a lot if you understand shortest path bridging (https://en.wikipedia.org/wiki/IEEE_802.1aq).

* Another important technique is MPLS (https://en.wikipedia.org/wiki/Multiprotocol_Label_Switching). See the proceeding link for MPLS format.

