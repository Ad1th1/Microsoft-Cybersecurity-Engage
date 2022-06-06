18 minutes -> ARP spoofing on linux not watched
28 minutes -> DOS on apache

- password sniffing = attack to capture passwords in plain text
  > - man in the middle attack 
  >   > - using a sniffer tool like WireShark
      > - be in the same network as the victim
      > - ensure that communication is not encrypted
      > - if encrypted, trick the user into using sslstrip or whatever -> HTTP between client and attacker, HTTPS between attacker and server


- Precautions:
  > - HTTPS
  > - hash passwords 
  > - SSL = Secure Sockets Layer Protocol -> Authentication + Confidentiality + Integrity
  
  
- Precautions for session hijacking: use secure communication
- Common way to perform session hijacking: stolen cookie (small piece of data to track users) -> apply developer tools of Chrome browser

- Stolen Cookie Example:
  > - attacker and client are in same network
  > - attacker uses Wireshark to capture packets and analyzes traffic
  > - HTTPS and mandatory certificate verification avoids this problem, but can be bypassed using SSLStrip


- ARP Spoofing:
  > - man-in-the-middle attack -> a step towards sesion-hijacking
  > - ARP table combines MAC and IP addresses = cache
  > - ARP -> Address Resolution Protocol
  > - provides physical address of host, given the IP address
  > - ARP Poisoning
  
  
- authentication: recipient can identify the sender
- integrity: data in transit is not altered
- confidentiality: transmitted data is only accessed by the receiver

- cookie:
  > - small piece of data used by web-servers to link different connections made by the same user
  > - less secure cookies = keyboard language
  > - more secure cookies = browsed web-pages

- ARP Spoofing:
  - ARP poisoning -> google it, lol!
  - 16 minutes
  - fake mac is sent and data is sent to person intercepting

- Preventive measures for ARP spoofing
  - static ARP tables can be used
  - Intrusion detection systems(IDS's) to filter traffic
  - linked to man in the middle attacks -> session hijacking

 
- Denial of Service - DOS
  - prevents users from accessing a service
  - flooding is a common attack
  - Eg: HSBC cyber attack due to DOS Attack
  - Types:
    - smurfing / flooding -> lots of ping messages(sent to identify live hosts)
    - slowloris -> establish multiple connections to a server 
      - countermeasures:   1. firewall configuration  2. load balancers to allow full HTTP connections
  
- Distributed Denial of Service:
  - DOS prevents users from accessing a service
  - sometimes caused by human errors
 
 
 How can DOS be identified?
 - slow network performance
 - inability to access a service or web-site
 - lots of spam messages received
 
 Preventive measures for DOS
 - install antivirus
 - proper firewall configuration
 - be cautious and sensible when opening emails and other links
