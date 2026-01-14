# Difference between AES & DES?

Both AES & DES are symmetric block cipher encryption. So lets differentiate how AES and DES works and what is the difference betwwen both.

## What is AES?

- AES stands for **Advanced Encryption Standard**. It is a symmetric block cipher used everywhere: TLS, disk encryption, Wi-Fi, password managers, cloud storage etc...
- Core properties of AES:

  - AES encryption cipher type is symmetric block cipher.
  - Its block size is 128 bits meaning it will divide the data into 128 bit blocks.
  - Key sizes supported by AES are: 128 bits, 192 bits, 256 bits.
  - Depending upon the key size the rounds ofencryption is determined.
  - Its structure is substitution-permutation network (SPN)

### AES State - Heart of AES

- AES converts 128 bits (16 bytes) of plaintext into 4x4 byte matrix called the state.

  Example plain text
  ```bash
  Plaintext (128 bits):
  32 88 31 e0 43 5a 31 37 f6 30 98 07 a8 8d a2 34
  ```

  State matrix (column major order):

  ```bash
  [ 32 43 f6 a8 ]
  [ 88 5a 30 8d ]
  [ 31 31 98 a2 ]
  [ e0 37 07 34 ]
  ```
### High-Level AES Flow

AES encryption has 3 phases:

**Phase 1: Initial Round**

AddRoundKey

**Phase 2: Main Rounds (Repeated)**

- SubBytes
- ShiftRows
- MixColumns
- AddRoundKey

**Phase 3: Final Round**

- SubBytes
- ShiftRows
- AddRoundKey
