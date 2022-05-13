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
- Example: RSA algorithm multiplying two large prime numbers.
- Attacks on these types of cryptosystems do not necessarily try every possible key value, but rather try to factor the large number, which will give the attacker the private key.
- When a user encrypts a message with a public key, this message is encoded with a one-way function (breaking a glass). This function supplies a trapdoor (knowledge of how to put the glass back together), but the only way the trapdoor can be taken advantage of is if it is known about and the correct code is applied. The private key provides this service. 
- only the public key can carry out encryption and signature verification and only the private key can carry out decryption and signature generation.
- work factor is the amount of time and resources it would take for someone to break an encryption method. 
### El Gamal 
It is based not on the difficulty of factoring large numbers but on calculating discrete logarithms in a finite field. It is extension of Diffie-Hellman. Slowest algorithm.
### Elliptic Curve Cryptosystems
Elliptic curves are rich mathematical structures that have shown usefulness in many different types of applications. ECC is more efficient than RSA and any other asymmetric algorithm. They are very efficient.
### Knapsack
Over the year, different versions of this algorithm have arisen.
- This algorithm was discovered to eb insecure and is not in use in cryptosystems.

### Zero Knowledge Proof
I am proving to you I have my private key—but I do not give or show you my private key.

## Message integrity
- CRC - Cyclic Redundancy Checks are used to spot modifications in message made while travelling.
- Parity bits cannot identify whether a message was captured by an intruder, altered, and then sent on to the intended destination as parity bits can be regenrated.

### One way hash
- Takes a variable-length string and a message and produces a fixed-length value called a hash value.
- When Bilal receives the message, he performs the same hashing function Ahmad used and then compares his result with the hash value sent with the message. 
- The hashing algorithm is not a secret—it is publicly known.
- Hashing is one-way function without keys.
- Message Authentication Code is needed to make things secure if inruder modifies the message and hash.
- A MAC function is an authentication scheme derived by applying a secret key to a message in some form.
- Message Authentication Codes (MACs).

### Hashing
- A hashing value can also be called a message digest or fingerprint.
1. The sender puts the message through a hashing function.
2. A message digest value is generated.
3. The message digest is appended to the message.
4. The sender sends the message to the receiver.
5. The receiver puts the message through a hashing function.
6. The receiver generates his own message digest value.
7. The receiver compares the two message digest values. If they are the same, the message has not been altered.

### HMAC
1. The sender concatenates a symmetric key with the message.
2. The result is put through a hashing algorithm.
3. A MAC value is generated.
4. The MAC value is appended to the message.
5. The sender sends the message to the receiver. (Just the message with the attached MAC value. The sender does not send the symmetric key with the message.)
6. The receiver concatenates a symmetric key with the message.
7. The receiver puts the results through a hashing algorithm and generates his own MAC value.
8. The receiver compares the two MAC values. If they are the same, the message has not been modified.

Now, when we say that the message is concatenated with a symmetric key, we don’t mean a symmetric key is used to encrypt the message. The message is not encrypted in an HMAC function, so there is no confidentiality being provided. 

### CBC-MAC
If a CBC-MAC is being used, the message is encrypted with a symmetric block cipher in CBC mode, and the output of the final block of ciphertext is used as the MAC.
- The use of the symmetric key ensures that the only person who can verify the integrity of the message is the person who has a copy of this key.
- A private key is bound to an individual; a symmetric key is not. MAC authentication provides the weakest form of authentication because it is not bound to a user, just to a computer or device.

## CMAC (Cipher Based Message Authentication Code)
- CMAC provides the same type of data origin authentication and integrity as CBC-MAC, but is more secure mathematically.
- CMAC is a variation of CBC-MAC. It is approved to work with AES and Triple DES.
- So here is how CMAC works: the symmetric algorithm (AES or 3DES) creates the symmetric key. This key is used to create subkeys. The subkeys are used individually to encrypt the individual blocks of a message.
### Hash Functionality
1. Sender puts a message through a hashing algorithm and generates a message digest (MD) value.
2. Sender sends message and MD value to receiver.
3. Receiver runs just the message through the same hashing algorithm and creates an independent MD value.
4. Receiver compares both MD values. If they are the same, the message was not modified.

### HMAC Functionality
1. Sender concatenates a message and secret key and puts the result through a hashing algorithm. This creates a MAC value.
2. Sender appends the MAC value to the message and sends it to the receiver.
3. The receiver takes just the message and concatenates it with his own symmetric key. This results in an independent MAC value.
4. The receiver compares the two MAC values. If they are the same, the receiver knows the message was not modified and knows from which system it came.

