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
 
