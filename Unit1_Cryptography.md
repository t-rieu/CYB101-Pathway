# Cryptography: Encryption/Decryption
- **Ciphers** are algorithms used to encrypt and decode messages.
- **Encryption key -** a random string of bits used to scramble and unscramble data.

**Encryption methods**
  - **Symmetric -** uses one private key to encrypt and decrypt data.
    - Widely used today.
    - Comes in two forms: **stream ciphers** (encrypts bit by bit) and **block ciphers** (Data is transformed into blocks of data and is encrypted block by block).
    - Uses two cipher techniques: **substitution** and **transposition**.
      - **Substitution -** substitutes different letters, numbers, or other characters for each character in the original text.
      - **Transposition -** Scrambles the position of characters without changing the characters themselves.
  
     **Examples of substitution ciphers:**
    > ***1. Monoalphabetic cipher:*** letters of plaintext have a one-to-one relationship with letters of ciphertext. *Eg. Caesar cipher: a simple shifting method where letters are shifted by some fixed number. For example, a shift of 2 means A encodes as C.*

  

  - **Asymmetric -** uses a pair of a public key (encrypting) and a private key (decrypting).
    - Widely used today.
    - Only authorized users have access to the private key but the public key is accessible by anyone.

