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
  
  
  
- authentication: recipient can identify the sender
- integrity: data in transit is not altered
- confidentiality: transmitted data is only accessed by the receiver


