# EAPI-LEAF1B Commands Output

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
192.168.0.2 1343301590  371983514        NA multihop  08/27/21 17:14        NA  
192.168.0.3  839961824 3937651306        NA multihop  08/27/21 17:14        NA  

        LastDiag    State 
------------------- ----- 
   No Diagnostic       Up 
   No Diagnostic       Up
```
## show bgp evpn summary

```
BGP summary information for VRF default
Router identifier 192.168.255.4, local AS number 65101
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  EAPI-RS01                192.168.0.2      4  65000           2796      2970    0    0 18:09:44 Estab   77     77
  EAPI-RS02                192.168.0.3      4  65000           2750      3121    0    0 18:09:41 Estab   77     77
```
## show bgp evpn

```
BGP routing table information for VRF default
Router identifier 192.168.255.4, local AS number 65101
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
 * >     RD: 192.168.255.4:11 mac-ip 10110 5001.0056.2a6e
                                -                     -       -       0       i
 * >     RD: 192.168.255.4:11 mac-ip 10110 5001.0056.2a6e 10.1.10.1
                                -                     -       -       0       i
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
 * >     RD: 192.168.255.4:11 imet 10110 192.168.254.3
                                -                     -       -       0       i
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
 * >     RD: 192.168.255.4:11 imet 10111 192.168.254.3
                                -                     -       -       0       i
 * >Ec   RD: 192.168.255.5:11 imet 10111 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 imet 10111 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 imet 10111 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 imet 10111 192.168.254.5
                                192.168.254.5         -       100     0       65000 65102 i
 * >     RD: 192.168.255.4:11 imet 10112 192.168.254.3
                                -                     -       -       0       i
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
 * >     RD: 192.168.255.4:20201 imet 20201 192.168.254.3
                                -                     -       -       0       i
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
 * >Ec   RD: 192.168.254.8:1 ethernet-segment 0000:0000:0303:0202:0101 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.254.8:1 ethernet-segment 0000:0000:0303:0202:0101 192.168.254.8
                                192.168.254.8         -       100     0       65000 65104 i
 * >     RD: 192.168.255.4:11 ip-prefix 1.1.1.0/24
                                -                     -       100     0       65000 65105 ?
 * >Ec   RD: 192.168.255.9:11 ip-prefix 1.1.1.0/24
                                192.168.254.9         -       100     0       65000 65105 ?
 *  ec   RD: 192.168.255.9:11 ip-prefix 1.1.1.0/24
                                192.168.254.9         -       100     0       65000 65105 ?
 * >Ec   RD: 192.168.255.10:11 ip-prefix 1.1.1.0/24
                                192.168.254.9         -       100     0       65000 65105 ?
 *  ec   RD: 192.168.255.10:11 ip-prefix 1.1.1.0/24
                                192.168.254.9         -       100     0       65000 65105 ?
 * >     RD: 192.168.255.4:11 ip-prefix 10.1.10.0/24
                                -                     -       -       0       i
 *       RD: 192.168.255.4:11 ip-prefix 10.1.10.0/24
                                -                     -       100     0       ?
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
 * >     RD: 192.168.255.4:11 ip-prefix 10.1.10.2/32
                                -                     -       100     0       65000 65102 ?
 * >     RD: 192.168.255.4:11 ip-prefix 10.1.11.0/24
                                -                     -       -       0       i
 *       RD: 192.168.255.4:11 ip-prefix 10.1.11.0/24
                                -                     -       100     0       ?
 * >Ec   RD: 192.168.255.5:11 ip-prefix 10.1.11.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 ip-prefix 10.1.11.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 ip-prefix 10.1.11.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 ip-prefix 10.1.11.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >     RD: 192.168.255.4:11 ip-prefix 10.1.12.0/24
                                -                     -       -       0       i
 *       RD: 192.168.255.4:11 ip-prefix 10.1.12.0/24
                                -                     -       100     0       ?
 * >Ec   RD: 192.168.255.5:11 ip-prefix 10.1.12.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 ip-prefix 10.1.12.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 ip-prefix 10.1.12.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 ip-prefix 10.1.12.0/24
                                192.168.254.5         -       100     0       65000 65102 i
 * >     RD: 192.168.255.4:11 ip-prefix 10.1.12.2/32
                                -                     -       100     0       65000 65102 ?
 * >     RD: 192.168.255.4:11 ip-prefix 10.1.13.0/24
                                -                     -       100     0       65000 65104 ?
 * >Ec   RD: 192.168.255.7:11 ip-prefix 10.1.13.0/24
                                192.168.254.7         -       100     0       65000 65103 i
 *  ec   RD: 192.168.255.7:11 ip-prefix 10.1.13.0/24
                                192.168.254.7         -       100     0       65000 65103 i
 * >Ec   RD: 192.168.255.8:11 ip-prefix 10.1.13.0/24
                                192.168.254.8         -       100     0       65000 65104 i
 *  ec   RD: 192.168.255.8:11 ip-prefix 10.1.13.0/24
                                192.168.254.8         -       100     0       65000 65104 i
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
 * >     RD: 192.168.255.4:11 ip-prefix 172.31.253.2/31
                                -                     -       -       0       i
 *       RD: 192.168.255.4:11 ip-prefix 172.31.253.2/31
                                -                     -       100     0       ?
 * >     RD: 192.168.255.4:11 ip-prefix 172.31.253.6/31
                                -                     -       100     0       65000 65102 ?
 * >Ec   RD: 192.168.255.5:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.5:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 * >Ec   RD: 192.168.255.6:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 *  ec   RD: 192.168.255.6:11 ip-prefix 172.31.253.6/31
                                192.168.254.5         -       100     0       65000 65102 i
 * >     RD: 192.168.255.4:11 ip-prefix 172.31.253.14/31
                                -                     -       100     0       65000 65105 ?
 * >Ec   RD: 192.168.255.9:11 ip-prefix 172.31.253.14/31
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.9:11 ip-prefix 172.31.253.14/31
                                192.168.254.9         -       100     0       65000 65105 i
 * >Ec   RD: 192.168.255.10:11 ip-prefix 172.31.253.14/31
                                192.168.254.9         -       100     0       65000 65105 i
 *  ec   RD: 192.168.255.10:11 ip-prefix 172.31.253.14/31
                                192.168.254.9         -       100     0       65000 65105 i
 * >     RD: 192.168.255.4:11 ip-prefix 172.31.253.18/31
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
Et1                            up             up                 P2P_LINK_TO_EAPI-SPINE1_Ethernet2
Et2                            up             up                 P2P_LINK_TO_EAPI-SPINE2_Ethernet2
Et3                            up             up                 MLAG_PEER_EAPI-LEAF1A_Ethernet3
Et4                            up             up                 MLAG_PEER_EAPI-LEAF1A_Ethernet4
Et5                            up             up                 EAPI-AGG01_Ethernet2
Et6                            up             up                 
Et7                            up             up                 
Et8                            up             up                 
Lo0                            up             up                 EVPN_Overlay_Peering
Lo1                            up             up                 VTEP_VXLAN_Tunnel_Source
Ma1                            up             up                 oob_management
Po3                            up             up                 MLAG_PEER_EAPI-LEAF1A_Po3
Po5                            up             up                 EAPI-AGG01_Po1
Vl110                          up             up                 PR01-DEMO
Vl111                          up             up                 PR01-TRUST
Vl112                          up             up                 PR01-TRUST
Vl1188                         up             up                 
Vl1199                         up             up                 
Vl3010                         up             up                 MLAG_PEER_L3_iBGP: vrf TENANT_A_PROJECT01
Vl4093                         up             up                 MLAG_PEER_L3_PEERING
Vl4094                         up             up                 MLAG_PEER
Vx1                            up             up                 EAPI-LEAF1B_VTEP
```
## show ip bgp summary vrf all

```
BGP summary information for VRF default
Router identifier 192.168.255.4, local AS number 65101
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  EAPI-LEAF1A              172.31.253.2     4  65101           4352      4359    0    0    2d13h Estab   23     23
  EAPI-SPINE1_Ethernet2    172.31.255.4     4  65001           4578      4558    0    0    2d13h Estab   19     19
  EAPI-SPINE2_Ethernet2    172.31.255.6     4  65001           4577      4560    0    0    2d13h Estab   19     19

