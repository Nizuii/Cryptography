# Mod 26 Challenge

<img width="1908" height="1011" alt="image" src="https://github.com/user-attachments/assets/bc0ad8b3-cf94-46c1-b382-fc3ee3b7c78c" />


So inorder to complete this challenge we need to have a basuc understanding on what ROT-13 is.

## So what is ROT-13?

ROT13 is a simple letter substitution cipher that replaces a letter with the 13th letter after it in the Latin alphabet. It is a special case of the Caesar cipher which was developed in ancient Rome, and used by Julius Caesar in the 1st century BC. ROT13 may be referred to as Rotate13, ROT-13, rotate by 13 places.

<img width="250" height="145" alt="image" src="https://github.com/user-attachments/assets/0715ab33-1804-4d50-8d65-367f1bffb753" />

**Example:**

Input:

```bash
ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz
```

Output:

```bash
NOPQRSTUVWXYZABCDEFGHIJKLMnopqrstuvwxyzabcdefghijklm
```

## About the challenge

So in the CTF challenge we are assigned with a cipher text `cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_45559noq}` and our task is to decrypt it using any ROT-13 online decrypting algorithm or build one using python. Here i've used a python script to decrypt the cipher text.

<img width="1908" height="1011" alt="image" src="https://github.com/user-attachments/assets/445f5a79-9ad7-4622-84e4-80a3bbcd9efb" />

So after decrypting the cipher text i've got the original plain text flag that is `picoCTF{next_time_I'll_try_2_rounds_of_rot13_45559abd}`.
