# What is ECC

- Elliptic Curve Cryptography (ECC) is a public key cryptography technique that provides secure encryption, key exchange and digital signatures using elliptic curve mathematics.
- It works by generating a private key as a random number and a public key by multiplying that number with a fixed point on an elliptic curve.
- This multiplication is easy to perform but extremely hard to reverse which gives ECC it's security.
- Because of this, ECC achieves strong security with much smaller keys compared to RSA, making it faster and more efficient.
- ECC is widely used in TLS/HTTPS, SSH, mobile devices and cryptocurrencies.

## How does ECC works internally?

- Internally ECC works by performing repeated operations on points defined on the elliptic curve.
- These operations behave like multiplication, where the private key controls how many times the operation is applied.
- The resut is a public key that cannot realistically be reversed to find the private key.

## What is ECDHA?

- ECDHA also know as Elliptic Curve Diffie Hellman is used for secure key exchange.
- It solves the problem of how does two parties create a shared secret key over an insecure netwoek.
- ECDHA allows 2 parties to agree on the same secret key without ever sending the secret itself even if an attacker is listening.
