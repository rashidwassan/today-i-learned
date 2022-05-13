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
- In public key systems, each entity has different keys, or asymmetric keys.
- Both keys are mathematically related, one used for encryption and one for decryption of data.
- The public key locks, private key unlocks.
- Public can be known by third parties but private key must be kept secret.
- As keys are mathematically related, make sure no one is able to obtain private key from public key.
- It is not possible to encrypt and decrypt using the same key in assymetric systems.
- Authentication: As receiver decrypts the message using Bob's public key, this makes sure that the message is form Bob as only he is suppposed to have that key.