# EAPI-BL01A Commands Output

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
VRF name: default
-----------------
DstAddr         MyDisc   YourDisc Interface     Type          LastUp  LastDown  
----------- ---------- ---------- --------- --------- --------------- --------- 
192.168.0.2 3679388708 1337620493        NA multihop  08/27/21 17:14        NA  
192.168.0.3 3544063705 2652598855        NA multihop  08/27/21 17:14        NA  

        LastDiag    State 
------------------- ----- 
   No Diagnostic       Up 
   No Diagnostic       Up
```
## show bgp evpn summary

```
BGP summary information for VRF default
Router identifier 192.168.255.9, local AS number 65105
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  EAPI-RS01                192.168.0.2      4  65000           2997      3119    0    0 18:10:21 Estab   87     87
  EAPI-RS02                192.168.0.3      4  65000           2872      3465    0    0 18:10:19 Estab   87     87
```
## show bgp evpn

```
BGP routing table information for VRF default
Router identifier 192.168.255.9, local AS number 65105
Route status codes: s - suppressed, * - valid, > - active, # - not installed, E - ECMP head, e - ECMP
                    S - Stale, c - Contributing to ECMP, b - backup
                    % - Pending BGP convergence
Origin codes: i - IGP, e - EGP, ? - incomplete
AS Path Attributes: Or-ID - Originator ID, C-LST - Cluster List, LL Nexthop - Link Local Nexthop

          Network                Next Hop              Metric  LocPref Weight  Path
 * >Ec   RD: 192.168.255.7:11 auto-discovery 10110 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:11 auto-discovery 10110 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.255.8:11 auto-discovery 10110 0000:0000:0303:0202:0101
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.255.8:11 auto-discovery 10110 0000:0000:0303:0202:0101
                                192.168.254.8         -       100     0       65000 65104 i
 * >Ec   RD: 192.168.255.7:11 auto-discovery 10113 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:11 auto-discovery 10113 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.255.8:11 auto-discovery 10113 0000:0000:0303:0202:0101
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.255.8:11 auto-discovery 10113 0000:0000:0303:0202:0101
                                192.168.254.8         -       100     0       65000 65104 i
 * >Ec   RD: 192.168.255.7:20201 auto-discovery 20201 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:20201 auto-discovery 20201 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.255.8:20201 auto-discovery 20201 0000:0000:0303:0202:0101
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.255.8:20201 auto-discovery 20201 0000:0000:0303:0202:0101
                                192.168.254.8         -       100     0       65000 65104 i
 * >Ec   RD: 192.168.254.7:1 auto-discovery 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.254.7:1 auto-discovery 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.254.8:1 auto-discovery 0000:0000:0303:0202:0101
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.254.8:1 auto-discovery 0000:0000:0303:0202:0101
                                192.168.254.8         -       100     0       65000 65104 i
 * >Ec   RD: 192.168.255.5:11 mac-ip 10110 5001.0002.f6c5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 mac-ip 10110 5001.0002.f6c5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 mac-ip 10110 5001.0002.f6c5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 mac-ip 10110 5001.0002.f6c5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.5:11 mac-ip 10110 5001.0002.f6c5 10.1.10.2
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 mac-ip 10110 5001.0002.f6c5 10.1.10.2
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 mac-ip 10110 5001.0002.f6c5 10.1.10.2
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 mac-ip 10110 5001.0002.f6c5 10.1.10.2
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.3:11 mac-ip 10110 5001.0056.2a6e
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:11 mac-ip 10110 5001.0056.2a6e
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:11 mac-ip 10110 5001.0056.2a6e
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:11 mac-ip 10110 5001.0056.2a6e
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.3:11 mac-ip 10110 5001.0056.2a6e 10.1.10.1
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:11 mac-ip 10110 5001.0056.2a6e 10.1.10.1
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:11 mac-ip 10110 5001.0056.2a6e 10.1.10.1
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:11 mac-ip 10110 5001.0056.2a6e 10.1.10.1
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.5:11 mac-ip 10112 5001.0002.f6c5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 mac-ip 10112 5001.0002.f6c5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 mac-ip 10112 5001.0002.f6c5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 mac-ip 10112 5001.0002.f6c5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.5:11 mac-ip 10112 5001.0002.f6c5 10.1.12.2
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 mac-ip 10112 5001.0002.f6c5 10.1.12.2
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 mac-ip 10112 5001.0002.f6c5 10.1.12.2
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 mac-ip 10112 5001.0002.f6c5 10.1.12.2
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.253.2:13 mac-ip 30302 5001.0073.5ad7
                                192.168.252.2         -       100     0       65000 65107 i
 *  ec   RD: 192.168.253.2:13 mac-ip 30302 5001.0073.5ad7
                                192.168.252.2         -       100     0       65000 65107 i
 * >Ec   RD: 192.168.253.3:13 mac-ip 30302 5001.00bf.cca4
                                192.168.252.3         -       100     0       65000 65108 i
 *  ec   RD: 192.168.253.3:13 mac-ip 30302 5001.00bf.cca4
                                192.168.252.3         -       100     0       65000 65108 i
 * >Ec   RD: 192.168.255.3:11 imet 10110 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:11 imet 10110 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:11 imet 10110 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:11 imet 10110 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.5:11 imet 10110 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 imet 10110 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 imet 10110 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 imet 10110 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.7:11 imet 10110 192.168.254.7
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:11 imet 10110 192.168.254.7
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.255.8:11 imet 10110 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.255.8:11 imet 10110 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 * >     RD: 192.168.255.9:11 imet 10110 192.168.254.9
                                -                     -       -       0       i
 * >Ec   RD: 192.168.255.11:11 imet 10110 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:11 imet 10110 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:11 imet 10110 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:11 imet 10110 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.3:11 imet 10111 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:11 imet 10111 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:11 imet 10111 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:11 imet 10111 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.5:11 imet 10111 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 imet 10111 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 imet 10111 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 imet 10111 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.3:11 imet 10112 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:11 imet 10112 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:11 imet 10112 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:11 imet 10112 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.5:11 imet 10112 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 imet 10112 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 imet 10112 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 imet 10112 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.7:11 imet 10113 192.168.254.7
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:11 imet 10113 192.168.254.7
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.255.8:11 imet 10113 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.255.8:11 imet 10113 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 * >Ec   RD: 192.168.255.3:20201 imet 20201 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:20201 imet 20201 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:20201 imet 20201 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:20201 imet 20201 192.168.254.3
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.5:20201 imet 20201 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:20201 imet 20201 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:20201 imet 20201 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:20201 imet 20201 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.7:20201 imet 20201 192.168.254.7
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:20201 imet 20201 192.168.254.7
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.255.8:20201 imet 20201 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.255.8:20201 imet 20201 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 * >     RD: 192.168.255.9:20201 imet 20201 192.168.254.9
                                -                     -       -       0       i
 * >Ec   RD: 192.168.255.11:20201 imet 20201 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:20201 imet 20201 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:20201 imet 20201 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:20201 imet 20201 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.253.2:13 imet 30301 192.168.252.2
                                192.168.252.2         -       100     0       65000 65107 i
 *  ec   RD: 192.168.253.2:13 imet 30301 192.168.252.2
                                192.168.252.2         -       100     0       65000 65107 i
 * >Ec   RD: 192.168.255.11:13 imet 30301 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:13 imet 30301 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:13 imet 30301 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:13 imet 30301 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.253.2:13 imet 30302 192.168.252.2
                                192.168.252.2         -       100     0       65000 65107 i
 *  ec   RD: 192.168.253.2:13 imet 30302 192.168.252.2
                                192.168.252.2         -       100     0       65000 65107 i
 * >Ec   RD: 192.168.253.3:13 imet 30302 192.168.252.3
                                192.168.252.3         -       100     0       65000 65108 i
 *  ec   RD: 192.168.253.3:13 imet 30302 192.168.252.3
                                192.168.252.3         -       100     0       65000 65108 i
 * >Ec   RD: 192.168.255.11:13 imet 30302 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:13 imet 30302 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:13 imet 30302 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:13 imet 30302 192.168.254.11
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.254.7:1 ethernet-segment 0000:0000:0303:0202:0101 192.168.254.7
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.254.7:1 ethernet-segment 0000:0000:0303:0202:0101 192.168.254.7
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.254.8:1 ethernet-segment 0000:0000:0303:0202:0101 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.254.8:1 ethernet-segment 0000:0000:0303:0202:0101 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 * >     RD: 192.168.255.9:11 ip-prefix 1.1.1.0/24
                                -                     -       -       0       ?
 *       RD: 192.168.255.9:11 ip-prefix 1.1.1.0/24
                                -                     -       100     0       ?
 * >Ec   RD: 192.168.255.3:11 ip-prefix 10.1.10.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:11 ip-prefix 10.1.10.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:11 ip-prefix 10.1.10.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:11 ip-prefix 10.1.10.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.5:11 ip-prefix 10.1.10.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 ip-prefix 10.1.10.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 ip-prefix 10.1.10.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 ip-prefix 10.1.10.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.7:11 ip-prefix 10.1.10.0/24
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:11 ip-prefix 10.1.10.0/24
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.255.8:11 ip-prefix 10.1.10.0/24
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.255.8:11 ip-prefix 10.1.10.0/24
                                192.168.254.8         -       100     0       65000 65104 i
 * >     RD: 192.168.255.9:11 ip-prefix 10.1.10.0/24
                                -                     -       -       0       i
 *       RD: 192.168.255.9:11 ip-prefix 10.1.10.0/24
                                -                     -       100     0       ?
 * >Ec   RD: 192.168.255.11:11 ip-prefix 10.1.10.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:11 ip-prefix 10.1.10.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:11 ip-prefix 10.1.10.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:11 ip-prefix 10.1.10.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 * >     RD: 192.168.255.9:11 ip-prefix 10.1.10.1/32
                                -                     -       100     0       65000 65101 ?
 * >     RD: 192.168.255.9:11 ip-prefix 10.1.10.2/32
                                -                     -       100     0       65000 65102 ?
 * >Ec   RD: 192.168.255.3:11 ip-prefix 10.1.11.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:11 ip-prefix 10.1.11.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:11 ip-prefix 10.1.11.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:11 ip-prefix 10.1.11.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.5:11 ip-prefix 10.1.11.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 ip-prefix 10.1.11.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 ip-prefix 10.1.11.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 ip-prefix 10.1.11.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >     RD: 192.168.255.9:11 ip-prefix 10.1.11.0/24
                                -                     -       100     0       65000 65101 ?
 * >Ec   RD: 192.168.255.3:11 ip-prefix 10.1.12.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:11 ip-prefix 10.1.12.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:11 ip-prefix 10.1.12.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:11 ip-prefix 10.1.12.0/24
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.5:11 ip-prefix 10.1.12.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 ip-prefix 10.1.12.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 ip-prefix 10.1.12.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 ip-prefix 10.1.12.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >     RD: 192.168.255.9:11 ip-prefix 10.1.12.0/24
                                -                     -       100     0       65000 65101 ?
 * >     RD: 192.168.255.9:11 ip-prefix 10.1.12.2/32
                                -                     -       100     0       65000 65102 ?
 * >Ec   RD: 192.168.255.7:11 ip-prefix 10.1.13.0/24
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:11 ip-prefix 10.1.13.0/24
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.255.8:11 ip-prefix 10.1.13.0/24
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.255.8:11 ip-prefix 10.1.13.0/24
                                192.168.254.8         -       100     0       65000 65104 i
 * >     RD: 192.168.255.9:11 ip-prefix 10.1.13.0/24
                                -                     -       100     0       65000 65103 ?
 * >Ec   RD: 192.168.255.11:13 ip-prefix 10.3.1.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:13 ip-prefix 10.3.1.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:13 ip-prefix 10.3.1.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:13 ip-prefix 10.3.1.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.11:13 ip-prefix 10.3.2.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:13 ip-prefix 10.3.2.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:13 ip-prefix 10.3.2.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:13 ip-prefix 10.3.2.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.3:11 ip-prefix 172.31.253.2/31
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.3:11 ip-prefix 172.31.253.2/31
                                192.168.254.3         -       100     0       65000 65101 i
 * >Ec   RD: 192.168.255.4:11 ip-prefix 172.31.253.2/31
                                192.168.254.3         -       100     0       65000 65101 i
 *  ec   RD: 192.168.255.4:11 ip-prefix 172.31.253.2/31
                                192.168.254.3         -       100     0       65000 65101 i
 * >     RD: 192.168.255.9:11 ip-prefix 172.31.253.2/31
                                -                     -       100     0       65000 65101 ?
 * >Ec   RD: 192.168.255.5:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 * >     RD: 192.168.255.9:11 ip-prefix 172.31.253.6/31
                                -                     -       100     0       65000 65102 ?
 * >     RD: 192.168.255.9:11 ip-prefix 172.31.253.14/31
                                -                     -       -       0       i
 *       RD: 192.168.255.9:11 ip-prefix 172.31.253.14/31
                                -                     -       100     0       ?
 * >     RD: 192.168.255.9:11 ip-prefix 172.31.253.18/31
                                -                     -       100     0       65000 65106 ?
 * >Ec   RD: 192.168.255.11:11 ip-prefix 172.31.253.18/31
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:11 ip-prefix 172.31.253.18/31
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.11:13 ip-prefix 172.31.253.18/31
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:13 ip-prefix 172.31.253.18/31
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:11 ip-prefix 172.31.253.18/31
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:11 ip-prefix 172.31.253.18/31
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:13 ip-prefix 172.31.253.18/31
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:13 ip-prefix 172.31.253.18/31
                                192.168.254.11        -       100     0       65000 65106 i
