Key Vault: Stores Keys, Secrets, Certificates.
--
Available Tiers:
--
* Standard: Excrypts using software based keys.
* Premium: Uses Hardware Security Module(HSM) that increases security.

Architecture:
--
* Management Plane: Where we create, delete, retrieve key vault & its properties.
* Data Plane: Add, delete, modify secrets, keys, certificates.

For Authentication to key vault: Use Azure AD for Users & Applications.
--
For Authorization to key vault: Use RBAC for Management Plane & key vault access policies or RBAC for Data Plane.
--
General work flow:
--
* User--AD--Authentication--Authorization--(RBAC--Management Plane)--(RBAC or Key vault access policies--Data Plane)

Soft delete: To prevent unwanted deleteion.
--
Purge protection: Prevents data from deleting right away when enabled retention period or soft delete.
--
NOTE:
-- 
* Access to key vault is controlled at two iterfaces- Management Plane & Data Plane.
* Practice key vault recovery operations on regular basics.
                                         
