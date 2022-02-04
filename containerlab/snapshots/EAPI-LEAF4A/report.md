# EAPI-LEAF4A Commands Output

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
192.168.0.2  977979897  796752443        NA multihop  08/27/21 17:14        NA  
192.168.0.3 4057132875 3430836204        NA multihop  08/27/21 17:14        NA  

        LastDiag    State 
------------------- ----- 
   No Diagnostic       Up 
   No Diagnostic       Up
```
## show bgp evpn summary

```
BGP summary information for VRF default
Router identifier 192.168.255.8, local AS number 65104
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  EAPI-RS01                192.168.0.2      4  65000           3332      2961    0    0 18:10:21 Estab   87     87
  EAPI-RS02                192.168.0.3      4  65000           3086      3113    0    0 18:10:18 Estab   87     87
```
## show bgp evpn

```
BGP routing table information for VRF default
Router identifier 192.168.255.8, local AS number 65104
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
 * >     RD: 192.168.255.8:11 auto-discovery 10110 0000:0000:0303:0202:0101
                                -                     -       -       0       i
 * >Ec   RD: 192.168.255.7:11 auto-discovery 10113 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:11 auto-discovery 10113 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 * >     RD: 192.168.255.8:11 auto-discovery 10113 0000:0000:0303:0202:0101
                                -                     -       -       0       i
 * >Ec   RD: 192.168.255.7:20201 auto-discovery 20201 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:20201 auto-discovery 20201 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 * >     RD: 192.168.255.8:20201 auto-discovery 20201 0000:0000:0303:0202:0101
                                -                     -       -       0       i
 * >Ec   RD: 192.168.254.7:1 auto-discovery 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.254.7:1 auto-discovery 0000:0000:0303:0202:0101
                                192.168.254.7         -       100     0       65000 65103 i
 * >     RD: 192.168.254.8:1 auto-discovery 0000:0000:0303:0202:0101
                                -                     -       -       0       i
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
 * >     RD: 192.168.255.8:11 imet 10110 192.168.254.8
                                -                     -       -       0       i
 * >Ec   RD: 192.168.255.9:11 imet 10110 192.168.254.9
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.9:11 imet 10110 192.168.254.9
                                192.168.254.9         -       100     0       65000 65105 i
 * >Ec   RD: 192.168.255.10:11 imet 10110 192.168.254.9
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.10:11 imet 10110 192.168.254.9
                                192.168.254.9         -       100     0       65000 65105 i
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
 * >     RD: 192.168.255.8:11 imet 10113 192.168.254.8
                                -                     -       -       0       i
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
 * >     RD: 192.168.255.8:20201 imet 20201 192.168.254.8
                                -                     -       -       0       i
 * >Ec   RD: 192.168.255.9:20201 imet 20201 192.168.254.9
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.9:20201 imet 20201 192.168.254.9
                                192.168.254.9         -       100     0       65000 65105 i
 * >Ec   RD: 192.168.255.10:20201 imet 20201 192.168.254.9
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.10:20201 imet 20201 192.168.254.9
                                192.168.254.9         -       100     0       65000 65105 i
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
 * >     RD: 192.168.254.8:1 ethernet-segment 0000:0000:0303:0202:0101 192.168.254.8
                                -                     -       -       0       i
 * >Ec   RD: 192.168.255.9:11 ip-prefix 1.1.1.0/24
                                192.168.254.9         -       100     0       65000 65105 ?
 *  ec   RD: 192.168.255.9:11 ip-prefix 1.1.1.0/24
                                192.168.254.9         -       100     0       65000 65105 ?
 * >Ec   RD: 192.168.255.10:11 ip-prefix 1.1.1.0/24
                                192.168.254.9         -       100     0       65000 65105 ?
 *  ec   RD: 192.168.255.10:11 ip-prefix 1.1.1.0/24
                                192.168.254.9         -       100     0       65000 65105 ?
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
 * >     RD: 192.168.255.8:11 ip-prefix 10.1.10.0/24
                                -                     -       -       0       i
 * >Ec   RD: 192.168.255.9:11 ip-prefix 10.1.10.0/24
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.9:11 ip-prefix 10.1.10.0/24
                                192.168.254.9         -       100     0       65000 65105 i
 * >Ec   RD: 192.168.255.10:11 ip-prefix 10.1.10.0/24
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.10:11 ip-prefix 10.1.10.0/24
                                192.168.254.9         -       100     0       65000 65105 i
 * >Ec   RD: 192.168.255.11:11 ip-prefix 10.1.10.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.11:11 ip-prefix 10.1.10.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 * >Ec   RD: 192.168.255.12:11 ip-prefix 10.1.10.0/24
                                192.168.254.11        -       100     0       65000 65106 i
 *  ec   RD: 192.168.255.12:11 ip-prefix 10.1.10.0/24
                                192.168.254.11        -       100     0       65000 65106 i
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
 * >Ec   RD: 192.168.255.7:11 ip-prefix 10.1.13.0/24
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:11 ip-prefix 10.1.13.0/24
                                192.168.254.7         -       100     0       65000 65103 i
 * >     RD: 192.168.255.8:11 ip-prefix 10.1.13.0/24
                                -                     -       -       0       i
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
 * >Ec   RD: 192.168.255.5:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.9:11 ip-prefix 172.31.253.14/31
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.9:11 ip-prefix 172.31.253.14/31
                                192.168.254.9         -       100     0       65000 65105 i
 * >Ec   RD: 192.168.255.10:11 ip-prefix 172.31.253.14/31
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.10:11 ip-prefix 172.31.253.14/31
                                192.168.254.9         -       100     0       65000 65105 i
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
Et1                            up             up                 P2P_LINK_TO_EAPI-SPINE1_Ethernet8
Et2                            up             up                 P2P_LINK_TO_EAPI-SPINE2_Ethernet8
Et3                            up             up                 
Et4                            up             up                 
Et5                            up             up                 SRV-POD03_Eth2
Et6                            up             up                 
Et7                            up             up                 
Et8                            up             up                 
Lo0                            up             up                 EVPN_Overlay_Peering
Lo1                            up             up                 VTEP_VXLAN_Tunnel_Source
Ma1                            up             up                 oob_management
Po5                            up             up                 SRV-POD03_PortChanne1
Vl110                          up             up                 PR01-DEMO
Vl113                          up             up                 PR01-DMZ
Vl1196                         up             up                 
Vl1199                         up             up                 
Vx1                            up             up                 EAPI-LEAF4A_VTEP
```
## show ip bgp summary vrf all

```
BGP summary information for VRF default
Router identifier 192.168.255.8, local AS number 65104
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  EAPI-SPINE1_Ethernet8    172.31.255.20    4  65001           4579      4546    0    0    2d13h Estab   20     20
  EAPI-SPINE2_Ethernet8    172.31.255.22    4  65001           4577      4551    0    0    2d13h Estab   20     20

