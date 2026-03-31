# DNS in Active Directory

DNS (Domain Name System) is the backbone of an Active Directory environment. It is responsible for resolving hostnames to IP addresses and is a mandatory requirement for the domain to function correctly.

---

###  Technical Specifications
* **Default Port:** 53 (TCP/UDP)
* **Role:** Acts as the "map" for the network, allowing clients to locate specific resources and services.

###  Key Functions in AD
* **Locating Domain Controllers:** Clients use DNS queries to find the Domain Controllers (DCs) required for authentication and Group Policy updates.
* **Service Location (SRV) Records:** AD relies heavily on SRV records to identify the specific hosts that provide services like LDAP and Kerberos.
* **Active Directory Integration:** In most enterprise setups, DNS is integrated directly into AD, allowing for secure dynamic updates and replication across all DCs.

###  Security Considerations
* **Reconnaissance:** If misconfigured (e.g., allowing unauthorized Zone Transfers), an attacker can easily map out every host, server, and IP address in the domain.
* **Service Spoofing:** Attackers may attempt to manipulate DNS records to redirect legitimate traffic to malicious servers.
* **Enumeration:** Tools like `nslookup` or `dig` are commonly used by professionals to verify the existence of internal resources and identify potential targets.
