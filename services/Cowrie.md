## Cowrie

**Purpose:**<br>
SSH Honeypot.

**Why Implemented:**<br>
Controlled exposure into blue teaming operations, specifically to attract, monitor and analyse malicious activity. A continuation from [TryHackMe](https://tryhackme.com/) rooms I have completed.

**Dependencies:**<br>

- Docker
  
**Key concepts learned:**<br>

- Malicous activity starts almost instantly, configuring firewalls and changing default ports from the start is a must.
- Implementing brute-force security such as fail2ban is essential on a live environment.
- I found that turning off the ability to ping the host made a considerable difference on automated discovery and attacks.
- It seems a lot of automated malicious activity is based around discovery and initial access. 
