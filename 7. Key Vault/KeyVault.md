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
For Authorization to key vault: Use RBAC for
