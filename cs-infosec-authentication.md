
# Authentication

The history of passwords traces back to military messaging. In a [war](people-conflicts-war.md), military leaders must communicate, but without the enemy seeing that communication. The same philosophy holds true with protecting computer information, and is a critical subdomain of [keeping computers safe](cs-infosec.md).

Most operating system security consists of sequential layers of "authentication". More authentication factors means more complexity.

Most computers have "certificates" to authenticate with each other. Setting certificate deadlines prohibits someone salvaging your computer later and using an old certificate.

There is, however, a major risk of *too much* security. It is very easy to create a self-defeating loop by setting authentication *behind* the authentication wall (e.g., sending email authentication to an email on the same server).

## Factors

The concept of multi-factor authentication (MFA) is to prevent only one thing allowing unauthorized access.

There are three "factors" to give evidence that someone is who they say they are.

- Knowledge: something they know (e.g., a password or other "secret")
- Possession: something they have (e.g., a mobile phone or other object)
- Inherence: something they are (e.g., fingerprint or face)

They all have downsides:

- Someone can guess knowledge (especially with [social engineering](cs-infosec-socialengineering.md)).
- Someone can duplicate what someone possesses, or at least enough to fool a computer.
- Nobody can take someone's inherence very easily, but it can't be updated easily if they ever *do* succeed at stealing it (i.e., there's no easy way to rebuild fingerprints or reconstruct a face).

In particular, *everything* someone is that is unchanging (i.e., biometrics like facial recognition and fingerprints) are a terrible idea to use for absolutely anything that's not extremely top-secret.

- Essentially, there will be severe security standards for top-secret projects, which will include the systems that authenticate people.
- However, for more "mundane" authentication (e.g., personal banking), the standards will *not* be as high and the experts won't be as meticulous.
- The result of this is that the biometric data *will* get [hacked](cs-infosec-pentest.md), and there is absolutely no way to reset that information.

To that end, most authentication starts with knowledge (often through passwords) and possession.

For additional security, a system may use more than one authentication factor. It's typically a password and a phone code, but could be security questions and a specific computer, or a fingerprint and password.

The best authentication is through a human being observing something natural (like a person they see), but it's also the slowest method.

Very frequently, old authentications (such as a proprietary sign-on) can open the attack surface to a secondary and less-common breach (e.g., old password found, old secondary account hacked).

### Knowledge: Passwords

With a computer-enforced "password policy", nobody can enter obvious passwords hackers can guess at.

While using an arcane combination of letters, numbers, and symbols ("Y3ll0wB@1ly") is marginally helpful, it's better to have long strings of human-understandable text ("There are 14 ways to eat a tennis ball!"):

- Most substitutionary characters are interchangeable for a "dictionary attack" (e.g., add every iteration of "a" to also include "@").
- Strings of human-readable text are easier to remember, and take an exponentially longer time for a computer to guess.

However, this policy must also require renaming the "default" passwords. Very often, there are automatic passwords that the manufacturer sets, and those require zero guesswork and a few web searches for hackers to discover.

To store the information, it should be in ciphertext, where the password is inaccessible. If a computer ever cross-references the password with *anything*, it's likely waiting to [be compromised](cs-infosec-pentest.md).

However, user decisions are the best solution for password integrity. Every user should routinely change all their passwords, *especially* admin accounts.

Be careful with any 4-digit PIN.

- It may seem like a 1 in 10,000 chance for a hacker, but [there are ways to deduce it down](cs-infosec-authentication-pin.jpg).

### Possession: Checksum

The simplest version of verifying a downloaded file is to cross-reference its download with its [checksum](encryption.md), which is usually released on the website as a small separate download.

### Possession: Tokens

Another means of verifying is via an external hardware token. This could be a USB drive or smart card, and simply contains a hash that matches what the authentication software is looking for.

### Possession: Devices

One of the simplest ways to confirm someone possesses something is to send them a temporary message, such as a 6-digit code. Then, if they actually have the object and want to validate, they can enter a temporary 6-digit number.

- This is not always safe, though, since SMS messages can be intercepted and are unencrypted, as well as subject to [social engineering](cs-infosec-socialengineering.md).

### Inherence: Previous interaction

Cybersecurity professionals use human rules ("policies") and computer rules ("permissions") to create "protection rings" around computer information or technology, which creates a type of "perimeter security". The x86 protection rings, for example:

- Ring 0 - core operating system files
- Ring 1 - drivers for important hardware
- Ring 2 - drivers for not-as-important hardware
- Ring 3 - applications

One of the more recent trends has been to employ "zero-trust" networks, which assumes that every actor is by default untrustworthy before trusting them.

- While this is the safest approach compared to perimeter security, it is also *very* burdensome to everyone who uses it, since they'll need to re-authenticate every single time.

### Inherence: Biometrics

The most common "biometric" measurements are the fingerprint and facial recognition.

Ideally, a computer can only handle biometric data if it does the following:

1. *Never* store the information directly.
2. Only on secondary information from that biometric (e.g., an encoded "hash" from a fingerprint).
3. Delete that secondary information immediately after using it.

### Inherence: Human interaction

While it's not *specifically* authenticating an individual, one key filtering mechanism involves software requirements that prevent simple scripts from accessing something through a UI. This takes the form of CAPTCHA (Completely Automated Public Turing test to tell Computers and Humans Apart).

- This naturally gets more complicated as [machine learning](cs-ai-ml.md) gets better.

One other downside is that many [big tech companies](cs-bigtech.md) use CAPTCHA data to increase visual recognition for their machine learning, so there's a statistical likelihood that the user is trying to detect an edge case, such as a hard-to-see traffic light. This overall destroys the [user experience](engineering-design-cs.md).
