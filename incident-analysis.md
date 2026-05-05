# Cybersecurity Incident Analysis

## Timeline of Events
- 10:01–10:03 – Multiple failed SSH login attempts from 192.168.1.100 (root, admin, user)
- 10:05 – Successful login to admin account from 192.168.1.100
- 10:07 – Privilege escalation from admin to root
- 10:10 – Failed login attempts from 10.0.0.45
- 10:12 – Phishing email detected (fake login link)
- 10:13 – User reported entering credentials

## Analysis
The logs show a sequence of suspicious activities starting with multiple failed login attempts, indicating a brute-force attack from IP address 192.168.1.100. After several attempts, the attacker successfully accessed the admin account.

Following the unauthorized access, the attacker escalated privileges from admin to root, gaining full control of the system. This confirms a serious security breach.

Additionally, a phishing email containing a fake login link was identified. A user reported entering their credentials, suggesting that compromised credentials may have been used in the attack.

Another IP address (10.0.0.45) also showed failed login attempts, which may indicate further malicious activity or support for the attack.

## Suspicious IP Addresses
- 192.168.1.100 (Primary attacker)
- 10.0.0.45 (Secondary suspicious activity)

## Conclusion
This incident is a confirmed cyber attack involving brute-force attempts, phishing-based credential compromise, unauthorized access, and privilege escalation. The system is fully compromised.

## Severity
High

## Recommendations
- Immediately reset all compromised passwords
- Enable Multi-Factor Authentication (MFA)
- Block suspicious IP addresses
- Conduct phishing awareness training for users
- Monitor system logs for further suspicious activity
Sent 4m ago
Compose
Write to