BGP summary information for VRF TENANT_A_PROJECT01
Router identifier 192.168.255.4, local AS number 65101
Neighbor Status Codes: m - Under maintenance
  Neighbor         V  AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  172.31.253.2     4  65101           5322      5300    0    0    2d13h Estab   11     11
```
## show ip interface brief

```
Address 
Interface       IP Address           Status     Protocol         MTU    Owner   
--------------- -------------------- ---------- ------------ ---------- ------- 
Ethernet1       172.31.255.5/31      up         up              1500            
Ethernet2       172.31.255.7/31      up         up              1500            
Loopback0       192.168.255.4/32     up         up             65535            
Loopback1       192.168.254.3/32     up         up             65535            
Management1     10.73.254.12/24      up         up              1500            
Vlan110         10.1.10.254/24       up         up              1500            
Vlan111         10.1.11.254/24       up         up              1500            
Vlan112         10.1.12.254/24       up         up              1500            
Vlan1188        unassigned           up         up              9164            
Vlan1199        unassigned           up         up              9164            
Vlan3010        172.31.253.3/31      up         up              1500            
Vlan4093        172.31.253.3/31      up         up              1500            
Vlan4094        172.31.253.1/31      up         up              1500
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

 C        172.31.253.0/31 is directly connected, Vlan4094
 C        172.31.253.2/31 is directly connected, Vlan4093
 C        172.31.255.4/31 is directly connected, Ethernet1
 C        172.31.255.6/31 is directly connected, Ethernet2
 B E      192.168.0.2/32 [20/0] via 172.31.255.4, Ethernet1
 B E      192.168.0.3/32 [20/0] via 172.31.255.6, Ethernet2
 B E      192.168.1.1/32 [20/0] via 172.31.255.4, Ethernet1
 B E      192.168.1.2/32 [20/0] via 172.31.255.6, Ethernet2
 B E      192.168.252.2/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.252.3/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.253.2/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.253.3/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 C        192.168.254.3/32 is directly connected, Loopback1
 B E      192.168.254.5/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.254.7/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.254.8/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.254.9/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.254.11/32 [20/0] via 172.31.255.4, Ethernet1
                                   via 172.31.255.6, Ethernet2
 B I      192.168.255.3/32 [200/0] via 172.31.253.2, Vlan4093
 C        192.168.255.4/32 is directly connected, Loopback0
 B E      192.168.255.5/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.255.6/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.255.7/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.255.8/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.255.9/32 [20/0] via 172.31.255.4, Ethernet1
                                  via 172.31.255.6, Ethernet2
 B E      192.168.255.10/32 [20/0] via 172.31.255.4, Ethernet1
                                   via 172.31.255.6, Ethernet2
 B E      192.168.255.11/32 [20/0] via 172.31.255.4, Ethernet1
                                   via 172.31.255.6, Ethernet2
 B E      192.168.255.12/32 [20/0] via 172.31.255.4, Ethernet1
                                   via 172.31.255.6, Ethernet2


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
 B E      10.1.10.2/32 [20/0] via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 C        10.1.10.0/24 is directly connected, Vlan110
 C        10.1.11.0/24 is directly connected, Vlan111
 B E      10.1.12.2/32 [20/0] via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 C        10.1.12.0/24 is directly connected, Vlan112
 B E      10.1.13.0/24 [20/0] via VTEP 192.168.254.8 VNI 11 router-mac 0c:1d:c0:d2:9e:98
                              via VTEP 192.168.254.7 VNI 11 router-mac 0c:1d:c0:e4:77:7b
 C        172.31.253.2/31 is directly connected, Vlan3010
 B E      172.31.253.6/31 [20/0] via VTEP 192.168.254.5 VNI 11 router-mac 0e:1d:c0:a3:43:e0
 B E      172.31.253.14/31 [20/0] via VTEP 192.168.254.9 VNI 11 router-mac 0e:1d:c0:25:65:41
 B E      172.31.253.18/31 [20/0] via VTEP 192.168.254.11 VNI 11 router-mac 52:01:00:68:b4:46
