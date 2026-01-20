# Report: Analysis of SSL/TLS Vulnerabilities.

This report outlines critical vulnerabilities related to the SSL/TLS protocols. The goal of TLS is to provide Confidentiality (encryption), Integrity (no tampering), and Authentication (proof of identity). The following vulnerabilities and flaws undermine one or more of these guarantees.

## 1. Analysis of Mentioned Vulnerabilities

### A. Weak Cipher Suites.

**What it is**: A cipher suite is the recipie of the algorithms used for the TLS connection. It specifies four things:

- Key Exchange (e.g, RSA, ECDHE)
- Authentication (e.g, RSA, ECDSA)
- Bulk Encryption (e.g, AES, 3DES, RC4)
- Hashing (e.g, SHA-256, SHA-1, MD5)

**What makes it weak**: A cipher suite is weak if any of its components are broken.

- Weak Encryption: Using RC4 or DES/3DES (Vulnerable to Sweet32 attacks).  
- Weak Hashing: Using MD% or SHA-1 (vulnerable to collision attacks).  

**Root Cause**: Cryptographic Obsolescence.

### B. Lack of Forward Secrecy

- **What it is**: The abscence of forward secrecy makes TLS session vulnerable to decryption later.  
- **Without Forward Secerecy (e.g, TLS_RSA)**: If an attacker records traffic and later obtains the private key, all past sessions can be decrypted.  
- **With Forward Secrecy (e.g, TLS_ECDHE)**: Each session uses ephemeral keys that are discarded afterward, preventing retrospective decryption.  
- **Root Cause**: Static key exchange (RSA).  

### C. Weak Signature Algorithms

- **What it is**: Certificates signed used obsolete hashes like SHA-1.  
- **How it works**: SHA-1 collisions allow attackers to forge certificates that browsers may trust.  
- **Root Cause**: Cryptographic Obsolescence.  

## Additional SSL/TLS Vulnerabilities

### A. Poodle Attack (Padding Oracle On Downgraded Legacy Encryption)

- It is a man-in-the-middle attack that targets SSL 3.0, typically CBC mode and the weakness was no integrity check on padding.
- **How the attack works:**

  **1. Downgrade Attack**

  - Attacker forces browser +server to fall back from TLS to SSL 3.0.
  - This happens because browsers used to allow fallback for compatibility.
 
  **2. MITM Position**

  - Attacker sits between victim and server.
 
  **3. Block Manipulation**

  - Attacker modifies ciphertext blocks in HTTPS traffic.
 
  **4. Padding Oracle Leak**

  - Server responds differently depending on padding corectness.
  - Attacker learns whether a guess was right or wrong.
 
  **5. Byte-by-Byte decryption**

  - Repeated requests slowly reveal session cookies and authentication tokens.

### B. SWEET32 Attack

- Sweet32 is a cryptographic attack against 64-bit block ciphers used in TLS. It mainly targets 3DES & Blowfish.
- These ciphers are not broken cryptographically but the problem is their block size.

- **Core idea**

  - Block ciphers work by encrypting fixed size blocks.
  - With 64-bit blocks there are only

    > 2⁶⁴ possible block values

  - By birthday paradox, collisions become likely after about:
 
    > 2³² blocks (~34 GB of data)

  - When blocks repeat: pattern emerges, information leaks, parts of plaitext like cookies can be recovered.

### Heartbleed (CVE-2014-0160)

- Heartbleed was an implementation bug in OpenSSL's Heartbeat extension.
- Heartbeak is just a ping.

  > **Client**: "Hey server, are you alive?
  > Here is 3 bytes `ABC`
  > Please sent them back."

- Server should reply:

  > "Yep here is `ABC` i.e, 3 bytes"

- The prolem was when client sends 2 things **1. Data `ABC`** and **2. Length filed "I have sent 50,000 bytes".
- 
