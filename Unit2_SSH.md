# SSH
- **Secure Sockets Layer (SSL) -** a protocol that encrypts, secures, and authenticates communications taking place on the Internet.
  - Cannot issue commands, unlike SSH.
  - Commonly used to secure client-server communications. Eg. email, VoIP.
    - The client has a public key. The server has both public and private keys.
    - Clients are the entities that initiate a request for services or resources from a server. Eg. web browsers, database clients, email clients, and mobile apps.
  - Uses both symmetric and asymmetric encryption.
- **SSL certificate -** a digital document that validates a website’s identity.
  - Essentially a set of public keys for a server.

**Steps to an established SSL connection**

**1. Certificate Verification**
  - Client requests SSL certificate from the server.
  - Client uses public key to verify the certificate.
    
**2. TLS handshake**
  - Client generates a symmetric key.
  - Client secures the symmetric key using the public key.
  - Client sends the symmetric key to the server.

**3. Key decryption**
  - Server receives the symmetric key from the client and decrypts it using the private key.
    
**4. Data exchange**
  - The client and server can communicate securely by encrypting/decrypting messages with the same symmetric key.

## Lab
- Folders are directories. Files are not directories.

Some CLI commands:
```
1. ls | Lists all the files and directories in the current directory.
2. pwd | Shows the directory currently in and the path taken from the root.
3. sudo | Lets you run other commands as the root user.
4. cd [directory_name] | Used to change directories.
5. cd .. | Used to move back up to the parent directory.
6. tree | Displays directory paths and files in each subdirectory.
7. touch [file_name] | Used to add a new empty file into the current directory.
8. wget | Used to download content from web servers.
9. cat [file] | Outputs the content in a file.
10. mkdir [folder_name] | Creates a new folder in the current directory.
11. cp [file_name] [duplicate_file] | Makes a copy of a file.
12. mv [file] [moved_file] | Moves files and folders. It can also rename files and folders.
13. rm [file] | Deletes a file.
14. rm -r [folder] | Deletes a folder and everything in it.
```
## Project
- **Secure shell (SSH) -** a protocol that allows for remote access of a device such as a server over an insecure network.
  - It is used for managing networks, operating systems, and configurations.
- **SSH key -** authenticates the identity of a user or process that wants to access a remote system using SSH.
 
```
Command: ssh-keygen -t ___ -b ___ -c “___”
1. -t ___ specifies the type of key (the desired encryption algorithm).
2. -b ___ specifies the number of bits.
3. -c “___” is essentially a label/name for the key.
```

- **Passphrase -** a sequence of unrelated words.
  - Similar to a password, it can be created and applied to the private SSH key for an extra layer of security.
- **Key fingerprint -** a unique identifier derived from a key.
  - It is a way to verify the key’s authenticity.
  <img width="1320" alt="Screenshot 2024-11-10 at 4 44 40 PM" src="https://github.com/user-attachments/assets/9eb0d355-6967-4849-a0d0-f108ebcd618a">
  <img width="1314" alt="Screenshot 2024-11-10 at 4 44 53 PM" src="https://github.com/user-attachments/assets/f81d6cd8-0454-43f3-b083-94e830b094a8">


