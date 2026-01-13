# Difference Between Block Cipher & Stream Cipher

## What is Confusion & Diffusion?

- **Confusion**: Making the relationship between the encryption key and the ciphertext as complex as possible. Relationship between cipher text and plain text is obscured. If we are given with the cipher text obviously there will be no information or no details that can be guessed about the plain text, the key what encryption algorithm does the sender has used inorder to generate the cipher text and if all details are hidden then we can say there exist confusion property.

- **Diffusion**: Making each plaintext bit affect as many ciphertext bits as possible. 1 bit change in plain text, significally effect on cipher text.

## What is Stream Cipher?

- Each plaintext digit is encrypted one at a time with the corresponding digit of the keystream, to give a digit of the ciphertext stream.
<img width="1386" height="461" alt="image" src="https://github.com/user-attachments/assets/53886d26-9cc3-4aa9-a33e-be9fc24c1b98" />
