# What is Hashing?

Hashing is the process of converting data of any size into a fixed size output using the mathematical formulas known as hash functions. Hashed data cannot be reversed back to the original data. Hashing dies not provide encyption or secrecy. Its main purpose is has the data changed or not.

## Hash Properties

### 1️⃣ Pre-image Resistance

- Pre-image resistance means in a hash function means its computionally infeasible to find the original input when we aare given with only the fixed-size hash output.
- This makes the function one way function; this is crucial for security, preventing attackers from reversing hashes to find data like passwords.

### 2️⃣ Second Pre-image Resistance

- A second pre-image resistance hash function makes it computionally infeasible to find a different input that produces the same hash output as a given specific input.
- its hard to find x1 such that H(x) = H(X1) when x is known.
