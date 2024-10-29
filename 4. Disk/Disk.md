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
-- ZRS is not available when availability zone is selected.
  
* Standard SSD (zone-redundant storage)
-- ZRS is not available when availability zone is selected.
  
Key management: for encrypting data.
* Platform-managed key: encryption keys are managed by cloud.
* Customer-managed key: encryption keys are managed by us.
* Platform-managed and customer-managed keys: combo of both.
--
