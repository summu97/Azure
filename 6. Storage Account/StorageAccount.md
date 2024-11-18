Performance:
--
* Standard: for normal use
* Premium: for high IOPS

Premium account type:
--
* Block blobs: 4.7TB size, made up of blocks of data that can be managed individually.
* File shares: Best for enterprise or high performance applications that need to scale.
* Page blobs: best for random read and write operations. Up to 8TB size. Serves as Disk for VM-storing VHD's.

Different storage options a storage account offers:
--
* Containers: Just like folders- to store files and folders(Block level storage).
* File shares: Centralizes point to store files that are accessed by other machines(File level storage).
* Tables: To store un-structured data. no SQL(cosmos DB).
* Queues: Event based data machine. Notification service.

Note: 
--
* To access all these locally we need "Storage Explorer" tool.

Redundancy: How your data must replicate.(Replication kind)
--
* Locally-redundant storage(LRS): Low cost, maintains 3 copies in single data center.
* Geo-redundant-storage(GRS): Recommended for backup scenarios, Data replicated in secondary region. Maintains copies in Primary and Secondary regions.
* Zone-redundant storage(ZRS): For high availability scenarios, follows synchronous replication. Maintains copies in different availability zones.
* Geo-zone-redundant storage(GZRS): Combo of GRS and ZRS.

Access tier:
--
* Hot: For frequently accessed data.
* Cool: For infrequently accessed data.
* Cold: Rarely accessed data and backup scenarios.

Managed disks: Advanced topic than Storage accounts
--
* You directly create a file & attach to VM.

Note:
--
* Storage account follow HTTP/S protocol.
* When you create a storage account a unique URL is generated and use it to access storage account.
* Blob: Binary Large Object.
* All disks come undermanaged entities. By default disks have Availability set option applied.

Availability set:
--
* Data center level high availability.
* When ever you create a VM or disk, it will be created on data rack. If the rack fails immediately new resources come to action & creates ne resource on it.
