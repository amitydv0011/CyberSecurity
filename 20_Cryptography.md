What do you mean by cryptography?
Cryptography is the process of hiding or coding information so that only the person a message was intended for can read it.

  ~~~~~~~Encryption
Encryption is the process of converting plain text into cipher text using a secret key or algorithm. Encryption is used to protect sensitive information, such as passwords or credit card numbers, by making it unreadable to unauthorized parties. The cipher text can only be decrypted using the corresponding key or algorithm, which is kept secret. Encryption provides confidentiality, but not integrity or authenticity.
  Encryption is the process of translating plain text data (plaintext) into something that appears to be random and meaningless (ciphertext). Decryption is the process of converting ciphertext back to plaintext

 ~~~~~~~~~ What is Hashing?
Hashing is a one-way process where data is transformed into a fixed length alphanumeric string. This string is known as a hash or message digest. A hash cannot be reversed back to the original data because it is a one-way operation. Hashing is commonly used to verify the integrity of data, commonly referred to as a checksum. If two pieces of identical data are hashed using the same hash function, the resulting hash will be identical. If the two pieces of data are different, the resulting hashes will be different and unique.
  # Hashing
  Generating a unique Alphanumeric String for a short of Characters, Program, Application, Files, etc.
  Avalanche Effect --> If you change a binary bit, Hash Value Will Change Drastically. This is Called Avalanche Effect.
  Collision -->
 ~~~~~~~~~ What is Encoding?
Encoding data is a process involving changing data into a new format using a scheme. Encoding is a reversible process and data can be encoded to a new format and decoded to its original format. Encoding typically involves a publicly available scheme that is easily reversed. Encoding data is typically used to ensure the integrity and usability of data and is commonly used when data cannot be transferred in its current format between systems or applications. Encoding is not used to protect or secure data because it is easy to reverse.
     Decoding is the opposite process -- the conversion of an encoded format back into the original sequence of characters.
.
  - **Clear text / plaintext**: the unencrypted data
  - **Cipher text**: the encrypted data
  - **Key**: specifies the transformation of data for encryption / decryption ("key" is not synonymous with "password", although a password can in fact be used as a key)
- **Cipher**: an algorithm for performing encryption and decryption

# Symmetric cryptography
  - Use the same key for the encryption and the decryption
  - Symmetric-key either use stream cipher and block cipher
  - Popular algorithms: AES, DES

# Asymmetric / Public Key cryptography
  - Two key used: public and private
  - Public key is publicly known to everyone, issued by Public Key Infrastructure (PKI) and use to encrypt the data
  - Private key is a secret for the public,only known by the owner and it is used to decrypt the data
  - Asymmetric cryptography delivers confidentiality, integrity, authenticity and non-repudiation
  - Popular algorithms : RSA, DSA and Diffie-Hellman, ECDHA
------------------------------------------------------------------------------------------------------
# Substitution Cipher
  - Every character is substituted with another one
  - More on [Wikipedia](https://en.wikipedia.org/wiki/Substitution_cipher)
  - Example cipher : [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher)




| Action                | Key Used    | Purpose                                                        |
| --------------------- | ----------- | -------------------------------------------------------------- |
| Encrypting a message  | Public Key  | Ensures only the private key holder can decrypt it             |
| Decrypting a message  | Private Key | Recovers the original plaintext                                |
| Signing a message     | Private Key | Proves the sender created the message                          |
| Verifying a signature | Public Key  | Confirms the signature is valid and from the private-key owner |


⚖️ Side-by-Side Comparison
Feature	RSA	DSA
Supports encryption	✅ Yes	❌ No – signature only
Signature generation	Slower	   Faster
Signature verification	Faster	Slower
Key generation	Slower	Relatively faster
Typical key size	2048–4096 bits	2048 / 3072 bits
Security basis	Integer factorization	Discrete logarithm problem
Standard compliance	Broad, global support	NIST / FIPS-certified applications
Use cases	TLS/SSL, encryption & signing	Document signing, government systems

Example:
```
Plaintext :  THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG
Ciphertext : QEB NRFZH YOLTK CLU GRJMP LSBO QEB IXWV ALD

Key : right shift of 3
```

# Transposition Cipher
  - The positions held by units of plaintext are shifted according to a regular system
  - Example cipher [Rail Fence cipher](https://en.wikipedia.org/wiki/Rail_fence)

Example:
```
Clear text: WE ARE DISCOVERED. FLEE AT ONCE

W . . . E . . . C . . . R . . . L . . . T . . . E           00..........00..........00
. E . R . D . S . O . E . E . F . E . A . O . C .           ...00....00....00....00...
. . A . . . I . . . V . . . D . . . E . . . N . .           ......00..........00......

Ciphertext: WECRLTEERDSOEEFEAOCAIVDEN
```

# Polyalphabetic Cipher
- Based on substitution
- Using multiple substitution alphabets
- Example cipher : [Vigenère cipher](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher)

# Stream Cipher
- Text digits are combined with a pseudorandom cipher digit stream (keystream)
- Each plaintext digit is encrypted one at a time with the corresponding digit of the stream
- Example cipher: RC4, Salsalsa 20, Cacha20

# Block Cipher
  - Operating on fixed-length groups of bits, called a block, with an unvarying transformation that is specified by a symmetric key
  - Example cipher: AES, DES, 3DES, 2DES

# Symmetric Algorithms

# Data Encryption Standard (DES)
  - Introduced in 1975
  - Standardized in 1977 by NIST
  - Problem with DES: short key length (56 bits) -> ASICS Chips
  - Now considered as insecure
  - Improved version: Triple DES (involves DES three times)
  - Problem with Triple DES: slow, compute heavy                         

# Parameters
|   Parameter       |   Value  |
|:-----------------:|:--------:|
|   Block size      | 64 bits  |
|   Key size        | 56 bits  | --> ffffffff ->
|   No. of rounds   |    16    |


# Advanced Encryption Standard (AES)
  - First published in 1998-1999 - 2000
  - Became a federal government standard in 2002
  - First approved (and only) publicly accessible cipher approved by the NSA for top secret information

# Parameters
|      Parameter    |    AES-128 value   |    AES-192 value  |    AES-256 value   |
|:-----------------:|:------------------:|:-----------------:|:------------------:|
|    Block size     |      128 bits      |      128 bits     |      128 bits      |
|    Key size       |      128 bits      |      192 bits     |      256 bits      |
|   No. of rounds   |         10         |       12          |         14         |

# Modes of Operations
  - Electronic Code Book (ECB)
  - Cipher Block Chaining (CBC)
  - Output Feedback Mode (OFB)
  - Galois/Counter Mode (GCM)

# Hashing
  Generating a unique Alphanumeric String for a short of Characters, Program, Application, Files, etc.
  Avalanche Effect --> If you change a binary bit, Hash Value Will Change Drastically. This is Called Avalanche Effect.
  Collision -->
