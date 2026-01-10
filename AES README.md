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

**AES doesnot encrypt the whole file at once.**
It works like:

1. Split data into 128-bit blocks.
1. Each block goes through multiple rounds.
2. Each round scrambles data using the same secret key.
3. Output ➡️ encrypted ciphertext.
