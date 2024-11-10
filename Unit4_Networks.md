# Networks
**Network devices**

**1. Routers**
  - Communicates between the Internet and devices.
  - Operates on the Network layer.
  - Responsible for sending packets in the fastest route possible.
  - It can provide network-level protection against cyberattacks.

**2. Switches**
  - Connects devices to create a network.
  - It uses packet switching to receive and forward data.
  - Operates on the Data Link layer.

**3. Firewall**
  - It acts as a shield and filters the incoming and outgoing network traffic.

**4. Load balancers**
  - Distributes network traffic across multiple servers so one server is not overloaded with traffic.
    - This helps with availability.
  - It can be software or hardware.
  - It helps prevent DDoS attacks.

**Protocol -** a set of rules for transferring data over a network.

**1. Address Resolution Protocol (ARP)** - it is used for discovering MAC addresses from IP addresses in a LAN. (Builds a MAC-to-IP association).
  - **MAC address -** a unique identifier every device connected to a network has.
  - When a device knows the designated IP address to send data to, ARP is used to find the MAC address that corresponds with the IP address. This ensures data is sent to the correct device.
  - IP address changes when a device is disconnected from the Internet but its MAC address is fixed.

**2. Domain Name System (DNS) -** translates domain names to IP addresses.
  - **DNS resolution**
    1. Browser requests to visit a domain -> Local DNS is checked.
    2. If not found, ISP DNS is checked.
    3. If not found, root DNS is checked.
    4. The domain is returned to the browser.
   
**3. Dynamic Host Configuration Protocol (DHCP) -** a protocol that automatically assigns IP addresses and other communication parameters to devices on a network.

**4. Border Gateway Protocol (BGP) -** a routing protocol that determines the best path for packets to travel on.
  - **BGP hijacking -** an attacker maliciously redirects internet traffic so packets do not arrive at their intended destination; instead, they arrive at an incorrect network.
    - BGP filter systems can mitigate this.
    - It can be used to perform MitM attacks.
   
**Network intrusion -** unauthorized access of a computer or address within an assigned domain.
- **Network intrusion detection -** monitors a network for malicious activity.
  - Includes antivirus software and tiered monitoring systems.
  - **Signature detection:** detects possible threats by looking for specific patterns, such as byte sequences in network traffic, or known malicious instruction sequences.
  - **Anomaly-based detection:** detects and adapts to unknown attacks.
- **Prevention strategies**
  - **Network intrusion prevention system**
    - Monitors all network traffic and proactively scans for threats.
    - It can take action to block an attempted intrusion or remediate the incident.
  - **Host intrusion prevention system**
    - Installed at an endpoint and looks at the incoming and outgoing traffic from that only device.
      - It is the last line of defense.
  - **Wireless intrusion prevention system**
    - Scans the Wi-Fi network for unauthorized access.
  - **Network behavior analysis**
    - Detects unusual traffic flows and spot zero-day vulnerabilities.
   
**Distributed Denial of Service (DDoS) -** flooding a server with false traffic to disrupt services.
  - **Identifying a DDoS attack:**
    - A high volume of traffic from one IP address or IP range.
    - A flood of traffic from users with a similar profile. Eg. device type
    - Unexpected surge in requests to a single endpoint.
    - Spikes of traffic at odd hours.
  - **Mitigation techniques**
    - **Blackhole routing -** funnels traffic into a null route, but this makes the network inaccessible for everyone.
    - **Rate limiting -** limits the number of requests a server accepts in a given time span.
      - Struggles to handle a multi-vector DDoS.
    - **Traffic scrubbing -** traffic is redirected to a data center and cleaned before forwarding to the original destination.

## Lab
- The lab demonstrates how DNS IP addresses can be modified.
- The hosts file acts as a local DNS.
- Running ‘sudo nano hosts’ allows the hosts file to be edited.
  - In the lab, I had to swap the IP addresses between www.neverssl.com and eu.httpbin.org.
    - The IP addresses were first identified using the ‘dig’ command.
   
## Project
- Nmap is a networking tool. It was used to scan for open ports and vulnerabilities in the Metasploitable VM.
  - nmap -p0-65535 172.17.0.2
    - Scans ports 0-65535 and lists those that are opened.
  - nmap 172.17.0.2 --script vuln -p 21
    - A VSFTPD backdoor vulnerability was found.
- Using the Metasploit library, an exploit for the vulnerability was found and executed. From this, the Metasploitable VM was backdoored.
 <img width="846" alt="Screenshot 2024-11-10 at 4 48 57 PM" src="https://github.com/user-attachments/assets/6f242556-55e3-4e62-b973-14acf5bc2603">
 <img width="846" alt="Screenshot 2024-11-10 at 4 49 16 PM" src="https://github.com/user-attachments/assets/6b58c03c-53ae-4eae-8cf8-74b77642283e">
 
**Stretch challenge:** I was able to exploit the vulnerability in port 1099.
<img width="829" alt="Screenshot 2024-11-10 at 4 50 40 PM" src="https://github.com/user-attachments/assets/e830bf15-7a14-4dc2-b4e2-358538586924">
<img width="822" alt="Screenshot 2024-11-10 at 4 50 51 PM" src="https://github.com/user-attachments/assets/422f4e58-8d51-406b-9b95-a30da6cfd65c">
<img width="773" alt="Screenshot 2024-11-10 at 4 51 02 PM" src="https://github.com/user-attachments/assets/eee26c30-b851-4ed5-9f82-0fd2ab1ef25b">
<img width="778" alt="Screenshot 2024-11-10 at 4 51 12 PM" src="https://github.com/user-attachments/assets/b229203e-d2fd-4b03-9828-15b179bd22d1">
<img width="364" alt="Screenshot 2024-11-10 at 4 51 19 PM" src="https://github.com/user-attachments/assets/5dc39a9e-9419-4e42-8830-59e7b319f9c7">
