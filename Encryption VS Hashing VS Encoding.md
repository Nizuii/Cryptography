# Difference between Encryption, Hashing and Encoding

Encryption, hashing, and encoding are three different methods of cryptography each serving a unique purpose. 

- **Encryption** protects confidentiality and is reversible.
- **Hashing**: protects integrity, and is ireversible.
- **Encoding** ensures data compatibility and formatting and is reversible.

## What is Encryption?

Encryption is the process of converting readable data into unreadable cipher text or format. Encrypted text can only be reversed to original plain data with correct key. It is used to protect sensitive data during storage and transmission.

- Reversible with a key.
- Protects confidentiality.
- Used in secure communication and data protection.
- Algorithms include AES, RSA and BlowFish

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20210115134029/EncryptionvsEncodingvsHashing1-660x280.jpg">

## What is Hashing?

Hashing converts data into fixed length ireversible cipher value called hash. It is used for integrity checks, storage and fast look ups.

- One way transformation.
- Ensures Integrity (detects changes).
- Fixed length regardless of the data size.
- Algorithms include SHA-256, MD5.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20210115190611/NewProject-660x123.jpg">

## What is Encoding?

Encoding transforms data into a different format for safe transmission or storage. It is not a security mechanism and is fully reversible without a key.

- Reversible without a key.
- Ensures data compatibility and formatting.
- Used for data transport, not security.
- Examples include Base64, URL encoding, ASCII.

**Example**:

Input:
```bash
echo "hello" | base64
```
Output:
```bash
aGVsbG8K
```
