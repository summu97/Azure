Why Peering?
--
* For communication between different virtal Networks.

* Once peered, the virtual networks appear to be one.
* Traffic remain private between VNet's.
* No public Internet, gateways or encryption is required for communication between the resources in the networks.

Types of VNet peering:
--
* Global VNet Peering: Connects Azure virtual networks in different regions.
* Virtual Network Peering: Connects Azure virtual networks in same regions.

NOTE:
--
* Global peering not possible with GOVT cloud, only Regional peering is allowed.
* Peering is not transitive, i.e you can only communicate with VNet that is directly connected not the peer VNet's of peers.
