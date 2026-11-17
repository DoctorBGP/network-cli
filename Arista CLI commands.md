**Arista CLI commands list.** <br>
!------------------------------------------------! <br>
! To see MP-BGP routes from all routers, vrf, for every RD: <br>
**show bgp vpn-ipv4** <br>

! To see MP-BGP routes from a specific router, vrf on that router - specific RD. <br>
! Like to see BGP routes, AS-path, LP, Cluster-List etc: <br>
**show bgp vpn-ipv4 rd 65500:11111** <br>

! To see MP-BGP routes from all neighbors, but for a specific prefix: <br>
**show bgp vpn-ipv4 10.0.0.1/32**