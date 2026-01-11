# What is Cryptography

- Cryptography is the science of protecting information using mathematical techniques to ensure confidentiality, integrity and authentication.
- Basically what cryptography does is it turns readable data into unreadable format. Preventing it from unauthorized acess and tampering.

## Features of Cryptography.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20250804175653069660/features_of_cryptography.webp">

1. **Confidentiality**: Information can only be accessed by the person by whom the information is intended to. No outsiders can acess or understand.
1. **Integrity**: The information cannot be modified in storage or transition between sender and reciever.
1. **Authentication**: Identities of sender and reciever are confirmed,
1. **Non-Repudiation**: The creator or sender of the information cannot deny his intention to send information at a later stage.
1. **Adaptability**: Cryptography continuously evolves to stay ahead of security threats and technological advancements.
1. **Interoperability**: Cryptography allows for secure communication between different systems and platforms.

## Types of Cryptography

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20250203153143550520/Types-of-Cryptography.webp">

There are mainly 3 types of cryptography.

1. Symmetric Cryptography
1. Asymmetric Cryptography
1. Hash Functions

### 1. Symmetric Cryptography

Symmetric cryptography is an encryption system where the sender and the reciecver of a message uses a single common key to encrypt and decrypt messages.

- Symmetric key cryptography is faster and simpler but the problem is that the sender and reciever somehow exchange this key securely.
- The most popular symmetric key cryptography systems are Data Encryption Systems (DES) and Advanced Encryption Systems (AES).

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20240409123909/Private-Key-Encryption-(1).png">

### 2. Hash Functions

Hash functions does not require a key, instead  they use mathematical algorithms to convert messages of any arbitrary length into a fixed-length output, known as a hash value or digest. Hash functions are designed to be one-way, meaning the original input cannot be derived from the output.

### 3. Asymmetric Cryptography

In Asymmetric Key Cryptography a pair of keys is used to encrypt and decrypt information. A sender's public key is used for encryption and a receiver's private key is used for decryption. Public keys and Private keys are different. Even if the public key is known by everyone the intended receiver can only decode it because he holds his private key. The most popular asymmetric key cryptography algorithm is the RSA algorithm.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20240409125853/Asymmetric-.webp">