```
## show interfaces description

```
Interface                      Status         Protocol           Description
Et1                            up             up                 P2P_LINK_TO_EAPI-SPINE1_Ethernet5
Et2                            up             up                 P2P_LINK_TO_EAPI-SPINE2_Ethernet5
Et3                            up             up                 MLAG_PEER_EAPI-BL01B_Ethernet3
Et4                            up             up                 MLAG_PEER_EAPI-BL01B_Ethernet4
Et5                            up             up                 
Et6                            up             up                 
Et7                            up             up                 
Et8                            up             up                 
Lo0                            up             up                 EVPN_Overlay_Peering
Lo1                            up             up                 VTEP_VXLAN_Tunnel_Source
Ma1                            up             up                 oob_management
Po3                            up             up                 MLAG_PEER_EAPI-BL01B_Po3
Vl110                          up             up                 PR01-DEMO
Vl1196                         up             up                 
Vl1199                         up             up                 
Vl3010                         up             up                 MLAG_PEER_L3_iBGP: vrf TENANT_A_PROJECT01
Vl4093                         up             up                 MLAG_PEER_L3_PEERING
Vl4094                         up             up                 MLAG_PEER
Vx1                            up             up                 EAPI-BL01A_VTEP
```
## show ip bgp summary vrf all

```
BGP summary information for VRF default
Router identifier 192.168.255.9, local AS number 65105
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  EAPI-BL01B               172.31.253.15    4  65105           4375      4375    0    0    2d13h Estab   23     23
  EAPI-SPINE1_Ethernet5    172.31.255.24    4  65001           4604      4588    0    0    2d13h Estab   19     19
  EAPI-SPINE2_Ethernet5    172.31.255.26    4  65001           4583      4589    0    0    2d13h Estab   19     19

