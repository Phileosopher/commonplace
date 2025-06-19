
# Encryption

Not all information is safe to publicly use. Bank account information or your password, for example.

For that matter, a sufficiently experienced [hacker](hacking.md) can reconstruct information from seemingly useless information (discerning the user's routine by reading a log file of when the system powers on and off, for example).

No particular computer is trustworthy, either. "Whitelisting" MAC addresses or IP addresses is also a bad idea, since they're easy for hackers to "spoof".

Therefore, to keep data safe, it must often be routinely encrypted and decrypted:

1. Output the data wherever it's at.
2. Encrypt the information, typically with an encryption [algorithm](programming-algorithms.md).
3. Transfer or store the information.
4. When needed, decrypt the information.

Unencrypted "plaintext" information is usually readable without any further effort, but encrypted data (or "ciphertext") looks like completely random information.

Since the encryption is often using math calculations to convert binary data, encrypted data viewed in a text file often shows weird [non-alphabetic characters](computers-keyboard.md). (e.g., 01000100 for the character "D" may convert to 10101100 for the character "¬").

## History

The first enciphered messages were from a few thousand years ago. Up until computers, encryption has taken a variety of forms:

- Steganography: concealing words inside other things
  - *a* *w*ry sample *o*f it *r*eadily use*d* here -> a word
  - It's relatively weak because the secret message isn't enciphered and relies on the reader not noticing anything odd about the message.
  - However, once someone suspects a hidden message, they usually won't even need any special techniques or tools to decode it.
  - Simply look for anything unusual such as alignment, spacing, or word choice that could imply something forced into a pattern.
  - This can also express as a pattern beyond language (e.g., Morse code or binary information).
- Transposition: change the position of the letters
  - w ardo -> a word
  - By scrambling the word, it can create untold rearrangements (the word "transposition" alone has over 6 billion).
  - The problem is that it takes time to encipher and decipher it, as well as creating a long key for exchanging it.
  - For that reason, most transposition ciphers use a simple encipherment pattern (e.g., reading off every other letter in plaintext).
  - The easiest way to solve it is to begin with the simplest possible numerical pattern and work to more complex.
  - Often, vowel distribution and letter pairings can indicate whether a word has been decrypted, as well as finding patterns that link together common pairs of letters (like "th").
- Monoalphabetic substitution: swap letter-by-letter
  - b xpse -> a word (by shifting the letter 1 previously in the alphabet)
  - The Caesar cipher is relatively simple: shift the letter a certain number of letters down in the alphabet (e.g., the letter "a" becomes "e" with a shift of 4).
  - This had been used widely for hundreds of years until frequency analysis completely decimated them.
  - Frequency analysis requires simply finding highly frequent letters (e.g., "e" is frequent, so many instances of "z" will likely represent "e").
  - ROT13 ([rotate 13 characters](https://rot13.com/)) was an early cryptographic element of the early internet in the 1990's.

The Enigma Machine in 1925 was a very early computer designed for decrypting German military messages, and a key part of the history of [the computer's development](computers.md).

Data Encryption Standard (DES) was made in 1975 by the NSA. It had a key of 56 bits, and some of its design with the small key size left academics concerned. Apparently, the NSA had designed it to have a backdoor via the short number of bits, but they claimed it was a smaller cipher so they could break it by brute force attack. The critical response to DES was a driving force for many modern industry encryption standards.

## Philosophy

In the 19th century, Auguste Kerckhoffs made a principle of cryptography that a cryptographic system must be secure even when everything about the system except the key is public knowledge. He also gave six rules for effective military ciphers:

1. The system must be practically, if not mathematically, impossible to decipher.
2. By implication, that system can be compromised without any issues.
3. The key can be kept and transferred without a data record, and can be fully modified by the users.
4. The security policy must apply with any medium of communication.
5. The apparatus and documents must be portable, where only one person can work with it.
6. Finally, the system should be easy to use, without needing mental strain or knowing lots of rules.

To that end, most cryptographic ciphers compensate for everything *but* the key being public through vastly elaborate and complicated methods.

However, there is no such thing as a cipher that can't be cracked. All encryption is simply math, so if any computer can encode something, another computer with enough time and effort can theoretically decode it.

Instead, encryption creates a mandatory tradeoff for the people who wish to decode information. It requires the interfering entity must make priorities on *what* they want to decode, and this keeps the majority of the world that isn't as important safe from invasion.

Or, to put another way, the effort is less devoted to creating a perfectly unbeatable code, and more to creating a code that makes the effort not worth anyone's time. Someone will be more likely to trespass on a property without a fence than scale a 10-foot-high barbed-wire wall.

## Implementations

There are *many* places where encryption is necessary or, at least, a very good idea:

- The [operating system](computers-os.md) often needs encryption, especially core files. Sometimes an entire drive's data must be encrypted.
- Anytime something sends across [the internet](computers-webdev.md), it needs to be secure, since anyone can theoretically intercept it.
- All aspects of [cybersecurity](computers-cysec.md) involve some form of encryption, if not outright destruction, of data and data-bearing devices.

## Forms

Almost all computer-based encryption is doing the same thing:

1. Encoding the information (or simply the "message") using a "key". Stream algorithms process it bit-by-bit, while block algorithms process larger fixed-size chunks. The algorithm that does this is a cryptographic hash function (CHF)
2. Convert the final form into a fixed-size array of bits (a "hash" or message digest).
3. Transfer/store the information in its encoded form.
4. Decode/verify it later.

However, computers can use several possible types of encryption systems:

- Hash: read the hash instead of the data itself.
  - Because it's fast, can be useful for bulk encryption/decryption.
  - e.g., Computer 1 encodes ABC as XYZ, Computer 2 only looks for XYZ and never reads ABC.
  - Good for verifying information like "checksums", messages, and digital signatures.
  - In hashes, the original data is never directly used after it's encoded.
  - Unfortunately, sending a key to decrypt information is also sending the means to encrypt it as well.
- Assymetric/public key: one key encrypts, and another decrypts.
  - e.g., Computer 1 encodes ABC into XYZ with Key 1, Computer 2 uses Key 2 to decode XYZ back into ABC.
  - Very useful for internet transfers (on [Layer 6](networks-computer.md)), since *anyone* can freely access the encryption key as long as the decryption key is private. TLS and SSL are the most popular internet encryption [protocols](standards-computers.md).

These "ciphers" can be mixed and matched to create hybrid ciphers.

## Popular Cyphers

Some encryption can be cracked and "reverse engineered", but others are nearly unbeatable. Ciphers have been frequently compromised, so new ones must replace them with extra degrees of complexity.

Many forms of encryption use the Merkle--Damgård construction originally created in 1979:

1. Input the initialization vector (IV).
2. Process Message Block 1 through the algorithm's rounds and make it f1.
3. Process Message Block 2 through the algorithm's rounds and make it f2.
4. (repeat for all the rest)
5. Concatenate f1, f2, etc. together, then add zeroes at the end to reach a fixed number.
6. Finalize everything, maybe with more rounds of encryption, to make a hash.

Modern iterations use the Merkle--Damgård construction, but add other elements into the process (e.g., sponge construction, HAIFA construction) to avoid length extension attacks.

There are many types of encryption [algorithms](programming-algorithms.md) available now:

- Message-Digest Algorithm was made in 1989, and has iterated from MD2 to MD6. MD4 was compromised through collision attacks and MD6 was compromised by differential attacks. MD5 is still the de facto standard even though it's cryptographically insecure.
- Secure Hash Algorithm descended from MD4 by the NSA in 1993. It's a one-way encryption algorithm. SHA-2 has SHA-224, SHA-256, SHA-384, and SHA-512. SHA-3 has equivalent encoding, but more advanced. SHA-2 is more widely adopted right now, but SHA-3 is mean to directly substitute SHA-2.
- AES was developed by the NSA to replace DES (see above), and is now at AES-256. It's a symmetric encryption standard.
- John Daemen made a few algorithms (3-Way, BaseKing, and NOEKEON). While they were very efficient, they were susceptible to related-key attacks.
- RIPEMD was made in 1996, and based on the principles from MD4. RIPEMD-160 hasn't been broken yet.
- There are others: Whirlpool, BLAKE, Tiger, RadioGatún, PANAMA, and GOST, to name a few. They're constantly being developed, [a bit like programming languages](computers-languages.md), so there's no need to cover an exhaustive list here.

Key derivation functions (KDFs) become meta by encrypting the key itself with a different key. This creates another layer of complexity to break through.

## Attacks

Cryptanalysis uses a variety of techniques to break ciphers. It's worth noting that, while everyone who is cryptanalyzing is [hacking](hacking.md) (and many are [PenTesting](computers-cysec-pentest.md)), very few hackers or PenTesters will cryptanalyze.

It is impossible to have an indecipherable message. All encryption can be broken with a brute force attack. However, it's not sensible to apply resources toward it. Why spend 30,000 hours of computer processing cracking a password that will give the attacker $100 of payout or evidence of a misdemeanor? This is one of the strengths of [blockchain](computers-blockchain.md) cryptocurrency.

There are different attack models for defending against a cryptanalysis. One of the most popular is a chosen plaintext attack (CPA), which presume that the attacker can get a ciphertext for any plaintext, which is almost always the case if they can get a public key.

There are a variety of different cryptography attacks:

- A meet-in-the-middle (MITM) attacks is a generic attack that invalidates running a cryptographic message through multiple keys. What this does is map how plaintext converts to ciphertext, as well as how ciphertext converts to plaintext, which makes it *meet* in the middle where the two intersect.
- A related-key attack will use a known mathematical relationship to certain elements to infer other elements. [The birthday paradox](math-stat.md), in particular, has meant that block sizes must be at least 128 bits and why wireless doesn't use WEP encryption anymore.
- Collision attacks (aka hash collision) involve trying to find two inputs that produce the same hash value. This is often done with dictionary attacks (by running through all the possible human-readable words that could make the message). Collision resistance can help against this, but the ever-increasing speed of computers makes it a never-ending challenge.
- Preimage attacks are like collision attacks, but will try to find the message by inputting a specific hash value (further downstream than inputting the message). This is most effectively done with a brute force attack.
- Differential attacks take advantage of knowing that the cipher is always the same. The attacker uses multiple plaintext entries and finds the mathematical differences between them. This means that with a few chosen plaintext entries the cipher can be broken.
- Length extension attacks use the length of the encrypted message as a presumption to calculate the hash. Any encryption that uses the Merkle--Damgård construction (or always converts to a predictable length with the same number of characters) are susceptible to this type of attack.

It's worth noting that "concatenating" outputs will give as much collision resistance as the most powerful algorithms in the concatenated result.

## Passwords

Passwords *should* be easy to work with, but they often aren't. One major reason why is because a "hard-to-guess password" is different with a human than a computer.

Someone may imagine that "sK8thrul1fE" is harder to guess than "I skate through life.", a "dictionary attack" can find all the substitution characters ("8" for "ate", for example). The only way to make a dictionary attack difficult is to use a very long or complicated password (e.g., "I had 13 donuts after 7 of my friends went to work." or "1nfgdsi8@SGAc").

To that end, "passphrases" are more effective than passwords. People often forget their password when using substitution characters, but typing a complete sentence and remembering it is comparatively *much* easier.

## Further Reading

[Comparison of cryptographic hash functions](https://en.wikipedia.org/wiki/Comparison_of_cryptographic_hash_functions)
