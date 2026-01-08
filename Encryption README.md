# What is Encryption?

- Encryption is a method of converting readable data into an unreadable form so that only someone with the correct key can read it again.
- In cybersecurity, it is one of the core ways to protect confidentiality of data in storage and in transit.

## Simple idea of encryption.

- You start with readable data, called plain text (ex: Hello)
- An algorithm plus a secret value called a key transforms this plain text into scrambled ciphertext that looks random.
- To get the original data back, the correct key is used with the decryption process: without that key, the ciphertext should be practically impossible to understand.

## Why encryption is used

- **Privacy**: Prevents attackers, ISPs or others from reading messages, web traffic or stored files if they intercept or steal them.
- **Data protection**: If a laptop, database or backup driver is stolen, full-disk or database encryption can keep the data confidential without the decryption key.
- **Compliance**: Many laws and standards (like GDPR-style privacy rules) explicitly recommend or require encryption for sensitive personal information.

## Main types of encryption

### 1. Symmetric Encryption

- Same key is used for both encryption and decryption.
- Very fast; used for bulk data (ex: AES-128/192/256 for files, VPN's, HTTPS data after handshake).

### 2. Asymmetric Encrytpion

- Uses a public key to encrypt and a mathematically linked private key to decrypt.
- Enables secure key exchange and digital signatures; used in TLS handshakes, SSHz, PGP, etc...

## Symmetric VS Asymmetric

Symmetric encryption uses one shared key for both encryption and decryption, while asymmetric encryption uses a key pair: One public key and one private key. Symmetric is faster and better for bulk data; asymmetric is slower but solves secure key exchange and enables digital signatures.
