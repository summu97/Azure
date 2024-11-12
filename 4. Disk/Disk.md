Locally-redundant storage (data is replicated within a single datacenter)
--
types:
* Standard SSD: E-disk tier
-- Best for web servers, lightly used enterprise applications and dev/test.
  
* Premium SSD: P-disk tier
-- Best for production and performance sensitive workloads.
  
* Premium SSD v2: p-disk tier
-- Best for production and performance-sensitive workloads that consistently require low latency and high IOPS and throughput.

* Standard HDD: S-disk tier
-- Best for backup, non-critical, and infrequent access.
  
* Ultra Disk: U-disk tier
-- Best for IO-intensive workloads such as SAP HANA, top tier databases (for example, SQL, Oracle), and other transaction-heavy workloads.

Zone-redundant storage (data is replicated to three zones).
--
types:
* Premium SSD (zone-redundant storage)
-- Best for the production workloads that need storage resiliency against zone failures.
  
* Standard SSD (zone-redundant storage)
-- Best for web servers, lightly used enterprise applications and dev/test that need storage resiliency against zone failures.
  
Key management: for encrypting data.
--
* Platform-managed key: encryption keys are managed by cloud.
* Customer-managed key: encryption keys are managed by us.
* Platform-managed and customer-managed keys: combo of both.

Networking:
--
Network access: Enable access to your managed disk either publicly using public IP addresses or privately using private endpoints.

* Enable public access from all networks.
-- Make this resource available publicly.
  
* Disable public access and enable private access:
-- Access your resource using private endpoints.
  
Shared disk:
--
-- Allow this disk to be attached to two or more virtual machines, depending on storage type and disk size. When shared disk is enabled host caching is unavailable. 

Data access authentication mode
--
-- Allow Data Access with Azure Active Directory Authentication for disk upload/export.

Host caching: If enabled the caching will store into physical server's storage - local hard drive or any other and this is mostly used for data drives.
--


