# What is Cryptography

- Cryptography is the science of securing information so only the intented people can read it.
- Example: I am writing a letter and sealing it. Only the right person has the key to open it.
- Without cryptography, sending data online be like shouting and revealing all our secrets in a crowded room.
- Cryptography plays a huge role in everyday life ex:

  - **Online banking**: Keeps credit cards and transaction data safe.
  - **Messaing apps**: Whatsapp, Signal and Telegram use strong end to end encryption so that unauthorized persons can't access or see the messages.
  - **Passwords**: Stores passwords securely in databases so that attackers can't read them.
 
- Core principles of cryptography.

  1. **Confidentiality**: Only the intended person can read the message.
  2. **Integrity**: Ensures the message isn't altered along the way.
  3. **Authentication**: Confirms the identity of sender and reciever.
  4. **Non-repudiation**: Prevents someone from denying they sent a message.

## Difference between Encryption, Encoding & Hashing

1. **Encryption**: Encryption is like locking a letter in a box and sending it. Only the person with the correct key can open it.
  - Encryption is necessary in messaging application like whatsapp, banking websites, etc...
  - Encrption is reversible and needs the key to reverse it.
  - Used in: HTTPS websites, Messaging apps, VPN's, Disk encryption.

2. **Encoding**: Encoding is like translating english into morse code. So anyone who knows morse code can read it.
  - Encoding is necessary ex: computers store data in binary.
  - Encoding is also reversible. Encoding does not provide any security because unline encryption it does not have any keys to secure the data.
  - It is mainly used for compatibility.
  - Its mainly used in emails (attachments), images & videos, URL's etc...
