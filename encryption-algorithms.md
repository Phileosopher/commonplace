
# Specific encryption algorithms

There are many types of encryption [algorithms](cs-langs-algorithms.md), and these are simply some of the most popular.

Message-Digest Algorithm was made in 1989, and has iterated from MD2 to MD6. MD4 was compromised through collision attacks and MD6 was compromised by differential attacks. MD5 is still the de facto standard even though it's cryptographically insecure.

Secure Hash Algorithm descended from MD4 by the NSA in 1993. It's a one-way encryption algorithm. SHA-2 has SHA-224, SHA-256, SHA-384, and SHA-512. SHA-3 has equivalent encoding, but more advanced. SHA-2 is more widely adopted right now, but SHA-3 is mean to directly substitute SHA-2.

AES was developed by the NSA to replace DES (see above), and is now at AES-256. It's a symmetric encryption standard.

John Daemen made a few algorithms (3-Way, BaseKing, and NOEKEON). While they were very efficient, they were susceptible to related-key attacks.

RIPEMD was made in 1996, and based on the principles from MD4. RIPEMD-160 hasn't been broken yet.

SHA-1 is decent, but not great.

- It's useful for non-critical situations.
- The public key can make a digest, but can't decrypt one.

MD5 is another popular algorithm.

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

There are others: Whirlpool, BLAKE, Tiger, RadioGatún, PANAMA, and GOST, to name a few. They're constantly being developed, [a bit like programming languages](cs-langs.md), so there's no need to cover an exhaustive list here.
