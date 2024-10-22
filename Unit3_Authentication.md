# Authentication
- **Non-human identities:** workloads, services, machines.
  - These can be considered the majority of users in organizations.
  - They have more privileged accounts than humans.
  - Certificates or keys are used for these identities rather than traditional passwords.

**Securing device identities**
  - **Public Key Infrastructure (PKI):** issuance of digital certificates to provide unique digital identities for users.
  - **On-device code generation:** code generation apps ensure that only authorized users can access resources.
  - **Mutual authentication:** two sides of a communication channel verify each other’s identity.
  - **Zero trust:** don’t grant access to resources until the device verifies its identity.

**Three ways to authenticate:**

**1. Knows**
  - A password, pin, answer to a secret question, etc.
  - **Vulnerabilities:** forgetting passwords, weak passwords, reusing passwords, discoverable.

**2. Has**
  - ID, magnetic card, token, etc.
  - **Vulnerabilities:** loss duplication.

**3. Is**
  - Biometrics (fingerprints, facial recognition, etc.)
  - **Vulnerabilities:** error rates can be high, high costs, privacy concerns, and some people can have similar features.


**Types of permissions:**
- Every file and directory has an **owner** and **group**.
- There are **sets of permissions** for the owner, group, and world (all users that can log into the system).

**1. Read:** a user can see the contents.

**2. Write:** a user can modify the content.

**3. Execute:** a user can run a file.

**How passwords work:**

**1. Signup**
  - Encrypt the user’s password.
  - Stores encrypted string (hash) with the user’s record in the database.

**2. Login**
  - The user submits a username and password on a login page.
  - The attempted password is encrypted.
  - The new hash is verified against the stored hash.

## Lab
**[John the Ripper](https://www.openwall.com/john/doc/RULES.shtml) cracking methods**

**1. Single crack mode**
  - It uses the user’s information such as login names, full name fields, directory name fields, etc. stored in the GECOS field to guess user passwords.

**2. Wordlist mode** 
  - It uses a wordlist of passwords and tries every password in it. In this lab, the wordlist 'lower.lst' was used.
  - Mangling rules can be applied to modify the passwords in the list.

**3. Incremental mode**
  - Tries all possible character combinations as passwords, essentially like a brute force.
  - Educated guesses about the construct of passwords can be used. Using –mask can be used to look for a common pattern.

```
1. crackA.txt passwords | [john --single crackA.txt]
  - bulbasaur:kantograss
  - squirtle:waterSquirtle
  - charmander:charizard22

2. crackB.txt passwords
  - jim:paper | [john --wordlist=lower.lst crackB.txt]
  - pam:tEaPoT | [john --wordlist=lower.lst crackB.txt --rules=l33t]
  - dwight:b33t | [john --wordlist=lower.lst crackB.txt --rules=shifttoggle]

3. crackC.txt passwords
  - pinball:496821 | [john --incremental=digits --min-length=4 --max-length=6 crackC.txt]
  - pacman:8Bit | [john --mask=?d?u?l?l crackC.txt]
  - frogger:bugs7! | [john --mask=?l?l?l?l?d! crackC.txt

4. challengeCrack.txt passwords
  - pupper: bacon! | [john --single crackChallenge.txt]
  - Birb: birdseed | [john --wordlist=lower.lst crackChallenge.txt]
  - Kitty: pr3d4t0ry | [john --wordlist=lower.lst crackChallenge.txt --rules=l33t]
```

## Project






