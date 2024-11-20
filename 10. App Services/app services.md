App Service: Two types of hosting environments.
--
* App service plan: Basic level.
* App service environment: More features than app service plan.

For communication between apps, apps service plan & apps installed on VM's within VNet has two ways.
--
* Establishing P2S VPN from source to destination.
* Service plan and apps installed in same VNet.

For communication between apps, app service & apps installed on-prem has two ways:
--
* S2S VPN connection between VNet to On-prem.
* Hybrid connection between App service plan & On-prem network.

For Scalling:
--
* Automation
* Auto scalling

For Performance & High availability:
--
* Content distribution network(CDN): Mainly used if want to deliver content with optimum performance(fast deliver)
* Traffic manager

For backup:
--
* App service backup.

For monitoring & Diagnostics:
--
* App service diagnostics
* Application insights
* Alerts

For security:
--
* SSL Certificates
* Active Directory
* Key Vault

Pricing Tier:
--
* Shared Compute: Along with our application other user applications also run.
* Dedicated: Basic, Standard, Premium, Premium v2.
* Isolated: On dedicated VNet.
* Consumption: Only to deploy azure functions. Scales the functions dynamically if load increases.
