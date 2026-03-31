# NTLM Authentication

NTLM (New Technology LAN Manager) is a suite of Microsoft security protocols intended to provide authentication, integrity, and confidentiality to users. While it has been largely superseded by Kerberos, it remains a critical component for backward compatibility in many Windows environments.

---

###  Technical Specifications
* **Mechanism:** Challenge-Response Handshake.
* **Storage:** Credentials are stored as NTHashes in the LSASS memory process and the SAM database.
* **Versions:** Includes LAN Manager (legacy/insecure), NTLMv1, and NTLMv2 (most common).

###  The Three-Way Handshake
1. **NEGOTIATE_MESSAGE:** The client sends a request to the server to establish an authenticated session.
2. **CHALLENGE_MESSAGE:** The server responds with a 16-byte random number, known as a "nonce" or challenge.
3. **AUTHENTICATE_MESSAGE:** The client encrypts the challenge with its password hash and sends the result back to the server.

###  Security Considerations
* **Pass-the-Hash (PtH):** Because NTLM uses hashes for authentication, an attacker who captures an NTHash can authenticate to resources without ever knowing the cleartext password.
* **NTLM Relaying:** Attackers can intercept an NTLM authentication challenge and "relay" it to another machine on the network to gain unauthorized access.
* **Vulnerability:** Compared to Kerberos, NTLM is considered significantly less secure and is a primary target during internal penetration tests.
