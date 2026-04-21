# The-Secure-Web-APl
A cybersecurity audit and remediation project. I used Wireshark to identify cleartext vulnerabilities in a Web API and implemented a secure environment using OpenSSL to generate 2048-bit RSA keys. Finalized a hardened TLS 1.3 server on Port 3443 to ensure complete data confidentiality.

# The Secure Web API - Cybersecurity Implementation

## Overview
This project demonstrates the transition of a web application from an insecure state (HTTP) to a hardened, production-ready environment (HTTPS/TLS 1.3). 

## Technical Features
* **Protocol:** TLS 1.3
* **Encryption:** RSA 2048-bit
* **Port:** 3443
* **Tools:** OpenSSL, Wireshark, Node.js

## Vulnerability Assessment
Using Wireshark, I identified that user credentials were being transmitted in cleartext. This project remediates that vulnerability by implementing a Secure Socket Layer (SSL) to encrypt all traffic.

## How to Run
1. Install OpenSSL.
2. Generate certificates: `openssl req -nodes -new -x509 -keyout server.key -out server.cert`
3. Run the server: `node server.js`
4. Access via `https://localhost:3443`

## 🛡️ Project Gallery

### Phase 1: Vulnerability Identification
![Wireshark Cleartext Audit](Cleartext%20Data.png)
*Evidence of credentials exposed in an insecure environment.*

### Phase 2: Cryptographic Implementation
![OpenSSL Command Line](Screenshot%202026-03-26%20214612.png)
*Generating 2048-bit RSA keys and launching the hardened server.*

### Phase 3: Traffic Validation
![TLS 1.3 Encryption](Application%20Data%20Gig.png)
*Verification of encrypted Application Data packets via TLS 1.3.*

### Phase 4: Header Verification
![HSTS Headers](HSTS%20Security%20Header%20Verification.png)
*Ensuring long-term security with HSTS (Strict-Transport-Security) headers.*
