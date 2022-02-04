# SRV-POD05-23 Commands Output

## Table of Contents

- [show lldp neighbors](#show-lldp-neighbors)
- [show ip interface brief](#show-ip-interface-brief)
- [show interfaces description](#show-interfaces-description)
- [show version](#show-version)
- [show running-config](#show-running-config)
## show interfaces description

```
Interface                      Status         Protocol           Description
Et1                            up             up                 Connected to L2LEAF01 Ethernet5
Et2                            up             up                 
Et3                            up             up                 
Et4                            up             up                 
Et5                            up             up                 
Et6                            up             up                 
Et7                            up             up                 
Et8                            up             up                 
Ma1                            up             up                 oob_management
Vl301                          up             up                 SVI for Central Routing Left side
Vl302                          up             up                 SVI for Central Routing Right side
```
## show ip interface brief

```
Address 
Interface       IP Address          Status      Protocol         MTU    Owner   
--------------- ------------------- ----------- ------------- --------- ------- 
Management1     10.73.254.45/24     up          up              1500            
Vlan301         10.3.1.1/24         up          up              1500            
Vlan302         10.3.2.1/24         up          up              1500
```
## show lldp neighbors

```
Last table change time   : 2 days, 1:58:07 ago
Number of table inserts  : 17
Number of table deletes  : 0
Number of table drops    : 0
Number of table age-outs : 0

Port          Neighbor Device ID       Neighbor Port ID    TTL 
---------- ------------------------ ---------------------- --- 
Et1           EAPI-L2LEAF01            Ethernet5           120 
Ma1           EAPI-BL01A               Management1         120 
Ma1           EAPI-LEAF4A              Management1         120 
Ma1           EAPI-LEAF1B              Management1         120 
Ma1           EAPI-CL01B               Management1         120 
Ma1           EAPI-L2LEAF01            Management1         120 
Ma1           EAPI-BL01B               Management1         120 
Ma1           EAPI-AGG01               Management1         120 
Ma1           EAPI-LEAF3A              Management1         120 
Ma1           EAPI-L2LEAF02            Management1         120 
Ma1           EAPI-CL01A               Management1         120 
Ma1           EAPI-AGG02               Management1         120 
Ma1           EAPI-SPINE2              Management1         120 
Ma1           EAPI-SPINE1              Management1         120 
Ma1           EAPI-LEAF1A              Management1         120 
Ma1           EAPI-LEAF2B              Management1         120 
Ma1           EAPI-LEAF2A              Management1         120
```
## show running-config

```
! Command: show running-config
! device: SRV-POD05-23 (vEOS-lab, EOS-4.26.2F)
!
! boot system flash:/vEOS-lab.swi
!
no aaa root
!
username admin privilege 15 role network-admin nopassword
username ansible privilege 15 role network-admin secret sha512 $6$Dzu11L7yp9j3nCM9$FSptxMPyIL555OMO.ldnjDXgwZmrfMYwHSr0uznE5Qoqvd9a6UdjiFcJUhGLtvXVZR1r.A/iF5aAt50hf/EK4/
username cvpadmin privilege 15 role network-admin secret sha512 $6$rZKcbIZ7iWGAWTUM$TCgDn1KcavS0s.OV8lacMTUkxTByfzcGlFlYUWroxYuU7M/9bIodhRO7nXGzMweUxvbk8mJmQl8Bh44cRktUj.
username demo privilege 15 role network-admin secret sha512 $6$Dzu11L7yp9j3nCM9$FSptxMPyIL555OMO.ldnjDXgwZmrfMYwHSr0uznE5Qoqvd9a6UdjiFcJUhGLtvXVZR1r.A/iF5aAt50hf/EK4/
!
daemon TerminAttr
   exec /usr/bin/TerminAttr -ingestgrpcurl=10.73.254.1:9910 -cvcompression=gzip -ingestauth=key, -smashexcludes=ale,flexCounter,hardware,kni,pulse,strata -ingestexclude=/Sysdb/cell/1/agent,/Sysdb/cell/2/agent -ingestvrf=MGMT -taillogs
   no shutdown
!
vlan internal order ascending range 1006 1199
!
transceiver qsfp default-mode 4x10G
!
service routing protocols model multi-agent
!
hostname SRV-POD05-23
ip name-server vrf MGMT 10.73.1.254
ip name-server vrf MGMT 10.73.254.253
!
spanning-tree mode mstp
!
clock timezone Europe/Paris
!
vlan 110
   name PR01-DEMO
!
vlan 111-112
   name PR01-TRUST
!
vlan 201
   name B-ELAN-201
!
vlan 301
   name CENTRAL_LAN_01
!
vlan 302
   name CENTRAL_LAN_02
!
vrf instance MGMT
!
vrf instance central_301
!
vrf instance central_302
!
management api http-commands
   no shutdown
   !
   vrf MGMT
      no shutdown
!
interface Ethernet1
   description Connected to L2LEAF01 Ethernet5
   logging event link-status
   switchport trunk allowed vlan 1-4000
   switchport mode trunk
   spanning-tree portfast
!
interface Ethernet2
!
interface Ethernet3
!
interface Ethernet4
!
interface Ethernet5
!
interface Ethernet6
!
interface Ethernet7
!
interface Ethernet8
!
interface Management1
   description oob_management
   vrf MGMT
   ip address 10.73.254.45/24
!
interface Vlan301
   description SVI for Central Routing Left side
   vrf central_301
   ip address 10.3.1.1/24
!
interface Vlan302
   description SVI for Central Routing Right side
   vrf central_302
   ip address 10.3.2.1/24
!
ip routing
no ip routing vrf MGMT
ip routing vrf central_301
ip routing vrf central_302
!
ip route vrf central_301 0.0.0.0/0 10.3.1.254
ip route vrf central_302 0.0.0.0/0 10.3.2.254
!
ntp local-interface vrf MGMT Management1
ntp server vrf MGMT 10.73.1.254
ntp server vrf MGMT 10.73.254.253 prefer
!
aaa authorization exec default local
!
management ssh
   vrf MGMT
      no shutdown
!
end
```
## show version

```
Arista vEOS-lab
Hardware version: 
Serial number: 8196EEAD601B80EC4C50874DA70571A9
Hardware MAC address: 5001.0073.5ad7
System MAC address: 5001.0073.5ad7

Software image version: 4.26.2F
Architecture: i686
Internal build version: 4.26.2F-23563874.4262F
Internal build ID: fa3a49f3-6093-4925-ad11-55fe15eac5ae
Image format version: 1.0

Uptime: 2 days, 2 hours and 56 minutes
Total memory: 2006804 kB
Free memory: 1105292 kB
```
