# What is an encryption mode.

AES by itself is not enough. AES is a block cipher, it encrypts fixed size blocks (128 bits). Encryption modes define how blocks are chained together to securely encrypt real-world data. Without a mode pattern leaks, security breaks and attacks become trivial.

## ECB (Electronic codebook)

In ECB each block is encrypted independently. here no chaining is used no IV is used no randomness and its considered as broken encryption mode. Lets say block size  is128 bits and plain text is a long message.

**Step-1: Split plaintext into blocks**

```bash
P1 | P2 | P3 | P4
```

**Step-2: Encrypt each block separately**

```bash
C1 = AES(K, P1)
C2 = AES(K, P2)
C3 = AES(K, P3)
C4 = AES(K, P4)
```

**Step-3: Concatenate ciphertext**

```bash
C1 | C2 | C3 | C4
```

🔴 Critical flaw:

```bash
If P1 == P3  →  C1 == C3
```

## CBC (Cipher Block Chaining)

ECB failed because same plaintext block generates same ciphertext block and this results in pattern leaks. CBC fixes this by chaining blocks together. Every plain text block depends on the previous ciphertext block. So repetition dies.

In CBC a new concept called IV (Initialization Vector) is introduced. IV is a random unpredictable 128-bit value. It is used only for the first block. It does not needto be secret. It must be unique and unpredictable.


