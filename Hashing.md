# What is Hashing?

Hashing is the process of converting data of any size into a fixed size output using the mathematical formulas known as hash functions. Hashed data cannot be reversed back to the original data. Hashing dies not provide encyption or secrecy. Its main purpose is has the data changed or not.

## Hash Properties

### 1️⃣ Pre-image Resistance

- Given only a hash, it should be computionally infeasible to find any input that produces that hash.
- Formally:

  ```bash
  Given h = H(x)
  Find x such that H(x) = h
  ```

- In simple words: If we put a food in a blender, we get smoothie and we cannot un-blend it. The information is destroyed, not hidden.
- **Example**: A server stores passwords:

  ```bash
  H("password123") = 5e884898...
  ```

  Anattacker steals database.

  If pre-image resistance is strong:

  - Attacker must guess passwords
  - Trying billions of inputs (bruteforce).
 
  If it's weak:

  - Attacker computes the roiginal password directly.
 
### 2️⃣ Second Pre-image Resistance

- Given a specific input x1, it should be infeasible to find a different input x2 such that:

  ```bash
  H(x1) = H(x2)
  ```

  with x1 ≠ x2.