BGP summary information for VRF TENANT_A_PROJECT01
Router identifier 192.168.255.9, local AS number 65105
Neighbor Status Codes: m - Under maintenance
  Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  172.31.253.15    4  65105           6410      6470    0    0    2d13h Estab   12     12
```
## show ip interface brief

```
Address 
Interface       IP Address           Status     Protocol         MTU    Owner   
--------------- -------------------- ---------- ------------ ---------- ------- 
Ethernet1       172.31.255.25/31     up         up              1500            
Ethernet2       172.31.255.27/31     up         up              1500            
Loopback0       192.168.255.9/32     up         up             65535            
Loopback1       192.168.254.9/32     up         up             65535            
Management1     10.73.254.15/24      up         up              1500            
Vlan110         10.1.10.254/24       up         up              1500            
Vlan1196        unassigned           up         up              9164            
Vlan1199        unassigned           up         up              9164            
Vlan3010        172.31.253.14/31     up         up              1500            
Vlan4093        172.31.253.14/31     up         up              1500            
Vlan4094        172.31.253.12/31     up         up              1500
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

 C        172.31.253.12/31 is directly connected, Vlan4094
 C        172.31.253.14/31 is directly connected, Vlan4093
 C        172.31.255.24/31 is directly connected, Ethernet1
 C        172.31.255.26/31 is directly connected, Ethernet2
 B E      192.168.0.2/32 [20/0] via 172.31.255.24, Ethernet1
 B E      192.168.0.3/32 [20/0] via 172.31.255.26, Ethernet2
 B E      192.168.1.1/32 [20/0] via 172.31.255.24, Ethernet1
 B E      192.168.1.2/32 [20/0] via 172.31.255.26, Ethernet2
 B E      192.168.252.2/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.252.3/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.253.2/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.253.3/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.254.3/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.254.5/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.254.7/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.254.8/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 C        192.168.254.9/32 is directly connected, Loopback1
 B E      192.168.254.11/32 [20/0] via 172.31.255.24, Ethernet1
                                   via 172.31.255.26, Ethernet2
 B E      192.168.255.3/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.255.4/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.255.5/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.255.6/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.255.7/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 B E      192.168.255.8/32 [20/0] via 172.31.255.24, Ethernet1
                                  via 172.31.255.26, Ethernet2
 C        192.168.255.9/32 is directly connected, Loopback0
 B I      192.168.255.10/32 [200/0] via 172.31.253.15, Vlan4093
 B E      192.168.255.11/32 [20/0] via 172.31.255.24, Ethernet1
                                   via 172.31.255.26, Ethernet2
 B E      192.168.255.12/32 [20/0] via 172.31.255.24, Ethernet1
                                   via 172.31.255.26, Ethernet2


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

