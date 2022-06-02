16 minutes

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
  > - ARP Table combines MAC and IP addresses = cache
  > - ARP provides physical address of host, given the IP address
  > - ARP Poisoning

- authentication: recipient can identify the sender
- integrity: data in transit is not altered
- confidentiality: transmitted data is only accessed by the receiver

- cookie:
  > - small piece of data used by web-servers to link different connections made by the same user
  > - less secure cookies = keyboard language
  > - more secure cookies = browsed web-pages
 
