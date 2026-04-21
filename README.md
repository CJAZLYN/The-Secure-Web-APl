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
