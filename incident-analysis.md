# Cybersecurity Incident Analysis

## Timeline of Events
- 10:01:23–10:01:30: Multiple failed SSH login attempts from 192.168.1.100 (root, admin, user)
- 10:02:10: Successful login to admin account from 192.168.1.100
- 10:02:15–10:03:15: Privilege escalation (admin to root)
- 11:15:02–11:16:22: Failed login attempts from 10.0.0.45
- Phishing email detected (fake login link)
- User reported entering credentials

## Findings
The attack originated from IP 192.168.1.100, which performed multiple failed login attempts, indicating a brute-force attack. After several attempts, the attacker successfully logged in as the admin.

The attacker then escalated privileges to root, gaining full control of the system.

There is also evidence of phishing. A fake email containing a malicious link (http://fake-login.security.com) tricked a user into entering credentials, which likely contributed to the unauthorized access.

## Suspicious IP Addresses
- 192.168.1.100 (primary attacker)
- 10.0.0.45 (secondary suspicious activity)

## Conclusion
This is a critical security breach involving brute-force attack, unauthorized access, privilege escalation, and phishing-based credential compromise.

## Recommendations
- Reset all compromised passwords immediately
- Enable multi-factor authentication (MFA)
- Block suspicious IP addresses
- Conduct phishing awareness training
- Monitor system logs for further suspicious activity
