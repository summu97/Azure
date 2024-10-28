Azure Firewall: Network level security(Global Security).
-- Applied to entire V-Net.
--
NSG(Network Security Group): Resource level security-Ports-Inbound/Outbound rules.
NSG types:
-- Subnet level NSG: Applied to all instances in subnet.
-- Instance level NSG: Aplied to induvidual instances in subnet.
--
ASG(Application Security Group): Enhances ssecurity capabilities of NSG.
-- Applies only to group of servers.
-- Using ASG we can group VM's and apply firewall rules only to that particular group.
--
Route Table: One who maintains routes.
-- Default routes: System routes.
--
Routes: Define where the traffic goes.
--
LoadBalancer Types:
-- App gateway(Layer-7-HTTP/S).
  -- To differenciate the traffic path/host based.
-- Azure Load Balancer(Layer-4-TCP/UDP).
--
V-Net peering: Adds routes from one vnet to other.
-- We modify route tables of vnet's.
--
V-Net Gateway: To allow V-Net's to communicate with each other.
--
VPN Gateway: Similar to V-Net peering
-- For communication between V-Net on azure with any other network privately.
--
