# LDAP (Lightweight Directory Access Protocol)

LDAP is the standard protocol used to query and manage the Active Directory database. It serves as the primary "language" for accessing directory services and objects.

---

###  Technical Specifications
* **Standard Port:** 389 (Unencrypted)
* **Secure Port:** 636 (LDAPS - LDAP over SSL/TLS)

###  Key Functions
* **Authentication:** Verifying user credentials against the centralized directory.
* **Directory Queries:** Searching for specific objects such as users, groups, printers, or shared folders.
* **Object Management:** Facilitating the addition, deletion, or modification of objects within the AD hierarchy.

###  Security Considerations
* **Cleartext Risk:** Standard LDAP (389) transmits data unencrypted, making it vulnerable to credential sniffing.
* **Reconnaissance:** Attackers use LDAP queries to map out the domain structure and identify high-value targets like Domain Administrators.
