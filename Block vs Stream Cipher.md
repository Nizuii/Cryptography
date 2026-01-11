# Symmetric encryption algorithms are categorized into 2: Block & Stream ciphers. 

Block ciphers encrypt data in blocks of set lengths, while stream ciphersdo not and instead encrypt plain text one byte at a time.

## What are Block Ciphers?

- Block ciphers convert data in plaintext into ciphertext in fixed size blocks.
- The block size generally depends on the encryption scheme and is usually in octaves (64-bit or 128-bit blocks)
- If the plaintext length is not a multiple of 8, the encryption scheme uses padding to ensure complete blocks.
- For instance, to perform 128-bit encryption on a 150-bit plaintext, the encryption scheme provides two blocks, 1 with 128 bits and one with the 22 bits left. 106 Redundant bits are added to the last block to make the entire block equal to the encryption scheme’s ciphertext block size.
- There was a problem in block cipher that if we encrypt the same message with the same key again and again, we will get the same locked result again and again and this results in preedictability.
- Inorder to solve this issue a clever tric was added called IV (Initialization Vector).
- Think of IV as a random starting twist.

  - It’s a random or pseudorandom value
  - It is only used at the beginning at block 1.
  - Its job is to make sure encryption looks different every time.
 
### Block Cipher Operation Blocks

1. **Electronic Codebook (ECB)**: In this mode plain text messages are divided into blocks where encryption is applied to each block seperately. The ECB cipher mode does not hide data pattern because it lacks diffusion and is not recommended for security frameworks.
1. **Cipher Block Chaining Block**: This mode combhines cipher text from previous block with current plain text block using XOR operation before performing the encryption. An IV is applied to the first plaintext block in a CBC mode to ensure uniqueness.
1. **Galois/Counter Mode (GCM)**: It is a modern encryption mode that provides both confidentiality and integrity at the same time. It encrypts data using counter mode with a unique nonce, and simultaneously generates an authentication tag to detect any tampering. Because it’s fast, secure, and hard to misuse, GCM is widely used in TLS/HTTPS and secure APIs.
