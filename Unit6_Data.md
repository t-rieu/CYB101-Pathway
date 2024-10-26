# Data

- **Three states of data:**
  - **At rest -** data is sitting in storage locally on a hard drive, flash drive, etc., or in a cloud database such as AWS.
    - It can be vulnerable to insider attacks, and external hackers
    - Vulnerability = low.
    - Use strong encryption to protect it, and use access controls.
  - **In transit -** it is moving from one location to another. *Eg. downloading a file, email, instant messengers.*
    - Vulnerable to MiTM attacks.
    - Vulnerability = high.
  - **In-use -** actively accessed and processed by a user. *Eg. data stored in RAM, user input on a website.*
    - Highest vulnerability because of its immediate availability. 

 - **Data exfiltration -** the unauthorized transfer of data.
   - “Data theft”.
   - It can happen because of a threat actor or malware.
 - Data must be collected before exfiltration can occur.
   - **Collection methods:** clipboard data, MiTM, screen capture, etc.
   - Threat actors must work around data loss prevention controls.
  
 - **Likely targets for exfiltration:**
   - Login credentials.
   - Strategic decision information.
   - Cryptographic keys.
   - Personal or corporate financial information.
   - SSN, addresses, or other PII.

- **Methods of exfiltration**
  - **Low-tech methods**
    - Hiding files inside other files.
    - Taking a picture of data and then saving or sending the picture.
    - Saving a copy on a USB.
  - **High-tech methods**
    - **Traffic duplication:** mirroring or redirecting network traffic.
    - **Limited size data transfer:** exfiltration of fixed size chunks instead of whole files to avoid triggering threshold alerts.
    - **Use of another network medium:** exfiltration via Bluetooth.
   
- **Steganography -** concealing data within other non-secret text or data.
  - This is considered a form of data exfiltration.
  - The data is embedded in the least significant bits of a file.
 
- Companies must be in compliance with regional data laws.
- **Data governance laws: EU**
  - **GDPR:** EU data must stay and be managed by the EU.
- **Data governance laws: US**
  - **HIPPA:** protection of sensitive health information.
  - **COPPA:** protection of children’s data.
  - **FERPA:** protection of educational data.
 
- **Data loss prevention methods**
  - **Low-tech methods**
    - Showing a popup when a user might be sharing a sensitive item inappropriately.
    - Blocking certain sharing actions.
    - Following the principle of least privilege for data access.
  - **High-tech methods**
    - Move files to a quarantine folder before allowing sharing.
    - Audit or restrict copying sensitive data to a USB drive.
    - Establish honeypots that detect actions by threat actors.
   
## Lab
![jpgHexValues](https://github.com/user-attachments/assets/9cf0aa6c-5eb0-4a9c-a2d0-49a7bc670bf7)
- To find hidden files in images, extract the files through CyberChef. Download the largest embedded file and extract it.

## Project
```
- Used nano command to create a .txt file named ‘hiddenmessage.txt’.
- steghide embed -ef hiddenmessage.txt -cf cat.jpg was used to embed the message into the image.
```

<img width="701" alt="Screenshot 2024-10-26 at 5 37 27 PM" src="https://github.com/user-attachments/assets/e0f3bd25-74fb-4e32-9bd1-3ca3d5f763a9">

```
- steghide info mochi.jpg displays the metadata of the file.
```

<img width="705" alt="Screenshot 2024-10-26 at 5 38 04 PM" src="https://github.com/user-attachments/assets/f5f1e7f0-8f89-470e-a51d-ae86c0fbfe28">

```
- steghide extract -sf cat.jpg -xf hiddenmessage.txt extracts the hidden message from the image file.
```

<img width="702" alt="Screenshot 2024-10-26 at 5 46 51 PM" src="https://github.com/user-attachments/assets/43872652-d998-438f-9ab5-c8f45d4ce564">

```
cat hiddenmessage.txt shows the content of the extracted file.
```



 

    

   
