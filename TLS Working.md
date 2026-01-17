# What is TLS

TLS or Transport Layer Security is a protocol that ensures secure communication over an insecure network (Internet). TLS provides three guarentees:

1. Confidentiality.
2. Integrity.
3. Authentication.

TLS does this by combining asymmetric cryptography + symmetric cryptography + hashing + MAC.

## 1. TLS 1.2 Working

TLS 1.2 has 2 phases:

1. Handshake Phase ➡️ Agree on keys & verify identity.
1. Secure data phase ➡️ Exchange encrypted application data.

### TLS 1.2 Handshake

TLS Handshake be like: Lets agree on a shared sectret without sending it, and use that secret for the fast encrypted communication.

<img width="600" height="600" alt="image" src="https://github.com/user-attachments/assets/1def4e84-98bc-413c-b497-8e76a322ee13" />

#### 1️⃣ ClientHello

The client says:

- TLS version supported (TLS 1.2)
- Cipher suits it supports (ex: TLS_RSA_WITH_AES_128_CBC_SHA256)
- Client Random (32 bytes of randomness)

#### 2️⃣ ServerHello

Server replies with:

- Chosen TLS version
- Chosen cipher suite
- Servers Random

Now both sides have client random and server random.

#### 3️⃣ Server Certificate (AUTHENTICATION)

The server sends its X.509 certificate, containing:

- Servers public key
- Domain name
- CA signature

The client:

- Verifies CA signature
- Verifies domain name
- Verifies certificate validity

If verification fails connection is aborted.

#### 4️⃣ Key Exchange (The Critical Part)

This depends on the cipher suite.

**Case A: RSA key Exchange**

- Client generates a Pre-Master Secret
- Encrypts it using server's RSA public key
- Sends it to the server.

Only the server can decrypt it (private key).

#### 5️⃣ Key Derivation (Both sides do this independently)

Now both client & server have:

- Pre-Master Secret
- Client Random
- Server Random

They run a PRF (Pseudo-Random Function) to derive:

- Symmetric encryption key (AES)
- MAC key
- Initialization vectors

Now both sides have same key, no transmission.

#### 6️⃣ ChangeCipherSpec

Client says:

> From now on, everything is encrypted.

Server replies with the same.

#### 7️⃣ Finished Messages

Both sides send an encrypted hash of the handshake.

This proves:

- No one modified the handshake
- Keys match on both ends

Handshake complete.