### CBC MAC Functionality
1. Sender encrypts a message with a symmetric block algorithm in CBC mode.
2. The last block is used as the MAC.
3. The plaintext message and the appended MAC are sent to the receiver.
4. The receiver encrypts the message, creates a new MAC, and compares the two values. If they are the same, the receiver knows the message was not modified and from which system it came.

### CMAC Functionality
- CMAC works the same way as the CBC-MAC, but is based on more complex logic and mathematical functions.

### Hashing Algorithms
- the goal of using a one-way hash function is to provide a fingerprint of the message. If two different messages produce the same hash value, it would be easier for an attacker to break that security mechanism, because patterns would be revealed.

### Hashing Algorithms Used Today
- Message Digest 2 (MD2) algorithm: One-way function 128 bit hash value, slower.
- MD4: One-way, 128 bit value.
- MD5: 128 bit value, complex than MD4.
- HAVAL: Variable Length, mod of MD5 but secure.
- SHA: Produces 160 bit hash value used with DSA.
- Ross Anderson and Eli Biham developed a hashing algorithm called Tiger in 1995. It was designed to carry out hashing functionalities on 64-bit systems and to be faster than MD5 and SHA-1. The resulting hash value is 192 bits. 

## Secure MIME
- Secure MIME (S/MIME) is a standard for encrypting and digitally signing electronic mail and for providing secure data transmissions.
- S/MIME provides confidentiality through encryption algorithms, integrity through hashing algorithms, authentication through the use of X.509 public key certificates, and non-repudiation through cryptographically signed message digests.

## PGP
- Pretty Good Privacy (PGP)  was designed by Phil Zimmerman as a freeware e-mail security program and was released in 1991.It was the first widespread public key encryption program. PGP is a complete cryptosystem that uses cryptographic protection to protect e-mail and files.
- Uses RSA.

## Quantum Cryptography
- Because of the need to always build a better algorithm, some very smart people have mixed quantum physics and cryptography, which has resulted in a system (if built correctly) that is unbreakable and where any eavesdroppers can be detected.
- Quantum cryptography can be carried out using various methods. So, we will walk through one version to review how all this works.
- The electromagnetic waves have an orientation of horizontal or vertical, or left hand or right hand.
- Now both Kathy and Tom each have their own photon gun, which they will use to send photons (information) back and forth to each other. They also have a mapping between the polarization of a photon and a binary value.
-  In this example, a photon with a vertical (|) polarization maps to the binary value of 0. A left polarization (\) maps to 1, a right polarization (/) maps to 0, and a horizontal polarization (–) maps to 1. This mapping (or encoding) is the binary values that make up an encryption key. 
- So they both have to agree upon a key, which is the mapping between the polarization states of the photons and how those states are represented in a binary value. This happens at the beginning of a communication session over a dedicated fiber line. 
- Since this type of cryptography is based on quantum physics and not strictly mathematics, the sender and receiver can be confident that no eavesdropper is listening to the communication path used to establish their key and that a man-in-the-middle attack is not being carried out. 

## Internet Security
- Variety of protocols that browser cannot understand.
- But browsers have capabilities to process many commands.
- but they do not understand them all. For those protocols or commands the user’s browser does not know how to process, the user can download and install a viewer or plug-in, a modular component of code that integrates itself into the system or browser. 

### HTTP
TCP/IP is the protocol suite of the Internet, and HTTP is the protocol of the Web. HTTP sits on top of TCP/IP. When a user clicks a link on a web page with his mouse, his browser uses HTTP to send a request to the web server hosting that web site. The web server finds the corresponding file to that link and sends it to the user via HTTP.
- HTTP is a stateless protocol, which means the client and web server make and break a connection for each operation. When a user requests to view a web page, that web server finds the requested web page, presents it to the user, and then terminates the connection.

### HTTP Secure
HTTP Secure (HTTPS) is HTTP running over SSL. (HTTP works at the application layer and SSL works at the transport layer.) Secure Sockets Layer (SSL) uses public key encryption and provides data encryption, server authentication, message integrity, and optional client authentication.
- The server sends a message back to the client, indicating a secure session should be established, and the client in response sends its security parameters. The server compares those security parameters to its own until it finds a match. 
- The client generates a session key and encrypts it with the server’s public key. This encrypted key is sent to the web server, and they both use this symmetric key to encrypt the data they send back and forth. This is how the secure channel is established.


