# What is encryption

Encryption is the cryptographic method of converting a plain readable data into unreadable cipher data. There are mainly 2 types of encryption:
1. **Symmetric Encryption**
2. **Asymmetric Encryption**

## Symmetric Encryption

- Symmetric encryption only use a single key for both encryption and decryption.
- Symmetric encryption is fast.
- It is efficeint for large data.
- But key sharing is a problem.
- Example: AES & DES.

## Asymmetric Encryption

- Asymmetric encryption uses a pair of key instead of a single key, one public key to encrypt and one private key to decrypt.
- Asymmetric encryption solves the key distribution problem faced by symmetric encryption.
- It is very slow compared to symmetric encryption.
- It is not for bulk data.
- It is slow because of heavy math.

## Hybrid Encryption.

- AES is fast but needs shared keys, RSA/ECC is secure but slow.
- So inorder to solve this hybrid encryption is used.
- Work flow:

  1. Client generates random symmetric session key.
  1. Client encrypts session key using servers public key.
  1. Server decrypts it using private key.
  1. Both sides now share the same AES key.
  1. All data encrypted using AES.
 
- Hybrid encryption uses asymmetric cryptgraphy to securely exchange a symmetric key, then use symmetric encryption for faster data transfer.

> TLS uses RSA or ECC on;y during the handshake to exchange a session key, and then uses AES to encrypt all appication data.
