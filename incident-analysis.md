# Cybersecurity Incident Analysis

*Name:* Kathlyn M. Orillano  
*Role:* Tier 2 Analyst  

---

## Title
Advanced Persistent Attack: Unauthorized Access, Privilege Escalation, and Phishing Compromise

---

## Description
A coordinated cyber attack was detected involving brute-force login attempts, unauthorized access, privilege escalation, and phishing-based credential compromise.

Multiple failed SSH login attempts originated from IP address 192.168.1.105 targeting several accounts (root, admin, user). The attacker successfully gained access to the admin account and escalated privileges to root level, achieving full system control.

Additional suspicious activity was observed from IP address 10.0.0.50. Investigation also revealed a phishing email containing a malicious link (http://secure-login-alert.com), which deceived a user into entering credentials, contributing to the breach.

---

## Timeline of Events
- *10:05:10 – 10:06:00* → Multiple failed SSH login attempts (192.168.1.105)  
- *10:06:30* → Successful login to admin account  
- *10:07:00 – 10:08:00* → Privilege escalation (admin → root)  
- *11:20:15 – 11:21:30* → Failed login attempts (10.0.0.50)  
- *11:25:00* → Phishing email detected  
- *11:27:00* → User entered credentials  

---

## Findings
Analysis confirms that the primary attack vector was a brute-force attack from IP address 192.168.1.105. After several failed attempts, the attacker successfully accessed the admin account.

Privilege escalation techniques were then used to gain root-level access, allowing complete control over the affected system.

Furthermore, phishing activity played a significant role. A malicious email tricked a user into revealing credentials, which likely accelerated unauthorized access.

---

## Root Cause Analysis
- Weak or guessable passwords enabled brute-force success  
- Lack of Multi-Factor Authentication (MFA)  
- User vulnerability to phishing attacks  
- Insufficient monitoring and alerting mechanisms  

---

## Impact Assessment
- Unauthorized system access  
- Compromise of sensitive credentials  
- Full administrative (root) control obtained by attacker  
- Potential data breach and system manipulation  

---

## Suspicious IP Addresses
- 192.168.1.105 (Primary attacker)  
- 10.0.0.50 (Secondary suspicious activity)  

---

## Severity
*High / Critical*

---

## Recommendations
- Enforce strong password policies  
- Enable Multi-Factor Authentication (MFA) across all accounts  
- Implement account lockout policies after multiple failed attempts  
- Block malicious IP addresses at firewall level  
- Deploy intrusion detection/prevention systems (IDS/IPS)  
- Conduct regular security awareness training (phishing prevention)  
- Perform vulnerability assessments and patch management  

---

## Response Actions (Tier 2 Analyst)

Account Lockdown: Reset all compromised credentials and terminate active sessions.

Threat Containment: Block IPs 192.168.1.105 and 10.0.0.50 and isolate affected systems.

Privilege Review: Remove unauthorized root access and audit all privileged accounts.

Phishing Mitigation: Disable malicious URL (http://secure-login-alert.com) and notify users.

System Remediation: Scan and remove malware, backdoors, or unauthorized changes.

Continuous Monitoring: Enhance logging and real-time monitoring to detect future threats.

Incident Escalation: Report findings to Tier 3 team for deeper forensic investigation.
Sent
Compose
Write to
