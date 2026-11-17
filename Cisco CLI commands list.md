Cisco CLI commands list. <br>
!------------------------------------------------!  <br>
! To see routes from a specific router in MP-BGP network. From a router with the RD 65500:1111  <br>
! There could be many similar routes from a different routers in MP-BGP network, like redundant routers, but one can see routes from a specific router.  <br>
**show ip bgp vpnv4 rd 65500:1111**  <br>

! See BGP routes in a specific VRF. VRF name is VRF-TEST. <br>
! Shown: BGP prefixes, best and alternative paths, AS-PATH, LP, Communities, RD/RT etc <br>
**show ip bgp vpnv4 vrf VRF-TEST 10.0.0.0/8 longer-prefixes** <br>
