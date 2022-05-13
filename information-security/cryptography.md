### Definitions of Cryptography

## Some Common Terms

### Algorithm
Set of Mathematical rules used in encryption & decryption.

### Cipher
This is another name of algorithm.

### Cryptography
Science of writing and transmitting data in form that is only available of intended individuals.

### Cryptosystem
System of hardware & software that works in combination to convert plaintext into cyphertext or vice-versa.

### Entity Authentication
Proving the identity of the entity that sent a message.

### Decipher
Act of tranforming the data into a readable format.

### Key
Secret sequence of bits and instructions that governs the act of encryption and decryption.

### Keyspace
A range of possible values to construct keys.

### Plaintext (cleartext)
Is the data in readable format.

### Reciept
The acknowledgement of message reception.

### Work Factor
Estimated time, effort, and resources required to break a cryptosystem.

### Classification of the field of Cryptography

## Cryptology
### Cryptography
- Symmetric Ciphers
  - Block Cyphers
  - Stream Cyphers
- Asymmetric Ciphers
- Protocols
### Cryptanalysis

## One-Time Pad
- Encryption scheme (aka Vernam Cipher).
- Unbreakable if properly implemented.
- Invented by Gilbert Vernam in 1917.

### Encoding in One-Time Pad
- Uses a pad made up of random values instead of shifting aplhabets.
- Message is converted into bits and bits are randomised then using one-time pad constructed from them.
- It uses binary mathematic function XOR.
- Here, message and key bits are XORed and resulting bits form ecnrypted data.

### Decoding in One-Time Pad
- User must have that one time pad.
- The XOR process is then reversed (run again) to obtain the message.

### Requirements:
Each pad scheme must be:
- Made up of truly random values.
- Used only one time.
- Securely distributed to its destination.
- Secure at sender and receiver's site.
- At least as long as the message.

## Steganography
- Steganography is a method of hiding the data into another media types so that the actual data is concealed.
- Only sender and reciever are aware of that hidden data.
- Data is only hidden, not encrypted.

### Encrypting
- Message embedding requires the use of Least Significant Bit (LSB).
- Many types of files have some bits which can be altered without noticeable visible changes.
- Those bits can be modified to store message.
- Most suitable files to hide data can be high resolution images or high bit-rate audio files.
- No any increment in file size is noticeable as well.
- This can be used to hide images in images.

### Digital Watermarking
- The logo is embedded and visible to allow others not to copy the material which does not belong to them.
- This type fo steganography is reffered to as Digital Rights Management (DRM).

## Types of Ciphers
### Symmetric Encryption Ciphers have two types:
- Substitution
  - They replace bits, characters, and blocks with different ones.
  - In the Caesar cipher, each letter is replaced with the letter three places beyond it. The key is 'Shift up three'.
  - Substitutions used nowadays are very complex compared to this.
- Transportation
  - The values are scrambled or put into another order.
  - Key determines the positions the values are moved to.
Symmetric algorithms employed today use both long sequences of complicated substitutions and transpositions on messages.
- Consider algorithm a box of boxes, each box has own set of mathematical rules.
- If each of our messages always go through the same boxes and values, the evildoer can easily figure out the process.
- To foil the evildoer, we use the key which defines from which boxes and values will the message pass.
- If one message is encypted with key one for instance, it will pass through box 1, 5, & 6. If encrypted with another key, it will go through other boxes defined in the key.

# Methods of Encryption
- Two entities need same key or algorithm to communicate via encryption.
- Sometimes, diffrent but related keys are used.

## Symmetric VS Asymmetric Algorithms
- Asymmetric methods are slower & computationally expensive but provide authentication. They provde easier key management.
- Symmetric is used for bulk encryption, while asymmetric is used for key distribution and digital signatures.
### Symmetric Algoritms
- Symmetric algorithms use same symmetric or secret keys.
- Sender and receiver uses the instances of the same key for encryption and decryption.
- Key has dual functionality of encrypting and decrypting the message.
- Symmetric keys are also called secret keys as users have to keep the key a secret and properly protected.

### Asymmetric Algorithms
- Asymmetric algorithms use same asymmetric or public and private keys.
- The more the people to share message with, more instances of key are needed.
- The equation used to calculate the number of symmetric keys needed is: N(N – 1)/2 = number of keys
- Sharing and updating asymmetric keys can be a big hassle as we have to transfer keys through secure channel without anyone intercepting in the middle.
- Assymetric keys are much faster and less computationally intensive, and are hard to break.
- But they require secure tranfer mechanism, overwhelming key management, do not provide authenticity.
- Examples of Symetric Algorithms: DES, 3DES, Blowfish, IDEA, RC4, RC5, RC6, & AES.

