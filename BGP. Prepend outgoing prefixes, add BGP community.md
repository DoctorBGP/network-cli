### Prepend outgoing prefixes to ISP or eBGP neighbor. Add BGP community to advertised prefixes.
### Also prepending incoming prefixes. Config example to avoid, poison the specific neighbour/ISP.

**On Arista or Cisco:**
```cisco
conf t
!
# My prefixes:
ip prefix-list PF-BGP-ISP-XXX-INET-OUT seq 10 permit 10.100.0.0/24
!
# Advertise prefixes with community
# Prepend outgoing prefixes
route-map RM-BGP-ISP-XXX-INET-OUT permit 10
 match ip address prefix-list PF-BGP-ISP-XXX-INET-OUT
 set as-path prepend 65500 65500 65500
 set community 64999:10 additive
!
route-map RM-BP-ISP-XXX-INET-OUT deny 100
!
# Prepend incoming prefixes.
route-map RM-BGP-ISP-XXX-TNET-IN permit 10 
 set as-path prepend 64999 64999 64999
!
# update ISP XXX config with the RMs:
router bgp 65500
 neighbor 10.1.1.1 description ISP-XXX
 neighbor 10.1.1.1 route-map RM-BP-ISP-XXX-INET-IN in 
 neighbor 10.1.1.1 route-map RM-BP-ISP-XXX-INET-OUT out
!
end
wr
```