VRF: TENANT_A_PROJECT01
WARNING: Some of the routes are not programmed in     
kernel, and they are marked with '%'.                 
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

 S%       1.1.1.0/24 [1/0] via 10.1.10.1 VTEP 192.168.254.3 VNI 11 router-mac 0e:1d:c0:f0:bd:d1
 B E      10.1.10.1/32 [20/0] via VTEP 192.168.254.3 VNI 11 router-mac 0e:1d:c0:f0:bd:d1
 B E      10.1.10.2/32 [20/0] via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 C        10.1.10.0/24 is directly connected, Vlan110
 B E      10.1.11.0/24 [20/0] via VTEP 192.168.254.3 VNI 11 router-mac 0e:1d:c0:f0:bd:d1
                              via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 B E      10.1.12.2/32 [20/0] via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 B E      10.1.12.0/24 [20/0] via VTEP 192.168.254.3 VNI 11 router-mac 0e:1d:c0:f0:bd:d1
                              via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 B E      10.1.13.0/24 [20/0] via VTEP 192.168.254.8 VNI 11 router-mac 0c:1d:c0:d2:9e:98
                              via VTEP 192.168.254.7 VNI 11 router-mac 0c:1d:c0:e4:77:7b
 B E      172.31.253.2/31 [20/0] via VTEP 192.168.254.3 VNI 11 router-mac 0e:1d:c0:f0:bd:d1
 B E      172.31.253.6/31 [20/0] via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 C        172.31.253.14/31 is directly connected, Vlan3010
 B E      172.31.253.18/31 [20/0] via VTEP 192.168.254.11 VNI 11 router-mac 52:01:00:68:b4:46