```
## show lldp neighbors

```
Last table change time   : 2:42:42 ago
Number of table inserts  : 40
Number of table deletes  : 19
Number of table drops    : 0
Number of table age-outs : 19

Port          Neighbor Device ID       Neighbor Port ID    TTL 
---------- ------------------------ ---------------------- --- 
Et1           EAPI-SPINE1              Ethernet2           120 
Et2           EAPI-SPINE2              Ethernet2           120 
Et3           EAPI-LEAF1A              Ethernet3           120 
Et4           EAPI-LEAF1A              Ethernet4           120 
Et5           EAPI-AGG01               Ethernet2           120 
Ma1           EAPI-LEAF4A              Management1         120 
Ma1           EAPI-AGG02               Management1         120 
Ma1           EAPI-AGG01               Management1         120 
Ma1           EAPI-BL01B               Management1         120 
Ma1           EAPI-BL01A               Management1         120 
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
 110    0c1d.c0f0.bdd1    STATIC      Po3
 110    5001.0002.f6c5    DYNAMIC     Vx1        1       1:22:03 ago
 110    5001.0056.2a6e    DYNAMIC     Po5        1       2:03:26 ago
 111    0c1d.c0f0.bdd1    STATIC      Po3
 112    0c1d.c0f0.bdd1    STATIC      Po3
 112    5001.0002.f6c5    DYNAMIC     Vx1        1       1:26:55 ago
