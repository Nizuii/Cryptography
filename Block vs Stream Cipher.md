# Symmetric encryption algorithms are categorized into 2: Block & Stream ciphers. 

Block ciphers encrypt data in blocks of set lengths, while stream ciphersdo not and instead encrypt plain text one byte at a time.

## What are Block Ciphers?

- Block ciphers convert data in plaintext into ciphertext in fixed size blocks.
- The block size generally depends on the encryption scheme and is usually in octaves (64-bit or 128-bit blocks)
- If the plaintext length is not a multiple of 8, the encryption scheme uses padding to ensure complete blocks.
- For instance, to perform 128-bit encryption on a 150-bit plaintext, the encryption scheme provides two blocks, 1 with 128 bits and one with the 22 bits left. 106 Redundant bits are added to the last block to make the entire block equal to the encryption scheme’s ciphertext block size.