```
## show lldp neighbors

```
Last table change time   : 2 days, 1:57:05 ago
Number of table inserts  : 35
Number of table deletes  : 15
Number of table drops    : 0
Number of table age-outs : 15

Port          Neighbor Device ID       Neighbor Port ID    TTL 
---------- ------------------------ ---------------------- --- 
Et1           EAPI-SPINE1              Ethernet5           120 
Et2           EAPI-SPINE2              Ethernet5           120 
Et3           EAPI-BL01B               Ethernet3           120 
Et4           EAPI-BL01B               Ethernet4           120 
Ma1           EAPI-LEAF4A              Management1         120 
Ma1           EAPI-AGG02               Management1         120 
Ma1           EAPI-AGG01               Management1         120 
Ma1           EAPI-BL01B               Management1         120 
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
 110    0c1d.c0f5.1c0d    STATIC      Po3
 110    5001.0002.f6c5    DYNAMIC     Vx1        1       1:22:27 ago
 110    5001.0056.2a6e    DYNAMIC     Vx1        1       2:03:50 ago
1196    0c1d.c0f5.1c0d    STATIC      Po3
1196    5201.0068.b446    DYNAMIC     Vx1        1       18:10:44 ago
1199    0c1d.c0d2.9e98    DYNAMIC     Vx1        1       18:10:48 ago
1199    0c1d.c0e4.777b    DYNAMIC     Vx1        1       18:10:47 ago
1199    0c1d.c0f5.1c0d    STATIC      Po3
1199    0e1d.c0a3.43e0    DYNAMIC     Vx1        1       18:10:36 ago
1199    0e1d.c0f0.bdd1    DYNAMIC     Vx1        1       18:10:47 ago
1199    5201.0068.b446    DYNAMIC     Vx1        1       18:10:44 ago
3010    0c1d.c0f5.1c0d    STATIC      Po3
4093    0c1d.c0f5.1c0d    STATIC      Po3
4094    0c1d.c0f5.1c0d    STATIC      Po3
Total Mac Addresses for this criterion: 14

          Multicast Mac Address Table
