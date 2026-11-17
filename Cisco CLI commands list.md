Cisco CLI commands list.
!------------------------------------------------!
# To see routes from a specific router in MP-BGP network. From a router with the RD 65500:1111
# There could be many similar routes from a different routers in MP-BGP network, like redundant routers, but one can see routes from a specific router.
show ip bgp vpnv4 rt 65500:1111
