- using python to automate cybersecurity tasks
- check out MITRE ATT&CK and Shield frameworks

- Why Python?
  - popular
  - simple
  - capable -> large number of libraries, large amount of built-in functionality

MITRE ATT&CK
- tool developed by MITRE Corporation to improve cybersecurity understanding
- maps different techniques and procedures to the cyberattack life cycle and an adversary's goals

MITRE Shield
- developed by MITRE to promote active defense
- identifies different goals that an active defender may have and outline methods for achieving those goals

Important Terms:
- Tactic = goal at a particular stage of a cyber-attack or goal in active defense. Eg: lateral movement
- Technique = mechanism by which an attacker can achieve the goal outlined in a particular tactic. Eg: Brute force approach
  - Sub-technique = method for carrying out a particular technique
- Procedure = specific implementation of a particular technique or sub-technique

MITRE ATT&CK Tactics:
1. PRE-ATT&CK
2. Initial Access
3. Execution
4. Persistence
5. Privelege Escalation
6. DEfense Evasion
7. Credential Access
8. Discovery
9. Lateral Movement
10. Collection
11. Command and Control
12. Exfiltration
13. Impact

MITRE Shield Tactics:
1. Channel
2. Collect
3. Contain
4. Detect
5. Disrupt
6. Facilitate
7. Legitimize
8. Test

MITRE PRE-ATT&CK used to be it's own matrix:
- contained a collection of tactics and techniques
- mapped to the recon and weaponize stages of the cyberkill chain

Now, PRE-ATT&CK is the first two stages of MITRE ATT&CK for enterprise framework
- reconnaissance
- resource development

Reconnaisance -> information collection
- active scanning : interact with system and learn about it
- gather victim host, identity, networkn org information
- phishing for info
- search closed sources, open tech databases, open websites/domains and victim-owned websites


Resource Development -> attacker developing or acquiring tools needed to perform the attack
- acquire infrastructure
- compromise accounts and infrastructure
- develop capabilities
- establish accounts
- obtain capabilities

- occurs primarily on attacker's infrastructure
- depends on attacker's goals and resources

Reconnaissance tactics being explored:
- active scanning: network scanning
- search open technical databases: DNS exploration

_______________________________________________________________________________________

Network Scanning:
- Knowledge of target network is vital for an attacker  
  - identification of potential target systems
  - discovery of vulnerable applications

- method of learning a target network architecture:
  - port scanning 
  - banner collection
  - vulnerability scanning

- active scanning
  - scanning IP blocks
  - vulnerability scanning


scipy:
- python libraries


27 minutes


