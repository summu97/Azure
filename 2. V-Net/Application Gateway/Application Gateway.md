Application Gateway: Web Application Load-Balancer
--
* Operates at Layer-7
* SSL/TLS termination at gateway(add more security)
* Auto Scaling
* Zone redundancy: Multiple copies of LB gets created across zones, but only one copy is visible. If any of LB at a zone gets failed, then other comes to action.
* Web Application Firewall(WAF)
* Session affinity: Forwards yser requests to same server
* Path based routing
* Session based routing
* Additional functionality: Can route traffic to on prem servers if VPN or any other connection is established

Note: If SSL offloading is enabled then the user requests are encrypted till LB and un-encrypts the data and sends to backend-pool.
--

For Azure LB only Availability set option available but for Application Gateway Zone redundancy available.
--

Tier: defines the pricing and also the features we need
--

NOTE:
--
* For App Gateway we need separate Subnet.
* Main difference between Azure LB and App Gateway is App Gateway only workd with HTTP/HTTPS and also has more setting options
* replacement of App Gateway--App services
