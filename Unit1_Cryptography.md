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
    > 
    > ***2. Polyalphabetic cipher:*** a single plaintext letter has multiple substitution alphabets. *Eg. Vingenère cipher: uses a keyword used on the Vingenère table to encrypt and decrypt.*
    > 
    > ***3. Base64: encrypted texts end with a '=='.***
    >
    > ***4. Advanced Encryption Standard (AES): Currently one of the most widely used symmetric algorithms.***
    >
    > ***5. Blowfish (64-bit)/Twofish (128-bit): Alternative block ciphers to DES.***

    **Example of transposition ciphers:**
    > ***Rail fence cipher:*** rearranges text in a “wave” pattern and condenses the letters on the same rows.

  - **Asymmetric -** uses a pair of a public key (encrypting) and a private key (decrypting).
    - Widely used today.
    - Only authorized users have access to the private key but the public key is accessible by anyone.
   
    **Example of asymmetric algorithms:**
    > ***1. Rivest Shamir Adleman (RSA)***
    > ***2. Digital Signature Standard (DSS)***

- **[Magic number](https://gist.github.com/leommoore/f9e57ba2aa4bf197ebc5) -** the first bits of a file that uniquely identify the file type.
- **Hashing -** a one-way mathematical function that transforms data into a value or key that cannot be reversed or decoded.
  - Common hashing algorithms: MD5, SHA1, SHA2
- **Salting -** a random string added to a password before it’s hashed.
  - Helps enhance security.
  - The salt should be stored with the hash.
     

