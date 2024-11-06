Azure Firewall: Network level security(Global Security).
-- Applied to entire V-Net.
--
NSG(Network Security Group): Resource level security-Ports-Inbound/Outbound rules.
--
NSG types:
--
* Subnet level NSG: Applied to all instances in subnet.
* Instance level NSG: Aplied to induvidual instances in subnet.
  
ASG(Application Security Group): Enhances security capabilities of NSG.
--
* Applies only to group of servers.
* Using ASG we can group VM's and apply firewall rules only to that particular group.

Route Table: One who maintains routes.
--
* Default routes: System routes- created when a new subnet is created.

Routes: Define where the traffic goes.
--

Load Balancer Types:
--
* App gateway(Layer-7-HTTP/S): Applied for outside traffic.
* To differenciate the traffic path/host based.
* Azure Load Balancer(Layer-4-TCP/UDP): Applied for inside traffic.

V-Net peering: Adds routes from one vnet to other.
--
* Adds routes between V-Net's-We modify route tables of vnet's.
  
V-Net Gateway: To allow V-Net's to communicate with each other.
--
VPN Gateway: Similar to V-Net peering
--
* For communication between V-Net on azure with any other network privately.

Site to Site VPN Gateway(Network to network)
--
* To connect On-premises network with Azure VNet.

Point to Site VPN Gateway
--
* To connect induvidual devices(Laptops/Computers) to Azure virtual network.

Point to Point
--
* Direct link between two devices/locations, allowing then to communicate privately without going through any other networks.
* Connects two end points.

