# What is Symmetric encryption ?

- Symmetric encryption is a method of encryption where the same secret key is used for both encrypting and decrypting data. It is the workspace of modern cryptography for securing large volumes of data because it is much faster than asymmetric encryption.

## Core Idea

- One shared key: Sender and reciever use the same secret key; If an attacker gets this key, confidentiality is broken.
- Plaintext ➡️ ciphertext ➡️ Plaintext: An algorithm transforms readable data (plaintext) into unreadable ciphertext using the key, and the same key reverses the transformation.
- Main challenge: Securely generating, sharing, and storing this key without exposing it is the hardest part operationally.

## How it works

- Key generation: A random key (eg: 128 or 256 bits) is generated using a secure random number generator.
- Encryption: The algorithm and key take the plaintext and output ciphertext that should look random without the key.
- Transfer: Ciphertext can be sent or stored; Even if intercepted, it should be useless without the key.
- Decryption: Reciever applies the same algorithm and the same key to recover the original plaintext.

## Algorithm & Types

- Block ciphers: Encrypt fixed-size blocks (eg: 128-bit blocks). Examples: AES (modern standard), Triple DES (legacy).
- Stream ciphers: Encrypt data bit-by-bit or byte-by-byte, often used for streaming data.
- AES: The most widely used symmetric algorithm today, with key sizes like 128 and 256 bits, and approved for high-security use.