------------------------------------------------------------------

Vlan    Mac Address       Type        Ports
----    -----------       ----        -----
Total Mac Addresses for this criterion: 0
```
## show mlag config-sanity

```
No global configuration inconsistencies found.

No per interface configuration inconsistencies found.
```
## show mlag detail

```
MLAG Configuration:               
domain-id                          :           EAPI_BL01
local-interface                    :            Vlan4094
peer-address                       :       172.31.253.13
peer-link                          :       Port-Channel3
peer-config                        :          consistent
                                                        
MLAG Status:                      
state                              :              Active
negotiation status                 :           Connected
peer-link status                   :                  Up
local-int status                   :                  Up
system-id                          :   0e:1d:c0:25:65:41
dual-primary detection             :            Disabled
dual-primary interface errdisabled :               False
                                                        
MLAG Ports:                       
Disabled                           :                   0
Configured                         :                   0
Inactive                           :                   0
Active-partial                     :                   0
Active-full                        :                   0

MLAG Detailed Status:
State                           :                primary
Peer State                      :              secondary
State changes                   :                      4
Last state change time          :   2 days, 13:21:34 ago
Hardware ready                  :                   True
Failover                        :                  False
Failover Cause(s)               :                Unknown
Last failover change time       :                  never
Secondary from failover         :                  False
Peer MAC address                :      0c:1d:c0:f5:1c:0d
Peer MAC routing supported      :                  False
Reload delay                    :            300 seconds
Non-MLAG reload delay           :            330 seconds
Peer ports errdisabled          :                  False
Lacp standby                    :                  False
Configured heartbeat interval   :                4000 ms
Effective heartbeat interval    :                4000 ms
Heartbeat timeout               :               60000 ms
Last heartbeat timeout          :                  never
Heartbeat timeouts since reboot :                      0
UDP heartbeat alive             :                   True
Heartbeats sent/received        :            59761/59749
Peer monotonic clock offset     :       6.532848 seconds
Agent should be running         :                   True
P2p mount state changes         :                      3
Fast MAC redirection enabled    :                  False
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
System MAC address:  0c1d.c025.6541