1188    0c1d.c0f0.bdd1    STATIC      Po3
1188    5201.0068.b446    DYNAMIC     Vx1        1       14:05:40 ago
1199    0c1d.c0d2.9e98    DYNAMIC     Vx1        1       18:10:23 ago
1199    0c1d.c0e4.777b    DYNAMIC     Vx1        1       18:10:22 ago
1199    0c1d.c0f0.bdd1    STATIC      Po3
1199    0e1d.c025.6541    DYNAMIC     Vx1        1       18:10:22 ago
1199    0e1d.c0a3.43e0    DYNAMIC     Vx1        1       18:10:11 ago
1199    5201.0068.b446    DYNAMIC     Vx1        1       18:10:20 ago
3010    0c1d.c0f0.bdd1    STATIC      Po3
4093    0c1d.c0f0.bdd1    STATIC      Po3
4094    0c1d.c0f0.bdd1    STATIC      Po3
Total Mac Addresses for this criterion: 17

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
domain-id                          :          EAPI_LEAF1
local-interface                    :            Vlan4094
peer-address                       :        172.31.253.0
peer-link                          :       Port-Channel3
peer-config                        :          consistent
                                                        
MLAG Status:                      
state                              :              Active
negotiation status                 :           Connected
peer-link status                   :                  Up
local-int status                   :                  Up
system-id                          :   0e:1d:c0:f0:bd:d1
dual-primary detection             :            Disabled
dual-primary interface errdisabled :               False
                                                        
MLAG Ports:                       
Disabled                           :                   0
Configured                         :                   0
Inactive                           :                   0
Active-partial                     :                   0
Active-full                        :                   1