### Asymmetric Cryptography
- In public key systems (asymmetric cryptography), each entity has different keys, or asymmetric keys.
- Both keys are mathematically related, one used for encryption and one for decryption of data.
- The public key locks, private key unlocks.
- Public can be known by third parties but private key must be kept secret.
- As keys are mathematically related, make sure no one is able to obtain private key from public key.
- It is not possible to encrypt and decrypt using the same key in assymetric systems.
- Authentication: As receiver decrypts the message using Bob's public key, this makes sure that the message is form Bob as only he is suppposed to have that key.
- Open message format: If the message is encrypted with someone's private key, anyone can decrypt is with related public key. Confidentiality is not ensured.
- Confidentiality: Bob can encrypt data with the receivers public key, and the receiver can then decrypt it with his private key.
- Secure Message Format: If confidentiality is the most important security service to a sender, he would encrypt the file with the receiver’s public key. It can only be decrypted by the person who has the corresponding private key.
- Strengths: Better key distribution, better scalability, authenticaion, and nonrepudiation.
- Weaknesses: Slow, mathematically intensive.
- Examples: RSA (Rivest, Shamir, Adleman), Elliptic Curve Cryptosystem (ECC), Diffie-Hellman, El Gamal, Digital Signature Algorithm.


# Types of Symmetric Algorithms

## Block Ciphers
- Work on blocks of bits.
- The message to be encrypted is first divided into blocks of bits.
- Then these blocks go through functions to get encrypted.
- Data is divided into 64 bit blocks.
- Output is encypted blocks.
- A strong cipher contains the right level of confusion and diffusion.
- Confusion is carried out by substitution.
- Diffusion is carried out by transportation.
- The strong cipher must contain confusion & diffusion to ensure impossiblity of reverse engineering.
- The randomness of key value & complexity of mathematical functions dictate the level of confusion and diffusion.
- Confusion makes the relation between key and ciphertext very complex.
- Each value in ciphertext shoud depend upon the key. But this mapping should seem totally random to the observer.
- Diffusion means a single plaintext bit has high influence over other bits. Changing it should change many other bits too.
- S boxes: S-boxes are to be used when scrambling the original message from readable plaintext to encrypted non-readable cipher text.
## Stream Ciphers
- Work in bits by bits manner.
- a stream cipher treats the message as a stream of bits and performs mathematical functions on each bit individually.
- Uses keystream generators which used XOR operations on each bit to produce ciphertext.
- Similarity with one-pad: one pad also uses XOR, but in this case, keystream is generated instead of a pad.
- Function of Key: As we can XOR plaintext with ciphertext, we can find the message. So key protects the message in this case. Keys define the randomness of bits XORed in plaintext.
- Initialization vectors make sure that there is no pattern created.
- Characteristics of Strong Stream Ciphers: Statistically unpredictable keystream, keystream no linearly related to key, unbiased keystream.
- Stream ciphers require lot of power, block ciphers don't and are implemented at software level.
- Stream ciphers may not provide the level of protection that one-time pads do, but are more practical.

## Hybrid Encryption Systems:
- Use symmetric and asymmetric encryption methods together.

# Symmetric Algorithms
### DES (Data Encryption Standard)
- NSA announced in 1986.
- It's popularity made NSA skeptic about its success.
- Electronic Frontier Foundation made a computer which broke this encryption in 3 days using brute force attack.
- DES works in blocks of 64-bit.
- It uses 64-bit key, 56 for actual key and 8 for parity.
- Blocks are put through 16 rounds of transposition and substitution functions.
- The order and type of transposition depends upon key.

### When algorithm is broken?
- When someone uncovers the key that was used to encrypt.

### Cipher Feedback Mode (CFB)
- Email client uses CBC, which is ideal when data is sent in large chunks.
- Sometimes each keystroke is sent to backend terminal server in chunks of 8bits, as CBC works with 64bit chunks, we would use CBC mode. Which is combo of block cipher and stream cipher.
- For first 8bits we use initalization vectors.
- One 8bit ciphertext block goes to terminal server and second one is used to encrypt next block.
- ECB for encrypting small amount of data, CBC for larger chunks.
- Sensitive data should not be encrypted in CFB mode. Use OFB mode which reduces the chance of bit corruptions.
- Counter mode: increments counter with each next block. The unique counter value makes sure that block is XORed with unique keystream value. No chaining is involved. Parallel processing for performance. It is used for quite a while for ATMs.
- Why CTR?
  - As there is no chaining involved and ATM data is not sent in order, the decryption is faster and no need of waiting for full message.
- Double DES

### AES (Advanced Encryption Standard)

## Difference Between Public Key Cryptography & Public key infrastructure?
- Public key cryptography is use of asymmetric algorithm. Thus called public key cryptography and asymmetric cryptography mean same.
- RSA, Elliptic curve, diffie-hellman.
- Used to create public/private keys, perform exchanges, generate and verify digital signatures.
- Diffie-Hellman can only verify agreements.
- Public key infrastucture is not an algorithm, protocol, or a software, it is an infrastructure.

### One way functions
- A function which is easier to compute one way but difficult in vice-versa.
