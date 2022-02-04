# EAPI-SPINE2 Commands Output

## Table of Contents

- [show lldp neighbors](#show-lldp-neighbors)
- [show ip interface brief](#show-ip-interface-brief)
- [show interfaces description](#show-interfaces-description)
- [show version](#show-version)
- [show ip bgp summary vrf all](#show-ip-bgp-summary-vrf-all)
- [show bgp evpn summary](#show-bgp-evpn-summary)
- [show bgp evpn](#show-bgp-evpn)
- [show ip route vrf all](#show-ip-route-vrf-all)
- [show vxlan vtep](#show-vxlan-vtep)
- [show vxlan address-table](#show-vxlan-address-table)
- [show vxlan vni](#show-vxlan-vni)
- [show vlan](#show-vlan)
- [show mac address-table](#show-mac-address-table)
- [show bfd peers](#show-bfd-peers)
- [show mlag detail](#show-mlag-detail)
- [show mlag config-sanity](#show-mlag-config-sanity)
- [show system environment cooling](#show-system-environment-cooling)
## show bfd peers

```

```
## show bgp evpn summary

```
BGP summary information for VRF default
Router identifier 192.168.1.2, local AS number 65001
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
```
## show bgp evpn

```
BGP routing table information for VRF default
Router identifier 192.168.1.2, local AS number 65001
Route status codes: s - suppressed, * - valid, > - active, # - not installed, E - ECMP head, e - ECMP
                    S - Stale, c - Contributing to ECMP, b - backup
                    % - Pending BGP convergence
Origin codes: i - IGP, e - EGP, ? - incomplete
AS Path Attributes: Or-ID - Originator ID, C-LST - Cluster List, LL Nexthop - Link Local Nexthop

         Network                Next Hop              Metric  LocPref Weight  Path
```
## show interfaces description

```
Interface                      Status         Protocol           Description
Et1                            up             up                 P2P_LINK_TO_EAPI-LEAF1A_Ethernet2
Et2                            up             up                 P2P_LINK_TO_EAPI-LEAF1B_Ethernet2
Et3                            up             up                 P2P_LINK_TO_EAPI-LEAF2A_Ethernet2
Et4                            up             up                 P2P_LINK_TO_EAPI-LEAF2B_Ethernet2
Et5                            up             up                 P2P_LINK_TO_EAPI-BL01A_Ethernet2
Et6                            up             up                 P2P_LINK_TO_EAPI-BL01B_Ethernet2
Et7                            up             up                 P2P_LINK_TO_EAPI-LEAF3A_Ethernet2
Et8                            up             up                 P2P_LINK_TO_EAPI-LEAF4A_Ethernet2
Et9                            up             up                 P2P_LINK_TO_EAPI-CL01A_Ethernet2
Et10                           up             up                 P2P_LINK_TO_EAPI-CL01B_Ethernet2
Et11                           up             up                 P2P_LINK_TO_EAPI-L2LEAF01_Ethernet2
Et12                           up             up                 P2P_LINK_TO_EAPI-L2LEAF02_Ethernet2
Et13                           up             up                 P2P_LINK_TO_EAPI-RS02_Ethernet1
Et14                           up             up                 
Lo0                            up             up                 EVPN_Overlay_Peering
Ma1                            up             up                 oob_management
```
## show ip bgp summary vrf all

```
BGP summary information for VRF default
Router identifier 192.168.1.2, local AS number 65001
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  EAPI-RS02_Ethernet1      172.31.250.3     4  65000           1284      1291    0    0 18:09:41 Estab   1      1
  EAPI-L2LEAF01_Ethernet2  172.31.251.3     4  65107           4340      4376    0    0    2d12h Estab   2      2
  EAPI-L2LEAF02_Ethernet2  172.31.251.7     4  65108           4330      4343    0    0    1d23h Estab   2      2
  EAPI-LEAF1A_Ethernet2    172.31.255.3     4  65101           4461      4469    0    0    2d13h Estab   3      3
  EAPI-LEAF1B_Ethernet2    172.31.255.7     4  65101           4457      4485    0    0    2d13h Estab   3      3
  EAPI-LEAF2A_Ethernet2    172.31.255.11    4  65102           4450      4486    0    0    2d13h Estab   3      3
  EAPI-LEAF2B_Ethernet2    172.31.255.15    4  65102           4448      4470    0    0    2d13h Estab   3      3
  EAPI-LEAF3A_Ethernet2    172.31.255.19    4  65103           4452      4493    0    0    2d13h Estab   2      2
  EAPI-LEAF4A_Ethernet2    172.31.255.23    4  65104           4452      4483    0    0    2d13h Estab   2      2
  EAPI-BL01A_Ethernet2     172.31.255.27    4  65105           4478      4489    0    0    2d13h Estab   3      3
  EAPI-BL01B_Ethernet2     172.31.255.31    4  65105           4494      4486    0    0    2d13h Estab   3      3
  EAPI-CL01A_Ethernet2     172.31.255.35    4  65106           4360      4369    0    0    2d12h Estab   3      3
  EAPI-CL01B_Ethernet2     172.31.255.39    4  65106           4346      4378    0    0    2d12h Estab   3      3
```
## show ip interface brief

```
Address 
Interface       IP Address           Status     Protocol         MTU    Owner   
--------------- -------------------- ---------- ------------ ---------- ------- 
Ethernet1       172.31.255.2/31      up         up              1500            
Ethernet2       172.31.255.6/31      up         up              1500            
Ethernet3       172.31.255.10/31     up         up              1500            
Ethernet4       172.31.255.14/31     up         up              1500            
Ethernet5       172.31.255.26/31     up         up              1500            
Ethernet6       172.31.255.30/31     up         up              1500            
Ethernet7       172.31.255.18/31     up         up              1500            
Ethernet8       172.31.255.22/31     up         up              1500            
Ethernet9       172.31.255.34/31     up         up              1500            
Ethernet10      172.31.255.38/31     up         up              1500            
Ethernet11      172.31.251.2/31      up         up              1500            
Ethernet12      172.31.251.6/31      up         up              1500            
Ethernet13      172.31.250.2/31      up         up              1500            
Loopback0       192.168.1.2/32       up         up             65535            
Management1     10.73.254.2/24       up         up              1500
```
## show ip route vrf all

```
VRF: default
Codes: C - connected, S - static, K - kernel, 
       O - OSPF, IA - OSPF inter area, E1 - OSPF external type 1,
       E2 - OSPF external type 2, N1 - OSPF NSSA external type 1,
       N2 - OSPF NSSA external type2, B - BGP, B I - iBGP, B E - eBGP,
       R - RIP, I L1 - IS-IS level 1, I L2 - IS-IS level 2,
       O3 - OSPFv3, A B - BGP Aggregate, A O - OSPF Summary,
       NG - Nexthop Group Static Route, V - VXLAN Control Service,
       DH - DHCP client installed default route, M - Martian,
       DP - Dynamic Policy Route, L - VRF Leaked

Gateway of last resort is not set

 C        172.31.250.2/31 is directly connected, Ethernet13
 C        172.31.251.2/31 is directly connected, Ethernet11
 C        172.31.251.6/31 is directly connected, Ethernet12
 C        172.31.255.2/31 is directly connected, Ethernet1
 C        172.31.255.6/31 is directly connected, Ethernet2
 C        172.31.255.10/31 is directly connected, Ethernet3
 C        172.31.255.14/31 is directly connected, Ethernet4
 C        172.31.255.18/31 is directly connected, Ethernet7
 C        172.31.255.22/31 is directly connected, Ethernet8
 C        172.31.255.26/31 is directly connected, Ethernet5
 C        172.31.255.30/31 is directly connected, Ethernet6
 C        172.31.255.34/31 is directly connected, Ethernet9
 C        172.31.255.38/31 is directly connected, Ethernet10
 B E      192.168.0.3/32 [20/0] via 172.31.250.3, Ethernet13
 C        192.168.1.2/32 is directly connected, Loopback0
 B E      192.168.252.2/32 [20/0] via 172.31.251.3, Ethernet11
 B E      192.168.252.3/32 [20/0] via 172.31.251.7, Ethernet12
 B E      192.168.253.2/32 [20/0] via 172.31.251.3, Ethernet11
 B E      192.168.253.3/32 [20/0] via 172.31.251.7, Ethernet12
 B E      192.168.254.3/32 [20/0] via 172.31.255.3, Ethernet1
                                  via 172.31.255.7, Ethernet2
 B E      192.168.254.5/32 [20/0] via 172.31.255.11, Ethernet3
                                  via 172.31.255.15, Ethernet4
 B E      192.168.254.7/32 [20/0] via 172.31.255.19, Ethernet7
 B E      192.168.254.8/32 [20/0] via 172.31.255.23, Ethernet8
 B E      192.168.254.9/32 [20/0] via 172.31.255.27, Ethernet5
                                  via 172.31.255.31, Ethernet6
 B E      192.168.254.11/32 [20/0] via 172.31.255.35, Ethernet9
                                   via 172.31.255.39, Ethernet10
 B E      192.168.255.3/32 [20/0] via 172.31.255.3, Ethernet1
 B E      192.168.255.4/32 [20/0] via 172.31.255.7, Ethernet2
 B E      192.168.255.5/32 [20/0] via 172.31.255.11, Ethernet3
 B E      192.168.255.6/32 [20/0] via 172.31.255.15, Ethernet4
 B E      192.168.255.7/32 [20/0] via 172.31.255.19, Ethernet7
 B E      192.168.255.8/32 [20/0] via 172.31.255.23, Ethernet8
 B E      192.168.255.9/32 [20/0] via 172.31.255.27, Ethernet5
 B E      192.168.255.10/32 [20/0] via 172.31.255.31, Ethernet6
 B E      192.168.255.11/32 [20/0] via 172.31.255.35, Ethernet9
 B E      192.168.255.12/32 [20/0] via 172.31.255.39, Ethernet10


VRF: MGMT
Codes: C - connected, S - static, K - kernel, 
       O - OSPF, IA - OSPF inter area, E1 - OSPF external type 1,
       E2 - OSPF external type 2, N1 - OSPF NSSA external type 1,
       N2 - OSPF NSSA external type2, B - BGP, B I - iBGP, B E - eBGP,
       R - RIP, I L1 - IS-IS level 1, I L2 - IS-IS level 2,
       O3 - OSPFv3, A B - BGP Aggregate, A O - OSPF Summary,
       NG - Nexthop Group Static Route, V - VXLAN Control Service,
       DH - DHCP client installed default route, M - Martian,
       DP - Dynamic Policy Route, L - VRF Leaked

Gateway of last resort:
 S        0.0.0.0/0 [1/0] via 10.73.254.253, Management1

 C        10.73.254.0/24 is directly connected, Management1

! IP routing not enabled
```
## show lldp neighbors

```
Last table change time   : 18:09:26 ago
Number of table inserts  : 60
Number of table deletes  : 31
Number of table drops    : 0
Number of table age-outs : 26

Port       Neighbor Device ID               Neighbor Port ID           TTL
Et1        EAPI-LEAF1A                      Ethernet2                  120
Et2        EAPI-LEAF1B                      Ethernet2                  120
Et3        EAPI-LEAF2A                      Ethernet2                  120
Et4        EAPI-LEAF2B                      Ethernet2                  120
Et5        EAPI-BL01A                       Ethernet2                  120
Et6        EAPI-BL01B                       Ethernet2                  120
Et7        EAPI-LEAF3A                      Ethernet2                  120
Et8        EAPI-LEAF4A                      Ethernet2                  120
Et9        EAPI-CL01A                       Ethernet2                  120
Et10       EAPI-CL01B                       Ethernet2                  120
Et11       EAPI-L2LEAF01                    Ethernet2                  120
Et12       EAPI-L2LEAF02                    Ethernet2                  120
Et13       EAPI-RS02                        Ethernet1                  120
Ma1        EAPI-AGG02                       Management1                120
Ma1        EAPI-LEAF1B                      Management1                120
Ma1        EAPI-AGG01                       Management1                120
Ma1        EAPI-BL01B                       Management1                120
Ma1        EAPI-LEAF4A                      Management1                120
Ma1        EAPI-LEAF1A                      Management1                120
Ma1        EAPI-LEAF2A                      Management1                120
Ma1        EAPI-LEAF2B                      Management1                120
Ma1        EAPI-LEAF3A                      Management1                120
Ma1        EAPI-BL01A                       Management1                120
Ma1        EAPI-SPINE1                      Management1                120
Ma1        EAPI-CL01A                       Management1                120
Ma1        EAPI-L2LEAF02                    Management1                120
Ma1        EAPI-L2LEAF01                    Management1                120
Ma1        EAPI-CL01B                       Management1                120
Ma1        SRV-POD05-24                     Management1                120
```
## show mac address-table

```
Mac Address Table
------------------------------------------------------------------

Vlan    Mac Address       Type        Ports      Moves   Last Move
----    -----------       ----        -----      -----   ---------
   1    5001.0050.554b    DYNAMIC     Et11       1       2 days, 13:35:14 ago
   1    5001.0069.bdbc    DYNAMIC     Et10       1       2 days, 13:45:20 ago
Total Mac Addresses for this criterion: 2

          Multicast Mac Address Table
------------------------------------------------------------------

Vlan    Mac Address       Type        Ports
----    -----------       ----        -----
Total Mac Addresses for this criterion: 0
```
## show mlag config-sanity

```
Command not applicable for inactive MLAG state.
```
## show mlag detail

```
MLAG Configuration:   
domain-id              :                    
local-interface        :                    
peer-address           :             0.0.0.0
peer-link              :                    
peer-config            :                    
                                            
MLAG Status:          
state                  :            Disabled
negotiation status     :                    
peer-link status       :                    
local-int status       :                    
system-id              :   00:00:00:00:00:00
dual-primary detection :            Disabled
                                            
MLAG Ports:           
Disabled               :                   0
Configured             :                   0
Inactive               :                   0
Active-partial         :                   0
Active-full            :                   0

MLAG Detailed Status:
State                           :            disabled
Peer State                      :             unknown
State changes                   :                   0
Last state change time          :               never
Hardware ready                  :                True
Failover                        :               False
Failover Cause(s)               :             Unknown
Last failover change time       :               never
Secondary from failover         :               False
Peer MAC address                :   00:00:00:00:00:00
Peer MAC routing supported      :               False
Reload delay                    :         300 seconds
Non-MLAG reload delay           :         300 seconds
Ports errdisabled               :               False
Lacp standby                    :               False
Configured heartbeat interval   :             4000 ms
Effective heartbeat interval    :            disabled
Heartbeat timeout               :                0 ms
Last heartbeat timeout          :               never
Heartbeat timeouts since reboot :                   0
UDP heartbeat alive             :               False
Heartbeats sent/received        :                 0/0
Peer monotonic clock offset     :             unknown
Agent should be running         :               False
P2p mount state changes         :                   0
Fast MAC redirection enabled    :               False
```
## show system environment cooling

```
System cooling status is: Unknown
Ambient temperature: Unknown
           Config Actual        Speed     Stable
Fan Status  Speed  Speed Uptime Stability Uptime
--- ------ ------ ------ ------ --------- ------
```
## show version

```
vEOS
Hardware version:    
Serial number:       
System MAC address:  0c1d.c05f.613b

Software image version: 4.22.5M
Architecture:           i686
Internal build version: 4.22.5M-16511818.4225M
Internal build ID:      ca78196c-426c-40e9-9d55-80540fb5ac07

Uptime:                 0 weeks, 2 days, 14 hours and 40 minutes
Total memory:           2014520 kB
Free memory:            1133584 kB
```
## show vlan

```
VLAN  Name                             Status    Ports
----- -------------------------------- --------- -------------------------------
1     default                          active    Et14
```
## show vxlan address-table

```
Vxlan Mac Address Table
----------------------------------------------------------------------

VLAN  Mac Address     Type     Prt  VTEP             Moves   Last Move
----  -----------     ----     ---  ----             -----   ---------
Total Remote Mac Addresses for this criterion: 0
```
## show vxlan vni

```

```
## show vxlan vtep

```

```
