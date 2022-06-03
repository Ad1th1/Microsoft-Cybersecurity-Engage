- check the linux bit in the video

- Intrusion Detection Systems:
  - goal: identify entities trying to subvert security controls
  - IDS vs firewall?
    - firewall -> blocks
    - ID -> looks for intrusion
  - intrusion is the core of the system. When an event matches established rules and violates privacy -> intrucion
  - no policy -> no intrusion
  - Network based and host based

- Classified into:
  - anomalies / unauthorized uses
  - network / host based
  

- security policies -> network issues and computer aspects

- Network IDS
  - traffic inspection
  - need to be placed in areas of possible interception
  - need to see the packet content (avoid traffic that cannot be decrypted)

- Host based IDS
  - monitor internal computer activity
  - check applications, devices, services
  - checks for violation of security policy
 
- What if the IDS is attacked?
  - receiving traffic -> potential attack
  - approach: place IDS in a machine with no address
 
  
- 2 approaches to look for intrusion
  - anomalies 
    - build models 
    - best for unknown
    - needs a model for normality and a deviation from this
    - risk of false positives (wolf wolf, but no wolf)
    - false negative -> uneffective ID
    - ID needs to be configured rightly


  - unauthorized uses -> ID's are configured -> set of illegal events -> known issues only

- SNORT
  - Open source and multi-platform 
  - detection using unauthorized uses
  - Network IDS
  - intercept and extract each packet -> check policy -> check whether intrusion or not
  - packet decoder -> preprocessor(s) -> detection engine(rule) -> alert module -> output module(decides way of sending alarm)
  - supported by a large community -> huge set of rules and software improvements
  - easier to have up-to-date rules
  - expressive rules -> SNORT keeps dynamic knowledge
  - needs to be super fast
  - if slow, it can cause queues
  - SNORT uses plugins for almost real-time processing

- SNORT rules:
  - each rule has a header(condition to consider a packet) and options(what to do with said packet)
  - header 
    - action to take -> pass, alert, log, dynamic, activate
    - protocol -> IP, TCP, UDP, ICMP
    - connection -> IP, port -> <- IP, port

  - options
    - contains several options seperated by semicolons and carry information
    - 3 typical options: message, sid(snort id), revision status
    - Eg: detection filter

  - creating the rules
    - we can have reserved words
 
- SIEM = Security Information and Event Management
  - anivirus, ID, firewall -> all need to be managed by SIEM
  - helps us manage incidents
  - able to speak to several tools
  - receive logs and analyze them
  - data analysis is part of the job -> event creation
  - can even predict -> prediction module -> may fail -> use AI and are super complex -> probabilistic
  - produce grahs and reports in real time
  - turn raw info -> events
  - Origin:
    - Secrity Information Management(SIM) = gathering data from sources
    - Security Event Management(SEM) = tracks status of security events
  - event status?
  - phases of attack management:
    - data collection and preprocessing
    - threat detection
    - threat categorization and triage
    - threat mitigation
    - threat recovery
    
   - ticket-based way to manage incidents
   - show overall security status
   - user friendly -> graphs, barcharts, piecharts, linear trends, etc
   - supervisor NEEDS to act immediately
   - need:
     - overall knowledge
     - alignment witth security strategy
     - scalability -> big data -> huge amount of data to be processed all the times
     - resources -> money, infrastructure, staff
  

- MALWARE = Malicious Software
  - any program that causes malicious action to a system
  - many different kinds, with varying levels of danger
  - Morris Worm (1988) - developed to gauge the size of the Internet
  - Conficker (2008) - collected personal data and downloaded additional malware

- Basics on identifying malware infection:
  - slow speed when browsing or opening/closing files
  - network connection errors
  - deleted or modified files
  - emails are automatically sent
  - programs running without your consent

- Basics on defending against malware:
  - Firewalls
  - Intrusion Detection System
  - Antivirus
  - don't open emails if source is dodgy
  - scan downloaded files
  - don't visit suspicious websites
  - perform regular  backups

- Worms:
  - propogate themselves from one computer to another
  - damage caused by consuming bandwidth and cause overloading
  - may contain payload that deletes data
  - autonomous and don't need help propogating
  - propogate using system vulnerabilities
  - Propogation model:
    - initial infection -> exploit a vulnerability to infect target machine and find additional machines to exploit using IP addresses, shells, emails, etc
    - target found
    - worm is transmitted
    - system is compromised
  - Classified on basis of infection:
    - email worms -> spread through emails. Eg: I LOVE YOU -> 2000 -> 10 billion $ of loss -> caused generation of random files over-writing existing ones
 
 
- Virus:
  - machine doesn't work well enough
  - malware that copies itself and infects PC's
  - propogated through files -> copied and overwritten
  - most viruses are attached to executable files
  - different from worms -> require propogation of files
  - Eg 1: 1987 -> Jerusalem virus -> destroyed all executable files, on every Friday, the 13th
  - Eg 2: badBIOS -> May 2016 -> spread via microphones -> gets into the PC by infected PC's -> generate high frequency sounds that can't be heard by humans and are recieved by another machine

- Rootkit
  - malware that hide malicious processes/ programs
  - difficult to identify
  - propogates through copied files, USB sticks
  - try to hide themselves
  - 2 types:
    - user mode
      - run at application level
      - hide files, processes, ports
      - detected by tools like anti-viruses
    - kernel mode:
      - more dangerous
      - run at OS level
      - hard to detect and remove -> because they run at sudo mode
   - Eg: Hacker defender: user mode rootkit for Windows
         - modifies several Windows files and Native API functions
         - can create a backdoor for an attack
   
- How to check if computer has been compromised by a rootkit
  - screen goes blank, more than expected
  - application settings change without consent
  - web-pages work improperky due to heavy network traffic

- Disinfection:
  - User-mode rootkit: some tools. Eg: anti-virus
  - Kernel mode: need to use other sources to discover the truth

 
- Trojan
  - malware that tricks you into installing them
  - hide as a benign program
  - sit and create security holes
    - grant remote access
    - install malware
    - track user activity
  - cannot be distinguished from benign files
  - be very careful when downloading information
  - Eg: Zeus -> Trojan family since 2007 -> steals banking information
        - collected data is used for login purposes to perform unauthorized actions
        - if identified, there are tools to remove it and antiviruses for identification
     
- Ransomware
  - restrict access to data and demands a ransom(bitcoin) to get access
  - 2 types:
    - lock access to data: code to unlock access
    - encrypt data: very dangerous -> decryption key needed to decrypt
   - Eg: Cryptolocker -> 2013
          - 3 days to pay
          - files within a list were encrypted
  
- Spyware:
  - spies your activity without your consent
  - collects keystrokes, harvest data, monitors activity, modify security settings
  - problems caused: theft of personal data, slow system
  - Eg: Finfisher (developed by Gamma Group internationally)
        - infects computers by browser plugins
        - emails and documents -> copied and sent to remote server
        - outsiders can collect data
       



