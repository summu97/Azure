VNet is a regional resource
--
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

Important points about Virtual Network Gateways
--
* It supports both S2S & P2S VPN Gateway.
* VPN solution provides encrypted tunnels for secure communication.
* VPN solution requires authentication ensuring only authorized induviduals with VPN credentials to connect.
* Encrypts all communication via tunneling.









NOTE:
--
* By default all the VM's that you create will have "outbound" internet access(You have access to internet from inside. But outside people cant access you). No need of any additional configuration.
* They charge according to data we transfer.
* Subnet division: When you reserve an IP set, 5 IP's in that set are reserved for other uses.
* EX: 10.0.1.0/24 - you get 256 IP's in which 5 are reserved and 251 are for your use.
    * 10.0.1.0 - For identifying the network.
    * 10.0.1.1 - For Gateway.
    * 10.0.1.2 & 10.0.0.3 - For DNS server.
    * 10.0.1.255 - For Broadcast IP.

* Every class of IP has set of IP's reserved for Private-IP.
    * Class A: 10 series
    * Class B: 172 series
    * Class C 192 series
