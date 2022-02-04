# EAPI-AGG01 Commands Output

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
BGP is disabled for VRF default
```
## show bgp evpn

```
BGP is disabled for VRF default
BGP routing table information for VRF default
Router identifier 0.0.0.0, local AS number 0
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
Et1                            up             up                 EAPI-LEAF1A_Ethernet5
Et2                            up             up                 EAPI-LEAF1B_Ethernet5
Et3                            up             up                 SRV-POD01_Eth1
Et4                            up             up                 
Et5                            up             up                 
Et6                            up             up                 
Et7                            up             up                 
Et8                            up             up                 
Ma1                            up             up                 oob_management
Po1                            up             up                 EAPI_LEAF1_Po5
```
## show ip bgp summary vrf all

```
BGP is disabled for VRF default
```
## show ip interface brief

```
Address 
Interface       IP Address          Status      Protocol         MTU    Owner   
--------------- ------------------- ----------- ------------- --------- ------- 
Management1     10.73.254.21/24     up          up              1500
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
       DP - Dynamic Policy Route, L - VRF Leaked,
       RC - Route Cache Route

Gateway of last resort is not set



VRF: MGMT
Codes: C - connected, S - static, K - kernel, 
       O - OSPF, IA - OSPF inter area, E1 - OSPF external type 1,
       E2 - OSPF external type 2, N1 - OSPF NSSA external type 1,
       N2 - OSPF NSSA external type2, B - BGP, B I - iBGP, B E - eBGP,
       R - RIP, I L1 - IS-IS level 1, I L2 - IS-IS level 2,
       O3 - OSPFv3, A B - BGP Aggregate, A O - OSPF Summary,
       NG - Nexthop Group Static Route, V - VXLAN Control Service,
       DH - DHCP client installed default route, M - Martian,
       DP - Dynamic Policy Route, L - VRF Leaked,
       RC - Route Cache Route

Gateway of last resort:
 S        0.0.0.0/0 [1/0] via 10.73.254.253, Management1

 C        10.73.254.0/24 is directly connected, Management1

! IP routing not enabled
```
## show lldp neighbors

```
Last table change time   : 2:38:05 ago
Number of table inserts  : 36
Number of table deletes  : 17
Number of table drops    : 0
Number of table age-outs : 16

Port          Neighbor Device ID       Neighbor Port ID    TTL 
---------- ------------------------ ---------------------- --- 
Et1           EAPI-LEAF1A              Ethernet5           120 
Et2           EAPI-LEAF1B              Ethernet5           120 
Et3           SRV-POD01                Ethernet1           120 
Ma1           EAPI-LEAF4A              Management1         120 
Ma1           EAPI-AGG02               Management1         120 
Ma1           EAPI-BL01B               Management1         120 
Ma1           EAPI-BL01A               Management1         120 
Ma1           EAPI-LEAF1B              Management1         120 
Ma1           EAPI-LEAF1A              Management1         120 
Ma1           EAPI-LEAF2B              Management1         120 
Ma1           EAPI-LEAF2A              Management1         120 
Ma1           EAPI-LEAF3A              Management1         120 
Ma1           EAPI-SPINE2              Management1         120 
Ma1           EAPI-SPINE1              Management1         120 
Ma1           EAPI-CL01A               Management1         120 
Ma1           EAPI-L2LEAF02            Management1         120 
Ma1           EAPI-L2LEAF01            Management1         120 
Ma1           EAPI-CL01B               Management1         120 
Ma1           SRV-POD05-24             Management1         120
```
## show mac address-table

```
Mac Address Table
------------------------------------------------------------------

Vlan    Mac Address       Type        Ports      Moves   Last Move
----    -----------       ----        -----      -----   ---------
 110    0c1d.c0f4.7b39    DYNAMIC     Po1        1       1:59:13 ago
 110    5001.0002.f6c5    DYNAMIC     Po1        1       1:59:16 ago
 110    5001.0056.2a6e    DYNAMIC     Et3        1       2:04:22 ago
Total Mac Addresses for this criterion: 3

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
domain-id                          :                    
local-interface                    :                    
peer-address                       :             0.0.0.0
peer-link                          :                    
peer-config                        :                    
                                                        
MLAG Status:                      
state                              :            Disabled
negotiation status                 :                    
peer-link status                   :                    
local-int status                   :                    
system-id                          :   00:00:00:00:00:00
dual-primary detection             :            Disabled
dual-primary interface errdisabled :               False
                                                        
MLAG Ports:                       
Disabled                           :                   0
Configured                         :                   0
Inactive                           :                   0
Active-partial                     :                   0
Active-full                        :                   0

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
System MAC address:  0c1d.c090.1379

Software image version: 4.24.0F
Architecture:           i686
Internal build version: 4.24.0F-16270098.4240F
Internal build ID:      da8d6269-c25f-4a12-930b-c3c42c12c38a

Uptime:                 0 weeks, 2 days, 18 hours and 32 minutes
Total memory:           2014424 kB
Free memory:            1124868 kB
```
## show vlan

```
VLAN  Name                             Status    Ports
----- -------------------------------- --------- -------------------------------
1     default                          active    Et3, Et4, Et5, Et6, Et7, Et8
110   PR01-DEMO                        active    Et3, Po1
111   PR01-TRUST                       active    Et3, Po1
112   PR01-TRUST                       active    Et3, Po1
201   B-ELAN-201                       active    Et3, Po1
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
