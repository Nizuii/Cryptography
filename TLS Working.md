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

#### ServerHello

Server replies with:

- Chosen TLS version
- Chosen cipher suite
- Servers Random

Now both sides have client random and server random.