Software image version: 4.24.0F
Architecture:           i686
Internal build version: 4.24.0F-16270098.4240F
Internal build ID:      da8d6269-c25f-4a12-930b-c3c42c12c38a

Uptime:                 0 weeks, 2 days, 18 hours and 31 minutes
Total memory:           2014424 kB
Free memory:            1053828 kB
```
## show vlan

```
VLAN  Name                             Status    Ports
----- -------------------------------- --------- -------------------------------
1     default                          active    Et5, Et6, Et7, Et8, PEt5, PEt6
                                                 PEt7, PEt8
110   PR01-DEMO                        active    Cpu, Po3, Vx1
201   B-ELAN-201                       active    Po3, Vx1
1196* VLAN1196                         active    Cpu, Po3, Vx1
1199* VLAN1199                         active    Cpu, Po3, Vx1
3010  MLAG_iBGP_TENANT_A_PROJECT01     active    Cpu, Po3
4093  LEAF_PEER_L3                     active    Cpu, Po3
4094  MLAG_PEER                        active    Cpu, Po3

* indicates a Dynamic VLAN
```
## show vxlan address-table

```
Vxlan Mac Address Table
----------------------------------------------------------------------

VLAN  Mac Address     Type     Prt  VTEP             Moves   Last Move
----  -----------     ----     ---  ----             -----   ---------
 110  5001.0002.f6c5  EVPN     Vx1  192.168.254.5    1       1:22:19 ago
 110  5001.0056.2a6e  EVPN     Vx1  192.168.254.3    1       2:03:42 ago
1196  5201.0068.b446  EVPN     Vx1  192.168.254.11   1       18:10:36 ago
1199  0c1d.c0d2.9e98  EVPN     Vx1  192.168.254.8    1       18:10:40 ago
1199  0c1d.c0e4.777b  EVPN     Vx1  192.168.254.7    1       18:10:39 ago
1199  0e1d.c0a3.43e0  EVPN     Vx1  192.168.254.5    1       18:10:28 ago
1199  0e1d.c0f0.bdd1  EVPN     Vx1  192.168.254.3    1       18:10:39 ago
1199  5201.0068.b446  EVPN     Vx1  192.168.254.11   1       18:10:36 ago
Total Remote Mac Addresses for this criterion: 8
```
## show vxlan vni

```
VNI to VLAN Mapping for Vxlan1
VNI         VLAN        Source       Interface       802.1Q Tag 
----------- ----------- ------------ --------------- ---------- 
11          1199*       evpn         Vxlan1          1199       
13          1196*       evpn         Vxlan1          1196       
10110       110         static       Vxlan1          110        
20201       201         static       Vxlan1          201        

Note: * indicates a Dynamic VLAN
```
## show vxlan vtep

```
Remote VTEPS for Vxlan1:
192.168.254.3
192.168.254.5
192.168.254.7
192.168.254.8
192.168.254.11
Total number of remote VTEPS:  5
```