BGP summary information for VRF TENANT_A_PROJECT01
Router identifier 192.168.255.8, local AS number 65104
Neighbor Status Codes: m - Under maintenance
  Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
```
## show ip interface brief

```
Address 
Interface       IP Address           Status     Protocol         MTU    Owner   
--------------- -------------------- ---------- ------------ ---------- ------- 
Ethernet1       172.31.255.21/31     up         up              1500            
Ethernet2       172.31.255.23/31     up         up              1500            
Loopback0       192.168.255.8/32     up         up             65535            
Loopback1       192.168.254.8/32     up         up             65535            
Management1     10.73.254.18/24      up         up              1500            
Vlan110         10.1.10.254/24       up         up              1500            
Vlan113         10.1.13.254/24       up         up              1500            
Vlan1196        unassigned           up         up              9164            
Vlan1199        unassigned           up         up              9164
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

 C        172.31.255.20/31 is directly connected, Ethernet1
 C        172.31.255.22/31 is directly connected, Ethernet2
 B E      192.168.0.2/32 [20/0] via 172.31.255.20, Ethernet1
 B E      192.168.0.3/32 [20/0] via 172.31.255.22, Ethernet2
 B E      192.168.1.1/32 [20/0] via 172.31.255.20, Ethernet1
 B E      192.168.1.2/32 [20/0] via 172.31.255.22, Ethernet2
 B E      192.168.252.2/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.252.3/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.253.2/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.253.3/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.254.3/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.254.5/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.254.7/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 C        192.168.254.8/32 is directly connected, Loopback1
 B E      192.168.254.9/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.254.11/32 [20/0] via 172.31.255.20, Ethernet1
                                   via 172.31.255.22, Ethernet2
 B E      192.168.255.3/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.255.4/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.255.5/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.255.6/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.255.7/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 C        192.168.255.8/32 is directly connected, Loopback0
 B E      192.168.255.9/32 [20/0] via 172.31.255.20, Ethernet1
                                  via 172.31.255.22, Ethernet2
 B E      192.168.255.10/32 [20/0] via 172.31.255.20, Ethernet1
                                   via 172.31.255.22, Ethernet2
 B E      192.168.255.11/32 [20/0] via 172.31.255.20, Ethernet1
                                   via 172.31.255.22, Ethernet2
 B E      192.168.255.12/32 [20/0] via 172.31.255.20, Ethernet1
                                   via 172.31.255.22, Ethernet2


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

 B E      1.1.1.0/24 [20/0] via VTEP 192.168.254.9 VNI 11 router-mac 0e:1d:c0:25:65:41
 B E      10.1.10.1/32 [20/0] via VTEP 192.168.254.3 VNI 11 router-mac 0e:1d:c0:f0:bd:d1
 B E      10.1.10.2/32 [20/0] via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 C        10.1.10.0/24 is directly connected, Vlan110
 B E      10.1.11.0/24 [20/0] via VTEP 192.168.254.3 VNI 11 router-mac 0e:1d:c0:f0:bd:d1
                              via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 B E      10.1.12.2/32 [20/0] via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 B E      10.1.12.0/24 [20/0] via VTEP 192.168.254.3 VNI 11 router-mac 0e:1d:c0:f0:bd:d1
                              via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 C        10.1.13.0/24 is directly connected, Vlan113
 B E      172.31.253.2/31 [20/0] via VTEP 192.168.254.3 VNI 11 router-mac 0e:1d:c0:f0:bd:d1
 B E      172.31.253.6/31 [20/0] via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 B E      172.31.253.14/31 [20/0] via VTEP 192.168.254.9 VNI 11 router-mac 0e:1d:c0:25:65:41
 B E      172.31.253.18/31 [20/0] via VTEP 192.168.254.11 VNI 11 router-mac 52:01:00:68:b4:46
