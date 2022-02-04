# SRV-POD01 Commands Output

## Table of Contents

- [show lldp neighbors](#show-lldp-neighbors)
- [show ip interface brief](#show-ip-interface-brief)
- [show interfaces description](#show-interfaces-description)
- [show version](#show-version)
- [show running-config](#show-running-config)
## show interfaces description

```
Interface                      Status         Protocol           Description
Et1                            up             up                 
Et2                            up             up                 
Et3                            up             up                 
Et4                            up             up                 
Et5                            up             up                 
Et6                            up             up                 
Et7                            up             up                 
Et8                            up             up                 
Ma1                            up             up                 oob_management
Vl110                          up             up                 SVI for Tenant A vlan 110
Vl112                          up             up                 SVI for Tenant A vlan 112
Vl201                          up             up                 SVI for Tenant B vlan 201
```
## show ip interface brief

```
Address 
Interface       IP Address          Status      Protocol         MTU    Owner   
--------------- ------------------- ----------- ------------- --------- ------- 
Management1     10.73.254.41/24     up          up              1500            
Vlan110         10.1.10.1/24        up          up              1500            
Vlan112         10.1.12.1/24        up          up              1500            
Vlan201         10.2.1.1/24         up          up              1500
```
## show lldp neighbors

```
Last table change time   : 2 days, 2:52:22 ago
Number of table inserts  : 17
Number of table deletes  : 0
Number of table drops    : 0
Number of table age-outs : 0

Port          Neighbor Device ID       Neighbor Port ID    TTL 
---------- ------------------------ ---------------------- --- 
Et1           EAPI-AGG01               Ethernet3           120 
Ma1           EAPI-CL01A               Management1         120 
Ma1           EAPI-LEAF2A              Management1         120 
Ma1           EAPI-LEAF2B              Management1         120 
Ma1           EAPI-L2LEAF02            Management1         120 
Ma1           EAPI-L2LEAF01            Management1         120 
Ma1           EAPI-SPINE1              Management1         120 
Ma1           EAPI-LEAF3A              Management1         120 
Ma1           EAPI-SPINE2              Management1         120 
Ma1           EAPI-AGG02               Management1         120 
Ma1           EAPI-CL01B               Management1         120 
Ma1           EAPI-AGG01               Management1         120 
Ma1           EAPI-LEAF4A              Management1         120 
Ma1           EAPI-LEAF1B              Management1         120 
Ma1           EAPI-BL01A               Management1         120 
Ma1           EAPI-BL01B               Management1         120 
Ma1           EAPI-LEAF1A              Management1         120
```
## show running-config

```
! Command: show running-config
! device: SRV-POD01 (vEOS, EOS-4.24.0F)
!
! boot system flash:/vEOS-lab.swi
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
hostname SRV-POD01
ip name-server vrf MGMT 10.73.1.254
ip name-server vrf MGMT 10.73.254.253
!
ntp local-interface vrf MGMT Management1
ntp server vrf MGMT 10.73.1.254
ntp server vrf MGMT 10.73.254.253 prefer
!
spanning-tree mode mstp
!
aaa authorization exec default local
!
no aaa root
!
username admin privilege 15 role network-admin nopassword
username ansible privilege 15 role network-admin secret sha512 $6$Dzu11L7yp9j3nCM9$FSptxMPyIL555OMO.ldnjDXgwZmrfMYwHSr0uznE5Qoqvd9a6UdjiFcJUhGLtvXVZR1r.A/iF5aAt50hf/EK4/
username cvpadmin privilege 15 role network-admin secret sha512 $6$rZKcbIZ7iWGAWTUM$TCgDn1KcavS0s.OV8lacMTUkxTByfzcGlFlYUWroxYuU7M/9bIodhRO7nXGzMweUxvbk8mJmQl8Bh44cRktUj.
username demo privilege 15 role network-admin secret sha512 $6$Dzu11L7yp9j3nCM9$FSptxMPyIL555OMO.ldnjDXgwZmrfMYwHSr0uznE5Qoqvd9a6UdjiFcJUhGLtvXVZR1r.A/iF5aAt50hf/EK4/
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
vrf instance tenant_a_110
!
vrf instance tenant_a_112
!
vrf instance tenant_b_201
!
interface Ethernet1
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
   ip address 10.73.254.41/24
!
interface Vlan110
   description SVI for Tenant A vlan 110
   vrf tenant_a_110
   ip address 10.1.10.1/24
!
interface Vlan112
   description SVI for Tenant A vlan 112
   vrf tenant_a_112
   ip address 10.1.12.1/24
!
interface Vlan201
   description SVI for Tenant B vlan 201
   vrf tenant_b_201
   ip address 10.2.1.1/24
!
ip routing
no ip routing vrf MGMT
ip routing vrf tenant_a_110
ip routing vrf tenant_a_112
ip routing vrf tenant_b_201
!
ip route vrf tenant_a_110 0.0.0.0/0 10.1.10.254
ip route vrf tenant_a_112 0.0.0.0/0 10.1.12.254
!
management api http-commands
   no shutdown
   !
   vrf MGMT
      no shutdown
!
management ssh
   vrf MGMT
      no shutdown
!
end
```
## show version

```
vEOS
Hardware version:    
Serial number:       
System MAC address:  5001.0056.2a6e

Software image version: 4.24.0F
Architecture:           i686
Internal build version: 4.24.0F-16270098.4240F
Internal build ID:      da8d6269-c25f-4a12-930b-c3c42c12c38a

Uptime:                 0 weeks, 2 days, 2 hours and 55 minutes
Total memory:           2014424 kB
Free memory:            1145328 kB
```
