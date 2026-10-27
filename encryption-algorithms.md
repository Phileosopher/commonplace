
# Specific encryption algorithms

There are many types of encryption [algorithms](cs-langs-algorithms.md), and these are simply some of the most popular.

## Symmetric keys

Message-Digest Algorithm was made in 1989, and has iterated from MD2 to MD6. MD4 was compromised through collision attacks and MD6 was compromised by differential attacks. MD5 is still the de facto standard even though it's cryptographically insecure.

Secure Hash Algorithm (SHA) descended from MD4 by the NSA in 1993. It's a one-way encryption algorithm. SHA-2 has SHA-224, SHA-256, SHA-384, and SHA-512. SHA-3 has equivalent encoding, but more advanced. SHA-2 is more widely adopted right now, but SHA-3 is mean to directly substitute SHA-2.

Data Encryption Standard (DES) was made in 1975 by the NSA. It had a key of 56 bits, and some of its design with the small key size left academics concerned.

- Apparently, the NSA had designed it with a backdoor via the short number of bits, but they claimed it was a smaller cipher to break it by brute force attack.
- The critical response to DES was a driving force for many modern industry encryption standards.
- DES is still sometimes used three times over as 3DES.

AES was developed by the NSA to replace DES, and is now at AES-256.

- AES is most frequently used in WPA2 wireless encryption, but is in most encryption (email, Wi-Fi, file encryption via NTFS, BitLocker, etc.).

John Daemen made a few algorithms (3-Way, BaseKing, and NOEKEON). While they were very efficient, they were susceptible to related-key attacks.

RIPEMD was made in 1996, and based on the principles from MD4. RIPEMD-160 hasn't been broken yet.

SHA-1 is decent, but not great.

- It's useful for non-critical situations.
- The public key can make a digest, but can't decrypt one.

MD5 is another popular algorithm, especially for file checksums.

Blowfish is often used for SSH and VPNs.

- Twofish was an attempt to derive Blowfish to make a more secure algorithm, but AES was selected instead.

The base64 encoder and decoder uses the "secure socket layer" (SSL) [protocol](cs-standards.md) to send cryptographic data.

- The private key is the only one that decrypts, while the public key always encrypts.
- There are 2 kinds of public keys:
  1. Made-up public keys for general use.
  2. 3rd-party authorized public keys (e.g., GoDaddy, Comodo, Verisign, etc.).
     - These second public keys are "digital certificates", or "signed private keys".
     - It can be $100-200 or $1000-2000 to get your certificate formally signed.

TLS is the successor of SSL, which was deprecated from having serious flaws. TLS has developed a few times to version 1.3.

- TLS and SSL are the most popular internet encryption [protocols](cs-standards.md), however they only encryption the *transmitted* information and not the information itself.

OpenPGP is an open standard set in 1998 that can use public-key cryptography, with GnuPG as an [open-source](legal-ip-floss.md) implementation of it.

- It can be used for anything, but is most commonly used for email.

The International Data Encryption Algorithm (IDEA) is from Switzerland.

Ron Rivest's ciper #4 (RC4) was the original algorithm for wireless encryption in both WEP and WPA.

- WPA was the proper implementation of RC4, but it has been deprecated because most modern computers can crack it in about half a day.

## Asymmetric keys

RSA was the first public key algorithm in 1977.

Diffie-Hellman was alongside RSA in 1976, but solved the key exchange problem.

- We now use Diffie-Hellman Ephemeral, which improves on its randomness, or elliptic curve Diffie-Hellman Ephemeral, which makes it far more complex.

ElGamal was public domain product compared to Diffie-Hellman's [patent](legal-ip.md), but was slightly inferior. It was popular until 1994 when everyone moved to Diffie-Hellman, which we still use today.

Elliptic curve mathematics is improving on Diffie-Hellman, and is used frequently for [blockchain](cs-blockchain.md) matters.

Digital Signature Algorithm (DSA), which is also labeled the Digital Signature Standards (DSS), is essentially using RSA as the public key and SHA for private key.

## Others

There are others: Whirlpool, BLAKE, Tiger, RadioGatún, PANAMA, and GOST, to name a few. They're constantly being developed, [a bit like programming languages](cs-langs.md), so there's no need to cover an exhaustive list here.
