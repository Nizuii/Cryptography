# Difference Between Block Cipher & Stream Cipher

## What is Confusion & Diffusion?

- **Confusion**: Making the relationship between the encryption key and the ciphertext as complex as possible. Relationship between cipher text and plain text is obscured. If we are given with the cipher text obviously there will be no information or no details that can be guessed about the plain text, the key what encryption algorithm does the sender has used inorder to generate the cipher text and if all details are hidden then we can say there exist confusion property.

- **Diffusion**: Making each plaintext bit affect as many ciphertext bits as possible. 1 bit change in plain text, significally effect on cipher text.

## What is Stream Cipher?

- Each plaintext digit is encrypted one at a time with the corresponding digit of the keystream, to give a digit of the ciphertext stream.
- In stream cipher the length of the input is either a bit or a byte.
- In stream cipher the principle used is confusion.
- Stream ciphers are faster.
- Encryption modes used are CFB and OFB.
- XOR operation is used in decryption.
- Ex: Vernam Cipher.
<img width="1386" height="461" alt="image" src="https://github.com/user-attachments/assets/53886d26-9cc3-4aa9-a33e-be9fc24c1b98" />

## What is Block Cipher?

- A block cipher is a deterministic algorithm operating on fixed length groups of bits called blocks.
- In block cipher it is going to take a block of input. This block can be 64 bits or 128 bits, this is actually depending on the algorithm it use.
- In block both confusion and diffusion are used.
- Block ciphers are slower.
- Encryption modes used are ECB and CBC.
- Reverse of encryption is used to decrypt.
- Ex: DES, AES
<img width="1363" height="453" alt="image" src="https://github.com/user-attachments/assets/cd4539eb-772a-4490-97bd-103881e6d8f0" />
