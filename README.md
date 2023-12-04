Routers Configuration (A&B)



A#show run
Building configuration...

Current configuration : 681 bytes
!
version 12.4
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname A
!
!
!
!
!
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
!
!
!
!
!
!
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 ip address 10.1.1.1 255.255.255.0
 duplex auto
 speed auto
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial0/1/0
 ip address 192.168.1.1 255.255.255.0
 clock rate 2000000
!
interface Vlan1
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 192.168.2.2 
!
ip flow-export version 9
!
!
!
!
!
!
!
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end


---------------------------------------------------------------------------------
B#show run
Building configuration...

Current configuration : 1177 bytes
!
version 15.1
no service timestamps log datetime msec
no service timestamps debug datetime msec
no service password-encryption
!
hostname B
!
!
!
!
!
!
!
!
no ip cef
no ipv6 cef
!
!
!
!
license udi pid CISCO2811/K9 sn FTX10174J76-
!
!
!
!
!
!
!
!
!
!
!
spanning-tree mode pvst
!
!
!
!
!
!
interface FastEthernet0/0
 ip address 10.1.1.1 255.255.255.0
 duplex auto
 speed auto
!
interface FastEthernet0/1
 no ip address
 duplex auto
 speed auto
 shutdown
!
interface Serial1/0
 ip address 192.168.1.2 255.255.255.0
!
interface Serial1/1
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial1/2
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial1/3
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial1/4
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial1/5
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial1/6
 no ip address
 clock rate 2000000
 shutdown
!
interface Serial1/7
 no ip address
 clock rate 2000000
 shutdown
!
interface Vlan1
 no ip address
 shutdown
!
ip classless
ip route 0.0.0.0 0.0.0.0 192.168.2.2 
!
ip flow-export version 9
!
!
!
!
!
!
!
line con 0
!
line aux 0
!
line vty 0 4
 login
!
!
!
end
