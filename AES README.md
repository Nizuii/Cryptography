# What is AES.

- **AES** stands for **Advanced Encryption Standard**.
- It is a symmetric block cipher used to securely encrypt data.
- Because it is a symmetric block cipher it encrypts and decrypts the data using the same key.
- It is mainly used in HTTPS, Wi-Fi (WPA2/WPA3), disk encryption, ransomeware, cloud storage.
- AES replaced DES and is standardized by NIST.
- AES uses a fixed block size of 128 bits.
- It has a variant of 3 key sizes: 128, 192, 256 bits.

## AES High Level Flow

<img src="/images/aes.png">

**AES does not encrypt the whole file at once.**
It works like:

1. Split data into 128-bit blocks.
1. Each block goes through multiple rounds.
2. Each round scrambles data using the same secret key.
3. Output ➡️ encrypted ciphertext.

## AES Rounds

<table>
  <tr>
    <td><strong>AES Varient</strong></td>
    <td><strong>Key Size</strong></td>
    <td><strong>Rounds</strong></td>
  </tr>
  <tr>
    <td>AES-128</td>
    <td>128 bits</td>
    <td>10 rounds</td>
  </tr>
  <tr>
    <td>AES-192</td>
    <td>192 bits</td>
    <td>12 rounds</td>
  </tr>
  <tr>
    <td>AES-256</td>
    <td>256 bits</td>
    <td>14 rounds</td>
  </tr>
</table>

## What happens inside one AES round

### 1️⃣ SubBytes - Confusion

- Each byte replaced using a lookup table.
- Makes pattern disappear.
- Protects against statistical attacks.

### 2️⃣ ShiftRows – Diffusion

- Rows of the blocks are shifted left.
- Spreads byte influence across columns

### 3️⃣ MixColumns – Avalanche Effect

- Columns mixed using matrix math.
- One bit change → many bits change
