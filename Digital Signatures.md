# What is Digital Signature?

A digital signature is a cryptographic mechanism that proves three things at once.

1. Authenticity - Who sent the data.
1. Integrity - Whether the data was modified.
1. Non-repudiation - The sender cannot deny sending it.

**The core idea**: A digital signature  is created by hashing the message and encrypting the hash using the sender's private key.

## How a digital algorithm works?

<img width="617" height="380" alt="image" src="https://github.com/user-attachments/assets/fcd652b0-f855-46a7-801a-5e2ed7cad2dc" />

### 1️⃣ Sender side (Signing)

1. The sender writes a message

```bash
"Pay Nizam $500,000"
```

2. The message is hashed

```bash
Hash("Pay Nizam $500,000") ➡️ 9f3a...
```

3. The hash is encrypted with the sender's private key

```bash
Encrypt(hash, private_key) ➡️ Digital Signature
```
4. The sender sends the original message and digital signature.

### 2️⃣ Receiver side (Verification)

1. Reciever hashes the recieved message.
1. Reciever decrypts the signature using the sender's public key.
1. Compares both hashes and if hashes match thern message is authentic and untampered. And if not then message is altered or sender is fake.

## Real World Scenerio.

Lets walkthrough a real worl scenerio of a user communicating with web app.

### User logs into a secure web app (HTTPS)

<img width="2918" height="1667" alt="image" src="https://github.com/user-attachments/assets/306aa2da-f5bd-4c35-86cf-4ef916ee042f" />

**Actors**:
- User's Browser.
- Web Server.
- Certificate Authority (CA).

### Phase 0: Before the user even visits the site (Setup)

The server already has:

- A public / private key pair.
- A TLS certificate.

  - Contains servers public key
  - Digitally signed by a CA

Phase 1: User types https://www.example.com

This phase uses asymmetric cryptography + digital signatures.

**Step 1: Server sends its certificate**

The browser recieves:

- Servers public key
- CA's digital signature on the certificate.

**Step 2: Browser verifies the certificate**