```
## show lldp neighbors

```
Last table change time   : 2 days, 1:53:02 ago
Number of table inserts  : 39
Number of table deletes  : 20
Number of table drops    : 0
Number of table age-outs : 17

Port          Neighbor Device ID       Neighbor Port ID    TTL 
---------- ------------------------ ---------------------- --- 
Et1           EAPI-SPINE1              Ethernet8           120 
Et2           EAPI-SPINE2              Ethernet8           120 
Et5           SRV-POD03                Ethernet2           120 
Ma1           EAPI-AGG02               Management1         120 
Ma1           EAPI-AGG01               Management1         120 
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
 110    5001.0002.f6c5    DYNAMIC     Vx1        1       1:22:29 ago
 110    5001.0056.2a6e    DYNAMIC     Vx1        1       2:03:51 ago
1196    5201.0068.b446    DYNAMIC     Vx1        1       18:10:46 ago
1199    0c1d.c0e4.777b    DYNAMIC     Vx1        1       18:10:49 ago
1199    0e1d.c025.6541    DYNAMIC     Vx1        1       18:10:49 ago
1199    0e1d.c0a3.43e0    DYNAMIC     Vx1        1       18:10:37 ago
1199    0e1d.c0f0.bdd1    DYNAMIC     Vx1        1       18:10:49 ago
1199    5201.0068.b446    DYNAMIC     Vx1        1       18:10:46 ago
Total Mac Addresses for this criterion: 8

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
System MAC address:  0c1d.c0d2.9e98

Software image version: 4.24.0F
Architecture:           i686
Internal build version: 4.24.0F-16270098.4240F
Internal build ID:      da8d6269-c25f-4a12-930b-c3c42c12c38a

Uptime:                 0 weeks, 2 days, 18 hours and 31 minutes
Total memory:           2014424 kB
Free memory:            1084504 kB
```
## show vlan

```
VLAN  Name                             Status    Ports
----- -------------------------------- --------- -------------------------------
1     default                          active    Et3, Et4, Et6, Et7, Et8, Po5
110   PR01-DEMO                        active    Cpu, Po5, Vx1
113   PR01-DMZ                         active    Cpu, Po5, Vx1
201   B-ELAN-201                       active    Po5, Vx1
1196* VLAN1196                         active    Cpu, Vx1
1199* VLAN1199                         active    Cpu, Vx1

* indicates a Dynamic VLAN
```
## show vxlan address-table

```
Vxlan Mac Address Table
----------------------------------------------------------------------

VLAN  Mac Address     Type     Prt  VTEP             Moves   Last Move
----  -----------     ----     ---  ----             -----   ---------
 110  5001.0002.f6c5  EVPN     Vx1  192.168.254.5    1       1:22:20 ago
 110  5001.0056.2a6e  EVPN     Vx1  192.168.254.3    1       2:03:43 ago
1196  5201.0068.b446  EVPN     Vx1  192.168.254.11   1       18:10:37 ago
1199  0c1d.c0e4.777b  EVPN     Vx1  192.168.254.7    1       18:10:40 ago
1199  0e1d.c025.6541  EVPN     Vx1  192.168.254.9    1       18:10:40 ago
1199  0e1d.c0a3.43e0  EVPN     Vx1  192.168.254.5    1       18:10:29 ago
1199  0e1d.c0f0.bdd1  EVPN     Vx1  192.168.254.3    1       18:10:40 ago
1199  5201.0068.b446  EVPN     Vx1  192.168.254.11   1       18:10:37 ago
Total Remote Mac Addresses for this criterion: 8
```
## show vxlan vni

```
VNI to VLAN Mapping for Vxlan1
VNI         VLAN        Source       Interface           802.1Q Tag 
----------- ----------- ------------ ------------------- ---------- 
11          1199*       evpn         Vxlan1              1199       
13          1196*       evpn         Vxlan1              1196       
10110       110         static       Port-Channel5       110        
                                     Vxlan1              110        
10113       113         static       Port-Channel5       113        
                                     Vxlan1              113        
20201       201         static       Port-Channel5       201        
                                     Vxlan1              201        

Note: * indicates a Dynamic VLAN
```
## show vxlan vtep

```
Remote VTEPS for Vxlan1:
192.168.254.3
192.168.254.5
192.168.254.7
192.168.254.9
192.168.254.11
Total number of remote VTEPS:  5
```
