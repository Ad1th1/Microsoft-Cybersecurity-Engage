- yara not working -> checking again

- Malware Analysis: signatures
  - malware may mutate -> polymorphic malware -> defeat signatures
 

- tools:
  - debuggers
  - disassembles -> IDA

- To fight polymorphic malwarem
  - study how malware behaves by using quarantines

 
Tools for Malware Analysis
- based on signatures
- inspecting malware internal components
- studying malware behaviour

Malware analysis with decompilers and YARA:

- Sniffers:
  -  inspects incoming and outgoing traffic
  -  useful capability for malware

What's YARA?
- flexible classification engine
- detectd sniffing malware
- wcap.dll

Signatures and their effectiveness:
- well-known in antiviruses
- malware creators are always trying to defeat counter-measures
- not effective if obfuscated or changing malwares
- YARA always helps in the first steps of malware analysis

- Installed yara
- for c source code of malware obtained by reverse-engineering a file: https://github.com/gsingh93/simple-key-logger/blob/master/skeylogger.c
- issue with yara -> not working

APT = Advanced Persistent Threat
- advanced -> great technical capabilities
- persistent -> lasts as much as possible
- threat -> attacker harms the victim

APT vs other malwares:
- precise profiling and attacking of the victim
- targetted attack
- usually operate in the form of botnets:
  - group of compromised computers -> botnets
  - work when ordered by a "Command and Control" server
- like the flu -> cause bad effects for the victim
- remain as stealthy as possible
- when the victim discovers the infection, too much time has passed


Stuxnet:
- cyber weapon discovered in mid 2010
- found in Iran's nuclear plants
- nuclear plants require uranium -> and need to spin to isolate rich uranium
- use SCADA systems for managing purposes
- Technicians from Natanz power plant realized that centrifuges:
  - work at an unprecedented rate
  - started breaking for no apparent reason
  - centrifuges started soinning at high speeds and stopping
  - kept happening on a monthly basis
- centrifuges stopped working and a replacement was needed -> causing drop in productivity

- Features of Stuxnet that make it an APT:
  - targeted
  - act silently
  - sophisticated

How did Stuxnet achieve it's goal?
- Initial Infection: USB
- Reconnaissance: look for vulnerable devices, systems
- Exploit vulnerabilities
- Remain in the infected machine for as long as possible

Reccomendations based on Stuxnet:
- Be cautious -> USB was the friggin entry point
- Keep your systems up-to-date

____________________________________________________________________________________________

DEEP PANDA:
- Chinese sponsored initiative
- steal privilieged informationb from think tanks
- files in the systems are not left

Deep Panda Steps:
- Step 1
  - malware exploits a Windows vulnerability
  - it launches a command -> file is download
  - code is kept in a RAM
  - Some hours later:
    - malware calls back the C&C server to look for instructions
- Next few steps:
  Remote Access Tool(RAT)
  - Web Shell
  - Attacker executes commands remotely
  - attacker identifies the system
- Final Step:
  - information leakage -> tarball -> compressed file

Conclusions based on Deep Panda:
- involves great complexity:
  - discovering vulnerabilities
  - exploiting vulnerabilities
  - moving from one computer to another
  - execute malicious actions
- just by creating a light-weight piece of software
-  IF YOU WANT TO BE A TALENTED SECURITY EXPERT, KEEP LOOKING FOR MALWARE

- emails are hacked
- information is stolen from data-bases

- Exposure
  - a system configuration issue or mistake in software that allows access to information or capabilities that can be used by a hacker as a stepping-stone into a system or network (MITRE corporation)

- Vulnerability:
  - a mistake in software that can be used directly by a hacker to gain access to a system or a network (MITRE corporation)
  - allow an attacker to
    - impersonate a user and exeute commands
    - access unauthorized data
    - execute denial of service attacks

- Exposures:
  - may allow the same issues, despite not being vulnerable

- So many vulnerabilities according to CVE
- Eg 1: new vulnerability processing MP3/MP4 media -> caused by vulnerable library -> first flaw released in 2008 -> impacted every Android file -> patched in version 5
- Eg 2: Win32k Elevation of Privilege Vulnerability -> allows complete control of the system to be achieved -> already patched

Examples of Exposures:
- Wrong firewall configuration
- Wrong service configuration -> HTTP and FTP
- Well Trained experts


Vulnerabilities at different levels:
- software -> segmentation faults, race conditions, input validations
- network -> password sniffing, session hijacking, denial of service
- web -> cross site scripting(XSS), SQL Injection, undesired data disclosure

_____________________________________________________________________________________

Segmentation Faults  
- common in C language
- programs have memory reserved but some parts are not
- improper use of printf or scanf function. 
- Eg: null pointer, give space for variable, & in scanf


Buffer Overflow:
- arrays
- outof index -> if you try to access a memory that has not been allocated
- can occur in different objects and functions

Proper initialization error:

Prevention measures:
-> not general -> depends on particular case
-> experience helps
-> debuggers are reccomended

_____________________________________________________________________________________

- several processes may want to access the same resources -> race conditions
- common in thread programming
- prevention measures: synchronization -> established in critical section
- solutions in C: mutex, conditional variables
- solutions in Java: synchronized

File systems:
- using file name(identifies a file by it's name) instead of file handler (identifies a file internally)
- Time of check, time of use (toctou)
- getting the attack: create a symbolic link with "symbolic functions"

_____________________________________________________________________________________

- verify user supply data
- errors could cause improper input validation
- occured in - multiple language - assorted scenarios
- door to challenging attacks

- improper validation of data size
  - common in web application
  - gets .... !!!!!!!!!!!!!!!!
  - use fgets instead
  - can cause operation errors
  - general solution: proper validation of all input data
  - assume that users may be attackers, or can perform unexpected bad actions, unintentionally
  - 

