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
   
  


