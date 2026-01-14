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

### 1️⃣ AddRoundKey (XOR With Key)

This is the only step that uses the key directly.

```bash
State ⊕ RoundKey = New State
```

- XOR each byte with the corresponding key byte.
- Without this AES is reversible by anyone.

### 1️⃣ SubBytes - Confusion

- Each byte in the state is replaced using a lookup table called S-Box.

  <img width="1063" height="341" alt="image" src="https://github.com/user-attachments/assets/eeb2c0ff-e2f9-455b-bb2c-c0cc5bb4d8fb" />

- An S-Box is just atable with 256 entries (0x00 ➡️ 0xFF). Each possbile byte value: 00, 01, 02, ..., FF maps to another byte.
- Example: if input byte is 0x52 output byte os 0xED.
- This mapping is fixed, public, same for every AES implementation and same in every round.
- Here is what happens to state in SubBytes:

  AES state - 4x4 bytes.

  Before SubBytes:

  ```bash
  [ 19 a0 9a e9 ]
  [ 3d f4 c6 f8 ]
  [ e3 e2 8d 48 ]
  [ be 2b 2a 08 ]
  ```

  After SubBytes:

  ```bash
  [ d4 e0 b8 1e ]
  [ 27 bf b4 41 ]
  [ 11 98 5d 52 ]
  [ ae f1 e5 30 ]

### 2️⃣ ShiftRows - Horizontal Difussion

- In horizontal difussion rach row of the state is rotated left.

<table>
  <tr>
    <td><b>Row</b></td>
    <td><b>Shift</b></td>
  </tr>
  <tr>
    <td>Row 0</td>
    <td>0 bytes</td>
  </tr>
  <tr>
    <td>Row 1</td>
    <td>1 byte</td>
  </tr>
  <tr>
    <td>Row 2</td>
    <td>2 bytes</td>
  </tr>
  <tr>
    <td>Row 3</td>
    <td>3 bytes</td>
  </tr>
</table>
