Cisco CLI commands list.
!------------------------------------------------!
! To see routes from a specific router in MP-BGP network. From a router with the RD 65500:1111
! There could be many similar routes from a different routers in MP-BGP network, like redundant routers, but one can see routes from a specific router.
show ip bgp vpnv4 rd 65500:1111

! See BGP routes in a specific VRF. VRF name is VRF-TEST
show ip bgp vpnv4 vrf VRF-TEST 10.0.0.0/8
