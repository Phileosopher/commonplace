
# Authentication

The history of passwords traces back to military messaging. In a [war](people-conflicts-war.md), military leaders must communicate, but without the enemy seeing that communication. The same philosophy holds true with protecting computer information, and is a critical subdomain of [keeping computers safe](computers-cysec.md).

Most computers have "certificates" to authenticate with each other. Setting certificate deadlines prohibits someone salvaging your computer later and using an old certificate.

## Factors

There are three ways to give evidence that someone is who they say they are.

- Knowledge: something they know (e.g., a password or other "secret")
- Possession: something they have (e.g., a mobile phone or other object)
- Inherence: something they are (e.g., fingerprint or face)

They all have downsides:

- Someone can guess knowledge (especially with [social engineering](social-engineering.md)).
- Someone can duplicate what someone possesses, or at least enough to fool a computer.
- Nobody can take someone's inherence very easily, but it can't be updated easily if they ever *do* succeed at stealing it (i.e., there's no easy way to rebuild fingerprints or reconstruct a face).

To that end, most authentication starts with knowledge (often through passwords) and possession.

For additional security, a system may use more than one authentication factor. It's typically a password and a phone code, but could be security questions and a specific computer, or a fingerprint and password.

### Knowledge: Passwords

With a computer-enforced "password policy", nobody can enter obvious passwords hackers can guess at.

While using an arcane combination of letters, numbers, and symbols ("Y3ll0wB@1ly") is marginally helpful, it's better to have long strings of human-understandable text ("There are 14 ways to eat a tennis ball!"):

- Most substitutionary characters are interchangeable for a "dictionary attack" (e.g., add every iteration of "a" to also include "@").
- Strings of human-readable text are easier to remember, and take an exponentially longer time for a computer to guess.

However, this policy must also require renaming the "default" passwords. Very often, there are automatic passwords that the manufacturer sets, and those require zero guesswork and a few web searches for hackers to discover.

To store the information, it should be in ciphertext, where the password is inaccessible. If a computer ever cross-references the password with *anything*, it's likely waiting to [be compromised](https://trendless.tech/pentest/).

### Possession: Checksum

The simplest version of verifying a downloaded file is to cross-reference its download with its [checksum](encryption.md), which is usually released on the website as a small separate download.

### Possession: Tokens

Another means of verifying is via an external hardware token. This could be a USB drive or smart card, and simply contains a hash that matches what the authentication software is looking for.

### Possession: Devices

One of the simplest ways to confirm someone possesses something is to send them a temporary message, such as a 6-digit code. Then, if they actually have the object and want to validate, they can enter a temporary 6-digit number.

### Inherence: Biometrics

The most common "biometric" measurements are the fingerprint and facial recognition.

Ideally, a computer can only handle biometric data if it does the following:

1. *Never* store the information directly.
2. Only on secondary information from that biometric (e.g., an encoded "hash" from a fingerprint).
3. Delete that secondary information immediately after using it.