MLAG Detailed Status:
State                           :              secondary
Peer State                      :                primary
State changes                   :                      5
Last state change time          :   2 days, 13:13:37 ago
Hardware ready                  :                   True
Failover                        :                  False
Failover Cause(s)               :                Unknown
Last failover change time       :   2 days, 13:21:50 ago
Secondary from failover         :                  False
Peer MAC address                :      0c:1d:c0:f0:bd:d1
Peer MAC routing supported      :                  False
Reload delay                    :            300 seconds
Non-MLAG reload delay           :            330 seconds
Ports errdisabled               :                  False
Lacp standby                    :                  False
Configured heartbeat interval   :                4000 ms
Effective heartbeat interval    :                4000 ms
Heartbeat timeout               :               60000 ms
Last heartbeat timeout          :   2 days, 14:05:16 ago
Heartbeat timeouts since reboot :                      1
UDP heartbeat alive             :                   True
Heartbeats sent/received        :            59752/59305
Peer monotonic clock offset     :      -2.197488 seconds
Agent should be running         :                   True
P2p mount state changes         :                     10
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
System MAC address:  0c1d.c0f4.7b39

Software image version: 4.24.0F
Architecture:           i686
Internal build version: 4.24.0F-16270098.4240F
Internal build ID:      da8d6269-c25f-4a12-930b-c3c42c12c38a

Uptime:                 0 weeks, 2 days, 18 hours and 30 minutes
Total memory:           2014424 kB
Free memory:            1045804 kB
```
## show vlan

```
VLAN  Name                             Status    Ports
----- -------------------------------- --------- -------------------------------
1     default                          active    Et6, Et7, Et8, PEt6, PEt7, PEt8
110   PR01-DEMO                        active    Cpu, Po3, Po5, Vx1
111   PR01-TRUST                       active    Cpu, Po3, Po5, Vx1
112   PR01-TRUST                       active    Cpu, Po3, Po5, Vx1
201   B-ELAN-201                       active    Po3, Po5, Vx1
1188* VLAN1188                         active    Cpu, Po3, Vx1
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
 110  5001.0002.f6c5  EVPN     Vx1  192.168.254.5    1       1:21:44 ago
 112  5001.0002.f6c5  EVPN     Vx1  192.168.254.5    1       1:26:36 ago
1188  5201.0068.b446  EVPN     Vx1  192.168.254.11   1       14:05:22 ago
1199  0c1d.c0d2.9e98  EVPN     Vx1  192.168.254.8    1       18:10:04 ago
1199  0c1d.c0e4.777b  EVPN     Vx1  192.168.254.7    1       18:10:04 ago
1199  0e1d.c025.6541  EVPN     Vx1  192.168.254.9    1       18:10:04 ago
1199  0e1d.c0a3.43e0  EVPN     Vx1  192.168.254.5    1       18:09:52 ago
1199  5201.0068.b446  EVPN     Vx1  192.168.254.11   1       18:10:01 ago
Total Remote Mac Addresses for this criterion: 8
```
## show vxlan vni

```
VNI to VLAN Mapping for Vxlan1
VNI         VLAN        Source       Interface           802.1Q Tag 
----------- ----------- ------------ ------------------- ---------- 
11          1199*       evpn         Vxlan1              1199       
13          1188*       evpn         Vxlan1              1188       
10110       110         static       Port-Channel5       110        
                                     Vxlan1              110        
10111       111         static       Port-Channel5       111        
                                     Vxlan1              111        
10112       112         static       Port-Channel5       112        
                                     Vxlan1              112        
20201       201         static       Port-Channel5       201        
                                     Vxlan1              201        

Note: * indicates a Dynamic VLAN
```
## show vxlan vtep

```
Remote VTEPS for Vxlan1:
192.168.254.5
192.168.254.7
192.168.254.8
192.168.254.9
192.168.254.11
Total number of remote VTEPS:  5
```
