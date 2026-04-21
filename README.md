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
<img width="642" height="77" alt="image" src="https://github.com/user-attachments/assets/0da2de99-e896-4f2a-af32-70f20abfc319" />
*Evidence of credentials exposed in an insecure environment.*

### Phase 2: Cryptographic Implementation
<img width="365" height="220" alt="37ea2018-3c22-4d67-be4a-132ef77be5d2" src="https://github.com/user-attachments/assets/93181051-5c5a-48d3-ada3-737e9f137f2d" />
*Generating 2048-bit RSA keys and launching the hardened server.*

### Phase 3: Traffic Validation
<img width="1495" height="371" alt="9d4e939d-37bc-470b-b563-5c75ece6c61c" src="https://github.com/user-attachments/assets/919fb5ac-21a2-4f2e-a187-5e938da483b2" />
*Verification of encrypted Application Data packets via TLS 1.3.*

### Phase 4: Header Verification
<img width="340" height="653" alt="ac8e2170-f6a4-4862-bb58-f06ad6d3b084" src="https://github.com/user-attachments/assets/e39d77cf-4689-4268-aeba-a3461d0b5d12" />
*Ensuring long-term security with HSTS (Strict-Transport-Security) headers.*



[Cybersecurity Project 2_ Secure APL Lab (1).pdf](https://github.com/user-attachments/files/26915483/Cybersecurity.Project.2_.Secure.APL.Lab.1.pdf)




