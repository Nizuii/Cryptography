# What is encryption

Encryption is the cryptographic method of converting a plain readable data into unreadable cipher data. There are mainly 2 types of encryption:
1. **Symmetric Encryption**
2. **Asymmetric Encryption**

## Symmetric Encryption

- In symmetric encryption the encription key that is used to encrypt and decrypt is the same. Basically here only one key is used for both purpose of encryption and decryption.
- A good example of this is Ceasar Cipher. However now a days we commonly use an encryption algorithm called AES which has 1.1579 x 10^77 possible combinations or 256 bits.

## Asymmetric Encryption

- In asymmetric encryption it uses a pair of keys. A public key and a private key.
- The public key is the one we send to whoever needs to communicate with us securely.
- The private key should remain private to ourself.
- These 2 keys are linked together mathematically.
- Example: If someone wants to communicate with me, they must encrypt their plain text with my public key. When i recieve that encrypted message i must decrypt it using my private key.
- This method is slow compared to symmetric encryption.
